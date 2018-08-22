---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Get content properties
  description: "Returns the properties for a piece of content. For more information
    \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'View' permission for the space, and permission to view the content
    if it is a page."
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /audit:
    get:
      summary: Get audit records
      description: "Returns all records in the audit log, optionally for a certain
        date range. \nThis contains information about events like space exports, group
        membership \nchanges, app installations, etc. For more information, see \n[Audit
        log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)
        \nin the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AuditResource.getAuditRecords_get
      x-api-path-slug: audit-get
      parameters:
      - in: query
        name: endDate
        description: Filters the results to the records on or before the `endDate`
      - in: query
        name: limit
        description: The maximum number of records to return per page
      - in: query
        name: searchString
        description: Filters the results to records that have string property values
          matching the `searchString`
      - in: query
        name: start
        description: The starting index of the returned records
      - in: query
        name: startDate
        description: Filters the results to the records on or after the `startDate`
      responses:
        200:
          description: OK
      tags:
      - Audit
      - Records
    post:
      summary: Create audit record
      description: "Creates a record in the audit log. \n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AuditResource.createAuditRecord_post
      x-api-path-slug: audit-post
      responses:
        200:
          description: OK
      tags:
      - Audit
      - Record
  /audit/export:
    get:
      summary: Export audit records
      description: "Exports audit records as a CSV file or ZIP file.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AuditResource.exportAuditRecords_get
      x-api-path-slug: auditexport-get
      parameters:
      - in: query
        name: endDate
        description: Filters the exported results to the records on or before the
          `endDate`
      - in: query
        name: format
        description: The format of the export file for the audit records
      - in: query
        name: searchString
        description: Filters the exported results to records that have string property
          values matching the `searchString`
      - in: query
        name: startDate
        description: Filters the exported results to the records on or after the `startDate`
      responses:
        200:
          description: OK
      tags:
      - Export
      - Audit
      - Records
  /audit/retention:
    get:
      summary: Get retention period
      description: "Returns the retention period for records in the audit log. The
        retention \nperiod is how long an audit record is kept for, from creation
        date until \nit is deleted.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AuditResource.getRetentionPeriod_get
      x-api-path-slug: auditretention-get
      responses:
        200:
          description: OK
      tags:
      - Retention
      - Period
    put:
      summary: Set retention period
      description: "Sets the retention period for records in the audit log. The retention
        period \ncan be set to a maximum of 20 years.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AuditResource.setRetentionPeriod_put
      x-api-path-slug: auditretention-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Retention
      - Period
  /audit/since:
    get:
      summary: Get audit records for time period
      description: "Returns records from the audit log, for a time period back from
        the current \ndate. For example, you can use this method to get the last 3
        months of records.\n\nThis contains information about events like space exports,
        group membership \nchanges, app installations, etc. For more information,
        see \n[Audit log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)
        \nin the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AuditResource.getAuditRecordsForTimePeriod_get
      x-api-path-slug: auditsince-get
      parameters:
      - in: query
        name: limit
        description: The maximum number of records to return per page
      - in: query
        name: number
        description: The number of units for the time period
      - in: query
        name: searchString
        description: Filters the results to records that have string property values
          matching the `searchString`
      - in: query
        name: start
        description: The starting index of the returned records
      - in: query
        name: units
        description: The unit of time that the time period is measured in
      responses:
        200:
          description: OK
      tags:
      - Audit
      - Recordstime
      - Period
  /content:
    get:
      summary: Get content
      description: "Returns all content in a Confluence instance.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission).
        \nOnly content that the user has permission to view will be returned."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.getContent_get
      x-api-path-slug: content-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          to expand
      - in: query
        name: limit
        description: The maximum number of content objects to return per page
      - in: query
        name: orderby
        description: Orders the content by a particular field
      - in: query
        name: postingDay
        description: The posting date of the blog post to be returned
      - in: query
        name: spaceKey
        description: The key of the space to be queried for its content
      - in: query
        name: start
        description: The starting index of the returned content
      - in: query
        name: status
        description: Filter the results to a set of content based on their status
      - in: query
        name: title
        description: The title of the page to be returned
      - in: query
        name: trigger
        description: If set to `viewed`, the request will trigger a viewed event for
          the content
      - in: query
        name: type
        description: The type of content to return
      responses:
        200:
          description: OK
      tags:
      - Content
    post:
      summary: Create content
      description: "Creates a new piece of content or publishes an existing draft.
        \n\nTo publish a draft, add the `id` and `status` properties to the body of
        the request. \nSet the `id` to the ID of the draft and set the `status` to
        'current'. When the \nrequest is sent, a new piece of content will be created
        and the metadata from the \ndraft will be transferred into it.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: 'Add' permission for the \nspace that the content will be created
        in, and permission to view the draft if publishing a draft."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.createContent_post
      x-api-path-slug: content-post
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the new
          content to expand
      - in: query
        name: status
        description: Filter the returned content by status
      responses:
        200:
          description: OK
      tags:
      - Content
  /content/blueprint/instance/{draftId}:
    post:
      summary: Publish legacy draft
      description: "Publishes a legacy draft of a page created from a blueprint. Legacy
        drafts \nwill eventually be removed in favour of shared drafts. For now, this
        method \nworks the same as [Publish shared draft](#api-content-blueprint-instance-draftId-put).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the draft and 'Add' permission for the space
        that \nthe content will be created in."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentBlueprintResource.publishLegacyDraft_post
      x-api-path-slug: contentblueprintinstancedraftid-post
      parameters:
      - in: path
        name: draftId
        description: The ID of the draft page that was created from a blueprint
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the new
          content to expand when returned
      - in: query
        name: status
        description: The status of the content to be updated, i
      responses:
        200:
          description: OK
      tags:
      - Publish
      - Legacy
      - Draft
    put:
      summary: Publish shared draft
      description: "Publishes a shared draft of a page created from a blueprint.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the draft and 'Add' permission for the space
        that \nthe content will be created in."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentBlueprintResource.publishSharedDraft_put
      x-api-path-slug: contentblueprintinstancedraftid-put
      parameters:
      - in: path
        name: draftId
        description: The ID of the draft page that was created from a blueprint
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the new
          content to expand when returned
      - in: query
        name: status
        description: The status of the content to be updated, i
      responses:
        200:
          description: OK
      tags:
      - Publish
      - Shared
      - Draft
  /content/search:
    get:
      summary: Search content by CQL
      description: "Returns the list of content that matches a Confluence Query Language
        \n(CQL) query. For information on CQL, see: \n[Advanced searching using CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission).
        \nOnly content that the user has permission to view will be returned."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.searchContentByCQL_get
      x-api-path-slug: contentsearch-get
      parameters:
      - in: query
        name: cql
        description: The CQL string that is used to find the requested content
      - in: query
        name: cqlcontext
        description: The space, content, and content status to execute the search
          against
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          to expand
      - in: query
        name: limit
        description: The maximum number of content objects to return per page
      - in: query
        name: start
        description: The starting index of the returned content
      responses:
        200:
          description: OK
      tags:
      - Search
      - Content
      - By
      - CQL
  /content/{id}:
    get:
      summary: Get content by ID
      description: "Returns a single piece of content, like a page or a blog post.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content. If the content is a blog post,
        'View' permission \nfor the space is required."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.getContentById_get
      x-api-path-slug: contentid-get
      parameters:
      - in: query
        name: embeddedContentRender
        description: The version of embedded content (e
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          to expand
      - in: path
        name: id
        description: The ID of the content to be returned
      - in: query
        name: status
        description: Filter the results to a set of content based on their status
      - in: query
        name: trigger
        description: If set to `viewed`, the request will trigger a viewed event for
          the content
      - in: query
        name: version
        description: The version number of the content to be returned
      responses:
        200:
          description: OK
      tags:
      - Content
      - By
      - ID
    put:
      summary: Update content
      description: "Updates a piece of content. Use this method to update the title
        or body \nof a piece of content, change the status, change the parent page,
        and more.\n\nNote, updating draft content is currently not supported.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.updateContent_put
      x-api-path-slug: contentid-put
      parameters:
      - in: query
        name: conflictPolicy
        description: The action that should be taken when conflicts are discovered
      - in: path
        name: id
        description: The ID of the content to be updated
      - in: query
        name: status
        description: The updated status of the content
      responses:
        200:
          description: OK
      tags:
      - Content
    delete:
      summary: Delete content
      description: "Moves a piece of content to the space's trash or purges it from
        the trash, \ndepending on the content's type and status:\n\n- If the content's
        type is `page` or `blogpost` and its status is `current`, \nit will be trashed.\n-
        If the content's type is `page` or `blogpost` and its status is `trashed`,
        \nthe content will be purged from the trash and deleted permanently. Note,
        \nyou must also set the `status` query parameter to `trashed` in your request.\n-
        If the content's type is `comment` or `attachment`, it will be deleted \npermanently
        without being trashed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Delete' permission for the space that the content is in, and
        permission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.deleteContent_delete
      x-api-path-slug: contentid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the content to be deleted
      - in: query
        name: status
        description: Set this to `trashed`, if the contents status is `trashed` and
          you want to purge it
      responses:
        200:
          description: OK
      tags:
      - Content
  /content/{id}/child:
    get:
      summary: Get content children
      description: "Returns a map of the direct children of a piece of content. A
        piece of content \nhas different types of child content, depending on its
        type. These are \nthe default parent-child content type relationships:\n\n-
        `page`: child content is `page`, `comment`, `attachment`\n- `blogpost`: child
        content is `comment`, `attachment`\n- `attachment`: child content is `comment`\n-
        `comment`: child content is `attachment`\n\nApps can override these default
        relationships. Apps can also introduce \nnew content types that create new
        parent-child content relationships.\n\nNote, the map will always include all
        child content types that are valid \nfor the content. However, if the content
        has no instances of a child content \ntype, the map will contain an empty
        array for that child content type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: 'View' permission for the space, \nand permission to view the
        content if it is a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentChildren_get
      x-api-path-slug: contentidchild-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the children
          to expand, where:- `attachment` returns all attachments for the content
      - in: path
        name: id
        description: The ID of the content to be queried for its children
      - in: query
        name: parentVersion
        description: The version of the parent content to retrieve children for
      responses:
        200:
          description: OK
      tags:
      - Content
      - Children
  /content/{id}/child/attachment:
    get:
      summary: Get attachments
      description: "Returns the attachments for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content. If the content is a blog post,
        'View' permission \nfor the space is required."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.getAttachments_get
      x-api-path-slug: contentidchildattachment-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the attachments
          to expand
      - in: query
        name: filename
        description: Filter the results to attachments that match the filename
      - in: path
        name: id
        description: The ID of the content to be queried for its attachments
      - in: query
        name: limit
        description: The maximum number of attachments to return per page
      - in: query
        name: mediaType
        description: Filter the results to attachments that match the media type
      - in: query
        name: start
        description: The starting index of the returned attachments
      responses:
        200:
          description: OK
      tags:
      - Attachments
    post:
      summary: Create attachment
      description: "Adds an attachment to a piece of content. This method only adds
        a new \nattachment. If you want to update an existing attachment, use \n[Create
        or update attachments](#api-content-id-child-attachment-put).\n\nNote, you
        must set a `X-Atlassian-Token: nocheck` header on the request \nfor this method,
        otherwise it will be blocked. This protects against XSRF \nattacks, which
        is necessary as this method accepts multipart/form-data.\n\nThe media type
        'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt).
        \nMost client libraries have classes that make it easier to implement \nmultipart
        posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html)
        \nJava class provided by Apache HTTP Components.\n\nExample: This curl command
        attaches a file ('example.txt') to a container \n(id='123') with a comment
        and `minorEdits`=true.\n\n``` bash\ncurl -D- \\\n  -u admin:admin \\\n  -X
        POST \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\"
        \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\"
        \\\n  http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.createAttachments_post
      x-api-path-slug: contentidchildattachment-post
      parameters:
      - in: path
        name: id
        description: The ID of the content to add the attachment to
      - in: query
        name: status
        description: The status of the content that the attachment is being added
          to
      responses:
        200:
          description: OK
      tags:
      - Attachment
    put:
      summary: Create or update attachment
      description: "Adds an attachment to a piece of content. If the attachment already
        exists \nfor the content, then the attachment is updated (i.e. a new version
        of the \nattachment is created).\n\nNote, you must set a `X-Atlassian-Token:
        nocheck` header on the request \nfor this method, otherwise it will be blocked.
        This protects against XSRF \nattacks, which is necessary as this method accepts
        multipart/form-data.\n\nThe media type 'multipart/form-data' is defined in
        [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client libraries
        have classes that make it easier to implement \nmultipart posts, like the
        [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html)
        \nJava class provided by Apache HTTP Components.\n\nExample: This curl command
        attaches a file ('example.txt') to a piece of \ncontent (id='123') with a
        comment and `minorEdits`=true. If the 'example.txt' \nfile already exists,
        it will update it with a new version of the attachment.\n\n``` bash\ncurl
        -D- \\\n  -u admin:admin \\\n  -X PUT \\\n  -H \"X-Atlassian-Token: nocheck\"
        \\\n  -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example
        attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.createOrUpdateAttachments_put
      x-api-path-slug: contentidchildattachment-put
      parameters:
      - in: path
        name: id
        description: The ID of the content to add the attachment to
      - in: query
        name: status
        description: The status of the content that the attachment is being added
          to
      responses:
        200:
          description: OK
      tags:
      - Update
      - Attachment
  /content/{id}/child/attachment/{attachmentId}:
    put:
      summary: Update attachment properties
      description: "Updates the attachment properties, i.e. the non-binary data of
        an attachment \nlike the filename, media-type, comment, and parent container.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.updateAttachmentProperties_put
      x-api-path-slug: contentidchildattachmentattachmentid-put
      parameters:
      - in: path
        name: attachmentId
        description: The ID of the attachment to update
      - in: path
        name: id
        description: The ID of the content that the attachment is attached to
      responses:
        200:
          description: OK
      tags:
      - Attachment
      - Properties
  /content/{id}/child/attachment/{attachmentId}/data:
    post:
      summary: Update attachment data
      description: "Updates the binary data of an attachment, given the attachment
        ID, and \noptionally the comment and the minor edit field.\n\nThis method
        is essentially the same as [Create or update attachments](#api-content-id-child-attachment-put),
        \nexcept that it matches the attachment ID rather than the name.\n\nNote,
        you must set a `X-Atlassian-Token: nocheck` header on the request \nfor this
        method, otherwise it will be blocked. This protects against XSRF \nattacks,
        which is necessary as this method accepts multipart/form-data.\n\nThe media
        type 'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt).
        \nMost client libraries have classes that make it easier to implement \nmultipart
        posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html)
        \nJava class provided by Apache HTTP Components.\n\nExample: This curl command
        updates an attachment (id='att456') that is attached  \nto a piece of content
        (id='123') with a comment and `minorEdits`=true. \n\n``` bash\ncurl -D- \\\n
        \ -u admin:admin \\\n  -X POST \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n
        \ -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example
        attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment/att456/data\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.updateAttachmentData_post
      x-api-path-slug: contentidchildattachmentattachmentiddata-post
      parameters:
      - in: path
        name: attachmentId
        description: The ID of the attachment to update
      - in: path
        name: id
        description: The ID of the content that the attachment is attached to
      responses:
        200:
          description: OK
      tags:
      - Attachment
      - Data
  /content/{id}/child/comment:
    get:
      summary: Get content comments
      description: "Returns the comments on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: 'View' permission for the space, \nand permission to view the
        content if it is a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentComments_get
      x-api-path-slug: contentidchildcomment-get
      parameters:
      - in: query
        name: depth
        description: Currently, this parameter is not used
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the attachments
          to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its comments
      - in: query
        name: limit
        description: The maximum number of comments to return per page
      - in: query
        name: location
        description: The location of the comments in the page
      - in: query
        name: parentVersion
        description: The version of the parent content to retrieve children for
      - in: query
        name: start
        description: The starting index of the returned comments
      responses:
        200:
          description: OK
      tags:
      - Content
      - Comments
  /content/{id}/child/{type}:
    get:
      summary: Get content children by type
      description: "Returns all children of a given type, for a piece of content.
        \nA piece of content has different types of child content, depending on its
        type:\n\n- `page`: child content is `page`, `comment`, `attachment`\n- `blogpost`:
        child content is `comment`, `attachment`\n- `attachment`: child content is
        `comment`\n- `comment`: child content is `attachment`\n\nCustom content types
        that are provided by apps can also be returned.\n\nNote, this method only
        returns direct children. To return children at all \nlevels, use [Get descendants
        by type](#api-content-id-descendant-type-get).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: 'View' permission for the space, \nand permission to view the
        content if it is a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentChildrenByType_get
      x-api-path-slug: contentidchildtype-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the new
          content to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its children
      - in: query
        name: limit
        description: The maximum number of content to return per page
      - in: query
        name: parentVersion
        description: The version of the parent content to retrieve children for
      - in: query
        name: start
        description: The starting index of the returned content
      - in: path
        name: type
        description: The type of children to return
      responses:
        200:
          description: OK
      tags:
      - Content
      - Children
      - By
      - Type
  /content/{id}/descendant:
    get:
      summary: Get content descendants
      description: "Returns a map of the descendants of a piece of content. This is
        similar \nto [Get content children](#api-content-id-child-get), except that
        this \nmethod returns child pages at all levels, rather than just the direct
        \nchild pages.\n\nA piece of content has different types of descendants, depending
        on its type:\n\n- `page`: descendant is `page`, `comment`, `attachment`\n-
        `blogpost`: descendant is `comment`, `attachment`\n- `attachment`: descendant
        is `comment`\n- `comment`: descendant is `attachment`\n\nThe map will always
        include all descendant types that are valid for the content. \nHowever, if
        the content has no instances of a descendant type, the map will \ncontain
        an empty array for that descendant type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'View' permission for the space, and permission to view the
        content if it \nis a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.DescendantContentResource.getContentDescendants_g
      x-api-path-slug: contentiddescendant-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the children
          to expand, where:- `attachment` returns all attachments for the content
      - in: path
        name: id
        description: The ID of the content to be queried for its descendants
      responses:
        200:
          description: OK
      tags:
      - Content
      - Descendants
  /content/{id}/descendant/{type}:
    get:
      summary: Get content descendants by type
      description: "Returns all descendants of a given type, for a piece of content.
        This is \nsimilar to [Get content children by type](#api-content-id-child-type-get),
        \nexcept that this method returns child pages at all levels, rather than just
        \nthe direct child pages.\n\nA piece of content has different types of descendants,
        depending on its type:\n\n- `page`: descendant is `page`, `comment`, `attachment`\n-
        `blogpost`: descendant is `comment`, `attachment`\n- `attachment`: descendant
        is `comment`\n- `comment`: descendant is `attachment`\n\nCustom content types
        that are provided by apps can also be returned.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'View' permission for the space, and permission to view the
        content if it \nis a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.DescendantContentResource.descendantsOfType_get
      x-api-path-slug: contentiddescendanttype-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the new
          content to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its descendants
      - in: query
        name: limit
        description: The maximum number of content to return per page
      - in: query
        name: start
        description: The starting index of the returned content
      - in: path
        name: type
        description: The type of descendants to return
      responses:
        200:
          description: OK
      tags:
      - Content
      - Descendants
      - By
      - Type
  /content/{id}/history:
    get:
      summary: Get history for content
      description: |-
        Returns the most recent update for a piece of content.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: Permission to view the content.
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.getHistoryForContent_get
      x-api-path-slug: contentidhistory-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          history to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its history
      responses:
        200:
          description: OK
      tags:
      - Historycontent
  /content/{id}/history/{version}/macro/id/{macroId}:
    get:
      summary: Get macro body by macro ID
      description: "Returns the body of a macro in storage format, for the given macro
        ID. \nThis includes information like the name of the macro, the body of the
        macro, \nand any macro parameters. This method is mainly used by Cloud apps.\n\nAbout
        the macro ID: When a macro is created in a new version of content, \nConfluence
        will generate a random ID for it, unless an ID is specified \n(by an app).
        The macro ID will look similar to this: '50884bd9-0cb8-41d5-98be-f80943c14f96'.
        \nThe ID is then persisted as new versions of content are created, and is
        \nonly modified by Confluence if there are conflicting IDs.\n\nNote, to preserve
        backwards compatibility this resource will also match on \nthe hash of the
        macro body, even if a macro ID is found. This check will \neventually become
        redundant, as macro IDs are generated for pages and \ntransparently propagate
        out to all instances.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content that the macro is in."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentResource.getMacroBodyByMacroId_get
      x-api-path-slug: contentidhistoryversionmacroidmacroid-get
      parameters:
      - in: path
        name: id
        description: The ID for the content that contains the macro
      - in: path
        name: macroId
        description: The ID of the macro
      - in: path
        name: version
        description: The version of the content that contains the macro
      responses:
        200:
          description: OK
      tags:
      - Macro
      - Body
      - By
      - Macro
      - ID
  /content/{id}/label:
    get:
      summary: Get labels for content
      description: "Returns the labels on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'View' permission for the space and permission to view the content
        if it is a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.getLabelsForContent_get
      x-api-path-slug: contentidlabel-get
      parameters:
      - in: path
        name: id
        description: The ID of the content to be queried for its labels
      - in: query
        name: limit
        description: The maximum number of labels to return per page
      - in: query
        name: prefix
        description: Filters the results to labels with the specified prefix
      - in: query
        name: start
        description: The starting index of the returned labels
      responses:
        200:
          description: OK
      tags:
      - Labelscontent
    post:
      summary: Add labels to content
      description: "Adds labels to a piece of content. Does not modify the existing
        labels.\n\nNotes:\n\n- Labels can also be added when creating content ([Create
        content](#api-content-post)).\n- Labels can be updated when updating content
        ([Update content](#api-content-id-put)). \nThis will delete the existing labels
        and replace them with the labels in \nthe request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.addLabelsToContent_post
      x-api-path-slug: contentidlabel-post
      parameters:
      - in: path
        name: id
        description: The ID of the content that will have labels added to it
      responses:
        200:
          description: OK
      tags:
      - Labels
      - To
      - Content
    delete:
      summary: Remove label from content using query parameter
      description: "Removes a label from a piece of content. This is similar to \n[Remove
        label from content](#api-content-id-label-label-delete) \nexcept that the
        label name is specified via a query parameter. \n\nUse this method if the
        label name has \"/\" characters, as \n[Remove label from content using query
        parameter](#api-content-id-label-delete) \ndoes not accept \"/\" characters
        for the label name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.removeLabelFromContentUsing
      x-api-path-slug: contentidlabel-delete
      parameters:
      - in: path
        name: id
        description: The ID of the content that the label will be removed from
      - in: query
        name: name
        description: The name of the label to be removed
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Label
      - From
      - Content
      - Using
      - Query
      - Parameter
  /content/{id}/label/{label}:
    delete:
      summary: Remove label from content
      description: "Removes a label from a piece of content. This is similar to \n[Remove
        label from content using query parameter](#api-content-id-label-delete) \nexcept
        that the label name is specified via a path parameter. \n\nUse this method
        if the label name does not have \"/\" characters, as the path \nparameter
        does not accept \"/\" characters for security reasons. Otherwise, \nuse [Remove
        label from content using query parameter](#api-content-id-label-delete).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.removeLabelFromContent_dele
      x-api-path-slug: contentidlabellabel-delete
      parameters:
      - in: path
        name: id
        description: The ID of the content that the label will be removed from
      - in: path
        name: label
        description: The name of the label to be removed
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Label
      - From
      - Content
  /content/{id}/notification/child-created:
    get:
      summary: Get watches for page
      description: "Returns the watches for a page. A user that watches a page will
        receive \nreceive notifications when the page is updated.\n\nIf you want to
        manage watches for a page, use the following `user` methods:\n\n- [Get content
        watch status for user](#api-user-watch-content-contentId-get)\n- [Add content
        watch](#api-user-watch-content-contentId-post)\n- [Remove content watch](#api-user-watch-content-contentId-delete)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentNotificationsResource.getWatchesForPage_ge
      x-api-path-slug: contentidnotificationchildcreated-get
      parameters:
      - in: path
        name: id
        description: The ID of the content to be queried for its watches
      - in: query
        name: limit
        description: The maximum number of watches to return per page
      - in: query
        name: start
        description: The starting index of the returned watches
      responses:
        200:
          description: OK
      tags:
      - Watchespage
  /content/{id}/notification/created:
    get:
      summary: Get watches for space
      description: "Returns all space watches for the space that the content is in.
        A user that \nwatches a space will receive receive notifications when any
        content in the \nspace is updated.\n\nIf you want to manage watches for a
        space, use the following `user` methods:\n\n- [Get space watch status for
        user](#api-user-watch-space-spaceKey-get)\n- [Add space watch](#api-user-watch-space-spaceKey-post)\n-
        [Remove space watch](#api-user-watch-space-spaceKey-delete)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentNotificationsResource.getWatchesForSpace_g
      x-api-path-slug: contentidnotificationcreated-get
      parameters:
      - in: path
        name: id
        description: The ID of the content to be queried for its watches
      - in: query
        name: limit
        description: The maximum number of watches to return per page
      - in: query
        name: start
        description: The starting index of the returned watches
      responses:
        200:
          description: OK
      tags:
      - Watchesspace
  /content/{id}/pagehierarchy/copy:
    post:
      summary: Copy page hierarchy
      description: |-
        Copy page hierarchy allows the copying of an entire hierarchy of pages and their associated properties, permissions and attachments.
         The id path parameter refers to the content id of the page to copy, and the new parent of this copied page is defined using the destinationPageId in the request body.
         The titleOptions object defines the rules of renaming page titles during the copy;
         for example, search and replace can be used in conjunction to rewrite the copied page titles.

         Response example:
         <pre><code>
         {
              "id" : "1180606",
              "links" : {
                   "status" : "/rest/api/longtask/1180606"
              }
         }
         </code></pre>
         Use the /longtask/<taskId> REST API to get the copy task status.
      operationId: com.atlassian.confluence.plugins.restapi.resources.PageHierarchyResource.copyPageHierarchy_post
      x-api-path-slug: contentidpagehierarchycopy-post
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Copy
      - Page
      - Hierarchy
  /content/{id}/property:
    get:
      summary: Get content properties
      description: "Returns the properties for a piece of content. For more information
        \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'View' permission for the space, and permission to view the
        content if it is a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.getContentProperties_get
      x-api-path-slug: contentidproperty-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its properties
      - in: query
        name: limit
        description: The maximum number of properties to return per page
      - in: query
        name: start
        description: The starting index of the returned properties
      responses:
        200:
          description: OK
      tags:
      - Content
      - Properties
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---