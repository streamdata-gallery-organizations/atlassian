---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Get group memberships for user
  description: "Returns the groups that a user is a member of.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
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
    post:
      summary: Create content property
      description: "Creates a property for an existing piece of content. For more
        information \nabout content properties, see [Content properties in the REST
        API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis
        is the same as [Create content property for key](#api-content-id-property-key-post)
        \nexcept that the key is specified in the request body instead of as a \npath
        parameter.\n\nContent properties can also be added when creating a new piece
        of content \nby including them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.createContentProperty_pos
      x-api-path-slug: contentidproperty-post
      parameters:
      - in: path
        name: id
        description: The ID of the content to add the property to
      responses:
        200:
          description: OK
      tags:
      - Content
      - Property
  /content/{id}/property/{key}:
    get:
      summary: Get content property
      description: "Returns a content property for a piece of content. For more information,
        see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'View' permission for the space, and permission to view the
        content if it is a page."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.getContentProperty_get
      x-api-path-slug: contentidpropertykey-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          to expand
      - in: path
        name: id
        description: The ID of the content to be queried for the property
      - in: path
        name: key
        description: The key of the content property
      responses:
        200:
          description: OK
      tags:
      - Content
      - Property
    post:
      summary: Create content property for key
      description: "Creates a property for an existing piece of content. For more
        information \nabout content properties, see [Content properties in the REST
        API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis
        is the same as [Create content property](#api-content-id-property-post) \nexcept
        that the key is specified as a path parameter instead of in the \nrequest
        body.\n\nContent properties can also be added when creating a new piece of
        content \nby including them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.createContentPropertyForK
      x-api-path-slug: contentidpropertykey-post
      parameters:
      - in: path
        name: id
        description: The ID of the content to add the property to
      - in: path
        name: key
        description: The key of the content property
      responses:
        200:
          description: OK
      tags:
      - Content
      - Propertykey
    put:
      summary: Update content property
      description: "Updates an existing content property. This method will also create
        a new \nproperty for a piece of content, if the property key does not exist
        and \nthe property version is 1. For more information about content properties,
        see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.updateContentProperty_put
      x-api-path-slug: contentidpropertykey-put
      parameters:
      - in: path
        name: id
        description: The ID of the content that the property belongs to
      - in: path
        name: key
        description: The key of the property
      responses:
        200:
          description: OK
      tags:
      - Content
      - Property
    delete:
      summary: Delete content property
      description: "Deletes a content property. For more information about content
        properties, see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.deleteContentProperty_del
      x-api-path-slug: contentidpropertykey-delete
      parameters:
      - in: path
        name: id
        description: The ID of the content that the property belongs to
      - in: path
        name: key
        description: The key of the property
      responses:
        200:
          description: OK
      tags:
      - Content
      - Property
  /content/{id}/restriction:
    get:
      summary: Get restrictions
      description: "Returns the restrictions on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getRestrictions_get
      x-api-path-slug: contentidrestriction-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          restrictions to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its restrictions
      - in: query
        name: limit
        description: The maximum number of users and the maximum number of groups,
          in the returned restrictions, to return per page
      - in: query
        name: start
        description: The starting index of the users and groups in the returned restrictions
      responses:
        200:
          description: OK
      tags:
      - Restrictions
    post:
      summary: Add restrictions
      description: "Adds restrictions to a piece of content. Note, this does not change
        any \nexisting restrictions on the content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.addRestrictions_post
      x-api-path-slug: contentidrestriction-post
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          restrictions (returned in response) to expand
      - in: path
        name: id
        description: The ID of the content to add restrictions to
      responses:
        200:
          description: OK
      tags:
      - Restrictions
    put:
      summary: Update restrictions
      description: "Updates restrictions for a piece of content. This removes the
        existing \nrestrictions and replaces them with the restrictions in the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.updateRestrictions_put
      x-api-path-slug: contentidrestriction-put
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          restrictions (returned in response) to expand
      - in: path
        name: id
        description: The ID of the content to update restrictions for
      responses:
        200:
          description: OK
      tags:
      - Restrictions
    delete:
      summary: Delete restrictions
      description: "Removes all restrictions (read and update) on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.deleteRestrictions_del
      x-api-path-slug: contentidrestriction-delete
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          restrictions (returned in response) to expand
      - in: path
        name: id
        description: The ID of the content to remove restrictions from
      responses:
        200:
          description: OK
      tags:
      - Restrictions
  /content/{id}/restriction/byOperation:
    get:
      summary: Get restrictions by operation
      description: "Returns restrictions on a piece of content by operation. This
        method is \nsimilar to [Get restrictions](#api-content-id-restriction-get)
        except that \nthe operations are properties of the return object, rather than
        items in \na results array. \n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getRestrictionsByOpera
      x-api-path-slug: contentidrestrictionbyoperation-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          restrictions to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its restrictions
      responses:
        200:
          description: OK
      tags:
      - Restrictions
      - By
      - Operation
  /content/{id}/restriction/byOperation/{operationKey}:
    get:
      summary: Get restrictions for operation
      description: "Returns the restictions on a piece of content for a given operation
        (read \nor update).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getRestrictionsForOper
      x-api-path-slug: contentidrestrictionbyoperationoperationkey-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          restrictions to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its restrictions
      - in: query
        name: limit
        description: The maximum number of users and the maximum number of groups,
          in the returned restrictions, to return per page
      - in: path
        name: operationKey
        description: The operation type of the restrictions to be returned
      - in: query
        name: start
        description: The starting index of the users and groups in the returned restrictions
      responses:
        200:
          description: OK
      tags:
      - Restrictionsoperation
  /content/{id}/restriction/byOperation/{operationKey}/group/{groupName}:
    get:
      summary: Get content restriction status for group
      description: "Returns whether the specified content restriction applies to a
        group. \nFor example, if the 'admins' group has permission to read a page
        with an \nID of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/group/admins`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getContentRestrictionS
      x-api-path-slug: contentidrestrictionbyoperationoperationkeygroupgroupname-get
      parameters:
      - in: path
        name: groupName
        description: The name of the group to be queried for whether the content restriction
          applies to it
      - in: path
        name: id
        description: The ID of the content that the restriction applies to
      - in: path
        name: operationKey
        description: The operation that the restriction applies to
      responses:
        200:
          description: OK
      tags:
      - Content
      - Restriction
      - Statusgroup
    put:
      summary: Add group to content restriction
      description: "Adds a group to a content restriction. That is, grant read or
        update \npermission to the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.addGroupToContentRestr
      x-api-path-slug: contentidrestrictionbyoperationoperationkeygroupgroupname-put
      parameters:
      - in: path
        name: groupName
        description: The name of the group to add to the content restriction
      - in: path
        name: id
        description: The ID of the content that the restriction applies to
      - in: path
        name: operationKey
        description: The operation that the restriction applies to
      responses:
        200:
          description: OK
      tags:
      - Group
      - To
      - Content
      - Restriction
    delete:
      summary: Remove group from content restriction
      description: "Removes a group from a content restriction. That is, remove read
        or update \npermission for the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.removeGroupFromContent
      x-api-path-slug: contentidrestrictionbyoperationoperationkeygroupgroupname-delete
      parameters:
      - in: path
        name: groupName
        description: The name of the group to remove from the content restriction
      - in: path
        name: id
        description: The ID of the content that the restriction applies to
      - in: path
        name: operationKey
        description: The operation that the restriction applies to
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Group
      - From
      - Content
      - Restriction
  /content/{id}/restriction/byOperation/{operationKey}/user:
    get:
      summary: Get content restriction status for user
      description: "Returns whether the specified content restriction applies to a
        user. \nFor example, if the user 'admin' has permission to read a page with
        an \nID of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/user?username=admin`\n\nOne
        of `key`, `username`, or `accountId` must be specified as a query \nparameter
        to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getContentRestrictionS
      x-api-path-slug: contentidrestrictionbyoperationoperationkeyuser-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user to be queried for whether the content
          restriction applies to it
      - in: path
        name: id
        description: The ID of the content that the restriction applies to
      - in: query
        name: key
        description: The key of the user to be queried for whether the content restriction
          applies to it
      - in: path
        name: operationKey
        description: The operation that is restricted
      - in: query
        name: userName
        description: The username of the user to be queried for whether the content
          restriction applies to it
      responses:
        200:
          description: OK
      tags:
      - Content
      - Restriction
      - Statususer
    put:
      summary: Add user to content restriction
      description: "Adds a user to a content restriction. That is, grant read or update
        \npermission to the user for a piece of content.\n\nOne of `key`, `username`,
        or `accountId` must be specified as a query \nparameter to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.addUserToContentRestri
      x-api-path-slug: contentidrestrictionbyoperationoperationkeyuser-put
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user to add to the content restriction
      - in: path
        name: id
        description: The ID of the content that the restriction applies to
      - in: query
        name: key
        description: The key of the user to add to the content restriction
      - in: path
        name: operationKey
        description: The operation that the restriction applies to
      - in: query
        name: userName
        description: The username of the user to add to the content restriction
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - Content
      - Restriction
    delete:
      summary: Remove user from content restriction
      description: "Removes a group from a content restriction. That is, remove read
        or update \npermission for the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to edit the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.removeUserFromContentR
      x-api-path-slug: contentidrestrictionbyoperationoperationkeyuser-delete
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user to remove from the content restriction
      - in: path
        name: id
        description: The ID of the content that the restriction applies to
      - in: query
        name: key
        description: The key of the user to remove from the content restriction
      - in: path
        name: operationKey
        description: The operation that the restriction applies to
      - in: query
        name: userName
        description: The username of the user to remove from the content restriction
      responses:
        200:
          description: OK
      tags:
      - Remove
      - User
      - From
      - Content
      - Restriction
  /content/{id}/version:
    get:
      summary: Get content versions
      description: "Returns the versions for a piece of content in descending order.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content. If the content is a blog post,
        'View' permission \nfor the space is required."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.getContentVersions_get
      x-api-path-slug: contentidversion-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its versions
      - in: query
        name: limit
        description: The maximum number of versions to return per page
      - in: query
        name: start
        description: The starting index of the returned versions
      responses:
        200:
          description: OK
      tags:
      - Content
      - Versions
    post:
      summary: Restore content version
      description: "Restores a historical version to be the latest version. That is,
        a new version \nis created with the content of the historical version.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.restoreContentVersion_post
      x-api-path-slug: contentidversion-post
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the returnedcontent
          to expand
      - in: path
        name: id
        description: The ID of the content for which the history will be restored
      responses:
        200:
          description: OK
      tags:
      - Restore
      - Content
      - Version
  /content/{id}/version/{versionNumber}:
    get:
      summary: Get content version
      description: "Returns a version for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the content. If the content is a blog post,
        'View' permission \nfor the space is required."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.getContentVersion_get
      x-api-path-slug: contentidversionversionnumber-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the content
          to expand
      - in: path
        name: id
        description: The ID of the content to be queried for its version
      - in: path
        name: versionNumber
        description: The number of the version to be retrieved
      responses:
        200:
          description: OK
      tags:
      - Content
      - Version
    delete:
      summary: Delete content version
      description: "Delete a historical version. This does not delete the changes
        made to the \ncontent in that version, rather the changes for the deleted
        version are \nrolled up into the next version. Note, you cannot delete the
        current version.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to update the content."
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.deleteContentVersion_delet
      x-api-path-slug: contentidversionversionnumber-delete
      parameters:
      - in: path
        name: id
        description: The ID of the content that the version will be deleted from
      - in: path
        name: versionNumber
        description: The number of the version to be deleted
      responses:
        200:
          description: OK
      tags:
      - Content
      - Version
  /contentbody/convert/{to}:
    post:
      summary: Convert content body
      description: |-
        Converts a content body from one format to another format.

        Supported conversions:

        - storage: view, export_view, styled_view, editor
        - editor: storage
        - view: none
        - export_view: none
        - styled_view: none

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        If request specifies 'contentIdContext', 'View' permission for the space, and permission to view the content.
      operationId: com.atlassian.confluence.plugins.restapi.resources.ContentBodyResource.convertContentBody_post
      x-api-path-slug: contentbodyconvertto-post
      parameters:
      - in: query
        name: contentIdContext
        description: The content ID used to find the space for resolving embedded
          content (page includes, files, and links) in the content body
      - in: query
        name: embeddedContentRender
        description: Mode used for rendering embedded content, like attachments
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the new
          content to expand
      - in: query
        name: spaceKeyContext
        description: The space key used for resolving embedded content (page includes,
          files, and links) in the content body
      - in: path
        name: to
        description: The name of the target format for the content body
      responses:
        200:
          description: OK
      tags:
      - Convert
      - Content
      - Body
  /group:
    get:
      summary: Get groups
      description: |-
        Returns all user groups. The returned groups are ordered alphabetically in
        ascending order by group name.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        Permission to access the Confluence site ('Can use' global permission).
      operationId: com.atlassian.confluence.plugins.restapi.resources.GroupResource.getGroups_get
      x-api-path-slug: group-get
      parameters:
      - in: query
        name: limit
        description: The maximum number of groups to return per page
      - in: query
        name: start
        description: The starting index of the returned groups
      responses:
        200:
          description: OK
      tags:
      - Groups
  /group/{groupName}:
    get:
      summary: Get group
      description: |-
        Returns a user group for a given group name.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        Permission to access the Confluence site ('Can use' global permission).
      operationId: com.atlassian.confluence.plugins.restapi.resources.GroupResource.getGroup_get
      x-api-path-slug: groupgroupname-get
      parameters:
      - in: path
        name: groupName
        description: The name of the group
      responses:
        200:
          description: OK
      tags:
      - Group
  /group/{groupName}/member:
    get:
      summary: Get group members
      description: |-
        Returns the users that are members of a group.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        Permission to access the Confluence site ('Can use' global permission).
      operationId: com.atlassian.confluence.plugins.restapi.resources.GroupResource.getGroupMembers_get
      x-api-path-slug: groupgroupnamemember-get
      parameters:
      - in: path
        name: groupName
        description: The name of the group to be queried for its members
      - in: query
        name: limit
        description: The maximum number of users to return per page
      - in: query
        name: start
        description: The starting index of the returned users
      responses:
        200:
          description: OK
      tags:
      - Group
      - Members
  /longtask:
    get:
      summary: Get long-running tasks
      description: "Returns information about all active long-running tasks (e.g.
        space export), \nsuch as how long each task has been running and the percentage
        of each task \nthat has completed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.LongTaskResource.getTasks_get
      x-api-path-slug: longtask-get
      parameters:
      - in: query
        name: limit
        description: The maximum number of tasks to return per page
      - in: query
        name: start
        description: The starting index of the returned tasks
      responses:
        200:
          description: OK
      tags:
      - Long-running
      - Tasks
  /longtask/{id}:
    get:
      summary: Get long-running task
      description: "Returns information about an active long-running task (e.g. space
        export), \nsuch as how long it has been running and the percentage of the
        task that \nhas completed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.LongTaskResource.getTask_get
      x-api-path-slug: longtaskid-get
      parameters:
      - in: path
        name: id
        description: The ID of the task
      responses:
        200:
          description: OK
      tags:
      - Long-running
      - Task
  /relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}:
    get:
      summary: Find target entities related to a source entity
      description: "Returns all target entities that have a particular relationship
        to the \nsource entity. Note, relationships are one way.\n\nFor example, the
        following method finds all content that the current user \nhas an 'ignore'
        relationship with:\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/ignore/from/user/current/to/content`\nNote,
        'ignore' is an example custom relationship type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view both the target entity and source entity."
      operationId: com.atlassian.confluence.plugins.restapi.resources.RelationResource.findTargetFromSource_get
      x-api-path-slug: relationrelationnamefromsourcetypesourcekeytotargettype-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the response
          object to expand
      - in: query
        name: limit
        description: The maximum number of relationships to return per page
      - in: path
        name: relationName
        description: The name of the relationship
      - in: path
        name: sourceKey
        description: '- The identifier for the source entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: sourceStatus
        description: The status of the source
      - in: path
        name: sourceType
        description: The source entity type of the relationship
      - in: query
        name: sourceVersion
        description: The version of the source
      - in: query
        name: start
        description: The starting index of the returned relationships
      - in: query
        name: targetStatus
        description: The status of the target
      - in: path
        name: targetType
        description: The target entity type of the relationship
      - in: query
        name: targetVersion
        description: The version of the target
      responses:
        200:
          description: OK
      tags:
      - Find
      - Target
      - Entities
      - Related
      - To
      - Source
      - Entity
  /relation/{relationName}/from/{sourceType}/{sourceKey}/to/{targetType}/{targetKey}:
    get:
      summary: Find relationship from source to target
      description: "Find whether a particular type of relationship exists from a source
        \nentity to a target entity. Note, relationships are one way.\n\nFor example,
        you can use this method to find whether the current user has \nselected a
        particular page as a favorite (i.e. 'save for later'):\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/favourite/from/user/current/to/content/123`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view both the target entity and source entity."
      operationId: com.atlassian.confluence.plugins.restapi.resources.RelationResource.GetRelationship_get
      x-api-path-slug: relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the response
          object to expand
      - in: path
        name: relationName
        description: The name of the relationship
      - in: path
        name: sourceKey
        description: '- The identifier for the source entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: sourceStatus
        description: The status of the source
      - in: path
        name: sourceType
        description: The source entity type of the relationship
      - in: query
        name: sourceVersion
        description: The version of the source
      - in: path
        name: targetKey
        description: '- The identifier for the target entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: targetStatus
        description: The status of the target
      - in: path
        name: targetType
        description: The target entity type of the relationship
      - in: query
        name: targetVersion
        description: The version of the target
      responses:
        200:
          description: OK
      tags:
      - Find
      - Relationship
      - From
      - Source
      - To
      - Target
    put:
      summary: Create relationship
      description: "Creates a relationship between two entities (user, space, content).
        The \n'favourite' relationship is supported by default, but you can use this
        method \nto create any type of relationship between two entities.\n\nFor example,
        the following method creates a 'sibling' relationship between \ntwo pieces
        of content:\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/sibling/from/content/123/to/content/456`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.RelationResource.createRelationship_put
      x-api-path-slug: relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-put
      parameters:
      - in: path
        name: relationName
        description: The name of the relationship
      - in: path
        name: sourceKey
        description: '- The identifier for the source entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: sourceStatus
        description: The status of the source
      - in: path
        name: sourceType
        description: The source entity type of the relationship
      - in: query
        name: sourceVersion
        description: The version of the source
      - in: path
        name: targetKey
        description: '- The identifier for the target entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: targetStatus
        description: The status of the target
      - in: path
        name: targetType
        description: The target entity type of the relationship
      - in: query
        name: targetVersion
        description: The version of the target
      responses:
        200:
          description: OK
      tags:
      - Relationship
    delete:
      summary: Delete
      description: "Deletes a relationship between two entities (user, space, content).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission).
        \nFor favourite relationships, the current user can only delete their own
        \nfavourite relationships. A space administrator can delete favourite \nrelationships
        for any user."
      operationId: com.atlassian.confluence.plugins.restapi.resources.RelationResource.delete_delete
      x-api-path-slug: relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-delete
      parameters:
      - in: path
        name: relationName
        description: The name of the relationship
      - in: path
        name: sourceKey
        description: '- The identifier for the source entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: sourceStatus
        description: The status of the source
      - in: path
        name: sourceType
        description: The source entity type of the relationship
      - in: query
        name: sourceVersion
        description: The version of the source
      - in: path
        name: targetKey
        description: '- The identifier for the target entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: targetStatus
        description: The status of the target
      - in: path
        name: targetType
        description: The target entity type of the relationship
      - in: query
        name: targetVersion
        description: The version of the target
      responses:
        200:
          description: OK
      tags:
      - ""
  /relation/{relationName}/to/{targetType}/{targetKey}/from/{sourceType}:
    get:
      summary: Find target entities related to a source entity
      description: "Returns all target entities that have a particular relationship
        to the \nsource entity. Note, relationships are one way.\n\nFor example, the
        following method finds all users that have a 'collaborator' \nrelationship
        to a piece of content with an ID of '1234':\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/collaborator/to/content/1234/from/user`\nNote,
        'collaborator' is an example custom relationship type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view both the target entity and source entity."
      operationId: com.atlassian.confluence.plugins.restapi.resources.RelationResource.findSourcesForTarget_get
      x-api-path-slug: relationrelationnametotargettypetargetkeyfromsourcetype-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the response
          object to expand
      - in: query
        name: limit
        description: The maximum number of relationships to return per page
      - in: path
        name: relationName
        description: The name of the relationship
      - in: query
        name: sourceStatus
        description: The status of the source
      - in: path
        name: sourceType
        description: The source entity type of the relationship
      - in: query
        name: sourceVersion
        description: The version of the source
      - in: query
        name: start
        description: The starting index of the returned relationships
      - in: path
        name: targetKey
        description: '- The identifier for the target entity:- If `sourceType` is
          user, then specify either current (logged-in   user) or the user key'
      - in: query
        name: targetStatus
        description: The status of the target
      - in: path
        name: targetType
        description: The target entity type of the relationship
      - in: query
        name: targetVersion
        description: The version of the target
      responses:
        200:
          description: OK
      tags:
      - Find
      - Target
      - Entities
      - Related
      - To
      - Source
      - Entity
  /search:
    get:
      summary: Search
      description: "Searches for content using the \n[Confluence Query Language (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to view the entities. Note, only entities that the
        user has \npermission to view will be returned."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SearchResource.search_get
      x-api-path-slug: search-get
      parameters:
      - in: query
        name: cql
        description: The CQL query to be used for the search
      - in: query
        name: cqlcontext
        description: The space, content, and content status to execute the searchagainst
      - in: query
        name: includeArchivedSpaces
        description: Include content from archived spaces in the results
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
  /settings/lookandfeel:
    get:
      summary: Get look and feel settings
      description: "Returns the look and feel settings for the site or a single space.
        This \nincludes attributes such as the color scheme, padding, and border radius.\n\nThe
        look and feel settings for a space can be inherited from the global \nlook
        and feel settings or provided by a theme.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nNone"
      operationId: com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.getLookAndFeelSettings_get
      x-api-path-slug: settingslookandfeel-get
      parameters:
      - in: query
        name: spaceKey
        description: The key of the space for which the look and feel settings will
          bereturned
      responses:
        200:
          description: OK
      tags:
      - Look
      - Feel
      - Settings
  /settings/lookandfeel/custom:
    post:
      summary: Update look and feel settings
      description: "Updates the look and feel settings for the site or for a single
        space.\nIf custom settings exist, they are updated. If no custom settings
        exist, \nthen a set of custom settings is created.\n\nNote, if a theme is
        selected for a space, the space look and feel settings \nare provided by the
        theme and cannot be overridden.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Admin' permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.updateLookAndFeelSettings_pos
      x-api-path-slug: settingslookandfeelcustom-post
      parameters:
      - in: query
        name: spaceKey
        description: The key of the space for which the look and feel settings will
          beupdated
      responses:
        200:
          description: OK
      tags:
      - Look
      - Feel
      - Settings
    delete:
      summary: Reset look and feel settings
      description: "Resets the custom look and feel settings for the site or a single
        space.\nThis changes the values of the custom settings to be the same as the
        \ndefault settings. It does not change which settings (default or custom)
        \nare selected. Note, the default space settings are inherited from the \ncurrent
        global settings.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Admin' permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.resetLookAndFeelSettings_dele
      x-api-path-slug: settingslookandfeelcustom-delete
      parameters:
      - in: query
        name: spaceKey
        description: The key of the space for which the look and feel settings will
          bereset
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Look
      - Feel
      - Settings
  /settings/lookandfeel/selected:
    put:
      summary: Set look and feel settings
      description: "Sets the look and feel settings to either the default settings
        or the\ncustom settings, for the site or a single space. Note, the default
        \nspace settings are inherited from the current global settings.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Admin' permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.setLookAndFeelSettings_put
      x-api-path-slug: settingslookandfeelselected-put
      parameters:
      - in: query
        name: spaceKey
        description: The key of the space for which the look and feel settings will
          beset
      responses:
        200:
          description: OK
      tags:
      - Set
      - Look
      - Feel
      - Settings
  /settings/systemInfo:
    get:
      summary: Get system info
      description: "Returns the system information for the Confluence Cloud tenant.
        This\ninformation is used by Atlassian.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SystemInfoResource.getSystemInfo_get
      x-api-path-slug: settingssysteminfo-get
      responses:
        200:
          description: OK
      tags:
      - System
      - Info
  /settings/theme:
    get:
      summary: Get themes
      description: |-
        Returns all themes, not including the default theme.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
      operationId: com.atlassian.confluence.plugins.restapi.resources.ThemeResource.getThemes_get
      x-api-path-slug: settingstheme-get
      parameters:
      - in: query
        name: limit
        description: The maximum number of themes to return per page
      - in: query
        name: start
        description: The starting index of the returned themes
      responses:
        200:
          description: OK
      tags:
      - Themes
  /settings/theme/selected:
    get:
      summary: Get global theme
      description: |-
        Returns the globally assigned theme.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
      operationId: com.atlassian.confluence.plugins.restapi.resources.ThemeResource.getGlobalTheme_get
      x-api-path-slug: settingsthemeselected-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Theme
  /settings/theme/{themeKey}:
    get:
      summary: Get theme
      description: |-
        Returns a theme. This includes information about the theme name,
        description, and icon.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
      operationId: com.atlassian.confluence.plugins.restapi.resources.ThemeResource.getTheme_get
      x-api-path-slug: settingsthemethemekey-get
      parameters:
      - in: path
        name: themeKey
        description: The key of the theme to be returned
      responses:
        200:
          description: OK
      tags:
      - Theme
  /space:
    get:
      summary: Get spaces
      description: |-
        Returns all spaces. The returned spaces are ordered alphabetically in
        ascending order by space key.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        Permission to access the Confluence site ('Can use' global permission).
        Note, the returned list will only contain spaces that the current user
        has permission to view.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpaces_get
      x-api-path-slug: space-get
      parameters:
      - in: query
        name: expand
        description: 'A multi-value parameter indicating which properties of the spaces
          toexpand, where:  - `settings` returns the settings for the space, similar
          to [Get space settings](#api-space-spaceKey-settings-get)'
      - in: query
        name: favourite
        description: Filter the results to the favourite spaces of the user specified
          by`favouriteUserKey`
      - in: query
        name: favouriteUserKey
        description: The userKey of the user, whose favourite spaces are used to filterthe
          results when using the `favourite` parameter
      - in: query
        name: label
        description: Filter the results to spaces based on their label
      - in: query
        name: limit
        description: The maximum number of spaces to return per page
      - in: query
        name: spaceKey
        description: The key of the space to be returned
      - in: query
        name: start
        description: The starting index of the returned spaces
      - in: query
        name: status
        description: Filter the results to spaces based on their status
      - in: query
        name: type
        description: Filter the results to spaces based on their type
      responses:
        200:
          description: OK
      tags:
      - Spaces
    post:
      summary: Create space
      description: |-
        Creates a new space. Note, currently you cannot set space labels when
        creating a space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Create Space(s)' global permission.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.createSpace_post
      x-api-path-slug: space-post
      responses:
        200:
          description: OK
      tags:
      - Space
  /space/_private:
    post:
      summary: Create private space
      description: |-
        Creates a new space that is only visible to the creator. This method is
        the same as the [Create space](#api-space-post) method with permissions
        set to the current user only. Note, currently you cannot set space
        labels when creating a space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Create Space(s)' global permission.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.createPrivateSpace_post
      x-api-path-slug: space-private-post
      responses:
        200:
          description: OK
      tags:
      - Private
      - Space
  /space/{spaceKey}:
    get:
      summary: Get space
      description: |-
        Returns a space. This includes information like the name, description,
        and permissions, but not the content in the space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'View' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpace_get
      x-api-path-slug: spacespacekey-get
      parameters:
      - in: query
        name: expand
        description: 'A multi-value parameter indicating which properties of the space
          toexpand, where:  - `settings` returns the settings for the space, similar
          to [Get space settings](#api-space-spaceKey-settings-get)'
      - in: path
        name: spaceKey
        description: The key of the space to be returned
      responses:
        200:
          description: OK
      tags:
      - Space
    put:
      summary: Update space
      description: |-
        Updates the name, description, or homepage of a space.

        -   For security reasons, permissions cannot be updated via the API and
        must be changed via the user interface instead.
        -   Currently you cannot set space labels when updating a space.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Admin' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.updateSpace_put
      x-api-path-slug: spacespacekey-put
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to update
      responses:
        200:
          description: OK
      tags:
      - Space
    delete:
      summary: Delete space
      description: |-
        Deletes a space. Note, the space will be deleted in a long running task.
        Therefore, the space may not be deleted yet when this method has
        returned. Clients should poll the status link that is returned in the
        response until the task completes.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Admin' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.deleteSpace_delete
      x-api-path-slug: spacespacekey-delete
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to delete
      responses:
        200:
          description: OK
      tags:
      - Space
  /space/{spaceKey}/content:
    get:
      summary: Get content for space
      description: |-
        Returns all content in a space. The returned content is grouped by type
        (pages then blogposts), then ordered by content ID in ascending order.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'View' permission for the space. Note, the returned list will only
        contain content that the current user has permission to view.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getContentForSpace_get
      x-api-path-slug: spacespacekeycontent-get
      parameters:
      - in: query
        name: depth
        description: Filter the results to content at the root level of the space
          or all content
      - in: query
        name: expand
        description: 'A multi-value parameter indicating which properties of the contentto
          expand, where:  - `childTypes'
      - in: query
        name: limit
        description: The maximum number of content objects to return per page
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its content
      - in: query
        name: start
        description: The starting index of the returned content
      responses:
        200:
          description: OK
      tags:
      - Contentspace
  /space/{spaceKey}/content/{type}:
    get:
      summary: Get content by type for space
      description: |-
        Returns all content of a given type, in a space. The returned content is
        ordered by content ID in ascending order.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'View' permission for the space. Note, the returned list will only
        contain content that the current user has permission to view.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getContentByTypeForSpace_get
      x-api-path-slug: spacespacekeycontenttype-get
      parameters:
      - in: query
        name: depth
        description: Filter the results to content at the root level of the space
          or allcontent
      - in: query
        name: expand
        description: 'A multi-value parameter indicating which properties of the contentto
          expand, where:  - `childTypes'
      - in: query
        name: limit
        description: The maximum number of content objects to return per page
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its content
      - in: query
        name: start
        description: The starting index of the returned content
      - in: path
        name: type
        description: The type of content to return
      responses:
        200:
          description: OK
      tags:
      - Content
      - By
      - Typespace
  /space/{spaceKey}/property:
    get:
      summary: Get space properties
      description: "Returns all properties for the given space. Space properties are
        a key-value storage associated with a space.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
        \u2018View\u2019 permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.getSpaceProperties_get
      x-api-path-slug: spacespacekeyproperty-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the spaceproperty
          to expand
      - in: query
        name: limit
        description: The maximum number of properties to return per page
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its properties
      - in: query
        name: start
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Space
      - Properties
    post:
      summary: Create space property
      description: "Creates a new space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.createSpaceProperty_post
      x-api-path-slug: spacespacekeyproperty-post
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space that the property will be created in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
  /space/{spaceKey}/property/{key}:
    get:
      summary: Get space property
      description: "Returns a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
        \u2018View\u2019 permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.getSpaceProperty_get
      x-api-path-slug: spacespacekeypropertykey-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the spaceproperty
          to expand
      - in: path
        name: key
        description: The key of the space property
      - in: path
        name: spaceKey
        description: The key of the space that the property is in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
    post:
      summary: Create space property for key
      description: "Creates a new space property. This is the same as `POST\n/space/{spaceKey}/property`
        but the key for the property is passed as a\npath parameter, rather than in
        the request body.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.createSpacePropertyForKey_p
      x-api-path-slug: spacespacekeypropertykey-post
      parameters:
      - in: path
        name: key
        description: The key of the property to be created
      - in: path
        name: spaceKey
        description: The key of the space that the property will be created in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Propertykey
    put:
      summary: Update space property
      description: "Updates a space property. Note, you cannot update the key of a
        space\nproperty, only the value.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.updateSpaceProperty_put
      x-api-path-slug: spacespacekeypropertykey-put
      parameters:
      - in: path
        name: key
        description: The key of the property to be updated
      - in: path
        name: spaceKey
        description: The key of the space that the property is in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
    delete:
      summary: Delete space property
      description: "Deletes a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
        permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.deleteSpaceProperty_delete
      x-api-path-slug: spacespacekeypropertykey-delete
      parameters:
      - in: path
        name: key
        description: The key of the property to be deleted
      - in: path
        name: spaceKey
        description: The key of the space that the property is in
      responses:
        200:
          description: OK
      tags:
      - Space
      - Property
  /space/{spaceKey}/settings:
    get:
      summary: Get space settings
      description: |-
        Returns the settings of a space. Currently only the
        `routeOverrideEnabled` setting can be returned.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'View' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpaceSettings_get
      x-api-path-slug: spacespacekeysettings-get
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its settings
      responses:
        200:
          description: OK
      tags:
      - Space
      - Settings
    put:
      summary: Update space settings
      description: |-
        Updates the settings for a space. Currently only the
        `routeOverrideEnabled` setting can be updated.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        'Admin' permission for the space.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.updateSpaceSettings_put
      x-api-path-slug: spacespacekeysettings-put
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space whose settings will be updated
      responses:
        200:
          description: OK
      tags:
      - Space
      - Settings
  /space/{spaceKey}/theme:
    get:
      summary: Get space theme
      description: "Returns the theme selected for a space, if one is set. If no space
        \ntheme is set, this means that the space is inheriting the global look \nand
        feel settings.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
        \u2018View\u2019 permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.getSpaceTheme_get
      x-api-path-slug: spacespacekeytheme-get
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to be queried for its theme
      responses:
        200:
          description: OK
      tags:
      - Space
      - Theme
    put:
      summary: Set space theme
      description: "Sets the theme for a space. Note, if you want to reset the space
        theme to \nthe default Confluence theme, use the 'Reset space theme' method
        instead \nof this method.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\n'Admin' permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.setSpaceTheme_put
      x-api-path-slug: spacespacekeytheme-put
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to set the theme for
      responses:
        200:
          description: OK
      tags:
      - Set
      - Space
      - Theme
    delete:
      summary: Reset space theme
      description: "Resets the space theme. This means that the space will inherit
        the \nglobal look and feel settings\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**:\n'Admin' permission for the space."
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.resetSpaceTheme_delete
      x-api-path-slug: spacespacekeytheme-delete
      parameters:
      - in: path
        name: spaceKey
        description: The key of the space to reset the theme for
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Space
      - Theme
  /template:
    post:
      summary: Create content template
      description: "Creates a new content template. Note, blueprint templates cannot
        be created via the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Admin' permission for the space to create a space template
        or 'Confluence Administrator' \nglobal permission to create a global template."
      operationId: com.atlassian.confluence.plugins.restapi.resources.TemplateResource.createContentTemplate_post
      x-api-path-slug: template-post
      responses:
        200:
          description: OK
      tags:
      - Content
      - Template
    put:
      summary: Update content template
      description: "Updates a content template. Note, blueprint templates cannot be
        updated\nvia the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Admin' permission for the space to create a space template
        or 'Confluence Administrator' \nglobal permission to create a global template."
      operationId: com.atlassian.confluence.plugins.restapi.resources.TemplateResource.updateContentTemplate_put
      x-api-path-slug: template-put
      responses:
        200:
          description: OK
      tags:
      - Content
      - Template
  /template/blueprint:
    get:
      summary: Get blueprint templates
      description: "Returns all templates provided by blueprints. Use this method
        to retrieve \nall global blueprint templates or all blueprint templates in
        a space.\n\nNote, all global blueprints are inherited by each space. Space
        blueprints \ncan be customised without affecting the global blueprints.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getBlueprintTemplates_get
      x-api-path-slug: templateblueprint-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the templateto
          expand
      - in: query
        name: limit
        description: The maximum number of templates to return per page
      - in: query
        name: spaceKey
        description: The key of the space to be queried for templates
      - in: query
        name: start
        description: The starting index of the returned templates
      responses:
        200:
          description: OK
      tags:
      - Blueprint
      - Templates
  /template/page:
    get:
      summary: Get content templates
      description: "Returns all content templates. Use this method to retrieve all
        global\ncontent templates or all content templates in a space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Admin' permission for the space to view space templates and
        'Confluence \nAdministrator' global permission to view global templates."
      operationId: com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getContentTemplates_get
      x-api-path-slug: templatepage-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the templateto
          expand
      - in: query
        name: limit
        description: The maximum number of templates to return per page
      - in: query
        name: spaceKey
        description: The key of the space to be queried for templates
      - in: query
        name: start
        description: The starting index of the returned templates
      responses:
        200:
          description: OK
      tags:
      - Content
      - Templates
  /template/{contentTemplateId}:
    get:
      summary: Get content template
      description: "Returns a content template. This includes information about template,
        \nlike the name, the space or blueprint that the template is in, the body
        \nof the template, and more.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Admin' permission for the space to view space templates and
        'Confluence \nAdministrator' global permission to view global templates."
      operationId: com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getContentTemplate_get
      x-api-path-slug: templatecontenttemplateid-get
      parameters:
      - in: path
        name: contentTemplateId
        description: The ID of the content template to be returned
      responses:
        200:
          description: OK
      tags:
      - Content
      - Template
    delete:
      summary: Remove template
      description: "Deletes a template. This results in different actions depending
        on the \ntype of template:\n\n- If the template is a content template, it
        is deleted.\n- If the template is a modified space-level blueprint template,
        it reverts \nto the template inherited from the global-level blueprint template.\n-
        If the template is a modified global-level blueprint template, it reverts
        \nto the default global-level blueprint template.\n\n Note, unmodified blueprint
        templates cannot be deleted."
      operationId: com.atlassian.confluence.plugins.restapi.resources.TemplateResource.removeTemplate_delete
      x-api-path-slug: templatecontenttemplateid-delete
      parameters:
      - in: path
        name: contentTemplateId
        description: The ID of the template to be deleted
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Template
  /user:
    get:
      summary: Get user
      description: "Returns a user. This includes information about the user, like
        the\ndisplay name, userKey, account ID, profile picture, and more.\n\nThe
        `username`, `key`, or `accountId` parameter must be specified, in \norder
        to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserResource.getUser_get
      x-api-path-slug: user-get
      parameters:
      - in: query
        name: accountId
        description: The accountId of the user to be returned
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the user
          toexpand
      - in: query
        name: key
        description: The userKey of the user to be returned
      - in: query
        name: username
        description: The username of the user to be returned
      responses:
        200:
          description: OK
      tags:
      - User
  /user/anonymous:
    get:
      summary: Get anonymous user
      description: "Returns information about how anonymous users are represented,
        like the\nprofile picture and display name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserResource.getAnonymousUser_get
      x-api-path-slug: useranonymous-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the user
          toexpand
      responses:
        200:
          description: OK
      tags:
      - Anonymous
      - User
  /user/current:
    get:
      summary: Get current user
      description: "Returns the currently logged-in user. This includes information
        about\nthe user, like the display name, userKey, account ID, profile picture,\nand
        more.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        \nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserResource.getCurrentUser_get
      x-api-path-slug: usercurrent-get
      parameters:
      - in: query
        name: expand
        description: A multi-value parameter indicating which properties of the user
          toexpand
      responses:
        200:
          description: OK
      tags:
      - Current
      - User
  /user/memberof:
    get:
      summary: Get group memberships for user
      description: "Returns the groups that a user is a member of.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \nPermission to access the Confluence site ('Can use' global permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserResource.getGroupMembershipsForUser_get
      x-api-path-slug: usermemberof-get
      parameters:
      - in: query
        name: accountId
        description: The accountId of the user to be queried
      - in: query
        name: key
        description: The userKey of the user to be queried
      - in: query
        name: limit
        description: The maximum number of groups to return per page
      - in: query
        name: start
        description: The starting index of the returned groups
      - in: query
        name: username
        description: The username of the user to be queried
      responses:
        200:
          description: OK
      tags:
      - Group
      - Membershipsuser
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