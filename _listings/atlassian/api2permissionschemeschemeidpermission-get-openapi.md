---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get permission scheme grants
  description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
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
  /user/watch/content/{contentId}:
    get:
      summary: Get content watch status
      description: "Returns whether a user is watching a piece of content. Choose
        the user by \ndoing one of the following:\n\n- Specify a user via a query
        parameter: Use the `username`, `key`, or `accountId` \nto identify the user.
        The user making the request must be a Confluence administrator.\n- Do not
        specify a user: The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.getContentWatchStatus_get
      x-api-path-slug: userwatchcontentcontentid-get
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user to be queried for whether they are
          watching the content
      - in: path
        name: contentId
        description: The ID of the content to be queried for whether the specified
          user is watching it
      - in: query
        name: key
        description: The `key` of the user to be queried for whether they are watching
          the content
      - in: query
        name: username
        description: The `username` of the user to be queried for whether they are
          watching the content
      responses:
        200:
          description: OK
      tags:
      - Content
      - Watch
      - Status
    post:
      summary: Add content watcher
      description: "Adds a user as a watcher to a piece of content. Choose the user
        by doing \none of the following:\n\n- Specify a user via a query parameter:
        Use the `username`, `key`, or `accountId` \nto identify the user. The user
        making the request must be a Confluence administrator.\n- Do not specify a
        user: The currently logged-in user will be used.\n\nNote, you must add the
        `X-Atlassian-Token: no-check` header when making a \nrequest, as this operation
        has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.addContentWatcher_post
      x-api-path-slug: userwatchcontentcontentid-post
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be added as a watcher
      - in: path
        name: contentId
        description: The ID of the content to add the watcher to
      - in: query
        name: key
        description: The `key` of the user that will be added as a watcher
      - in: query
        name: username
        description: The `username` of the user that will be added as a watcher
      responses:
        200:
          description: OK
      tags:
      - Content
      - Watcher
    delete:
      summary: Remove content watcher
      description: "Removes a user as a watcher from a piece of content. Choose the
        user by \ndoing one of the following:\n\n- Specify a user via a query parameter:
        Use the `username`, `key`, or `accountId` \nto identify the user. The user
        making the request must be a Confluence administrator.\n- Do not specify a
        user: The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.removeContentWatcher_delete
      x-api-path-slug: userwatchcontentcontentid-delete
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be removed as a watcher
      - in: path
        name: contentId
        description: The ID of the content to remove the watcher from
      - in: query
        name: key
        description: The `key` of the user that will be removed as a watcher
      - in: query
        name: username
        description: The `username` of the user that will be removed as a watcher
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Content
      - Watcher
  /user/watch/label/{labelName}:
    get:
      summary: Get label watch status
      description: "Returns whether a user is watching a label. Choose the user by
        doing one \nof the following:\n\n- Specify a user via a query parameter: Use
        the `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.isWatchingLabel_get
      x-api-path-slug: userwatchlabellabelname-get
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user to be queried for whether they are
          watching the label
      - in: query
        name: key
        description: The `key` of the user to be queried for whether they are watching
          the label
      - in: path
        name: labelName
        description: The name of the label to be queried for whether the specified
          user is watching it
      - in: query
        name: username
        description: The `username` of the user to be queried for whether they are
          watching the label
      responses:
        200:
          description: OK
      tags:
      - Label
      - Watch
      - Status
    post:
      summary: Add label watcher
      description: "Adds a user as a watcher to a label. Choose the user by doing
        one of the \nfollowing:\n\n- Specify a user via a query parameter: Use the
        `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\nNote, you must add the `X-Atlassian-Token:
        no-check` header when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.addLabelWatcher_post
      x-api-path-slug: userwatchlabellabelname-post
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be added as a watcher
      - in: query
        name: key
        description: The `key` of the user that will be added as a watcher
      - in: path
        name: labelName
        description: The name of the label to add the watcher to
      - in: query
        name: username
        description: The `username` of the user that will be added as a watcher
      responses:
        200:
          description: OK
      tags:
      - Label
      - Watcher
    delete:
      summary: Remove label watcher
      description: "Removes a user as a watcher from a label. Choose the user by doing
        one of \nthe following:\n\n- Specify a user via a query parameter: Use the
        `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.removeLabelWatcher_delete
      x-api-path-slug: userwatchlabellabelname-delete
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be removed as a watcher
      - in: query
        name: key
        description: The `key` of the user that will be removed as a watcher
      - in: path
        name: labelName
        description: The name of the label to remove the watcher from
      - in: query
        name: username
        description: The `username` of the user that will be removed as a watcher
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Label
      - Watcher
  /user/watch/space/{spaceKey}:
    get:
      summary: Get space watch status
      description: "Returns whether a user is watching a space. Choose the user by
        \ndoing one of the following:\n\n- Specify a user via a query parameter: Use
        the `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.isWatchingSpace_get
      x-api-path-slug: userwatchspacespacekey-get
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user to be queried for whether they are
          watching the space
      - in: query
        name: key
        description: The `key` of the user to be queried for whether they are watching
          the space
      - in: path
        name: spaceKey
        description: The key of the space to be queried for whether the specified
          user is watching it
      - in: query
        name: username
        description: The `username` of the user to be queried for whether they are
          watching the space
      responses:
        200:
          description: OK
      tags:
      - Space
      - Watch
      - Status
    post:
      summary: Add space watcher
      description: "Adds a user as a watcher to a space. Choose the user by doing
        one of the \nfollowing:\n\n- Specify a user via a query parameter: Use the
        `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\nNote, you must add the `X-Atlassian-Token:
        no-check` header when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.addSpaceWatcher_post
      x-api-path-slug: userwatchspacespacekey-post
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be added as a watcher
      - in: query
        name: key
        description: The `key` of the user that will be added as a watcher
      - in: path
        name: spaceKey
        description: The key of the space to add the watcher to
      - in: query
        name: username
        description: The `username` of the user that will be added as a watcher
      responses:
        200:
          description: OK
      tags:
      - Space
      - Watcher
    delete:
      summary: Remove space watch
      description: "Removes a user as a watcher from a space. Choose the user by doing
        one of \nthe following:\n\n- Specify a user via a query parameter: Use the
        `username`, `key`, or `accountId` \nto identify the user. The user making
        the request must be a Confluence administrator.\n- Do not specify a user:
        The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
        required**: \n'Confluence Administrator' global permission if specifying a
        user, otherwise \npermission to access the Confluence site ('Can use' global
        permission)."
      operationId: com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.removeSpaceWatch_delete
      x-api-path-slug: userwatchspacespacekey-delete
      parameters:
      - in: query
        name: accountId
        description: The `accountId` of the user that will be removed as a watcher
      - in: query
        name: key
        description: The `key` of the user that will be removed as a watcher
      - in: path
        name: spaceKey
        description: The key of the space to remove the watcher from
      - in: query
        name: username
        description: The `username` of the user that will be removed as a watcher
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Space
      - Watch
  /api/2/application-properties:
    get:
      summary: Get application property
      description: Returns an application property.
      operationId: com.atlassian.jira.rest.v2.admin.ApplicationPropertiesResource.getApplicationProperty_get
      x-api-path-slug: api2applicationproperties-get
      parameters:
      - in: query
        name: key
        description: a String containing the property key
      - in: query
        name: keyFilter
        description: when fetching a list allows the list to be filtered by the propertys
          start of key e
      - in: query
        name: permissionLevel
        description: when fetching a list specifies the permission level of all items
          in the list see {@link com
      responses:
        200:
          description: OK
      tags:
      - Application
      - Property
  /api/2/application-properties/advanced-settings:
    get:
      summary: Get advanced settings
      description: Returns the properties that are displayed on the General Configuration
        Advanced Settings page.
      operationId: com.atlassian.jira.rest.v2.admin.ApplicationPropertiesResource.getAdvancedSettings_get
      x-api-path-slug: api2applicationpropertiesadvancedsettings-get
      responses:
        200:
          description: OK
      tags:
      - Advanced
      - Settings
  /api/2/application-properties/{id}:
    put:
      summary: Set application property
      description: Modify an application property via PUT. The "value" field present
        in the PUT will override the existing value.
      operationId: com.atlassian.jira.rest.v2.admin.ApplicationPropertiesResource.setApplicationProperty_put
      x-api-path-slug: api2applicationpropertiesid-put
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Set
      - Application
      - Property
  /api/2/applicationrole:
    get:
      summary: Get all application roles
      description: Returns all ApplicationRoles in the system. Will also return an
        ETag header containing a version hash of the collection of ApplicationRoles.
      operationId: com.atlassian.jira.rest.v2.admin.applicationrole.ApplicationRoleResource.getAllApplicationRoles_get
      x-api-path-slug: api2applicationrole-get
      responses:
        200:
          description: OK
      tags:
      - Application
      - Roles
  /api/2/applicationrole/{key}:
    get:
      summary: Get application role
      description: Returns the ApplicationRole with passed key if it exists.
      operationId: com.atlassian.jira.rest.v2.admin.applicationrole.ApplicationRoleResource.getApplicationRole_get
      x-api-path-slug: api2applicationrolekey-get
      parameters:
      - in: path
        name: key
        description: the key of the role to use
      responses:
        200:
          description: OK
      tags:
      - Application
      - Role
  /api/2/attachment/meta:
    get:
      summary: Get global attachment settings
      description: "Returns the global attachment settings, that is, whether attachments
        are enabled and the maximum attachment size allowed.  \n  \nNote that there
        are also [project permissions](https://confluence.atlassian.com/x/yodKLg)
        that restrict whether users can create and delete attachments or not.  \n
        \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        None."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.getAttachmentMeta_get
      x-api-path-slug: api2attachmentmeta-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Attachment
      - Settings
  /api/2/attachment/{id}:
    get:
      summary: Get attachment metadata
      description: "Returns the metadata for an attachment. Note that the attachment
        itself is not returned.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        issue that the attachment belongs to."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.getAttachment_get
      x-api-path-slug: api2attachmentid-get
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Attachment
      - Metadata
    delete:
      summary: Delete attachment
      description: "Deletes an attachment from an issue.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Any of the following permissions in the project that the issue
        is in:\n\n*   _Delete own attachments_ [project permission](https://confluence.atlassian.com/x/yodKLg)
        to delete an attachment created by the calling user.\n*   _Delete all attachments_
        [project permission](https://confluence.atlassian.com/x/yodKLg) to delete
        an attachment created by any user."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.removeAttachment_delete
      x-api-path-slug: api2attachmentid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Attachment
  /api/2/attachment/{id}/expand/human:
    get:
      summary: Get all metadata for an expanded attachment
      description: "Returns the metadata for the contents of an attachment, if it
        is an archive, and metadata for the attachment itself. For example, if the
        attachment is a ZIP archive, then information about the files in the archive
        is returned and metadata for the ZIP archive. Currently, only the ZIP archive
        format is supported.  \n  \nUse this method to retrieve data that is presented
        in the UI, as this method returns the metadata for the attachment itself,
        such as the attachment's ID and name. Otherwise, use [Get contents metadata
        for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-raw-get),
        which only returns the metadata for the attachment's contents.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        issue that the attachment belongs to."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.expandAttachmentForHumans_get
      x-api-path-slug: api2attachmentidexpandhuman-get
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Metadataan
      - Expanded
      - Attachment
  /api/2/attachment/{id}/expand/raw:
    get:
      summary: Get contents metadata for an expanded attachment
      description: "Returns the metadata for the contents of an attachment, if it
        is an archive. For example, if the attachment is a ZIP archive, then information
        about the files in the archive is returned. Currently, only the ZIP archive
        format is supported.  \n  \nUse this method if you are processing the data
        without presenting it in the UI, as this method only returns the metadata
        for the contents of the attachment. Otherwise, to retrieve data to present
        in the UI, use [Get all metadata for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-human-get)
        which also returns the metadata for the attachment itself, such as the attachment's
        ID and name.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        issue that the attachment belongs to."
      operationId: com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.expandAttachmentForMachines_get
      x-api-path-slug: api2attachmentidexpandraw-get
      parameters:
      - in: path
        name: id
        description: The ID of the attachment
      responses:
        200:
          description: OK
      tags:
      - Contents
      - Metadataan
      - Expanded
      - Attachment
  /api/2/auditing/record:
    get:
      summary: Get audit records
      description: Returns auditing records filtered using provided parameters
      operationId: com.atlassian.jira.rest.v2.admin.auditing.AuditingResource.getAuditRecords_get
      x-api-path-slug: api2auditingrecord-get
      parameters:
      - in: query
        name: filter
        description: \- text query; each record that will be returned must contain
          the provided text in one of its fields
      - in: query
        name: from
        description: \- timestamp in past; from must be less or equal to, otherwise
          the result set will be empty only records that where created in the same
          moment or after the from timestamp will be provided in response
      - in: query
        name: limit
        description: '\- maximum number of returned results (if is limit is  1000,
          it will be set do default value: 1000)'
      - in: query
        name: offset
        description: \- the number of record from which search starts
      - in: query
        name: to
        description: \- timestamp in past; from must be less or equal to, otherwise
          the result set will be empty only records that where created in the same
          moment or earlier than the to timestamp will be provided in response
      responses:
        200:
          description: OK
      tags:
      - Audit
      - Records
  /api/2/avatar/{type}/system:
    get:
      summary: Get all system avatars
      description: Returns all system avatars of the given type.
      operationId: com.atlassian.jira.rest.v2.issue.AvatarResource.getAllSystemAvatars_get
      x-api-path-slug: api2avatartypesystem-get
      parameters:
      - in: path
        name: type
        description: the avatar type
      responses:
        200:
          description: OK
      tags:
      - System
      - Avatars
  /api/2/comment/list:
    post:
      summary: Get comments by ids
      description: Returns comments for given comments ids. Only comments to which
        the user has permissions, will be included in the result. The returned set
        of comments is limited to 1000 elements.
      operationId: com.atlassian.jira.rest.v2.issue.IssueCommentListResource.getCommentsByIds_post
      x-api-path-slug: api2commentlist-post
      parameters:
      - in: query
        name: expand
        description: 'optional comma separated list of parameters to expand: renderedBody
          (provides body rendered in HTML), properties (provides comment properties)'
      responses:
        200:
          description: OK
      tags:
      - Comments
      - By
      - Ids
  /api/2/comment/{commentId}/properties:
    get:
      summary: Get comment property keys
      description: Returns the keys of all properties for the comment identified by
        the key or by the id.
      operationId: com.atlassian.jira.rest.v2.issue.CommentPropertyResource.getCommentPropertyKeys_get
      x-api-path-slug: api2commentcommentidproperties-get
      parameters:
      - in: path
        name: commentId
        description: the comment from which keys will be returned
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Property
      - Keys
  /api/2/comment/{commentId}/properties/{propertyKey}:
    get:
      summary: Get comment property
      description: Returns the value of the property with a given key from the comment
        identified by the key or by the id. The user who retrieves the property is
        required to have permissions to read the comment.
      operationId: com.atlassian.jira.rest.v2.issue.CommentPropertyResource.getCommentProperty_get
      x-api-path-slug: api2commentcommentidpropertiespropertykey-get
      parameters:
      - in: path
        name: commentId
        description: the comment from which the property will be returned
      - in: path
        name: propertyKey
        description: the key of the property to return
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Property
    put:
      summary: Set comment property
      description: |-
        Sets the value of the specified comment's property.

        You can use this resource to store a custom data against the comment identified by the key or by the id. The user who stores the data is required to have permissions to administer the comment.
      operationId: com.atlassian.jira.rest.v2.issue.CommentPropertyResource.setCommentProperty_put
      x-api-path-slug: api2commentcommentidpropertiespropertykey-put
      parameters:
      - in: path
        name: commentId
        description: the comment on which the property will be set
      - in: path
        name: propertyKey
        description: the key of the comments property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Comment
      - Property
    delete:
      summary: Delete comment property
      description: Removes the property from the comment identified by the key or
        by the id. Ths user removing the property is required to have permissions
        to administer the comment.
      operationId: com.atlassian.jira.rest.v2.issue.CommentPropertyResource.deleteCommentProperty_delete
      x-api-path-slug: api2commentcommentidpropertiespropertykey-delete
      parameters:
      - in: path
        name: commentId
        description: the comment from which the property will be removed
      - in: path
        name: propertyKey
        description: the key of the property to remove
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Property
  /api/2/component:
    post:
      summary: Create component
      description: |-
        Creates a component. Use components to provide containers for issues within a project. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

        *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
        *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.createComponent_post
      x-api-path-slug: api2component-post
      parameters:
      - in: header
        name: force-account-id
      responses:
        200:
          description: OK
      tags:
      - Component
  /api/2/component/{id}:
    get:
      summary: Get component
      description: 'Returns a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required: _Browse projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).'
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.getComponent_get
      x-api-path-slug: api2componentid-get
      parameters:
      - in: path
        name: id
        description: The ID of the component
      responses:
        200:
          description: OK
      tags:
      - Component
    put:
      summary: Update component
      description: |-
        Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string ("") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

        *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
        *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.updateComponent_put
      x-api-path-slug: api2componentid-put
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Component
    delete:
      summary: Delete component
      description: |-
        Deletes a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

        *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
        *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.deleteComponent_delete
      x-api-path-slug: api2componentid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the component
      - in: query
        name: moveIssuesTo
        description: The ID of the component to replace the deleted component
      responses:
        200:
          description: OK
      tags:
      - Component
  /api/2/component/{id}/relatedIssueCounts:
    get:
      summary: Get component issues count
      description: Returns the counts of issues assigned to the component. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.getComponentRelatedIssues_get
      x-api-path-slug: api2componentidrelatedissuecounts-get
      parameters:
      - in: path
        name: id
        description: The ID of the component
      responses:
        200:
          description: OK
      tags:
      - Component
      - Issues
      - Count
  /api/2/configuration:
    get:
      summary: Get global settings
      description: "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM)
        in Jira. These settings determine whether optional features (for example,
        sub-tasks, time tracking, and others) are enabled. If time tracking is enabled,
        this method also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.ConfigurationResource.getConfiguration_get
      x-api-path-slug: api2configuration-get
      responses:
        200:
          description: OK
      tags:
      - Global
      - Settings
  /api/2/configuration/timetracking:
    get:
      summary: Get selected time tracking provider
      description: "Returns the time tracking provider that is currently selected.
        Note that if time tracking is disabled, then a successful but empty response
        is returned.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getSelectedTimeTrackingImplementa
      x-api-path-slug: api2configurationtimetracking-get
      responses:
        200:
          description: OK
      tags:
      - Selected
      - Time
      - Tracking
      - Provider
    put:
      summary: Select time tracking provider
      description: "Selects a time tracking provider.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.selectTimeTrackingImplementation_
      x-api-path-slug: api2configurationtimetracking-put
      responses:
        200:
          description: OK
      tags:
      - Select
      - Time
      - Tracking
      - Provider
    delete:
      summary: Disable time tracking
      description: "Disables time tracking.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.disableTimeTracking_delete
      x-api-path-slug: api2configurationtimetracking-delete
      responses:
        200:
          description: OK
      tags:
      - Disable
      - Time
      - Tracking
  /api/2/configuration/timetracking/list:
    get:
      summary: Get all time tracking providers
      description: "Returns all time tracking providers. By default, Jira only has
        one time tracking provider: _JIRA provided time tracking_. However, you can
        install other time tracking providers via apps from the Atlassian Marketplace.
        For more information on time tracking providers, see the documentation for
        the [Time Tracking Provider](https://developer.atlassian.com/cloud/jira/platform/modules/time-tracking-provider/)
        module.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getAvailableTimeTrackingImplement
      x-api-path-slug: api2configurationtimetrackinglist-get
      responses:
        200:
          description: OK
      tags:
      - Time
      - Tracking
      - Providers
  /api/2/configuration/timetracking/options:
    get:
      summary: Get time tracking settings
      description: "Returns the time tracking settings. This includes settings such
        as the time format, default time unit, and others. For more information, see
        [Configuring time tracking](https://confluence.atlassian.com/x/qoXKM).  \n
        \ \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getSharedTimeTrackingConfiguratio
      x-api-path-slug: api2configurationtimetrackingoptions-get
      responses:
        200:
          description: OK
      tags:
      - Time
      - Tracking
      - Settings
    put:
      summary: Set time tracking settings
      description: "Sets the time tracking settings.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
      operationId: com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.setSharedTimeTrackingConfiguratio
      x-api-path-slug: api2configurationtimetrackingoptions-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Time
      - Tracking
      - Settings
  /api/2/customFieldOption/{id}:
    get:
      summary: Get custom field option
      description: "Returns a custom field option. For example, an option in a cascading
        select list.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
        required:** None."
      operationId: com.atlassian.jira.rest.v2.issue.customfield.CustomFieldOptionResource.getCustomFieldOption_get
      x-api-path-slug: api2customfieldoptionid-get
      parameters:
      - in: path
        name: id
        description: The ID of the custom field option
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Field
      - Option
  /api/2/dashboard:
    get:
      summary: Get all dashboards
      description: "Returns a list of dashboards owned by or shared with the user.
        The list may be filtered to include only favorite or owned dashboards.  \n
        \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to access Jira."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardResource.getAllDashboards_get
      x-api-path-slug: api2dashboard-get
      parameters:
      - in: query
        name: filter
        description: The filter applied to the list of dashboards
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Dashboards
  /api/2/dashboard/{dashboardId}/items/{itemId}/properties:
    get:
      summary: Get dashboard item property keys
      description: "Returns the keys of all properties for a dashboard item.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira. However, to get the property keys the
        user must be the owner of the dashboard or be shared the dashboard. Note,
        users with the _Administer Jira_ [global permission](href=) are considered
        owners of the System dashboard. The System dashboard is considered to be shared
        with all other users."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.getDashboardItemPropertyKeys_get
      x-api-path-slug: api2dashboarddashboardiditemsitemidproperties-get
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Item
      - Property
      - Keys
  /api/2/dashboard/{dashboardId}/items/{itemId}/properties/{propertyKey}:
    get:
      summary: Get dashboard item property
      description: "Returns the key and value of a dashboard item property.  \n  \nA
        dashboard item enables an app to add user-specific information to a user dashboard.
        Dashboard items are exposed to users as gadgets that users can add to their
        dashboards. For more information on how users do this, see [Adding and customizing
        gadgets](https://confluence.atlassian.com/x/7AeiLQ).  \n  \nWhen an app creates
        a dashboard item it registers a callback to receive the dashboard item ID.
        The callback fires whenever the item is rendered or, where the item is configurable,
        the user edits the item. The app then uses this resource to store the item's
        content or configuration details. For more information on working with dashboard
        items, see [Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
        and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
        documentation.  \n  \nThere is no resource to set or get dashboard items.
        \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to access Jira. However, to get a dashboard item property the user
        must be the owner of the dashboard or be shared the dashboard. Note, users
        with the _Administer Jira_ [global permission](href=) are considered owners
        of the System dashboard. The System dashboard is considered to be shared with
        all other users."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.getDashboardItemProperty_get
      x-api-path-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-get
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      - in: path
        name: propertyKey
        description: The key of the dashboard item property
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Item
      - Property
    put:
      summary: Set dashboard item property
      description: "Sets the value of a dashboard item property. Use this resource
        in apps to store custom data against a dashboard item.  \n  \nA dashboard
        item enables an app to add user-specific information to a user dashboard.
        Dashboard items are exposed to users as gadgets that users can add to their
        dashboards. For more information on how users do this, see [Adding and customizing
        gadgets](https://confluence.atlassian.com/x/7AeiLQ).  \n  \nWhen an app creates
        a dashboard item it registers a callback to receive the dashboard item ID.
        The callback fires whenever the item is rendered or, where the item is configurable,
        the user edits the item. The app then uses this resource to store the item's
        content or configuration details. For more information on working with dashboard
        items, see [Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
        and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
        documentation.  \n  \nThere is no resource to set or get dashboard items.
        \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to access Jira. However, to set a dashboard item property the user
        must be the owner of the dashboard. Note, users with the _Administer Jira_
        [global permission](href=) are considered owners of the System dashboard.
        \ \n  \nThe value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627),
        non-empty JSON blob. The maximum length is 32768 bytes."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.setDashboardItemProperty_put
      x-api-path-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-put
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      - in: path
        name: propertyKey
        description: The key of the dashboard item property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Dashboard
      - Item
      - Property
    delete:
      summary: Delete dashboard item property
      description: "Deletes a dashboard item property.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira. However, to delete a dashboard item
        property the user must be the owner of the dashboard. Note, users with the
        _Administer Jira_ [global permission](href=) are considered owners of the
        System dashboard."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.deleteDashboardItemProperty_delet
      x-api-path-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-delete
      parameters:
      - in: path
        name: dashboardId
        description: The ID of the dashboard
      - in: path
        name: itemId
        description: The ID of the dashboard item
      - in: path
        name: propertyKey
        description: The key of the dashboard item property
      responses:
        200:
          description: OK
      tags:
      - Dashboard
      - Item
      - Property
  /api/2/dashboard/{id}:
    get:
      summary: Get dashboard
      description: "Returns a dashboard.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira. However, to get a dashboard, the dashboard
        must be shared with the user or the user must own it. Note, users with the
        _Administer Jira_ [global permission](href=) are considered owners of the
        System dashboard. The System dashboard is considered to be shared with all
        other users."
      operationId: com.atlassian.jira.rest.v2.dashboard.DashboardResource.getDashboard_get
      x-api-path-slug: api2dashboardid-get
      parameters:
      - in: path
        name: id
        description: The ID of the dashboard
      responses:
        200:
          description: OK
      tags:
      - Dashboard
  /api/2/expression/eval:
    post:
      summary: Evaluate Jira expression
      description: Evaluates a Jira expression and returns its value. Jira expressions
        is the name of a domain-specific language for Jira that can be used to evaluate
        expressions in the context of Jira entities.
      operationId: com.atlassian.jira.rest.v2.expression.JiraExpressionsResource.evaluateJiraExpression_post
      x-api-path-slug: api2expressioneval-post
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Evaluate
      - Jira
      - Expression
  /api/2/field:
    get:
      summary: Get fields
      description: |-
        Returns all issue fields in Jira, both system and custom fields.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the following rules apply:

        *   Fields that cannot be added to the issue navigator are always returned.
        *   Fields that cannot be placed on an issue screen are always returned.
        *   Fields that depend on global Jira settings are only returned if the setting is enabled. That is, timetracking fields, subtasks, votes, and watches.
        *   For all other fields, this method only returns the fields that the current user has permission to see (that is, the field can be used in at least one project that the user can see).
      operationId: com.atlassian.jira.rest.v2.issue.FieldResource.getFields_get
      x-api-path-slug: api2field-get
      responses:
        200:
          description: OK
      tags:
      - Fields
    post:
      summary: Create custom field
      description: |-
        Creates a custom field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.FieldResource.createCustomField_post
      x-api-path-slug: api2field-post
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Field
  /api/2/field/{fieldKey}/option:
    get:
      summary: Get all issue field options
      description: |-
        Returns all options defined for a select list issue field. A select list issue field is a type of [issue field](https://developer.atlassian.com/cloud/jira/platform/modules/issue-field/) that allows a user to select an value from a list of options.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getAllIssueFieldOptions_get
      x-api-path-slug: api2fieldfieldkeyoption-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Options
    post:
      summary: Create issue field option
      description: |-
        Creates an option for a select list issue field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.createIssueFieldOption_post
      x-api-path-slug: api2fieldfieldkeyoption-post
      parameters:
      - in: path
        name: fieldKey
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
  /api/2/field/{fieldKey}/option/suggestions/edit:
    get:
      summary: Get selectable issue field options
      description: |-
        Returns options defined for a select list issue field that can be viewed and selected by the currently logged in user.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getSelectableIssueFieldOptions_get
      x-api-path-slug: api2fieldfieldkeyoptionsuggestionsedit-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: projectId
        description: Filters the results to options that are only available in the
          specified project
      - in: query
        name: startAt
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Selectable
      - Issue
      - Field
      - Options
  /api/2/field/{fieldKey}/option/suggestions/search:
    get:
      summary: Get visible issue field options
      description: |-
        Returns options defined for a select list issue field that can be viewed by the currently logged in user.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getVisibleIssueFieldOptions_get
      x-api-path-slug: api2fieldfieldkeyoptionsuggestionssearch-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: projectId
        description: Filters the results to options that are only available in the
          specified project
      - in: query
        name: startAt
        description: The starting index of the returned objects
      responses:
        200:
          description: OK
      tags:
      - Visible
      - Issue
      - Field
      - Options
  /api/2/field/{fieldKey}/option/{optionId}:
    get:
      summary: Get issue field option
      description: |-
        Returns an option from a select list issue field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getIssueFieldOption_get
      x-api-path-slug: api2fieldfieldkeyoptionoptionid-get
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: path
        name: optionId
        description: The ID of the option to be returned
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
    put:
      summary: Update issue field option
      description: |-
        Updates an option for a select list issue field. If the option does not exist, a new option is created.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.updateIssueFieldOption_put
      x-api-path-slug: api2fieldfieldkeyoptionoptionid-put
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: path
        name: optionId
        description: The ID of the option to be updated
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
    delete:
      summary: Delete issue field option
      description: |-
        Deletes an option from a select list issue field.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.deleteIssueFieldOption_delete
      x-api-path-slug: api2fieldfieldkeyoptionoptionid-delete
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: path
        name: optionId
        description: The ID of the option to be deleted
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Field
      - Option
  /api/2/field/{fieldKey}/option/{optionId}/issue:
    delete:
      summary: Replace issue field option
      description: |-
        Deselects a select list issue field option in all issues that it has been selected in. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.

        This is an [asynchronous method](#async). The response object will contain a link to the long-running task. For example, _https://your-domain.atlassian.net/rest/api/2/task/10127_.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
      operationId: com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.replaceIssueFieldOption_delete
      x-api-path-slug: api2fieldfieldkeyoptionoptionidissue-delete
      parameters:
      - in: path
        name: fieldKey
        description: 'The field key is specified in the following format: **$(app-key)__$(field-key)**'
      - in: query
        name: jql
        description: A JQL query that specifies the issues to be updated
      - in: path
        name: optionId
        description: The ID of the option to be deselected
      - in: query
        name: replaceWith
        description: The ID of the option that will replace the currently selected
          option
      responses:
        200:
          description: OK
      tags:
      - Replace
      - Issue
      - Field
      - Option
  /api/2/filter:
    get:
      summary: Get filters
      description: |-
        Returns all filters. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned:

        *   Filters owned by the user.
        *   Filters shared with a group that the user is a member of.
        *   Filters shared with a private project that the user can browse.
        *   Filters shared with a public project, even if the user is anonymous.
        *   Filters shared with the public, even if the user is anonymous.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFilters_get
      x-api-path-slug: api2filter-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Filters
    post:
      summary: Create filter
      description: Creates a new filter. The new filter is not shared and not selected
        as a favorite. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.createFilter_post
      x-api-path-slug: api2filter-post
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Filter
  /api/2/filter/defaultShareScope:
    get:
      summary: Get default share scope
      description: Returns the default sharing settings for new filters and dashboards
        for a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getDefaultShareScope_get
      x-api-path-slug: api2filterdefaultsharescope-get
      responses:
        200:
          description: OK
      tags:
      - Default
      - Share
      - Scope
    put:
      summary: Set default share scope
      description: Sets the default sharing for new filters and dashboards for a user.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
        to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.setDefaultShareScope_put
      x-api-path-slug: api2filterdefaultsharescope-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Default
      - Share
      - Scope
  /api/2/filter/favourite:
    get:
      summary: Get favourite filters
      description: Returns the favorite filters of the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFavouriteFilters_get
      x-api-path-slug: api2filterfavourite-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      responses:
        200:
          description: OK
      tags:
      - Favourite
      - Filters
  /api/2/filter/my:
    get:
      summary: Get my filters
      description: Returns the filters owned by the calling user. If `includeFavourites`
        is `true`, the user's favorite filters are also returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getMyFilters_get
      x-api-path-slug: api2filtermy-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: includeFavourites
        description: Include the users favorite filters in the response
      responses:
        200:
          description: OK
      tags:
      - My
      - Filters
  /api/2/filter/search:
    get:
      summary: Search for filters
      description: |-
        Search for filters. This method is similar to [Get filters](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-get) except that you can refine the results to include filters that have specific attributes. For example, filters with a particular name. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned (if no search parameters are set):

        *   Filters owned by the user.
        *   Filters shared with a group that the user is a member of.
        *   Filters shared with a private project that the user can browse.
        *   Filters shared with a public project, even if the user is anonymous.
        *   Filters shared with the public, even if the user is anonymous.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFiltersPaginated_get
      x-api-path-slug: api2filtersearch-get
      parameters:
      - in: query
        name: accountId
        description: Returns filters with an owner that exactly matches `accountId`
          of the owner
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: filterName
        description: Returns filters with a name that partially matches `filterName`
      - in: header
        name: force-account-id
      - in: query
        name: groupname
        description: Returns filters that are shared with a group that has a name
          that exactly matches `groupname`
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: orderBy
        description: '[Orders](https://developer'
      - in: query
        name: owner
        description: Returns filters with an owner that exactly matches `owner`
      - in: query
        name: projectId
        description: Returns filters that are shared with a project that has an ID
          that exactly matches `projectId`
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Searchfilters
  /api/2/filter/{id}:
    get:
      summary: Get filter
      description: Returns a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getFilter_get
      x-api-path-slug: api2filterid-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter to return
      responses:
        200:
          description: OK
      tags:
      - Filter
    put:
      summary: Update filter
      description: |-
        Updates an existing filter. Use this method to update a filter's name, description, JQL, or sharing. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can update:

        *   Private filters (i.e., not shared) can only be updated by the creator of the filter.
        *   Shared filters can only be updated by the creator of the filter or a Jira administrator.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.updateFilter_put
      x-api-path-slug: api2filterid-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter to update
      responses:
        200:
          description: OK
      tags:
      - Filter
    delete:
      summary: Delete filter
      description: |-
        Delete a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can delete:

        *   Private filters (i.e., not shared) can only be deleted by the creator of the filter.
        *   Shared filters can only be deleted by the creator of the filter or a Jira administrator.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.deleteFilter_delete
      x-api-path-slug: api2filterid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the filter to delete
      responses:
        200:
          description: OK
      tags:
      - Filter
  /api/2/filter/{id}/columns:
    get:
      summary: Get columns
      description: Returns the columns configured for a filter. The column configuration
        is used when the filter's results are viewed in _List View_ with the _Columns_
        set to _Filter_. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getColumns_get
      x-api-path-slug: api2filteridcolumns-get
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Columns
    put:
      summary: Set columns
      description: Sets the columns for a filter. Only navigable fields can be set
        as columns. Use [Get fields](https://developer.atlassian.com/cloud/jira/platform/rest#api-api-2-field-get)
        to get the list fields in Jira. A navigable field has `navigable` set to `true`.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
        to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.setColumns_put
      x-api-path-slug: api2filteridcolumns-put
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Set
      - Columns
    delete:
      summary: Reset columns
      description: Reset the user's column configuration for the filter to the default.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
        to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.resetColumns_delete
      x-api-path-slug: api2filteridcolumns-delete
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Columns
  /api/2/filter/{id}/favourite:
    put:
      summary: Add filter as favorite
      description: Add a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.setFavouriteForFilter_put
      x-api-path-slug: api2filteridfavourite-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Filter
      - As
      - Favorite
    delete:
      summary: Remove filter as favorite
      description: Removes a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and permission to view the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.deleteFavouriteForFilter_delete
      x-api-path-slug: api2filteridfavourite-delete
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Filter
      - As
      - Favorite
  /api/2/filter/{id}/permission:
    get:
      summary: Get share permissions
      description: Returns the share permissions for a filter. A filter can be shared
        with groups, projects, all logged-in users, or the public. Sharing with all
        logged-in users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getSharePermissions_get
      x-api-path-slug: api2filteridpermission-get
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permissions
    post:
      summary: Add share permission
      description: "Add a share permissions to a filter. If you add a global share
        permission (i.e., all logged-in users or the public) it will overwrite all
        share permissions for the filter.  \nBe aware that this method uses different
        objects for updating share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put).
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share
        dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
        and the calling user must own the filter."
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.addSharePermission_post
      x-api-path-slug: api2filteridpermission-post
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permission
  /api/2/filter/{id}/permission/{permissionId}:
    get:
      summary: Get share permission
      description: Returns a share permission for a filter. A filter can be shared
        with groups, projects, all logged-in users, or the public. Sharing with all
        logged-in users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None, however the calling user must have permission to view the
        filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.getSharePermission_get
      x-api-path-slug: api2filteridpermissionpermissionid-get
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      - in: path
        name: permissionId
        description: The ID of the share permission
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permission
    delete:
      summary: Delete share permission
      description: Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
        and the calling user must own the filter.
      operationId: com.atlassian.jira.rest.v2.search.FilterResource.deleteSharePermission_delete
      x-api-path-slug: api2filteridpermissionpermissionid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the filter
      - in: path
        name: permissionId
        description: The ID of the share permission
      responses:
        200:
          description: OK
      tags:
      - Share
      - Permission
  /api/2/group:
    get:
      summary: Get group
      description: |-
        This resource is deprecated, use [`group/member`](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-group-member-get).

        Returns all users in a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.getGroup_get
      x-api-path-slug: api2group-get
      parameters:
      - in: query
        name: expand
        description: List of fields to expand
      - in: query
        name: groupname
        description: The name of the group
      responses:
        200:
          description: OK
      tags:
      - Group
    post:
      summary: Create group
      description: |-
        Creates a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.createGroup_post
      x-api-path-slug: api2group-post
      responses:
        200:
          description: OK
      tags:
      - Group
    delete:
      summary: Remove group
      description: |-
        Deletes a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.removeGroup_delete
      x-api-path-slug: api2group-delete
      parameters:
      - in: query
        name: groupname
        description: The name of the group
      - in: query
        name: swapGroup
        description: The group to transfer restrictions to
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Group
  /api/2/group/member:
    get:
      summary: Get users from group
      description: |-
        Returns all users in a group. Users are ordered by username.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.getUsersFromGroup_get
      x-api-path-slug: api2groupmember-get
      parameters:
      - in: query
        name: groupname
        description: The name of the group
      - in: query
        name: includeInactiveUsers
        description: Include inactive users
      - in: query
        name: maxResults
        description: The maximum number of users to return per page
      - in: query
        name: startAt
        description: The index of the first user to return
      responses:
        200:
          description: OK
      tags:
      - Users
      - From
      - Group
  /api/2/group/user:
    post:
      summary: Add user to group
      description: |-
        Adds a user to a group.

        **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.addUserToGroup_post
      x-api-path-slug: api2groupuser-post
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: groupname
        description: The name of the group
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - Group
    delete:
      summary: Remove user from group
      description: Removes a user from a group. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
        _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.GroupResource.removeUserFromGroup_delete
      x-api-path-slug: api2groupuser-delete
      parameters:
      - in: query
        name: accountid
        description: The account id of the user to remove
      - in: header
        name: force-account-id
      - in: query
        name: groupname
        description: The name of the group
      - in: query
        name: username
        description: The username of the user to remove
      responses:
        200:
          description: OK
      tags:
      - Remove
      - User
      - From
      - Group
  /api/2/groups/picker:
    get:
      summary: Find groups
      description: |-
        Returns groups with substrings matching a given query. This is mainly for use with the group picker, so the returned groups contain html to be used as picker suggestions. The groups are also wrapped in a single response object that also contains a header for use in the picker, specifically _Showing X of Y matching groups_.

        The number of groups returned is limited by the system property "jira.ajax.autocomplete.limit"

        The groups will be unique and sorted.
      operationId: com.atlassian.jira.rest.v2.issue.GroupPickerResource.findGroups_get
      x-api-path-slug: api2groupspicker-get
      parameters:
      - in: query
        name: accountId
      - in: query
        name: exclude
      - in: header
        name: force-account-id
      - in: query
        name: maxResults
      - in: query
        name: query
        description: a String to match groups agains
      - in: query
        name: userName
      responses:
        200:
          description: OK
      tags:
      - Find
      - Groups
  /api/2/groupuserpicker:
    get:
      summary: Find users and groups
      description: Returns a list of users and groups matching query with highlighting.
        This resource cannot be accessed anonymously.
      operationId: com.atlassian.jira.rest.v2.issue.GroupAndUserPickerResource.findUsersAndGroups_get
      x-api-path-slug: api2groupuserpicker-get
      parameters:
      - in: query
        name: avatarSize
        description: The size of the avatar to return
      - in: query
        name: caseInsensitive
        description: whether the search for groups should be case insensitive
      - in: query
        name: excludeConnectAddons
        description: Boolean indicating whether Connect Add-on users and groups should
          be excluded from the search results
      - in: query
        name: fieldId
        description: The custom field id, if this request comes from a custom field,
          such as a user picker
      - in: query
        name: issueTypeId
        description: The list of issue type ids to further restrict the search
      - in: query
        name: maxResults
        description: the maximum number of users to return (defaults to 50)
      - in: query
        name: projectId
        description: The list of project ids to further restrict the search This parameter
          can occur multiple times to pass in multiple project ids
      - in: query
        name: query
        description: A string used to search username, Name or e-mail address
      - in: query
        name: showAvatar
        description: If the user avatar should be returned or not
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Groups
  /api/2/issue:
    post:
      summary: Create issue
      description: |-
        Creates an issue or a sub-task from a JSON representation.

        You can provide two parameters in request's body: `update` or `fields`. The fields, that can be set on an issue create operation, can be determined using the **/rest/api/2/issue/createmeta** resource. If a particular field is not configured to appear on the issue's Create screen, then it will not be returned in the createmeta response. A field validation error will occur if such field is submitted in request.

        Creating a sub-task is similar to creating an issue with the following differences:

        *   `issueType` field must be set to a sub-task issue type (use `/issue/createmeta` to find sub-task issue types), and
        *   You must provide a `parent` field with the ID or key of the parent issue.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.createIssue_post
      x-api-path-slug: api2issue-post
      parameters:
      - in: query
        name: updateHistory
        description: If set to true, then project an issue was created in is added
          to the current users project history
      responses:
        200:
          description: OK
      tags:
      - Issue
  /api/2/issue/bulk:
    post:
      summary: Create issues
      description: |-
        Creates multiple issues or sub-tasks from a JSON representation, in a single bulk operation.

        Creating a sub-task is similar to creating an issue - check Create issue section for details: {@link IssueResource#createIssue(boolean, IssueUpdateBean)}}
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.createIssues_post
      x-api-path-slug: api2issuebulk-post
      responses:
        200:
          description: OK
      tags:
      - Issues
  /api/2/issue/createmeta:
    get:
      summary: Get create issue meta
      description: |-
        Returns the metadata for creating issues. This includes the available projects, issue types, fields (with information whether those fields are required) and field types. Projects, in which the user does not have permission to create issues, will not be returned.

        The fields in the createmeta response correspond to the fields on the issue's Create screen for the specific project/issuetype. Fields hidden from the screen will not be returned in the createmeta response.

        Fields will only be returned if `expand=projects.issuetypes.fields` is set.

        The results can be filtered by project and/or issue type, controlled by the query parameters.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getCreateIssueMeta_get
      x-api-path-slug: api2issuecreatemeta-get
      parameters:
      - in: query
        name: issuetypeIds
        description: Multi-value parameter defining issue type IDs to be used for
          the results filtering
      - in: query
        name: issuetypeNames
        description: Multi-value parameter defining issue type names to be used for
          the results filtering
      - in: query
        name: projectIds
        description: Multi-value parameter defining project IDs to be used for the
          results filtering
      - in: query
        name: projectKeys
        description: Multi-value parameter defining project keys to be used for the
          results filtering
      responses:
        200:
          description: OK
      tags:
      - Create
      - Issue
      - Meta
  /api/2/issue/picker:
    get:
      summary: Get issue picker resource
      description: Returns a list of suggested issues matching the auto-completion
        query for the user executing this request. This REST method checks the user's
        history and browsing context to return issue suggestions.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getIssuePickerResource_get
      x-api-path-slug: api2issuepicker-get
      parameters:
      - in: query
        name: currentIssueKey
        description: Key of the issue defining search context
      - in: query
        name: currentJQL
        description: JQL defining search context
      - in: query
        name: currentProjectId
        description: ID of a project defining search context
      - in: query
        name: query
        description: Query used to filter issue search results
      - in: query
        name: showSubTaskParent
        description: Set to false to exclude parent issue from the suggestions list
          if search is performed in the context of a sub-task
      - in: query
        name: showSubTasks
        description: Set to false to exclude subtasks from the suggestions list
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Picker
      - Resource
  /api/2/issue/properties/{propertyKey}:
    put:
      summary: Bulk set issue property
      description: |-
        Allows to set a property for all issues identified by a given filter. Only entities the user has permissions to edit will be updated.

        Currently the following filters are available:

        *   **entityIds** \- A list of issues to update. Only issues with ids from this list will be considered for updating. This is an optional filter, if not provided, then any editable issue that matches all other filters will be updated.
        *   **currentValue** \- If provided, then only issues with the property currently set to that value will be updated.
        *   **hasProperty** \- If true, then only existing properties will be updated. If false, then only issues that do not have any value associated with this property will be updated. If omitted, the property will be set on all issues, regardless of whether it previously existed or not.

        If more than one filter is given, then they are all joined with the logical "and", that is: only issues that satisfy all filters are updated. If no filters are provided at all, then the property will be updated on _all_ issues editable by the caller (i.e. issues in projects with the EDIT_ISSUES permission).

        If an invalid combination of filters is provided, an error will be returned by the API. For example, specifying the current value and "hasProperty" to "false" would never match any issues (as it would mean: update this property if the current value is something, oh, but only if there is no value at all) and is therefore not allowed.

        This method is [asynchronous](#async), meaning that it will not return the results immediately, instead creating a task to perform the requested update operation (unless preliminary validation, e.g. of the provided filter, fails).

        The operation is transactional: either all eligible issues are updated, or none (if there are any errors).
      operationId: com.atlassian.jira.rest.v2.property.IssuePropertyBulkUpdateResource.bulkSetIssueProperty_put
      x-api-path-slug: api2issuepropertiespropertykey-put
      parameters:
      - in: path
        name: propertyKey
        description: The key of the property to update
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Set
      - Issue
      - Property
    delete:
      summary: Bulk delete issue property
      description: Allows to delete a property from all issues identified by a given
        filter. Only entities the user has permissions to edit will be updated. See
        the [issue property bulk set endpoint documentation](#api-api-2-issue-properties-propertyKey-put)
        for more details.
      operationId: com.atlassian.jira.rest.v2.property.IssuePropertyBulkUpdateResource.bulkDeleteIssueProperty_delete
      x-api-path-slug: api2issuepropertiespropertykey-delete
      parameters:
      - in: path
        name: propertyKey
        description: The key of the property to delete
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Delete
      - Issue
      - Property
  /api/2/issue/{issueIdOrKey}:
    get:
      summary: Get issue
      description: |-
        Returns a full representation of the issue for the given issue key.

        The issue JSON consists of the issue key and a collection of fields. Additional information like links to workflow transition sub-resources, or HTML rendered values of the fields supporting HTML rendering can be retrieved with `expand` request parameter specified.

        The `fields` request parameter accepts a comma-separated list of fields to include in the response. It can be used to retrieve a subset of fields. By default all fields are returned in the response. A particular field can be excluded from the response if prefixed with a "-" (minus) sign. Parameter can be provided multiple times on a single request.

        By default, all fields are returned in the response. Note: this is different from a JQL search - only navigable fields are returned by default (`*navigable`).
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getIssue_get
      x-api-path-slug: api2issueissueidorkey-get
      parameters:
      - in: query
        name: expand
        description: Multi-value parameter defining the additional issue attributes
          to be included in the response
      - in: query
        name: fields
        description: Multi-value parameter defining the fields returned for the issue
      - in: query
        name: fieldsByKeys
        description: If true then issue fields are referenced by keys instead of IDs
      - in: path
        name: issueIdOrKey
        description: 'ID or key of the issue, for example: JRACLOUD-1549'
      - in: query
        name: properties
        description: Multi-value parameter defining the list of properties returned
          for the issue
      - in: query
        name: updateHistory
        description: If set to true, adds the issue retrieved by this method to the
          current users issue history
      responses:
        200:
          description: OK
      tags:
      - Issue
    put:
      summary: Edit issue
      description: "Edits the issue from a JSON representation.\n\nThe fields available
        for update can be determined using the **/rest/api/2/issue/{issueIdOrKey}/editmeta**
        resource.  \nIf a field is hidden from the Edit screen then it will not be
        returned by the editmeta resource. A field validation error will occur if
        such field is submitted in an edit request. However connect add-on with admin
        scope may override a screen security configuration.\n\nIf an issue cannot
        be edited in Jira because of its workflow status (for example the issue is
        closed), then you will not be able to edit it with this resource.\n\nField
        to be updated should appear either in `fields` or `update` request's body
        parameter, but not in both.  \nTo update a single sub-field of a complex field
        (e.g. timetracking) please use the `update` parameter of the edit operation.
        Using a `\"field_id\": field_value` construction in the `fields` parameter
        is a shortcut of \"set\" operation in the `update` parameter."
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.editIssue_put
      x-api-path-slug: api2issueissueidorkey-put
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to be updated
      - in: query
        name: notifyUsers
        description: Sends the notification email on issue update to all watchers
      - in: query
        name: overrideEditableFlag
        description: Updates the issue even if it is not editable (issue in status
          with jira
      - in: query
        name: overrideScreenSecurity
        description: Allows update of the fields that are hidden from the issues Edit
          screen
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Issue
    delete:
      summary: Delete issue
      description: |-
        Deletes an individual issue.

        If the issue has sub-tasks you must set the `deleteSubtasks=true` parameter to delete the issue. You cannot delete an issue without deleting its sub-tasks.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.deleteIssue_delete
      x-api-path-slug: api2issueissueidorkey-delete
      parameters:
      - in: query
        name: deleteSubtasks
        description: A `true` or `false` value indicating if sub-tasks should be deleted
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to be deleted
      responses:
        200:
          description: OK
      tags:
      - Issue
  /api/2/issue/{issueIdOrKey}/assignee:
    put:
      summary: Assign issue
      description: Assigns the issue to the user. Use this resource to assign issues
        for the users having "Assign Issue" permission, and not having the "Edit Issue"
        permission. If `name` body parameter is set to "-1" then automatic issue assignee
        is used. A `name` set to `null` will remove the assignee.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.assignIssue_put
      x-api-path-slug: api2issueissueidorkeyassignee-put
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to be updated
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Issue
  /api/2/issue/{issueIdOrKey}/attachments:
    post:
      summary: Add attachment
      description: |-
        Add one or more attachments to an issue.

        This resource expects a multipart post. The media-type multipart/form-data is defined in RFC 1867. Most client libraries have classes that make dealing with multipart posts simple. For instance, in Java the Apache HTTP Components library provides a [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) that makes it simple to submit a multipart POST.

        In order to protect against XSRF attacks, because this method accepts multipart/form-data, it has XSRF protection on it. This means you must submit a header of X-Atlassian-Token: no-check with the request, otherwise it will be blocked.

        The name of the multipart/form-data parameter that contains attachments must be "file"

        A simple example to upload a file called "myfile.txt" to issue REST-123:

        curl -D- -u admin:admin -X POST -H "X-Atlassian-Token: no-check" -F "file=@myfile.txt" http://myhost/rest/api/2/issue/TEST-123/attachments
      operationId: com.atlassian.jira.rest.v2.issue.IssueAttachmentsResource.addAttachment_post
      x-api-path-slug: api2issueissueidorkeyattachments-post
      parameters:
      - in: path
        name: issueIdOrKey
        description: the issue that you want to add the attachments to
      responses:
        200:
          description: OK
      tags:
      - Attachment
  /api/2/issue/{issueIdOrKey}/changelog:
    get:
      summary: Get change logs
      description: Returns a [paginated](#pagination) list of all updates of an issue,
        sorted by date, starting from the oldest.
      operationId: com.atlassian.jira.rest.v2.issue.IssueChangelogResource.getChangeLogs_get
      x-api-path-slug: api2issueissueidorkeychangelog-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue
      - in: query
        name: maxResults
        description: Maximum number of items to return per page
      - in: query
        name: startAt
        description: Page offset, ie
      responses:
        200:
          description: OK
      tags:
      - Change
      - Logs
  /api/2/issue/{issueIdOrKey}/comment:
    get:
      summary: Get comments
      description: |-
        Returns all comments for an issue.

        Results can be ordered by the "created" field which means the date a comment was added.
      operationId: com.atlassian.jira.rest.v2.issue.IssueCommentResource.getComments_get
      x-api-path-slug: api2issueissueidorkeycomment-get
      parameters:
      - in: query
        name: expand
        description: 'optional flags: renderedBody (provides body rendered in HTML)'
      - in: path
        name: issueIdOrKey
        description: to get comments for
      - in: query
        name: maxResults
        description: how many results on the page should be included
      - in: query
        name: orderBy
        description: ordering of the results
      - in: query
        name: startAt
        description: the page offset, if not specified then defaults to 0
      responses:
        200:
          description: OK
      tags:
      - Comments
    post:
      summary: Add comment
      description: Adds a new comment to an issue.
      operationId: com.atlassian.jira.rest.v2.issue.IssueCommentResource.addComment_post
      x-api-path-slug: api2issueissueidorkeycomment-post
      parameters:
      - in: query
        name: expand
        description: 'optional flags: renderedBody (provides body rendered in HTML)'
      - in: path
        name: issueIdOrKey
        description: a string containing the issue id or key the comment will be added
          to
      responses:
        200:
          description: OK
      tags:
      - Comment
  /api/2/issue/{issueIdOrKey}/comment/{id}:
    get:
      summary: Get comment
      description: Returns a single comment.
      operationId: com.atlassian.jira.rest.v2.issue.IssueCommentResource.getComment_get
      x-api-path-slug: api2issueissueidorkeycommentid-get
      parameters:
      - in: query
        name: expand
        description: 'optional flags: renderedBody (provides body rendered in HTML)'
      - in: path
        name: id
        description: the ID of the comment to request
      - in: path
        name: issueIdOrKey
        description: of the issue the comment belongs to
      responses:
        200:
          description: OK
      tags:
      - Comment
    put:
      summary: Update comment
      description: Updates an existing comment using its JSON representation.
      operationId: com.atlassian.jira.rest.v2.issue.IssueCommentResource.updateComment_put
      x-api-path-slug: api2issueissueidorkeycommentid-put
      parameters:
      - in: query
        name: expand
        description: 'optional flags: renderedBody (provides body rendered in HTML)'
      - in: path
        name: id
        description: id of the comment to be updated
      - in: path
        name: issueIdOrKey
        description: a string containing the issue id or key the comment belongs to
      responses:
        200:
          description: OK
      tags:
      - Comment
    delete:
      summary: Delete comment
      description: Deletes an existing comment .
      operationId: com.atlassian.jira.rest.v2.issue.IssueCommentResource.deleteComment_delete
      x-api-path-slug: api2issueissueidorkeycommentid-delete
      parameters:
      - in: path
        name: id
        description: id of the comment to be deleted
      - in: path
        name: issueIdOrKey
        description: a string containing the issue id or key the comment belongs to
      responses:
        200:
          description: OK
      tags:
      - Comment
  /api/2/issue/{issueIdOrKey}/editmeta:
    get:
      summary: Get edit issue meta
      description: |-
        Returns the metadata for editing an issue.

        The fields returned by editmeta resource are the ones shown on the issue's Edit screen. Fields hidden from the screen will not be returned unless `overrideScreenSecurity` parameter is set to true.

        If an issue cannot be edited in Jira because of its workflow status (for example the issue is closed), then no fields will be returned, unless `overrideEditableFlag` is set to true.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getEditIssueMeta_get
      x-api-path-slug: api2issueissueidorkeyeditmeta-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue
      - in: query
        name: overrideEditableFlag
        description: Allows retrieving edit metadata for fields in non-editable status
          (jira
      - in: query
        name: overrideScreenSecurity
        description: Allows retrieving edit metadata for the fields hidden on Edit
          screen
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Issue
      - Meta
  /api/2/issue/{issueIdOrKey}/notify:
    post:
      summary: Notify
      description: Sends an email notification to the list of users defined in the
        request body parameters.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.notify_post
      x-api-path-slug: api2issueissueidorkeynotify-post
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue a notification is sent for
      responses:
        200:
          description: OK
      tags:
      - Notify
  /api/2/issue/{issueIdOrKey}/properties:
    get:
      summary: Get issue property keys
      description: Returns the keys of all properties for the issue identified by
        the key or by the id.
      operationId: com.atlassian.jira.rest.v2.issue.IssuePropertyResource.getIssuePropertyKeys_get
      x-api-path-slug: api2issueissueidorkeyproperties-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: the issue from which keys will be returned
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Property
      - Keys
  /api/2/issue/{issueIdOrKey}/properties/{propertyKey}:
    get:
      summary: Get issue property
      description: Returns the value of the property with a given key from the issue
        identified by the key or by the id. The user who retrieves the property is
        required to have permissions to read the issue.
      operationId: com.atlassian.jira.rest.v2.issue.IssuePropertyResource.getIssueProperty_get
      x-api-path-slug: api2issueissueidorkeypropertiespropertykey-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: the issue from which the property will be returned
      - in: path
        name: propertyKey
        description: the key of the property to return
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Property
    put:
      summary: Set issue property
      description: |-
        Sets the value of the specified issue's property.

        You can use this resource to store a custom data against the issue identified by the key or by the id. The user who stores the data is required to have permissions to edit the issue.
      operationId: com.atlassian.jira.rest.v2.issue.IssuePropertyResource.setIssueProperty_put
      x-api-path-slug: api2issueissueidorkeypropertiespropertykey-put
      parameters:
      - in: path
        name: issueIdOrKey
        description: the issue on which the property will be set
      - in: path
        name: propertyKey
        description: the key of the issues property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Issue
      - Property
    delete:
      summary: Delete issue property
      description: Removes the property from the issue identified by the key or by
        the id. Ths user removing the property is required to have permissions to
        edit the issue.
      operationId: com.atlassian.jira.rest.v2.issue.IssuePropertyResource.deleteIssueProperty_delete
      x-api-path-slug: api2issueissueidorkeypropertiespropertykey-delete
      parameters:
      - in: path
        name: issueIdOrKey
        description: the issue from which the property will be removed
      - in: path
        name: propertyKey
        description: the key of the property to remove
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Property
  /api/2/issue/{issueIdOrKey}/remotelink:
    get:
      summary: Get remote issue links
      description: Returns the remote issue links for the issue. This may be links
        to other Jira instances, web applications or web pages.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getRemoteIssueLinks_get
      x-api-path-slug: api2issueissueidorkeyremotelink-get
      parameters:
      - in: query
        name: globalId
        description: ID of the remote issue link to be returned
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to retrieve remote links for
      responses:
        200:
          description: OK
      tags:
      - Remote
      - Issue
      - Links
    post:
      summary: Create or update remote issue link
      description: Creates or updates a remote issue link from a JSON representation.
        If a `globalId` is provided and a remote issue link exists with that globalId,
        the remote issue link is updated. Otherwise, the remote issue link is created.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.createOrUpdateRemoteIssueLink_post
      x-api-path-slug: api2issueissueidorkeyremotelink-post
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to create/update the remote issue link
          for
      responses:
        200:
          description: OK
      tags:
      - Update
      - Remote
      - Issue
      - Link
    delete:
      summary: Delete remote issue link by global id
      description: Deletes the issue's remote link with the given global ID.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.deleteRemoteIssueLinkByGlobalId_delete
      x-api-path-slug: api2issueissueidorkeyremotelink-delete
      parameters:
      - in: query
        name: globalId
        description: Global ID of a remote issue link to delete
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to delete a remote issue link for
      responses:
        200:
          description: OK
      tags:
      - Remote
      - Issue
      - Link
      - By
      - Global
      - Id
  /api/2/issue/{issueIdOrKey}/remotelink/{linkId}:
    get:
      summary: Get remote issue link by id
      description: Returns the remote issue link by the given ID.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getRemoteIssueLinkById_get
      x-api-path-slug: api2issueissueidorkeyremotelinklinkid-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to retrieve the remote issue links for
      - in: path
        name: linkId
        description: ID of the remote issue link
      responses:
        200:
          description: OK
      tags:
      - Remote
      - Issue
      - Link
      - By
      - Id
    put:
      summary: Update remote issue link
      description: Updates a remote issue link from a JSON representation. Sets all
        fields without values provided to null.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.updateRemoteIssueLink_put
      x-api-path-slug: api2issueissueidorkeyremotelinklinkid-put
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to update the remote issue link for
      - in: path
        name: linkId
      responses:
        200:
          description: OK
      tags:
      - Remote
      - Issue
      - Link
    delete:
      summary: Delete remote issue link by id
      description: Deletes the issue's remote link with the given ID.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.deleteRemoteIssueLinkById_delete
      x-api-path-slug: api2issueissueidorkeyremotelinklinkid-delete
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to delete a remote issue link for
      - in: path
        name: linkId
        description: ID of a remote issue link to delete
      responses:
        200:
          description: OK
      tags:
      - Remote
      - Issue
      - Link
      - By
      - Id
  /api/2/issue/{issueIdOrKey}/transitions:
    get:
      summary: Get transitions
      description: |-
        Returns a list of transitions available for this issue for the current user.

        Specify `expand=transitions.fields` parameter to retrieve the fields required for a transition together with their types.

        Fields metadata corresponds to the fields available in a transition screen for a particular transition. Fields hidden from the screen will not be returned in the metadata.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getTransitions_get
      x-api-path-slug: api2issueissueidorkeytransitions-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to return transitions for
      - in: query
        name: skipRemoteOnlyCondition
        description: Flag to skip evaluation of {@link RemoteOnlyCondition}
      - in: query
        name: transitionId
      responses:
        200:
          description: OK
      tags:
      - Transitions
    post:
      summary: Do transition
      description: |-
        Performs the issue transition. While performing the transition you can modify other issue fields.

        The fields that can be set on transition, in either `fields` or `update` parameter can be determined using the **/rest/api/2/issue/{issueIdOrKey}/transitions?expand=transitions.fields** resource. If a field is not configured to appear on the transition screen, it will not be returned in the transition metadata. A field validation error will occur if such field is submitted in issue transition request.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.doTransition_post
      x-api-path-slug: api2issueissueidorkeytransitions-post
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to transition
      responses:
        200:
          description: OK
      tags:
      - Do
      - Transition
  /api/2/issue/{issueIdOrKey}/votes:
    get:
      summary: Get votes
      description: Returns voting data for an issue - whether the issue was voted
        for, total number of votes and users who voted for the issue.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getVotes_get
      x-api-path-slug: api2issueissueidorkeyvotes-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to retrieve voting information for
      responses:
        200:
          description: OK
      tags:
      - Votes
    post:
      summary: Add vote
      description: Adds a vote on the issue for a current user.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.addVote_post
      x-api-path-slug: api2issueissueidorkeyvotes-post
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to vote for
      responses:
        200:
          description: OK
      tags:
      - Vote
    delete:
      summary: Remove vote
      description: Removes a current user's vote from an issue (aka "unvote").
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.removeVote_delete
      x-api-path-slug: api2issueissueidorkeyvotes-delete
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue that current user unvotes
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Vote
  /api/2/issue/{issueIdOrKey}/watchers:
    get:
      summary: Get issue watchers
      description: Returns the list of watchers for the issue with the given key.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.getIssueWatchers_get
      x-api-path-slug: api2issueissueidorkeywatchers-get
      parameters:
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to retrieve watchers for
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Watchers
    post:
      summary: Add watcher
      description: Adds the user to the issue's watcher list.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.addWatcher_post
      x-api-path-slug: api2issueissueidorkeywatchers-post
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to be updated
      responses:
        200:
          description: OK
      tags:
      - Watcher
    delete:
      summary: Remove watcher
      description: Removes the user from the issue's watcher list.
      operationId: com.atlassian.jira.rest.v2.issue.IssueResource.removeWatcher_delete
      x-api-path-slug: api2issueissueidorkeywatchers-delete
      parameters:
      - in: query
        name: accountId
        description: Account ID of the user to be removed from the watcher list
      - in: header
        name: force-account-id
      - in: path
        name: issueIdOrKey
        description: ID or key of the issue to be updated
      - in: query
        name: username
        description: Name of the user to be removed from the watcher list
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Watcher
  /api/2/issue/{issueIdOrKey}/worklog:
    get:
      summary: Get issue worklog
      description: "Returns all work logs for an issue. The response is [paginated](#pagination)
        \ \n**Note:** Work logs won't be returned if the Log work field is hidden
        for the project."
      operationId: com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.getIssueWorklog_get
      x-api-path-slug: api2issueissueidorkeyworklog-get
      parameters:
      - in: query
        name: expand
        description: 'Optional comma separated list of parameters to expand: properties
          (provides worklog properties)'
      - in: path
        name: issueIdOrKey
        description: The worklogs belongs to
      - in: query
        name: maxResults
        description: Maximum number of items to return per page
      - in: query
        name: startAt
        description: Page offset, ie
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Worklog
    post:
      summary: Add worklog
      description: Adds a new worklog entry to an issue.
      operationId: com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.addWorklog_post
      x-api-path-slug: api2issueissueidorkeyworklog-post
      parameters:
      - in: query
        name: adjustEstimate
        description: (optional) allows you to provide specific instructions to update
          the remaining time estimate of the issue
      - in: query
        name: expand
        description: 'optional comma separated list of parameters to expand: properties
          (provides worklog properties)'
      - in: path
        name: issueIdOrKey
        description: a string containing the issue id or key the worklog will be added
          to
      - in: query
        name: newEstimate
        description: (required when new is selected for adjustEstimate) the new value
          for the remaining estimate field
      - in: query
        name: notifyUsers
        description: (optional) whether or not users should be notified by email,
          true by default
      - in: query
        name: overrideEditableFlag
        description: Updates the issue even if the issue is not editable due to being
          in a status with jira
      - in: query
        name: reduceBy
        description: (required when manual is selected for adjustEstimate) the amount
          to reduce the remaining estimate by e
      responses:
        200:
          description: OK
      tags:
      - Worklog
  /api/2/issue/{issueIdOrKey}/worklog/{id}:
    get:
      summary: Get worklog
      description: "Returns a specific worklog.  \n**Note:** The work log won't be
        returned if the Log work field is hidden for the project."
      operationId: com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.getWorklog_get
      x-api-path-slug: api2issueissueidorkeyworklogid-get
      parameters:
      - in: query
        name: expand
        description: 'optional comma separated list of parameters to expand: properties
          (provides worklog properties)'
      - in: path
        name: id
        description: a String containing the work log id
      - in: path
        name: issueIdOrKey
        description: a string containing the issue id or key the worklog belongs to
      responses:
        200:
          description: OK
      tags:
      - Worklog
    put:
      summary: Update worklog
      description: |-
        Updates an existing worklog entry.

        Note that:

        *   Fields possible for editing are: comment, visibility, started, timeSpent and timeSpentSeconds.
        *   Either timeSpent or timeSpentSeconds can be set.
        *   Fields which are not set will not be updated.
        *   For a request to be valid, it has to have at least one field change.
      operationId: com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.updateWorklog_put
      x-api-path-slug: api2issueissueidorkeyworklogid-put
      parameters:
      - in: query
        name: adjustEstimate
        description: (optional) allows you to provide specific instructions to update
          the remaining time estimate of the issue
      - in: query
        name: expand
        description: 'optional comma separated list of parameters to expand: properties
          (provides worklog properties)'
      - in: path
        name: id
        description: id of the worklog to be updated
      - in: path
        name: issueIdOrKey
        description: a string containing the issue id or key the worklog belongs to
      - in: query
        name: newEstimate
        description: (required when new is selected for adjustEstimate) the new value
          for the remaining estimate field
      - in: query
        name: notifyUsers
        description: (optional) whether or not users should be notified by email,
          true by default
      - in: query
        name: overrideEditableFlag
        description: Updates the issue even if the issue is not editable due to being
          in a status with jira
      responses:
        200:
          description: OK
      tags:
      - Worklog
    delete:
      summary: Delete worklog
      description: Deletes an existing worklog entry.
      operationId: com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.deleteWorklog_delete
      x-api-path-slug: api2issueissueidorkeyworklogid-delete
      parameters:
      - in: query
        name: adjustEstimate
        description: (optional) allows you to provide specific instructions to update
          the remaining time estimate of the issue
      - in: path
        name: id
        description: id of the worklog to be deleted
      - in: query
        name: increaseBy
        description: (required when manual is selected for adjustEstimate) the amount
          to increase the remaining estimate by e
      - in: path
        name: issueIdOrKey
        description: a string containing the issue id or key the worklog belongs to
      - in: query
        name: newEstimate
        description: (required when new is selected for adjustEstimate) the new value
          for the remaining estimate field
      - in: query
        name: notifyUsers
        description: (optional) whether or not users should be notified by email,
          true by default
      - in: query
        name: overrideEditableFlag
        description: Updates the issue even if the issue is not editable due to being
          in a status with jira
      responses:
        200:
          description: OK
      tags:
      - Worklog
  /api/2/issue/{issueIdOrKey}/worklog/{worklogId}/properties:
    get:
      summary: Get worklog property keys
      description: Returns the keys of all properties for the worklog identified by
        the key or by the id.
      operationId: com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.getWorklogPropertyKeys_get
      x-api-path-slug: api2issueissueidorkeyworklogworklogidproperties-get
      parameters:
      - in: path
        name: issueIdOrKey
      - in: path
        name: worklogId
        description: the worklog from which keys will be returned
      responses:
        200:
          description: OK
      tags:
      - Worklog
      - Property
      - Keys
  /api/2/issue/{issueIdOrKey}/worklog/{worklogId}/properties/{propertyKey}:
    get:
      summary: Get worklog property
      description: Returns the value of the property with a given key from the worklog
        identified by the key or by the id. The user who retrieves the property is
        required to have permissions to read the worklog.
      operationId: com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.getWorklogProperty_get
      x-api-path-slug: api2issueissueidorkeyworklogworklogidpropertiespropertykey-get
      parameters:
      - in: path
        name: issueIdOrKey
      - in: path
        name: propertyKey
        description: the key of the property to return
      - in: path
        name: worklogId
        description: the worklog from which the property will be returned
      responses:
        200:
          description: OK
      tags:
      - Worklog
      - Property
    put:
      summary: Set worklog property
      description: |-
        Sets the value of the specified worklog's property.

        You can use this resource to store a custom data against the worklog identified by the key or by the id. The user who stores the data is required to have permissions to administer the worklog.
      operationId: com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.setWorklogProperty_put
      x-api-path-slug: api2issueissueidorkeyworklogworklogidpropertiespropertykey-put
      parameters:
      - in: path
        name: issueIdOrKey
      - in: path
        name: propertyKey
        description: the key of the worklogs property
      - in: path
        name: worklogId
        description: the worklog on which the property will be set
      responses:
        200:
          description: OK
      tags:
      - Set
      - Worklog
      - Property
    delete:
      summary: Delete worklog property
      description: Removes the property from the worklog identified by the key or
        by the id. Ths user removing the property is required to have permissions
        to administer the worklog.
      operationId: com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.deleteWorklogProperty_delete
      x-api-path-slug: api2issueissueidorkeyworklogworklogidpropertiespropertykey-delete
      parameters:
      - in: path
        name: issueIdOrKey
      - in: path
        name: propertyKey
        description: the key of the property to remove
      - in: path
        name: worklogId
        description: the worklog from which the property will be removed
      responses:
        200:
          description: OK
      tags:
      - Worklog
      - Property
  /api/2/issueLink:
    post:
      summary: Link issues
      description: Creates an issue link between two issues. The user requires the
        link issue permission for the issue which will be linked to another issue.
        The specified link type in the request is used to create the link and will
        create a link from the first issue to the second issue using the outward description.
        It also create a link from the second issue to the first issue using the inward
        description of the issue link type. It will add the supplied comment to the
        first issue. The comment can have a restriction who can view it. If group
        is specified, only users of this group can view this comment, if roleLevel
        is specified only users who have the specified role can view this comment.
        The user who creates the issue link needs to belong to the specified group
        or have the specified role.
      operationId: com.atlassian.jira.rest.v2.issue.LinkIssueResource.linkIssues_post
      x-api-path-slug: api2issuelink-post
      responses:
        200:
          description: OK
      tags:
      - Link
      - Issues
  /api/2/issueLink/{linkId}:
    get:
      summary: Get issue link
      description: Returns an issue link with the specified id.
      operationId: com.atlassian.jira.rest.v2.issue.LinkIssueResource.getIssueLink_get
      x-api-path-slug: api2issuelinklinkid-get
      parameters:
      - in: path
        name: linkId
        description: the issue link id
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Link
    delete:
      summary: Delete issue link
      description: Deletes an issue link with the specified id. To be able to delete
        an issue link you must be able to view both issues and must have the link
        issue permission for at least one of the issues.
      operationId: com.atlassian.jira.rest.v2.issue.LinkIssueResource.deleteIssueLink_delete
      x-api-path-slug: api2issuelinklinkid-delete
      parameters:
      - in: path
        name: linkId
        description: the issue link id
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Link
  /api/2/issueLinkType:
    get:
      summary: Get issue link types
      description: Returns a list of available issue link types, if issue linking
        is enabled. Each issue link type has an id, a name and a label for the outward
        and inward link relationship.
      operationId: com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.getIssueLinkTypes_get
      x-api-path-slug: api2issuelinktype-get
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Link
      - Types
    post:
      summary: Create issue link type
      description: Create a new issue link type.
      operationId: com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.createIssueLinkType_post
      x-api-path-slug: api2issuelinktype-post
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Link
      - Type
  /api/2/issueLinkType/{issueLinkTypeId}:
    get:
      summary: Get issue link type
      description: Returns for a given issue link type id all information about this
        issue link type.
      operationId: com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.getIssueLinkType_get
      x-api-path-slug: api2issuelinktypeissuelinktypeid-get
      parameters:
      - in: path
        name: issueLinkTypeId
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Link
      - Type
    put:
      summary: Update issue link type
      description: Update the specified issue link type.
      operationId: com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.updateIssueLinkType_put
      x-api-path-slug: api2issuelinktypeissuelinktypeid-put
      parameters:
      - in: path
        name: issueLinkTypeId
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Link
      - Type
    delete:
      summary: Delete issue link type
      description: Delete the specified issue link type.
      operationId: com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.deleteIssueLinkType_delete
      x-api-path-slug: api2issuelinktypeissuelinktypeid-delete
      parameters:
      - in: path
        name: issueLinkTypeId
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Link
      - Type
  /api/2/issuesecurityschemes:
    get:
      summary: Get issue security schemes
      description: Returns all issue security schemes that are defined.
      operationId: com.atlassian.jira.rest.v2.issue.IssueSecuritySchemeResource.getIssueSecuritySchemes_get
      x-api-path-slug: api2issuesecurityschemes-get
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Security
      - Schemes
  /api/2/issuesecurityschemes/{id}:
    get:
      summary: Get issue security scheme
      description: Returns the issue security scheme along with that are defined.
      operationId: com.atlassian.jira.rest.v2.issue.IssueSecuritySchemeResource.getIssueSecurityScheme_get
      x-api-path-slug: api2issuesecurityschemesid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Security
      - Scheme
  /api/2/issuetype:
    get:
      summary: Get all issue types for user
      description: Returns all issue types. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira, however, only issue types that are
        visible to the user are returned.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.getIssueAllTypes_get
      x-api-path-slug: api2issuetype-get
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Typesuser
    post:
      summary: Create issue type
      description: Creates an issue type and adds it to the default issue type scheme.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.createIssueType_post
      x-api-path-slug: api2issuetype-post
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
  /api/2/issuetype/{id}:
    get:
      summary: Get issue type
      description: |-
        Returns an issue type. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

        *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
        *   _Browse projects_ project permission to get the details of any issue type associated with the projects the user has permission to browse.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.getIssueType_get
      x-api-path-slug: api2issuetypeid-get
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
    put:
      summary: Update issue type
      description: Updates the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.updateIssueType_put
      x-api-path-slug: api2issuetypeid-put
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
    delete:
      summary: Delete issue type
      description: Deletes the issue type. If the issue type is in use, all uses are
        updated with the alternative issue type (`alternativeIssueTypeId`). A list
        of alternative issue types can be obtained from the [Get alternative issue
        types](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-alternatives-get)
        resource. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        _Administer Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.deleteIssueType_delete
      x-api-path-slug: api2issuetypeid-delete
      parameters:
      - in: query
        name: alternativeIssueTypeId
        description: The ID of the replacement issue type
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
  /api/2/issuetype/{id}/alternatives:
    get:
      summary: Get alternative issue types
      description: Returns a list of issue types that can be used to replace the issue
        type. The alternative issue types are those assigned to the same workflow
        scheme, field configuration scheme, and screen scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.getAlternativeIssueTypes_get
      x-api-path-slug: api2issuetypeidalternatives-get
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Alternative
      - Issue
      - Types
  /api/2/issuetype/{id}/avatar2:
    post:
      summary: Create issue type avatar
      description: |-
        Creates an avatar for the issue type. Specify the avatar's local file location as binary data in the body of the request. Also, include the following headers:

        *   `X-Atlassian-Token: no-check`
        *   `Content-Type: image/_image type_` Valid image types are JPEG, GIF, or PNG.

        For example: `curl --request POST \ --user email@example.com: \ --header 'X-Atlassian-Token: no-check' \ --header 'Content-Type: image/< image_type>' \ --data-binary "" \ --url 'https://your-domain.atlassian.net/rest/api/2/issuetype/{issueTypeId}'This` The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image. The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size. After creating the avatar, use [Update issue type](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-put) to set it as the issue type's active avatar. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypeResource.createIssueTypeAvatar_post
      x-api-path-slug: api2issuetypeidavatar2-post
      parameters:
      - in: path
        name: id
        description: The ID of the issue type
      - in: query
        name: size
        description: The length of each side of the crop region
      - in: query
        name: x
        description: The X coordinate of the top-left corner of the crop region
      - in: query
        name: "y"
        description: The Y coordinate of the top-left corner of the crop region
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Avatar
  /api/2/issuetype/{issueTypeId}/properties:
    get:
      summary: Get issue type property keys
      description: |-
        Returns all the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys of the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   _Administer Jira_ [global permission](href=) to get the property keys of any issue type.
        *   _Browse projects_ project permission to get the property keys of any issue types associated with the projects the user has permission to browse.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.getIssueTypePropertyKeys_get
      x-api-path-slug: api2issuetypeissuetypeidproperties-get
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Property
      - Keys
  /api/2/issuetype/{issueTypeId}/properties/{propertyKey}:
    get:
      summary: Get issue type property
      description: |-
        Returns the key and value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

        *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
        *   _Browse projects_ project permission to get the details of any issue types associated with the projects the user has permission to browse.
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.getIssueTypeProperty_get
      x-api-path-slug: api2issuetypeissuetypeidpropertiespropertykey-get
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      - in: path
        name: propertyKey
        description: The key of the property
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Property
    put:
      summary: Set issue type property
      description: Creates or updates the value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
        Use this resource to store and update data against an issue type. The value
        of the request body must be a [valid](http://tools.ietf.org/html/rfc4627),
        non-empty JSON blob. The maximum length of the property value is 32768 bytes.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.setIssueTypeProperty_put
      x-api-path-slug: api2issuetypeissuetypeidpropertiespropertykey-put
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      - in: path
        name: propertyKey
        description: The key of the issue type property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Issue
      - Type
      - Property
    delete:
      summary: Delete issue type property
      description: Deletes the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=).
      operationId: com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.deleteIssueTypeProperty_delete
      x-api-path-slug: api2issuetypeissuetypeidpropertiespropertykey-delete
      parameters:
      - in: path
        name: issueTypeId
        description: The ID of the issue type
      - in: path
        name: propertyKey
        description: The key of the property
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Type
      - Property
  /api/2/jql/autocompletedata:
    get:
      summary: Get auto complete
      description: Returns the auto complete data required for JQL searches.
      operationId: com.atlassian.jira.rest.v2.search.SearchAutoCompleteResource.getAutoComplete_get
      x-api-path-slug: api2jqlautocompletedata-get
      responses:
        200:
          description: OK
      tags:
      - Auto
      - Complete
  /api/2/jql/autocompletedata/suggestions:
    get:
      summary: Get field auto complete for query string
      description: Returns auto complete suggestions for JQL search.
      operationId: com.atlassian.jira.rest.v2.search.SearchAutoCompleteResource.getFieldAutoCompleteForQueryString_get
      x-api-path-slug: api2jqlautocompletedatasuggestions-get
      parameters:
      - in: query
        name: fieldName
        description: the field name for which the suggestions are generated
      - in: query
        name: fieldValue
        description: the portion of the field value that has already been provided
          by the user
      - in: query
        name: predicateName
        description: the predicate for which the suggestions are generated
      - in: query
        name: predicateValue
        description: the portion of the predicate value that has already been provided
          by the user
      responses:
        200:
          description: OK
      tags:
      - Field
      - Auto
      - Completequery
      - String
  /api/2/licenseValidator:
    post:
      summary: Validate license
      description: |-
        Validates a Jira license.

        Typically used by the setup phase of the Jira application. Returns an object with a list of errors as key, value pairs if the license is not valid.
      operationId: com.atlassian.jira.rest.v2.license.LicenceValidator.validateLicense_post
      x-api-path-slug: api2licensevalidator-post
      responses:
        200:
          description: OK
      tags:
      - Validate
      - License
  /api/2/mypermissions:
    get:
      summary: Get my permissions
      description: |-
        Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

        If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

        If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

        If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

        The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

        Global permissions work in the same way regardless of the scope.
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getMyPermissions_get
      x-api-path-slug: api2mypermissions-get
      parameters:
      - in: query
        name: issueId
        description: Id of the issue to scope returned permissions for
      - in: query
        name: issueKey
        description: Key of the issue to scope returned permissions for
      - in: query
        name: permissions
        description: A comma separated list of permission keys to check
      - in: query
        name: projectId
        description: Id of project to scope returned permissions for
      - in: query
        name: projectKey
        description: Key of project to scope returned permissions for
      responses:
        200:
          description: OK
      tags:
      - My
      - Permissions
  /api/2/mypreferences:
    get:
      summary: Get preference
      description: Returns preference of the currently logged in user. Preference
        key must be provided as input parameter (key). The value is returned exactly
        as it is.
      operationId: com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.getPreference_get
      x-api-path-slug: api2mypreferences-get
      parameters:
      - in: query
        name: key
        description: \- key of the preference to be returned
      responses:
        200:
          description: OK
      tags:
      - Preference
    put:
      summary: Set preference
      description: Sets preference of the currently logged in user. Preference key
        must be provided as input parameters (key). Value must be provided as POST
        body.
      operationId: com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.setPreference_put
      x-api-path-slug: api2mypreferences-put
      parameters:
      - in: query
        name: key
        description: \- key of the preference to be set
      responses:
        200:
          description: OK
      tags:
      - Set
      - Preference
    delete:
      summary: Remove preference
      description: Removes preference of the currently logged in user. Preference
        key must be provided as input parameters (key).
      operationId: com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.removePreference_delete
      x-api-path-slug: api2mypreferences-delete
      parameters:
      - in: query
        name: key
        description: \- key of the preference to be removed
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Preference
  /api/2/mypreferences/locale:
    get:
      summary: Get locale
      description: Returns the locale of the currently logged in user. If the user
        has no language preference explicitly set (the default setting), or is anonymous,
        this will be the browser locale detected by Jira. If browser detection is
        in effect, the "Accept-Language" browser header is used and falls back to
        the Jira site default locale if no match is found.
      operationId: com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.getLocale_get
      x-api-path-slug: api2mypreferenceslocale-get
      responses:
        200:
          description: OK
      tags:
      - Locale
    put:
      summary: Set locale
      description: Sets the locale of the currently logged in user. Locale JSON must
        be provided as PUT body.
      operationId: com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.setLocale_put
      x-api-path-slug: api2mypreferenceslocale-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Locale
    delete:
      summary: Delete locale
      description: Deletes the set locale of the currently logged in user, resetting
        it to default.
      operationId: com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.deleteLocale_delete
      x-api-path-slug: api2mypreferenceslocale-delete
      responses:
        200:
          description: OK
      tags:
      - Locale
  /api/2/myself:
    get:
      summary: Get current user
      description: |-
        Returns currently logged user. This resource cannot be accessed anonymously.

        The resource accepts the `expand` param that is used to include, hidden by default, parts of response. This can be used to include:

        *   `groups` \- all groups, including nested groups, to which user belongs
        *   `applicationRoles` \- application roles defines to which application user has access
      operationId: com.atlassian.jira.rest.v2.issue.CurrentUserResource.getCurrentUser_get
      x-api-path-slug: api2myself-get
      responses:
        200:
          description: OK
      tags:
      - Current
      - User
  /api/2/notificationscheme:
    get:
      summary: Get notification schemes paginated
      description: |-
        Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) list of [notification schemes](https://confluence.atlassian.com/x/8YdKLg) in order by display name.

        ### About notification schemes

        A notification scheme is a list of events and recipients who will receive notifications for those events. The list is contained within the `notificationSchemeEvents` object and contains pairs of `events` and `notifications`:

        *   `event` Identifies the type of event. The events can be [Jira system events](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-eventsEvents) or [custom events](https://confluence.atlassian.com/x/AIlKLg).
        *   `notifications` Identifies the [recipients](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-recipientsRecipients) of notifications for each event. Recipients can be any of the following types:

        *   `CurrentAssignee`
        *   `Reporter`
        *   `CurrentUser`
        *   `ProjectLead`
        *   `ComponentLead`
        *   `User` (the `parameter` is the user key)
        *   `Group` (the `parameter` is the group name)
        *   `ProjectRole` (the `parameter` is the project role ID)
        *   `EmailAddress`
        *   `AllWatchers`
        *   `UserCustomField` (the `parameter` is the ID of the custom field)
        *   `GroupCustomField`(the `parameter` is the ID of the custom field)

        _Note that you should allow for events without recipients to appear in responses._

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with a notification scheme for it to be returned.
      operationId: com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationSchemes_get
      x-api-path-slug: api2notificationscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Schemes
      - Paginated
  /api/2/notificationscheme/{id}:
    get:
      summary: Get notification scheme
      description: |-
        Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with the requested notification scheme.
      operationId: com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationScheme_get
      x-api-path-slug: api2notificationschemeid-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: id
        description: The ID of the notification scheme
      responses:
        200:
          description: OK
      tags:
      - Notification
      - Scheme
  /api/2/permissions:
    get:
      summary: Get all permissions
      description: Returns all permissions that are present in the Jira instance -
        Global, Project and the global ones added by plugins
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getAllPermissions_get
      x-api-path-slug: api2permissions-get
      responses:
        200:
          description: OK
      tags:
      - Permissions
  /api/2/permissions/project:
    post:
      summary: Get permitted projects
      description: Returns all projects where currently logged in user was granted
        ALL requested project permissions.
      operationId: com.atlassian.jira.rest.v2.permission.PermissionsResource.getPermittedProjects_post
      x-api-path-slug: api2permissionsproject-post
      responses:
        200:
          description: OK
      tags:
      - Permitted
      - Projects
  /api/2/permissionscheme:
    get:
      summary: Get all permission schemes
      description: |-
        Returns all permission schemes.

        ### About permission schemes and grants

        A permission scheme is a collection of permission grants. A permission grant consists of a `holder` and a `permission`.

        #### Holder

        The `holder` object contains information about the user or group being granted the permission. For example, the _Administer projects_ permission is granted to a group named _Teams in space administrators_. In this case, the type is `"type": "group"`, and the parameter is the group name, `"parameter": "Teams in space administrators"`. The `holder` object is defined by the following properties:

        *   `type` Identifies the user or group (see the list of types below).
        *   `parameter` The value of this property depends on the `type`. For example, if the `type` is a group, then you need to specify the group name.

        The following `types` are available. The expected values for the `parameter` are given in parenthesis (some `types` may not have a `parameter`):

        *   `anyone` Grant for anonymous users.
        *   `applicationRole` Grant for users with access to the specified application (application name). See [Manage application access](https://confluence.atlassian.com/cloud/manage-application-access-744721629.html) for more information.
        *   `assignee` Grant for the user currently assigned to an issue.
        *   `group` Grant for the specified group (group name).
        *   `groupCustomField` Grant for a user in the group selected in the specified custom field (custom field ID).
        *   `projectLead` Grant for a project lead.
        *   `projectRole` Grant for the specified project role (project role ID).
        *   `reporter` Grant for the user who reported the issue.
        *   `sd.customer.portal.only` Jira Service Desk only. Grants customers permission to access the customer portal but not Jira. See [Customizing Jira Service Desk permissions](https://confluence.atlassian.com/x/24dKLg) for more information.
        *   `user` Grant for the specified user (user ID).
        *   `userCustomField` Grant for a user selected in the specified custom field (custom field ID).

        #### Permissions

        The [built-in Jira permissions](https://confluence.atlassian.com/x/yodKLg) are listed below. Apps can also define custom permissions. See the [project permission](https://developer.atlassian.com/cloud/jira/platform/modules/project-permission/) and [global permission](https://developer.atlassian.com/cloud/jira/platform/modules/global-permission/) module documentation for more information.

        **Project permissions**

        *   `ADMINISTER_PROJECTS`
        *   `BROWSE_PROJECTS`
        *   `MANAGE_SPRINTS_PERMISSION` (Jira Software only)
        *   `SERVICEDESK_AGENT` (Jira Service Desk only)
        *   `VIEW_DEV_TOOLS` (Jira Software only)
        *   `VIEW_READONLY_WORKFLOW`

        **Issue permissions**

        *   `ASSIGNABLE_USER`
        *   `ASSIGN_ISSUES`
        *   `CLOSE_ISSUES`
        *   `CREATE_ISSUES`
        *   `DELETE_ISSUES`
        *   `EDIT_ISSUES`
        *   `LINK_ISSUES`
        *   `MODIFY_REPORTER`
        *   `MOVE_ISSUES`
        *   `RESOLVE_ISSUES`
        *   `SCHEDULE_ISSUES`
        *   `SET_ISSUE_SECURITY`
        *   `TRANSITION_ISSUES`

        **Voters and watchers permissions**

        *   `MANAGE_WATCHERS`
        *   `VIEW_VOTERS_AND_WATCHERS`

        **Comments permissions**

        *   `ADD_COMMENTS`
        *   `DELETE_ALL_COMMENTS`
        *   `DELETE_OWN_COMMENTS`
        *   `EDIT_ALL_COMMENTS`
        *   `EDIT_OWN_COMMENTS`

        **Attachments permissions**

        *   `CREATE_ATTACHMENTS`
        *   `DELETE_ALL_ATTACHMENTS`
        *   `DELETE_OWN_ATTACHMENTS`

        **Time tracking permissions**

        *   `DELETE_ALL_WORKLOGS`
        *   `DELETE_OWN_WORKLOGS`
        *   `EDIT_ALL_WORKLOGS`
        *   `EDIT_OWN_WORKLOGS`
        *   `WORK_ON_ISSUES`

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getAllPermissionSchemes_g
      x-api-path-slug: api2permissionscheme-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Schemes
    post:
      summary: Create permission scheme
      description: Creates a new permission scheme. You can create a permission scheme
        with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.createPermissionScheme_po
      x-api-path-slug: api2permissionscheme-post
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
  /api/2/permissionscheme/{schemeId}:
    get:
      summary: Get permission scheme
      description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionScheme_get
      x-api-path-slug: api2permissionschemeschemeid-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme to return (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
    put:
      summary: Update permission scheme
      description: |-
        Updates a permission scheme. Below are some important things to note when using this resource:

        *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
        *   If you want to update only the name and description, then do not send a permissions list in the request.
        *   Sending an empty list will remove all permission grants from the permission scheme.

        If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.updatePermissionScheme_pu
      x-api-path-slug: api2permissionschemeschemeid-put
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme to update (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
    delete:
      summary: Delete permission scheme
      description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionScheme_de
      x-api-path-slug: api2permissionschemeschemeid-delete
      parameters:
      - in: path
        name: schemeId
        description: The ID of the permission scheme being deleted (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
  /api/2/permissionscheme/{schemeId}/permission:
    get:
      summary: Get permission scheme grants
      description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrants
      x-api-path-slug: api2permissionschemeschemeidpermission-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Grants
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