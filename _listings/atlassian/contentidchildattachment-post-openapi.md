---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Create attachment
  description: "Adds an attachment to a piece of content. This method only adds a
    new \nattachment. If you want to update an existing attachment, use \n[Create
    or update attachments](#api-content-id-child-attachment-put).\n\nNote, you must
    set a `X-Atlassian-Token: nocheck` header on the request \nfor this method, otherwise
    it will be blocked. This protects against XSRF \nattacks, which is necessary as
    this method accepts multipart/form-data.\n\nThe media type 'multipart/form-data'
    is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client
    libraries have classes that make it easier to implement \nmultipart posts, like
    the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html)
    \nJava class provided by Apache HTTP Components.\n\nExample: This curl command
    attaches a file ('example.txt') to a container \n(id='123') with a comment and
    `minorEdits`=true.\n\n``` bash\ncurl -D- \\\n  -u admin:admin \\\n  -X POST \\\n
    \ -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\"
    \\\n  -F \"comment=Example attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
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