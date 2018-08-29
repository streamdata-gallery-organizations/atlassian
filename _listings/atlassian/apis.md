---
name: Atlassian
x-slug: atlassian
description: Millions of users globally rely on Atlassian products every day for improving
  software development, project management, collaboration, and code quality.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
x-kinRank: "8"
x-alexaRank: "1656"
tags: Atlassian
created: "2018-08-29"
modified: "2018-08-29"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/apis.md
specificationVersion: "0.14"
apis:
- name: The Confluence Cloud REST API - Get audit records
  x-api-slug: audit-get
  description: "Returns all records in the audit log, optionally for a certain date
    range. \nThis contains information about events like space exports, group membership
    \nchanges, app installations, etc. For more information, see \n[Audit log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html)
    \nin the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/audit-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/audit-get-openapi.md
- name: The Confluence Cloud REST API - Create audit record
  x-api-slug: audit-post
  description: "Creates a record in the audit log. \n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/audit-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/audit-post-openapi.md
- name: The Confluence Cloud REST API - Export audit records
  x-api-slug: auditexport-get
  description: "Exports audit records as a CSV file or ZIP file.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditexport-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditexport-get-openapi.md
- name: The Confluence Cloud REST API - Get retention period
  x-api-slug: auditretention-get
  description: "Returns the retention period for records in the audit log. The retention
    \nperiod is how long an audit record is kept for, from creation date until \nit
    is deleted.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    \n'Confluence Administrator' global permission."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditretention-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditretention-get-openapi.md
- name: The Confluence Cloud REST API - Set retention period
  x-api-slug: auditretention-put
  description: "Sets the retention period for records in the audit log. The retention
    period \ncan be set to a maximum of 20 years.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditretention-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditretention-put-openapi.md
- name: The Confluence Cloud REST API - Get audit records for time period
  x-api-slug: auditsince-get
  description: "Returns records from the audit log, for a time period back from the
    current \ndate. For example, you can use this method to get the last 3 months
    of records.\n\nThis contains information about events like space exports, group
    membership \nchanges, app installations, etc. For more information, see \n[Audit
    log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html) \nin
    the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditsince-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auditsince-get-openapi.md
- name: The Confluence Cloud REST API - Get content
  x-api-slug: content-get
  description: "Returns all content in a Confluence instance.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission).
    \nOnly content that the user has permission to view will be returned."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/content-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/content-get-openapi.md
- name: The Confluence Cloud REST API - Create content
  x-api-slug: content-post
  description: "Creates a new piece of content or publishes an existing draft. \n\nTo
    publish a draft, add the `id` and `status` properties to the body of the request.
    \nSet the `id` to the ID of the draft and set the `status` to 'current'. When
    the \nrequest is sent, a new piece of content will be created and the metadata
    from the \ndraft will be transferred into it.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: 'Add' permission for the \nspace that the content will be created
    in, and permission to view the draft if publishing a draft."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/content-post-openapi.md
- name: The Confluence Cloud REST API - Publish legacy draft
  x-api-slug: contentblueprintinstancedraftid-post
  description: "Publishes a legacy draft of a page created from a blueprint. Legacy
    drafts \nwill eventually be removed in favour of shared drafts. For now, this
    method \nworks the same as [Publish shared draft](#api-content-blueprint-instance-draftId-put).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the draft and 'Add' permission for the space
    that \nthe content will be created in."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentblueprintinstancedraftid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentblueprintinstancedraftid-post-openapi.md
- name: The Confluence Cloud REST API - Publish shared draft
  x-api-slug: contentblueprintinstancedraftid-put
  description: "Publishes a shared draft of a page created from a blueprint.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the draft and 'Add' permission for the space
    that \nthe content will be created in."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentblueprintinstancedraftid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentblueprintinstancedraftid-put-openapi.md
- name: The Confluence Cloud REST API - Search content by CQL
  x-api-slug: contentsearch-get
  description: "Returns the list of content that matches a Confluence Query Language
    \n(CQL) query. For information on CQL, see: \n[Advanced searching using CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission).
    \nOnly content that the user has permission to view will be returned."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentsearch-get-openapi.md
- name: The Confluence Cloud REST API - Get content by ID
  x-api-slug: contentid-get
  description: "Returns a single piece of content, like a page or a blog post.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content. If the content is a blog post, 'View'
    permission \nfor the space is required."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentid-get-openapi.md
- name: The Confluence Cloud REST API - Update content
  x-api-slug: contentid-put
  description: "Updates a piece of content. Use this method to update the title or
    body \nof a piece of content, change the status, change the parent page, and more.\n\nNote,
    updating draft content is currently not supported.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentid-put-openapi.md
- name: The Confluence Cloud REST API - Delete content
  x-api-slug: contentid-delete
  description: "Moves a piece of content to the space's trash or purges it from the
    trash, \ndepending on the content's type and status:\n\n- If the content's type
    is `page` or `blogpost` and its status is `current`, \nit will be trashed.\n-
    If the content's type is `page` or `blogpost` and its status is `trashed`, \nthe
    content will be purged from the trash and deleted permanently. Note, \nyou must
    also set the `status` query parameter to `trashed` in your request.\n- If the
    content's type is `comment` or `attachment`, it will be deleted \npermanently
    without being trashed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Delete' permission for the space that the content is in, and permission
    to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentid-delete-openapi.md
- name: The Confluence Cloud REST API - Get content children
  x-api-slug: contentidchild-get
  description: "Returns a map of the direct children of a piece of content. A piece
    of content \nhas different types of child content, depending on its type. These
    are \nthe default parent-child content type relationships:\n\n- `page`: child
    content is `page`, `comment`, `attachment`\n- `blogpost`: child content is `comment`,
    `attachment`\n- `attachment`: child content is `comment`\n- `comment`: child content
    is `attachment`\n\nApps can override these default relationships. Apps can also
    introduce \nnew content types that create new parent-child content relationships.\n\nNote,
    the map will always include all child content types that are valid \nfor the content.
    However, if the content has no instances of a child content \ntype, the map will
    contain an empty array for that child content type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: 'View' permission for the space, \nand permission to view the content
    if it is a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchild-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchild-get-openapi.md
- name: The Confluence Cloud REST API - Get attachments
  x-api-slug: contentidchildattachment-get
  description: "Returns the attachments for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content. If the content is a blog post, 'View'
    permission \nfor the space is required."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachment-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachment-get-openapi.md
- name: The Confluence Cloud REST API - Create attachment
  x-api-slug: contentidchildattachment-post
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachment-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachment-post-openapi.md
- name: The Confluence Cloud REST API - Create or update attachment
  x-api-slug: contentidchildattachment-put
  description: "Adds an attachment to a piece of content. If the attachment already
    exists \nfor the content, then the attachment is updated (i.e. a new version of
    the \nattachment is created).\n\nNote, you must set a `X-Atlassian-Token: nocheck`
    header on the request \nfor this method, otherwise it will be blocked. This protects
    against XSRF \nattacks, which is necessary as this method accepts multipart/form-data.\n\nThe
    media type 'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt).
    \nMost client libraries have classes that make it easier to implement \nmultipart
    posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html)
    \nJava class provided by Apache HTTP Components.\n\nExample: This curl command
    attaches a file ('example.txt') to a piece of \ncontent (id='123') with a comment
    and `minorEdits`=true. If the 'example.txt' \nfile already exists, it will update
    it with a new version of the attachment.\n\n``` bash\ncurl -D- \\\n  -u admin:admin
    \\\n  -X PUT \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\"
    \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\" \\\n
    \ http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachment-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachment-put-openapi.md
- name: The Confluence Cloud REST API - Update attachment properties
  x-api-slug: contentidchildattachmentattachmentid-put
  description: "Updates the attachment properties, i.e. the non-binary data of an
    attachment \nlike the filename, media-type, comment, and parent container.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachmentattachmentid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachmentattachmentid-put-openapi.md
- name: The Confluence Cloud REST API - Update attachment data
  x-api-slug: contentidchildattachmentattachmentiddata-post
  description: "Updates the binary data of an attachment, given the attachment ID,
    and \noptionally the comment and the minor edit field.\n\nThis method is essentially
    the same as [Create or update attachments](#api-content-id-child-attachment-put),
    \nexcept that it matches the attachment ID rather than the name.\n\nNote, you
    must set a `X-Atlassian-Token: nocheck` header on the request \nfor this method,
    otherwise it will be blocked. This protects against XSRF \nattacks, which is necessary
    as this method accepts multipart/form-data.\n\nThe media type 'multipart/form-data'
    is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client
    libraries have classes that make it easier to implement \nmultipart posts, like
    the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html)
    \nJava class provided by Apache HTTP Components.\n\nExample: This curl command
    updates an attachment (id='att456') that is attached  \nto a piece of content
    (id='123') with a comment and `minorEdits`=true. \n\n``` bash\ncurl -D- \\\n  -u
    admin:admin \\\n  -X POST \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\"
    \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\" \\\n
    \ http://myhost/rest/api/content/123/child/attachment/att456/data\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachmentattachmentiddata-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildattachmentattachmentiddata-post-openapi.md
- name: The Confluence Cloud REST API - Get content comments
  x-api-slug: contentidchildcomment-get
  description: "Returns the comments on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: 'View' permission for the space, \nand permission to view the content
    if it is a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildcomment-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildcomment-get-openapi.md
- name: The Confluence Cloud REST API - Get content children by type
  x-api-slug: contentidchildtype-get
  description: "Returns all children of a given type, for a piece of content. \nA
    piece of content has different types of child content, depending on its type:\n\n-
    `page`: child content is `page`, `comment`, `attachment`\n- `blogpost`: child
    content is `comment`, `attachment`\n- `attachment`: child content is `comment`\n-
    `comment`: child content is `attachment`\n\nCustom content types that are provided
    by apps can also be returned.\n\nNote, this method only returns direct children.
    To return children at all \nlevels, use [Get descendants by type](#api-content-id-descendant-type-get).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: 'View' permission for the space, \nand permission to view the content
    if it is a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildtype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidchildtype-get-openapi.md
- name: The Confluence Cloud REST API - Get content descendants
  x-api-slug: contentiddescendant-get
  description: "Returns a map of the descendants of a piece of content. This is similar
    \nto [Get content children](#api-content-id-child-get), except that this \nmethod
    returns child pages at all levels, rather than just the direct \nchild pages.\n\nA
    piece of content has different types of descendants, depending on its type:\n\n-
    `page`: descendant is `page`, `comment`, `attachment`\n- `blogpost`: descendant
    is `comment`, `attachment`\n- `attachment`: descendant is `comment`\n- `comment`:
    descendant is `attachment`\n\nThe map will always include all descendant types
    that are valid for the content. \nHowever, if the content has no instances of
    a descendant type, the map will \ncontain an empty array for that descendant type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'View' permission for the space, and permission to view the content
    if it \nis a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentiddescendant-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentiddescendant-get-openapi.md
- name: The Confluence Cloud REST API - Get content descendants by type
  x-api-slug: contentiddescendanttype-get
  description: "Returns all descendants of a given type, for a piece of content. This
    is \nsimilar to [Get content children by type](#api-content-id-child-type-get),
    \nexcept that this method returns child pages at all levels, rather than just
    \nthe direct child pages.\n\nA piece of content has different types of descendants,
    depending on its type:\n\n- `page`: descendant is `page`, `comment`, `attachment`\n-
    `blogpost`: descendant is `comment`, `attachment`\n- `attachment`: descendant
    is `comment`\n- `comment`: descendant is `attachment`\n\nCustom content types
    that are provided by apps can also be returned.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'View' permission for the space, and permission to view the content
    if it \nis a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentiddescendanttype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentiddescendanttype-get-openapi.md
- name: The Confluence Cloud REST API - Get history for content
  x-api-slug: contentidhistory-get
  description: |-
    Returns the most recent update for a piece of content.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: Permission to view the content.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidhistory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidhistory-get-openapi.md
- name: The Confluence Cloud REST API - Get macro body by macro ID
  x-api-slug: contentidhistoryversionmacroidmacroid-get
  description: "Returns the body of a macro in storage format, for the given macro
    ID. \nThis includes information like the name of the macro, the body of the macro,
    \nand any macro parameters. This method is mainly used by Cloud apps.\n\nAbout
    the macro ID: When a macro is created in a new version of content, \nConfluence
    will generate a random ID for it, unless an ID is specified \n(by an app). The
    macro ID will look similar to this: '50884bd9-0cb8-41d5-98be-f80943c14f96'. \nThe
    ID is then persisted as new versions of content are created, and is \nonly modified
    by Confluence if there are conflicting IDs.\n\nNote, to preserve backwards compatibility
    this resource will also match on \nthe hash of the macro body, even if a macro
    ID is found. This check will \neventually become redundant, as macro IDs are generated
    for pages and \ntransparently propagate out to all instances.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content that the macro is in."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidhistoryversionmacroidmacroid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidhistoryversionmacroidmacroid-get-openapi.md
- name: The Confluence Cloud REST API - Get labels for content
  x-api-slug: contentidlabel-get
  description: "Returns the labels on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'View' permission for the space and permission to view the content
    if it is a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabel-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabel-get-openapi.md
- name: The Confluence Cloud REST API - Add labels to content
  x-api-slug: contentidlabel-post
  description: "Adds labels to a piece of content. Does not modify the existing labels.\n\nNotes:\n\n-
    Labels can also be added when creating content ([Create content](#api-content-post)).\n-
    Labels can be updated when updating content ([Update content](#api-content-id-put)).
    \nThis will delete the existing labels and replace them with the labels in \nthe
    request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabel-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabel-post-openapi.md
- name: The Confluence Cloud REST API - Remove label from content using query parameter
  x-api-slug: contentidlabel-delete
  description: "Removes a label from a piece of content. This is similar to \n[Remove
    label from content](#api-content-id-label-label-delete) \nexcept that the label
    name is specified via a query parameter. \n\nUse this method if the label name
    has \"/\" characters, as \n[Remove label from content using query parameter](#api-content-id-label-delete)
    \ndoes not accept \"/\" characters for the label name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabel-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabel-delete-openapi.md
- name: The Confluence Cloud REST API - Remove label from content
  x-api-slug: contentidlabellabel-delete
  description: "Removes a label from a piece of content. This is similar to \n[Remove
    label from content using query parameter](#api-content-id-label-delete) \nexcept
    that the label name is specified via a path parameter. \n\nUse this method if
    the label name does not have \"/\" characters, as the path \nparameter does not
    accept \"/\" characters for security reasons. Otherwise, \nuse [Remove label from
    content using query parameter](#api-content-id-label-delete).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabellabel-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidlabellabel-delete-openapi.md
- name: The Confluence Cloud REST API - Get watches for page
  x-api-slug: contentidnotificationchildcreated-get
  description: "Returns the watches for a page. A user that watches a page will receive
    \nreceive notifications when the page is updated.\n\nIf you want to manage watches
    for a page, use the following `user` methods:\n\n- [Get content watch status for
    user](#api-user-watch-content-contentId-get)\n- [Add content watch](#api-user-watch-content-contentId-post)\n-
    [Remove content watch](#api-user-watch-content-contentId-delete)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidnotificationchildcreated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidnotificationchildcreated-get-openapi.md
- name: The Confluence Cloud REST API - Get watches for space
  x-api-slug: contentidnotificationcreated-get
  description: "Returns all space watches for the space that the content is in. A
    user that \nwatches a space will receive receive notifications when any content
    in the \nspace is updated.\n\nIf you want to manage watches for a space, use the
    following `user` methods:\n\n- [Get space watch status for user](#api-user-watch-space-spaceKey-get)\n-
    [Add space watch](#api-user-watch-space-spaceKey-post)\n- [Remove space watch](#api-user-watch-space-spaceKey-delete)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidnotificationcreated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidnotificationcreated-get-openapi.md
- name: The Confluence Cloud REST API - Copy page hierarchy
  x-api-slug: contentidpagehierarchycopy-post
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpagehierarchycopy-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpagehierarchycopy-post-openapi.md
- name: The Confluence Cloud REST API - Get content properties
  x-api-slug: contentidproperty-get
  description: "Returns the properties for a piece of content. For more information
    \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'View' permission for the space, and permission to view the content
    if it is a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidproperty-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidproperty-get-openapi.md
- name: The Confluence Cloud REST API - Create content property
  x-api-slug: contentidproperty-post
  description: "Creates a property for an existing piece of content. For more information
    \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis
    is the same as [Create content property for key](#api-content-id-property-key-post)
    \nexcept that the key is specified in the request body instead of as a \npath
    parameter.\n\nContent properties can also be added when creating a new piece of
    content \nby including them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidproperty-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidproperty-post-openapi.md
- name: The Confluence Cloud REST API - Get content property
  x-api-slug: contentidpropertykey-get
  description: "Returns a content property for a piece of content. For more information,
    see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'View' permission for the space, and permission to view the content
    if it is a page."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-get-openapi.md
- name: The Confluence Cloud REST API - Create content property for key
  x-api-slug: contentidpropertykey-post
  description: "Creates a property for an existing piece of content. For more information
    \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis
    is the same as [Create content property](#api-content-id-property-post) \nexcept
    that the key is specified as a path parameter instead of in the \nrequest body.\n\nContent
    properties can also be added when creating a new piece of content \nby including
    them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-post-openapi.md
- name: The Confluence Cloud REST API - Update content property
  x-api-slug: contentidpropertykey-put
  description: "Updates an existing content property. This method will also create
    a new \nproperty for a piece of content, if the property key does not exist and
    \nthe property version is 1. For more information about content properties, see
    \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-put-openapi.md
- name: The Confluence Cloud REST API - Delete content property
  x-api-slug: contentidpropertykey-delete
  description: "Deletes a content property. For more information about content properties,
    see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidpropertykey-delete-openapi.md
- name: The Confluence Cloud REST API - Get restrictions
  x-api-slug: contentidrestriction-get
  description: "Returns the restrictions on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-get-openapi.md
- name: The Confluence Cloud REST API - Add restrictions
  x-api-slug: contentidrestriction-post
  description: "Adds restrictions to a piece of content. Note, this does not change
    any \nexisting restrictions on the content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-post-openapi.md
- name: The Confluence Cloud REST API - Update restrictions
  x-api-slug: contentidrestriction-put
  description: "Updates restrictions for a piece of content. This removes the existing
    \nrestrictions and replaces them with the restrictions in the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-put-openapi.md
- name: The Confluence Cloud REST API - Delete restrictions
  x-api-slug: contentidrestriction-delete
  description: "Removes all restrictions (read and update) on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestriction-delete-openapi.md
- name: The Confluence Cloud REST API - Get restrictions by operation
  x-api-slug: contentidrestrictionbyoperation-get
  description: "Returns restrictions on a piece of content by operation. This method
    is \nsimilar to [Get restrictions](#api-content-id-restriction-get) except that
    \nthe operations are properties of the return object, rather than items in \na
    results array. \n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperation-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperation-get-openapi.md
- name: The Confluence Cloud REST API - Get restrictions for operation
  x-api-slug: contentidrestrictionbyoperationoperationkey-get
  description: "Returns the restictions on a piece of content for a given operation
    (read \nor update).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkey-get-openapi.md
- name: The Confluence Cloud REST API - Get content restriction status for group
  x-api-slug: contentidrestrictionbyoperationoperationkeygroupgroupname-get
  description: "Returns whether the specified content restriction applies to a group.
    \nFor example, if the 'admins' group has permission to read a page with an \nID
    of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/group/admins`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeygroupgroupname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeygroupgroupname-get-openapi.md
- name: The Confluence Cloud REST API - Add group to content restriction
  x-api-slug: contentidrestrictionbyoperationoperationkeygroupgroupname-put
  description: "Adds a group to a content restriction. That is, grant read or update
    \npermission to the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeygroupgroupname-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeygroupgroupname-put-openapi.md
- name: The Confluence Cloud REST API - Remove group from content restriction
  x-api-slug: contentidrestrictionbyoperationoperationkeygroupgroupname-delete
  description: "Removes a group from a content restriction. That is, remove read or
    update \npermission for the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeygroupgroupname-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeygroupgroupname-delete-openapi.md
- name: The Confluence Cloud REST API - Get content restriction status for user
  x-api-slug: contentidrestrictionbyoperationoperationkeyuser-get
  description: "Returns whether the specified content restriction applies to a user.
    \nFor example, if the user 'admin' has permission to read a page with an \nID
    of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/user?username=admin`\n\nOne
    of `key`, `username`, or `accountId` must be specified as a query \nparameter
    to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeyuser-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeyuser-get-openapi.md
- name: The Confluence Cloud REST API - Add user to content restriction
  x-api-slug: contentidrestrictionbyoperationoperationkeyuser-put
  description: "Adds a user to a content restriction. That is, grant read or update
    \npermission to the user for a piece of content.\n\nOne of `key`, `username`,
    or `accountId` must be specified as a query \nparameter to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeyuser-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeyuser-put-openapi.md
- name: The Confluence Cloud REST API - Remove user from content restriction
  x-api-slug: contentidrestrictionbyoperationoperationkeyuser-delete
  description: "Removes a group from a content restriction. That is, remove read or
    update \npermission for the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to edit the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeyuser-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidrestrictionbyoperationoperationkeyuser-delete-openapi.md
- name: The Confluence Cloud REST API - Get content versions
  x-api-slug: contentidversion-get
  description: "Returns the versions for a piece of content in descending order.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content. If the content is a blog post, 'View'
    permission \nfor the space is required."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversion-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversion-get-openapi.md
- name: The Confluence Cloud REST API - Restore content version
  x-api-slug: contentidversion-post
  description: "Restores a historical version to be the latest version. That is, a
    new version \nis created with the content of the historical version.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversion-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversion-post-openapi.md
- name: The Confluence Cloud REST API - Get content version
  x-api-slug: contentidversionversionnumber-get
  description: "Returns a version for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the content. If the content is a blog post, 'View'
    permission \nfor the space is required."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversionversionnumber-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversionversionnumber-get-openapi.md
- name: The Confluence Cloud REST API - Delete content version
  x-api-slug: contentidversionversionnumber-delete
  description: "Delete a historical version. This does not delete the changes made
    to the \ncontent in that version, rather the changes for the deleted version are
    \nrolled up into the next version. Note, you cannot delete the current version.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to update the content."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversionversionnumber-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentidversionversionnumber-delete-openapi.md
- name: The Confluence Cloud REST API - Convert content body
  x-api-slug: contentbodyconvertto-post
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentbodyconvertto-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/contentbodyconvertto-post-openapi.md
- name: The Confluence Cloud REST API - Get groups
  x-api-slug: group-get
  description: |-
    Returns all user groups. The returned groups are ordered alphabetically in
    ascending order by group name.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    Permission to access the Confluence site ('Can use' global permission).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/group-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/group-get-openapi.md
- name: The Confluence Cloud REST API - Get group
  x-api-slug: groupgroupname-get
  description: |-
    Returns a user group for a given group name.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    Permission to access the Confluence site ('Can use' global permission).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/groupgroupname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/groupgroupname-get-openapi.md
- name: The Confluence Cloud REST API - Get group members
  x-api-slug: groupgroupnamemember-get
  description: |-
    Returns the users that are members of a group.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    Permission to access the Confluence site ('Can use' global permission).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/groupgroupnamemember-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/groupgroupnamemember-get-openapi.md
- name: The Confluence Cloud REST API - Get long-running tasks
  x-api-slug: longtask-get
  description: "Returns information about all active long-running tasks (e.g. space
    export), \nsuch as how long each task has been running and the percentage of each
    task \nthat has completed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/longtask-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/longtask-get-openapi.md
- name: The Confluence Cloud REST API - Get long-running task
  x-api-slug: longtaskid-get
  description: "Returns information about an active long-running task (e.g. space
    export), \nsuch as how long it has been running and the percentage of the task
    that \nhas completed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/longtaskid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/longtaskid-get-openapi.md
- name: The Confluence Cloud REST API - Find target entities related to a source entity
  x-api-slug: relationrelationnamefromsourcetypesourcekeytotargettype-get
  description: "Returns all target entities that have a particular relationship to
    the \nsource entity. Note, relationships are one way.\n\nFor example, the following
    method finds all content that the current user \nhas an 'ignore' relationship
    with:\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/ignore/from/user/current/to/content`\nNote,
    'ignore' is an example custom relationship type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view both the target entity and source entity."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettype-get-openapi.md
- name: The Confluence Cloud REST API - Find relationship from source to target
  x-api-slug: relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-get
  description: "Find whether a particular type of relationship exists from a source
    \nentity to a target entity. Note, relationships are one way.\n\nFor example,
    you can use this method to find whether the current user has \nselected a particular
    page as a favorite (i.e. 'save for later'):\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/favourite/from/user/current/to/content/123`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view both the target entity and source entity."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-get-openapi.md
- name: The Confluence Cloud REST API - Create relationship
  x-api-slug: relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-put
  description: "Creates a relationship between two entities (user, space, content).
    The \n'favourite' relationship is supported by default, but you can use this method
    \nto create any type of relationship between two entities.\n\nFor example, the
    following method creates a 'sibling' relationship between \ntwo pieces of content:\n`GET
    https://your-domain.atlassian.net/wiki/rest/api/relation/sibling/from/content/123/to/content/456`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-put-openapi.md
- name: The Confluence Cloud REST API - Delete
  x-api-slug: relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-delete
  description: "Deletes a relationship between two entities (user, space, content).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission).
    \nFor favourite relationships, the current user can only delete their own \nfavourite
    relationships. A space administrator can delete favourite \nrelationships for
    any user."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnamefromsourcetypesourcekeytotargettypetargetkey-delete-openapi.md
- name: The Confluence Cloud REST API - Find target entities related to a source entity
  x-api-slug: relationrelationnametotargettypetargetkeyfromsourcetype-get
  description: "Returns all target entities that have a particular relationship to
    the \nsource entity. Note, relationships are one way.\n\nFor example, the following
    method finds all users that have a 'collaborator' \nrelationship to a piece of
    content with an ID of '1234':\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/collaborator/to/content/1234/from/user`\nNote,
    'collaborator' is an example custom relationship type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view both the target entity and source entity."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnametotargettypetargetkeyfromsourcetype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/relationrelationnametotargettypetargetkeyfromsourcetype-get-openapi.md
- name: The Confluence Cloud REST API - Search
  x-api-slug: search-get
  description: "Searches for content using the \n[Confluence Query Language (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to view the entities. Note, only entities that the user
    has \npermission to view will be returned."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/search-get-openapi.md
- name: The Confluence Cloud REST API - Get look and feel settings
  x-api-slug: settingslookandfeel-get
  description: "Returns the look and feel settings for the site or a single space.
    This \nincludes attributes such as the color scheme, padding, and border radius.\n\nThe
    look and feel settings for a space can be inherited from the global \nlook and
    feel settings or provided by a theme.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nNone"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeel-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeel-get-openapi.md
- name: The Confluence Cloud REST API - Update look and feel settings
  x-api-slug: settingslookandfeelcustom-post
  description: "Updates the look and feel settings for the site or for a single space.\nIf
    custom settings exist, they are updated. If no custom settings exist, \nthen a
    set of custom settings is created.\n\nNote, if a theme is selected for a space,
    the space look and feel settings \nare provided by the theme and cannot be overridden.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Admin' permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeelcustom-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeelcustom-post-openapi.md
- name: The Confluence Cloud REST API - Reset look and feel settings
  x-api-slug: settingslookandfeelcustom-delete
  description: "Resets the custom look and feel settings for the site or a single
    space.\nThis changes the values of the custom settings to be the same as the \ndefault
    settings. It does not change which settings (default or custom) \nare selected.
    Note, the default space settings are inherited from the \ncurrent global settings.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Admin' permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeelcustom-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeelcustom-delete-openapi.md
- name: The Confluence Cloud REST API - Set look and feel settings
  x-api-slug: settingslookandfeelselected-put
  description: "Sets the look and feel settings to either the default settings or
    the\ncustom settings, for the site or a single space. Note, the default \nspace
    settings are inherited from the current global settings.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Admin' permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeelselected-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingslookandfeelselected-put-openapi.md
- name: The Confluence Cloud REST API - Get system info
  x-api-slug: settingssysteminfo-get
  description: "Returns the system information for the Confluence Cloud tenant. This\ninformation
    is used by Atlassian.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingssysteminfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingssysteminfo-get-openapi.md
- name: The Confluence Cloud REST API - Get themes
  x-api-slug: settingstheme-get
  description: |-
    Returns all themes, not including the default theme.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingstheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingstheme-get-openapi.md
- name: The Confluence Cloud REST API - Get global theme
  x-api-slug: settingsthemeselected-get
  description: |-
    Returns the globally assigned theme.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingsthemeselected-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingsthemeselected-get-openapi.md
- name: The Confluence Cloud REST API - Get theme
  x-api-slug: settingsthemethemekey-get
  description: |-
    Returns a theme. This includes information about the theme name,
    description, and icon.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingsthemethemekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/settingsthemethemekey-get-openapi.md
- name: The Confluence Cloud REST API - Get spaces
  x-api-slug: space-get
  description: |-
    Returns all spaces. The returned spaces are ordered alphabetically in
    ascending order by space key.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    Permission to access the Confluence site ('Can use' global permission).
    Note, the returned list will only contain spaces that the current user
    has permission to view.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/space-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/space-get-openapi.md
- name: The Confluence Cloud REST API - Create space
  x-api-slug: space-post
  description: |-
    Creates a new space. Note, currently you cannot set space labels when
    creating a space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Create Space(s)' global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/space-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/space-post-openapi.md
- name: The Confluence Cloud REST API - Create private space
  x-api-slug: space-private-post
  description: |-
    Creates a new space that is only visible to the creator. This method is
    the same as the [Create space](#api-space-post) method with permissions
    set to the current user only. Note, currently you cannot set space
    labels when creating a space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Create Space(s)' global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/space-private-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/space-private-post-openapi.md
- name: The Confluence Cloud REST API - Get space
  x-api-slug: spacespacekey-get
  description: |-
    Returns a space. This includes information like the name, description,
    and permissions, but not the content in the space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'View' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekey-get-openapi.md
- name: The Confluence Cloud REST API - Update space
  x-api-slug: spacespacekey-put
  description: |-
    Updates the name, description, or homepage of a space.

    -   For security reasons, permissions cannot be updated via the API and
    must be changed via the user interface instead.
    -   Currently you cannot set space labels when updating a space.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Admin' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekey-put-openapi.md
- name: The Confluence Cloud REST API - Delete space
  x-api-slug: spacespacekey-delete
  description: |-
    Deletes a space. Note, the space will be deleted in a long running task.
    Therefore, the space may not be deleted yet when this method has
    returned. Clients should poll the status link that is returned in the
    response until the task completes.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Admin' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekey-delete-openapi.md
- name: The Confluence Cloud REST API - Get content for space
  x-api-slug: spacespacekeycontent-get
  description: |-
    Returns all content in a space. The returned content is grouped by type
    (pages then blogposts), then ordered by content ID in ascending order.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'View' permission for the space. Note, the returned list will only
    contain content that the current user has permission to view.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeycontent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeycontent-get-openapi.md
- name: The Confluence Cloud REST API - Get content by type for space
  x-api-slug: spacespacekeycontenttype-get
  description: |-
    Returns all content of a given type, in a space. The returned content is
    ordered by content ID in ascending order.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'View' permission for the space. Note, the returned list will only
    contain content that the current user has permission to view.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeycontenttype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeycontenttype-get-openapi.md
- name: The Confluence Cloud REST API - Get space properties
  x-api-slug: spacespacekeyproperty-get
  description: "Returns all properties for the given space. Space properties are a
    key-value storage associated with a space.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
    \u2018View\u2019 permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeyproperty-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeyproperty-get-openapi.md
- name: The Confluence Cloud REST API - Create space property
  x-api-slug: spacespacekeyproperty-post
  description: "Creates a new space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeyproperty-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeyproperty-post-openapi.md
- name: The Confluence Cloud REST API - Get space property
  x-api-slug: spacespacekeypropertykey-get
  description: "Returns a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
    \u2018View\u2019 permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-get-openapi.md
- name: The Confluence Cloud REST API - Create space property for key
  x-api-slug: spacespacekeypropertykey-post
  description: "Creates a new space property. This is the same as `POST\n/space/{spaceKey}/property`
    but the key for the property is passed as a\npath parameter, rather than in the
    request body.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-post-openapi.md
- name: The Confluence Cloud REST API - Update space property
  x-api-slug: spacespacekeypropertykey-put
  description: "Updates a space property. Note, you cannot update the key of a space\nproperty,
    only the value.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-put-openapi.md
- name: The Confluence Cloud REST API - Delete space property
  x-api-slug: spacespacekeypropertykey-delete
  description: "Deletes a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n\u2018Admin\u2019
    permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeypropertykey-delete-openapi.md
- name: The Confluence Cloud REST API - Get space settings
  x-api-slug: spacespacekeysettings-get
  description: |-
    Returns the settings of a space. Currently only the
    `routeOverrideEnabled` setting can be returned.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'View' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeysettings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeysettings-get-openapi.md
- name: The Confluence Cloud REST API - Update space settings
  x-api-slug: spacespacekeysettings-put
  description: |-
    Updates the settings for a space. Currently only the
    `routeOverrideEnabled` setting can be updated.

    **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    'Admin' permission for the space.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeysettings-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeysettings-put-openapi.md
- name: The Confluence Cloud REST API - Get space theme
  x-api-slug: spacespacekeytheme-get
  description: "Returns the theme selected for a space, if one is set. If no space
    \ntheme is set, this means that the space is inheriting the global look \nand
    feel settings.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:
    \u2018View\u2019 permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeytheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeytheme-get-openapi.md
- name: The Confluence Cloud REST API - Set space theme
  x-api-slug: spacespacekeytheme-put
  description: "Sets the theme for a space. Note, if you want to reset the space theme
    to \nthe default Confluence theme, use the 'Reset space theme' method instead
    \nof this method.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\n'Admin' permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeytheme-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeytheme-put-openapi.md
- name: The Confluence Cloud REST API - Reset space theme
  x-api-slug: spacespacekeytheme-delete
  description: "Resets the space theme. This means that the space will inherit the
    \nglobal look and feel settings\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**:\n'Admin' permission for the space."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeytheme-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/spacespacekeytheme-delete-openapi.md
- name: The Confluence Cloud REST API - Create content template
  x-api-slug: template-post
  description: "Creates a new content template. Note, blueprint templates cannot be
    created via the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Admin' permission for the space to create a space template or 'Confluence
    Administrator' \nglobal permission to create a global template."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/template-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/template-post-openapi.md
- name: The Confluence Cloud REST API - Update content template
  x-api-slug: template-put
  description: "Updates a content template. Note, blueprint templates cannot be updated\nvia
    the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
    \n'Admin' permission for the space to create a space template or 'Confluence Administrator'
    \nglobal permission to create a global template."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/template-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/template-put-openapi.md
- name: The Confluence Cloud REST API - Get blueprint templates
  x-api-slug: templateblueprint-get
  description: "Returns all templates provided by blueprints. Use this method to retrieve
    \nall global blueprint templates or all blueprint templates in a space.\n\nNote,
    all global blueprints are inherited by each space. Space blueprints \ncan be customised
    without affecting the global blueprints.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templateblueprint-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templateblueprint-get-openapi.md
- name: The Confluence Cloud REST API - Get content templates
  x-api-slug: templatepage-get
  description: "Returns all content templates. Use this method to retrieve all global\ncontent
    templates or all content templates in a space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Admin' permission for the space to view space templates and 'Confluence
    \nAdministrator' global permission to view global templates."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templatepage-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templatepage-get-openapi.md
- name: The Confluence Cloud REST API - Get content template
  x-api-slug: templatecontenttemplateid-get
  description: "Returns a content template. This includes information about template,
    \nlike the name, the space or blueprint that the template is in, the body \nof
    the template, and more.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Admin' permission for the space to view space templates and 'Confluence
    \nAdministrator' global permission to view global templates."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templatecontenttemplateid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templatecontenttemplateid-get-openapi.md
- name: The Confluence Cloud REST API - Remove template
  x-api-slug: templatecontenttemplateid-delete
  description: "Deletes a template. This results in different actions depending on
    the \ntype of template:\n\n- If the template is a content template, it is deleted.\n-
    If the template is a modified space-level blueprint template, it reverts \nto
    the template inherited from the global-level blueprint template.\n- If the template
    is a modified global-level blueprint template, it reverts \nto the default global-level
    blueprint template.\n\n Note, unmodified blueprint templates cannot be deleted."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templatecontenttemplateid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/templatecontenttemplateid-delete-openapi.md
- name: The Confluence Cloud REST API - Get user
  x-api-slug: user-get
  description: "Returns a user. This includes information about the user, like the\ndisplay
    name, userKey, account ID, profile picture, and more.\n\nThe `username`, `key`,
    or `accountId` parameter must be specified, in \norder to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/user-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/user-get-openapi.md
- name: The Confluence Cloud REST API - Get anonymous user
  x-api-slug: useranonymous-get
  description: "Returns information about how anonymous users are represented, like
    the\nprofile picture and display name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/useranonymous-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/useranonymous-get-openapi.md
- name: The Confluence Cloud REST API - Get current user
  x-api-slug: usercurrent-get
  description: "Returns the currently logged-in user. This includes information about\nthe
    user, like the display name, userKey, account ID, profile picture,\nand more.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/usercurrent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/usercurrent-get-openapi.md
- name: The Confluence Cloud REST API - Get group memberships for user
  x-api-slug: usermemberof-get
  description: "Returns the groups that a user is a member of.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \nPermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/usermemberof-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/usermemberof-get-openapi.md
- name: The Confluence Cloud REST API - Get content watch status
  x-api-slug: userwatchcontentcontentid-get
  description: "Returns whether a user is watching a piece of content. Choose the
    user by \ndoing one of the following:\n\n- Specify a user via a query parameter:
    Use the `username`, `key`, or `accountId` \nto identify the user. The user making
    the request must be a Confluence administrator.\n- Do not specify a user: The
    currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchcontentcontentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchcontentcontentid-get-openapi.md
- name: The Confluence Cloud REST API - Add content watcher
  x-api-slug: userwatchcontentcontentid-post
  description: "Adds a user as a watcher to a piece of content. Choose the user by
    doing \none of the following:\n\n- Specify a user via a query parameter: Use the
    `username`, `key`, or `accountId` \nto identify the user. The user making the
    request must be a Confluence administrator.\n- Do not specify a user: The currently
    logged-in user will be used.\n\nNote, you must add the `X-Atlassian-Token: no-check`
    header when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchcontentcontentid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchcontentcontentid-post-openapi.md
- name: The Confluence Cloud REST API - Remove content watcher
  x-api-slug: userwatchcontentcontentid-delete
  description: "Removes a user as a watcher from a piece of content. Choose the user
    by \ndoing one of the following:\n\n- Specify a user via a query parameter: Use
    the `username`, `key`, or `accountId` \nto identify the user. The user making
    the request must be a Confluence administrator.\n- Do not specify a user: The
    currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchcontentcontentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchcontentcontentid-delete-openapi.md
- name: The Confluence Cloud REST API - Get label watch status
  x-api-slug: userwatchlabellabelname-get
  description: "Returns whether a user is watching a label. Choose the user by doing
    one \nof the following:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchlabellabelname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchlabellabelname-get-openapi.md
- name: The Confluence Cloud REST API - Add label watcher
  x-api-slug: userwatchlabellabelname-post
  description: "Adds a user as a watcher to a label. Choose the user by doing one
    of the \nfollowing:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\nNote, you must add the `X-Atlassian-Token: no-check` header
    when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchlabellabelname-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchlabellabelname-post-openapi.md
- name: The Confluence Cloud REST API - Remove label watcher
  x-api-slug: userwatchlabellabelname-delete
  description: "Removes a user as a watcher from a label. Choose the user by doing
    one of \nthe following:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchlabellabelname-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchlabellabelname-delete-openapi.md
- name: The Confluence Cloud REST API - Get space watch status
  x-api-slug: userwatchspacespacekey-get
  description: "Returns whether a user is watching a space. Choose the user by \ndoing
    one of the following:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchspacespacekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchspacespacekey-get-openapi.md
- name: The Confluence Cloud REST API - Add space watcher
  x-api-slug: userwatchspacespacekey-post
  description: "Adds a user as a watcher to a space. Choose the user by doing one
    of the \nfollowing:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\nNote, you must add the `X-Atlassian-Token: no-check` header
    when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchspacespacekey-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchspacespacekey-post-openapi.md
- name: The Confluence Cloud REST API - Remove space watch
  x-api-slug: userwatchspacespacekey-delete
  description: "Removes a user as a watcher from a space. Choose the user by doing
    one of \nthe following:\n\n- Specify a user via a query parameter: Use the `username`,
    `key`, or `accountId` \nto identify the user. The user making the request must
    be a Confluence administrator.\n- Do not specify a user: The currently logged-in
    user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission if specifying a user,
    otherwise \npermission to access the Confluence site ('Can use' global permission)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchspacespacekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/userwatchspacespacekey-delete-openapi.md
- name: Jira Cloud REST API - Get application property
  x-api-slug: api2applicationproperties-get
  description: Returns an application property.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationproperties-get-openapi.md
- name: Jira Cloud REST API - Get advanced settings
  x-api-slug: api2applicationpropertiesadvancedsettings-get
  description: Returns the properties that are displayed on the General Configuration
    Advanced Settings page.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationpropertiesadvancedsettings-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationpropertiesadvancedsettings-get-openapi.md
- name: Jira Cloud REST API - Set application property
  x-api-slug: api2applicationpropertiesid-put
  description: Modify an application property via PUT. The "value" field present in
    the PUT will override the existing value.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationpropertiesid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationpropertiesid-put-openapi.md
- name: Jira Cloud REST API - Get all application roles
  x-api-slug: api2applicationrole-get
  description: Returns all ApplicationRoles in the system. Will also return an ETag
    header containing a version hash of the collection of ApplicationRoles.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationrole-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationrole-get-openapi.md
- name: Jira Cloud REST API - Get application role
  x-api-slug: api2applicationrolekey-get
  description: Returns the ApplicationRole with passed key if it exists.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationrolekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2applicationrolekey-get-openapi.md
- name: Jira Cloud REST API - Get global attachment settings
  x-api-slug: api2attachmentmeta-get
  description: "Returns the global attachment settings, that is, whether attachments
    are enabled and the maximum attachment size allowed.  \n  \nNote that there are
    also [project permissions](https://confluence.atlassian.com/x/yodKLg) that restrict
    whether users can create and delete attachments or not.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentmeta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentmeta-get-openapi.md
- name: Jira Cloud REST API - Get attachment metadata
  x-api-slug: api2attachmentid-get
  description: "Returns the metadata for an attachment. Note that the attachment itself
    is not returned.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentid-get-openapi.md
- name: Jira Cloud REST API - Delete attachment
  x-api-slug: api2attachmentid-delete
  description: "Deletes an attachment from an issue.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Any of the following permissions in the project that the issue is
    in:\n\n*   _Delete own attachments_ [project permission](https://confluence.atlassian.com/x/yodKLg)
    to delete an attachment created by the calling user.\n*   _Delete all attachments_
    [project permission](https://confluence.atlassian.com/x/yodKLg) to delete an attachment
    created by any user."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentid-delete-openapi.md
- name: Jira Cloud REST API - Get all metadata for an expanded attachment
  x-api-slug: api2attachmentidexpandhuman-get
  description: "Returns the metadata for the contents of an attachment, if it is an
    archive, and metadata for the attachment itself. For example, if the attachment
    is a ZIP archive, then information about the files in the archive is returned
    and metadata for the ZIP archive. Currently, only the ZIP archive format is supported.
    \ \n  \nUse this method to retrieve data that is presented in the UI, as this
    method returns the metadata for the attachment itself, such as the attachment's
    ID and name. Otherwise, use [Get contents metadata for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-raw-get),
    which only returns the metadata for the attachment's contents.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentidexpandhuman-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentidexpandhuman-get-openapi.md
- name: Jira Cloud REST API - Get contents metadata for an expanded attachment
  x-api-slug: api2attachmentidexpandraw-get
  description: "Returns the metadata for the contents of an attachment, if it is an
    archive. For example, if the attachment is a ZIP archive, then information about
    the files in the archive is returned. Currently, only the ZIP archive format is
    supported.  \n  \nUse this method if you are processing the data without presenting
    it in the UI, as this method only returns the metadata for the contents of the
    attachment. Otherwise, to retrieve data to present in the UI, use [Get all metadata
    for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-human-get)
    which also returns the metadata for the attachment itself, such as the attachment's
    ID and name.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the issue
    that the attachment belongs to."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentidexpandraw-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2attachmentidexpandraw-get-openapi.md
- name: Jira Cloud REST API - Get audit records
  x-api-slug: api2auditingrecord-get
  description: Returns auditing records filtered using provided parameters
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2auditingrecord-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2auditingrecord-get-openapi.md
- name: Jira Cloud REST API - Get all system avatars
  x-api-slug: api2avatartypesystem-get
  description: Returns all system avatars of the given type.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2avatartypesystem-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2avatartypesystem-get-openapi.md
- name: Jira Cloud REST API - Get comments by ids
  x-api-slug: api2commentlist-post
  description: Returns comments for given comments ids. Only comments to which the
    user has permissions, will be included in the result. The returned set of comments
    is limited to 1000 elements.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentlist-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentlist-post-openapi.md
- name: Jira Cloud REST API - Get comment property keys
  x-api-slug: api2commentcommentidproperties-get
  description: Returns the keys of all properties for the comment identified by the
    key or by the id.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidproperties-get-openapi.md
- name: Jira Cloud REST API - Get comment property
  x-api-slug: api2commentcommentidpropertiespropertykey-get
  description: Returns the value of the property with a given key from the comment
    identified by the key or by the id. The user who retrieves the property is required
    to have permissions to read the comment.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set comment property
  x-api-slug: api2commentcommentidpropertiespropertykey-put
  description: |-
    Sets the value of the specified comment's property.

    You can use this resource to store a custom data against the comment identified by the key or by the id. The user who stores the data is required to have permissions to administer the comment.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete comment property
  x-api-slug: api2commentcommentidpropertiespropertykey-delete
  description: Removes the property from the comment identified by the key or by the
    id. Ths user removing the property is required to have permissions to administer
    the comment.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2commentcommentidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Create component
  x-api-slug: api2component-post
  description: |-
    Creates a component. Use components to provide containers for issues within a project. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2component-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2component-post-openapi.md
- name: Jira Cloud REST API - Get component
  x-api-slug: api2componentid-get
  description: 'Returns a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required: _Browse projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentid-get-openapi.md
- name: Jira Cloud REST API - Update component
  x-api-slug: api2componentid-put
  description: |-
    Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string ("") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentid-put-openapi.md
- name: Jira Cloud REST API - Delete component
  x-api-slug: api2componentid-delete
  description: |-
    Deletes a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentid-delete-openapi.md
- name: Jira Cloud REST API - Get component issues count
  x-api-slug: api2componentidrelatedissuecounts-get
  description: Returns the counts of issues assigned to the component. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentidrelatedissuecounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2componentidrelatedissuecounts-get-openapi.md
- name: Jira Cloud REST API - Get global settings
  x-api-slug: api2configuration-get
  description: "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM)
    in Jira. These settings determine whether optional features (for example, sub-tasks,
    time tracking, and others) are enabled. If time tracking is enabled, this method
    also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configuration-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configuration-get-openapi.md
- name: Jira Cloud REST API - Get selected time tracking provider
  x-api-slug: api2configurationtimetracking-get
  description: "Returns the time tracking provider that is currently selected. Note
    that if time tracking is disabled, then a successful but empty response is returned.
    \ \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetracking-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetracking-get-openapi.md
- name: Jira Cloud REST API - Select time tracking provider
  x-api-slug: api2configurationtimetracking-put
  description: "Selects a time tracking provider.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetracking-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetracking-put-openapi.md
- name: Jira Cloud REST API - Disable time tracking
  x-api-slug: api2configurationtimetracking-delete
  description: "Disables time tracking.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetracking-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetracking-delete-openapi.md
- name: Jira Cloud REST API - Get all time tracking providers
  x-api-slug: api2configurationtimetrackinglist-get
  description: "Returns all time tracking providers. By default, Jira only has one
    time tracking provider: _JIRA provided time tracking_. However, you can install
    other time tracking providers via apps from the Atlassian Marketplace. For more
    information on time tracking providers, see the documentation for the [Time Tracking
    Provider](https://developer.atlassian.com/cloud/jira/platform/modules/time-tracking-provider/)
    module.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetrackinglist-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetrackinglist-get-openapi.md
- name: Jira Cloud REST API - Get time tracking settings
  x-api-slug: api2configurationtimetrackingoptions-get
  description: "Returns the time tracking settings. This includes settings such as
    the time format, default time unit, and others. For more information, see [Configuring
    time tracking](https://confluence.atlassian.com/x/qoXKM).  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetrackingoptions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetrackingoptions-get-openapi.md
- name: Jira Cloud REST API - Set time tracking settings
  x-api-slug: api2configurationtimetrackingoptions-put
  description: "Sets the time tracking settings.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetrackingoptions-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2configurationtimetrackingoptions-put-openapi.md
- name: Jira Cloud REST API - Get custom field option
  x-api-slug: api2customfieldoptionid-get
  description: "Returns a custom field option. For example, an option in a cascading
    select list.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions)
    required:** None."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2customfieldoptionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2customfieldoptionid-get-openapi.md
- name: Jira Cloud REST API - Get all dashboards
  x-api-slug: api2dashboard-get
  description: "Returns a list of dashboards owned by or shared with the user. The
    list may be filtered to include only favorite or owned dashboards.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboard-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboard-get-openapi.md
- name: Jira Cloud REST API - Get dashboard item property keys
  x-api-slug: api2dashboarddashboardiditemsitemidproperties-get
  description: "Returns the keys of all properties for a dashboard item.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to get the property keys the user
    must be the owner of the dashboard or be shared the dashboard. Note, users with
    the _Administer Jira_ [global permission](href=) are considered owners of the
    System dashboard. The System dashboard is considered to be shared with all other
    users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidproperties-get-openapi.md
- name: Jira Cloud REST API - Get dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-get
  description: "Returns the key and value of a dashboard item property.  \n  \nA dashboard
    item enables an app to add user-specific information to a user dashboard. Dashboard
    items are exposed to users as gadgets that users can add to their dashboards.
    For more information on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).
    \ \n  \nWhen an app creates a dashboard item it registers a callback to receive
    the dashboard item ID. The callback fires whenever the item is rendered or, where
    the item is configurable, the user edits the item. The app then uses this resource
    to store the item's content or configuration details. For more information on
    working with dashboard items, see [Building a dashboard item for a JIRA Connect
    add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
    and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
    documentation.  \n  \nThere is no resource to set or get dashboard items.  \n
    \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira. However, to get a dashboard item property the user must be the
    owner of the dashboard or be shared the dashboard. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard.
    The System dashboard is considered to be shared with all other users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-put
  description: "Sets the value of a dashboard item property. Use this resource in
    apps to store custom data against a dashboard item.  \n  \nA dashboard item enables
    an app to add user-specific information to a user dashboard. Dashboard items are
    exposed to users as gadgets that users can add to their dashboards. For more information
    on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).
    \ \n  \nWhen an app creates a dashboard item it registers a callback to receive
    the dashboard item ID. The callback fires whenever the item is rendered or, where
    the item is configurable, the user edits the item. The app then uses this resource
    to store the item's content or configuration details. For more information on
    working with dashboard items, see [Building a dashboard item for a JIRA Connect
    add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/)
    and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/)
    documentation.  \n  \nThere is no resource to set or get dashboard items.  \n
    \ \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira. However, to set a dashboard item property the user must be the
    owner of the dashboard. Note, users with the _Administer Jira_ [global permission](href=)
    are considered owners of the System dashboard.  \n  \nThe value of the request
    body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob.
    The maximum length is 32768 bytes."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete dashboard item property
  x-api-slug: api2dashboarddashboardiditemsitemidpropertiespropertykey-delete
  description: "Deletes a dashboard item property.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to delete a dashboard item property
    the user must be the owner of the dashboard. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboarddashboardiditemsitemidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get dashboard
  x-api-slug: api2dashboardid-get
  description: "Returns a dashboard.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira. However, to get a dashboard, the dashboard
    must be shared with the user or the user must own it. Note, users with the _Administer
    Jira_ [global permission](href=) are considered owners of the System dashboard.
    The System dashboard is considered to be shared with all other users."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboardid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2dashboardid-get-openapi.md
- name: Jira Cloud REST API - Evaluate Jira expression
  x-api-slug: api2expressioneval-post
  description: Evaluates a Jira expression and returns its value. Jira expressions
    is the name of a domain-specific language for Jira that can be used to evaluate
    expressions in the context of Jira entities.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2expressioneval-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2expressioneval-post-openapi.md
- name: Jira Cloud REST API - Get fields
  x-api-slug: api2field-get
  description: |-
    Returns all issue fields in Jira, both system and custom fields.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the following rules apply:

    *   Fields that cannot be added to the issue navigator are always returned.
    *   Fields that cannot be placed on an issue screen are always returned.
    *   Fields that depend on global Jira settings are only returned if the setting is enabled. That is, timetracking fields, subtasks, votes, and watches.
    *   For all other fields, this method only returns the fields that the current user has permission to see (that is, the field can be used in at least one project that the user can see).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2field-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2field-get-openapi.md
- name: Jira Cloud REST API - Create custom field
  x-api-slug: api2field-post
  description: |-
    Creates a custom field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2field-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2field-post-openapi.md
- name: Jira Cloud REST API - Get all issue field options
  x-api-slug: api2fieldfieldkeyoption-get
  description: |-
    Returns all options defined for a select list issue field. A select list issue field is a type of [issue field](https://developer.atlassian.com/cloud/jira/platform/modules/issue-field/) that allows a user to select an value from a list of options.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoption-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoption-get-openapi.md
- name: Jira Cloud REST API - Create issue field option
  x-api-slug: api2fieldfieldkeyoption-post
  description: |-
    Creates an option for a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoption-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoption-post-openapi.md
- name: Jira Cloud REST API - Get selectable issue field options
  x-api-slug: api2fieldfieldkeyoptionsuggestionsedit-get
  description: |-
    Returns options defined for a select list issue field that can be viewed and selected by the currently logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionsedit-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionsedit-get-openapi.md
- name: Jira Cloud REST API - Get visible issue field options
  x-api-slug: api2fieldfieldkeyoptionsuggestionssearch-get
  description: |-
    Returns options defined for a select list issue field that can be viewed by the currently logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionssearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionsuggestionssearch-get-openapi.md
- name: Jira Cloud REST API - Get issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-get
  description: |-
    Returns an option from a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-get-openapi.md
- name: Jira Cloud REST API - Update issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-put
  description: |-
    Updates an option for a select list issue field. If the option does not exist, a new option is created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-put-openapi.md
- name: Jira Cloud REST API - Delete issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionid-delete
  description: |-
    Deletes an option from a select list issue field.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionid-delete-openapi.md
- name: Jira Cloud REST API - Replace issue field option
  x-api-slug: api2fieldfieldkeyoptionoptionidissue-delete
  description: |-
    Deselects a select list issue field option in all issues that it has been selected in. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.

    This is an [asynchronous method](#async). The response object will contain a link to the long-running task. For example, _https://your-domain.atlassian.net/rest/api/2/task/10127_.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionidissue-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2fieldfieldkeyoptionoptionidissue-delete-openapi.md
- name: Jira Cloud REST API - Get filters
  x-api-slug: api2filter-get
  description: |-
    Returns all filters. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned:

    *   Filters owned by the user.
    *   Filters shared with a group that the user is a member of.
    *   Filters shared with a private project that the user can browse.
    *   Filters shared with a public project, even if the user is anonymous.
    *   Filters shared with the public, even if the user is anonymous.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filter-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filter-get-openapi.md
- name: Jira Cloud REST API - Create filter
  x-api-slug: api2filter-post
  description: Creates a new filter. The new filter is not shared and not selected
    as a favorite. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filter-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filter-post-openapi.md
- name: Jira Cloud REST API - Get default share scope
  x-api-slug: api2filterdefaultsharescope-get
  description: Returns the default sharing settings for new filters and dashboards
    for a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterdefaultsharescope-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterdefaultsharescope-get-openapi.md
- name: Jira Cloud REST API - Set default share scope
  x-api-slug: api2filterdefaultsharescope-put
  description: Sets the default sharing for new filters and dashboards for a user.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterdefaultsharescope-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterdefaultsharescope-put-openapi.md
- name: Jira Cloud REST API - Get favourite filters
  x-api-slug: api2filterfavourite-get
  description: Returns the favorite filters of the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterfavourite-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterfavourite-get-openapi.md
- name: Jira Cloud REST API - Get my filters
  x-api-slug: api2filtermy-get
  description: Returns the filters owned by the calling user. If `includeFavourites`
    is `true`, the user's favorite filters are also returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filtermy-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filtermy-get-openapi.md
- name: Jira Cloud REST API - Search for filters
  x-api-slug: api2filtersearch-get
  description: |-
    Search for filters. This method is similar to [Get filters](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-get) except that you can refine the results to include filters that have specific attributes. For example, filters with a particular name. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned (if no search parameters are set):

    *   Filters owned by the user.
    *   Filters shared with a group that the user is a member of.
    *   Filters shared with a private project that the user can browse.
    *   Filters shared with a public project, even if the user is anonymous.
    *   Filters shared with the public, even if the user is anonymous.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filtersearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filtersearch-get-openapi.md
- name: Jira Cloud REST API - Get filter
  x-api-slug: api2filterid-get
  description: Returns a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterid-get-openapi.md
- name: Jira Cloud REST API - Update filter
  x-api-slug: api2filterid-put
  description: |-
    Updates an existing filter. Use this method to update a filter's name, description, JQL, or sharing. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can update:

    *   Private filters (i.e., not shared) can only be updated by the creator of the filter.
    *   Shared filters can only be updated by the creator of the filter or a Jira administrator.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterid-put-openapi.md
- name: Jira Cloud REST API - Delete filter
  x-api-slug: api2filterid-delete
  description: |-
    Delete a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can delete:

    *   Private filters (i.e., not shared) can only be deleted by the creator of the filter.
    *   Shared filters can only be deleted by the creator of the filter or a Jira administrator.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filterid-delete-openapi.md
- name: Jira Cloud REST API - Get columns
  x-api-slug: api2filteridcolumns-get
  description: Returns the columns configured for a filter. The column configuration
    is used when the filter's results are viewed in _List View_ with the _Columns_
    set to _Filter_. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridcolumns-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridcolumns-get-openapi.md
- name: Jira Cloud REST API - Set columns
  x-api-slug: api2filteridcolumns-put
  description: Sets the columns for a filter. Only navigable fields can be set as
    columns. Use [Get fields](https://developer.atlassian.com/cloud/jira/platform/rest#api-api-2-field-get)
    to get the list fields in Jira. A navigable field has `navigable` set to `true`.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridcolumns-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridcolumns-put-openapi.md
- name: Jira Cloud REST API - Reset columns
  x-api-slug: api2filteridcolumns-delete
  description: Reset the user's column configuration for the filter to the default.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridcolumns-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridcolumns-delete-openapi.md
- name: Jira Cloud REST API - Add filter as favorite
  x-api-slug: api2filteridfavourite-put
  description: Add a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridfavourite-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridfavourite-put-openapi.md
- name: Jira Cloud REST API - Remove filter as favorite
  x-api-slug: api2filteridfavourite-delete
  description: Removes a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridfavourite-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridfavourite-delete-openapi.md
- name: Jira Cloud REST API - Get share permissions
  x-api-slug: api2filteridpermission-get
  description: Returns the share permissions for a filter. A filter can be shared
    with groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermission-get-openapi.md
- name: Jira Cloud REST API - Add share permission
  x-api-slug: api2filteridpermission-post
  description: "Add a share permissions to a filter. If you add a global share permission
    (i.e., all logged-in users or the public) it will overwrite all share permissions
    for the filter.  \nBe aware that this method uses different objects for updating
    share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share
    dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    and the calling user must own the filter."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermission-post-openapi.md
- name: Jira Cloud REST API - Get share permission
  x-api-slug: api2filteridpermissionpermissionid-get
  description: Returns a share permission for a filter. A filter can be shared with
    groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Delete share permission
  x-api-slug: api2filteridpermissionpermissionid-delete
  description: Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))
    and the calling user must own the filter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2filteridpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get group
  x-api-slug: api2group-get
  description: |-
    This resource is deprecated, use [`group/member`](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-group-member-get).

    Returns all users in a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2group-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2group-get-openapi.md
- name: Jira Cloud REST API - Create group
  x-api-slug: api2group-post
  description: |-
    Creates a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2group-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2group-post-openapi.md
- name: Jira Cloud REST API - Remove group
  x-api-slug: api2group-delete
  description: |-
    Deletes a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2group-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2group-delete-openapi.md
- name: Jira Cloud REST API - Get users from group
  x-api-slug: api2groupmember-get
  description: |-
    Returns all users in a group. Users are ordered by username.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupmember-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupmember-get-openapi.md
- name: Jira Cloud REST API - Add user to group
  x-api-slug: api2groupuser-post
  description: |-
    Adds a user to a group.

    **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupuser-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupuser-post-openapi.md
- name: Jira Cloud REST API - Remove user from group
  x-api-slug: api2groupuser-delete
  description: Removes a user from a group. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupuser-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupuser-delete-openapi.md
- name: Jira Cloud REST API - Find groups
  x-api-slug: api2groupspicker-get
  description: |-
    Returns groups with substrings matching a given query. This is mainly for use with the group picker, so the returned groups contain html to be used as picker suggestions. The groups are also wrapped in a single response object that also contains a header for use in the picker, specifically _Showing X of Y matching groups_.

    The number of groups returned is limited by the system property "jira.ajax.autocomplete.limit"

    The groups will be unique and sorted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupspicker-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupspicker-get-openapi.md
- name: Jira Cloud REST API - Find users and groups
  x-api-slug: api2groupuserpicker-get
  description: Returns a list of users and groups matching query with highlighting.
    This resource cannot be accessed anonymously.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupuserpicker-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2groupuserpicker-get-openapi.md
- name: Jira Cloud REST API - Create issue
  x-api-slug: api2issue-post
  description: |-
    Creates an issue or a sub-task from a JSON representation.

    You can provide two parameters in request's body: `update` or `fields`. The fields, that can be set on an issue create operation, can be determined using the **/rest/api/2/issue/createmeta** resource. If a particular field is not configured to appear on the issue's Create screen, then it will not be returned in the createmeta response. A field validation error will occur if such field is submitted in request.

    Creating a sub-task is similar to creating an issue with the following differences:

    *   `issueType` field must be set to a sub-task issue type (use `/issue/createmeta` to find sub-task issue types), and
    *   You must provide a `parent` field with the ID or key of the parent issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issue-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issue-post-openapi.md
- name: Jira Cloud REST API - Create issues
  x-api-slug: api2issuebulk-post
  description: |-
    Creates multiple issues or sub-tasks from a JSON representation, in a single bulk operation.

    Creating a sub-task is similar to creating an issue - check Create issue section for details: {@link IssueResource#createIssue(boolean, IssueUpdateBean)}}
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuebulk-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuebulk-post-openapi.md
- name: Jira Cloud REST API - Get create issue meta
  x-api-slug: api2issuecreatemeta-get
  description: |-
    Returns the metadata for creating issues. This includes the available projects, issue types, fields (with information whether those fields are required) and field types. Projects, in which the user does not have permission to create issues, will not be returned.

    The fields in the createmeta response correspond to the fields on the issue's Create screen for the specific project/issuetype. Fields hidden from the screen will not be returned in the createmeta response.

    Fields will only be returned if `expand=projects.issuetypes.fields` is set.

    The results can be filtered by project and/or issue type, controlled by the query parameters.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuecreatemeta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuecreatemeta-get-openapi.md
- name: Jira Cloud REST API - Get issue picker resource
  x-api-slug: api2issuepicker-get
  description: Returns a list of suggested issues matching the auto-completion query
    for the user executing this request. This REST method checks the user's history
    and browsing context to return issue suggestions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuepicker-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuepicker-get-openapi.md
- name: Jira Cloud REST API - Bulk set issue property
  x-api-slug: api2issuepropertiespropertykey-put
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuepropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuepropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Bulk delete issue property
  x-api-slug: api2issuepropertiespropertykey-delete
  description: Allows to delete a property from all issues identified by a given filter.
    Only entities the user has permissions to edit will be updated. See the [issue
    property bulk set endpoint documentation](#api-api-2-issue-properties-propertyKey-put)
    for more details.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuepropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuepropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get issue
  x-api-slug: api2issueissueidorkey-get
  description: |-
    Returns a full representation of the issue for the given issue key.

    The issue JSON consists of the issue key and a collection of fields. Additional information like links to workflow transition sub-resources, or HTML rendered values of the fields supporting HTML rendering can be retrieved with `expand` request parameter specified.

    The `fields` request parameter accepts a comma-separated list of fields to include in the response. It can be used to retrieve a subset of fields. By default all fields are returned in the response. A particular field can be excluded from the response if prefixed with a "-" (minus) sign. Parameter can be provided multiple times on a single request.

    By default, all fields are returned in the response. Note: this is different from a JQL search - only navigable fields are returned by default (`*navigable`).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkey-get-openapi.md
- name: Jira Cloud REST API - Edit issue
  x-api-slug: api2issueissueidorkey-put
  description: "Edits the issue from a JSON representation.\n\nThe fields available
    for update can be determined using the **/rest/api/2/issue/{issueIdOrKey}/editmeta**
    resource.  \nIf a field is hidden from the Edit screen then it will not be returned
    by the editmeta resource. A field validation error will occur if such field is
    submitted in an edit request. However connect add-on with admin scope may override
    a screen security configuration.\n\nIf an issue cannot be edited in Jira because
    of its workflow status (for example the issue is closed), then you will not be
    able to edit it with this resource.\n\nField to be updated should appear either
    in `fields` or `update` request's body parameter, but not in both.  \nTo update
    a single sub-field of a complex field (e.g. timetracking) please use the `update`
    parameter of the edit operation. Using a `\"field_id\": field_value` construction
    in the `fields` parameter is a shortcut of \"set\" operation in the `update` parameter."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkey-put-openapi.md
- name: Jira Cloud REST API - Delete issue
  x-api-slug: api2issueissueidorkey-delete
  description: |-
    Deletes an individual issue.

    If the issue has sub-tasks you must set the `deleteSubtasks=true` parameter to delete the issue. You cannot delete an issue without deleting its sub-tasks.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkey-delete-openapi.md
- name: Jira Cloud REST API - Assign issue
  x-api-slug: api2issueissueidorkeyassignee-put
  description: Assigns the issue to the user. Use this resource to assign issues for
    the users having "Assign Issue" permission, and not having the "Edit Issue" permission.
    If `name` body parameter is set to "-1" then automatic issue assignee is used.
    A `name` set to `null` will remove the assignee.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyassignee-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyassignee-put-openapi.md
- name: Jira Cloud REST API - Add attachment
  x-api-slug: api2issueissueidorkeyattachments-post
  description: |-
    Add one or more attachments to an issue.

    This resource expects a multipart post. The media-type multipart/form-data is defined in RFC 1867. Most client libraries have classes that make dealing with multipart posts simple. For instance, in Java the Apache HTTP Components library provides a [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) that makes it simple to submit a multipart POST.

    In order to protect against XSRF attacks, because this method accepts multipart/form-data, it has XSRF protection on it. This means you must submit a header of X-Atlassian-Token: no-check with the request, otherwise it will be blocked.

    The name of the multipart/form-data parameter that contains attachments must be "file"

    A simple example to upload a file called "myfile.txt" to issue REST-123:

    curl -D- -u admin:admin -X POST -H "X-Atlassian-Token: no-check" -F "file=@myfile.txt" http://myhost/rest/api/2/issue/TEST-123/attachments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyattachments-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyattachments-post-openapi.md
- name: Jira Cloud REST API - Get change logs
  x-api-slug: api2issueissueidorkeychangelog-get
  description: Returns a [paginated](#pagination) list of all updates of an issue,
    sorted by date, starting from the oldest.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeychangelog-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeychangelog-get-openapi.md
- name: Jira Cloud REST API - Get comments
  x-api-slug: api2issueissueidorkeycomment-get
  description: |-
    Returns all comments for an issue.

    Results can be ordered by the "created" field which means the date a comment was added.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycomment-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycomment-get-openapi.md
- name: Jira Cloud REST API - Add comment
  x-api-slug: api2issueissueidorkeycomment-post
  description: Adds a new comment to an issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycomment-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycomment-post-openapi.md
- name: Jira Cloud REST API - Get comment
  x-api-slug: api2issueissueidorkeycommentid-get
  description: Returns a single comment.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycommentid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycommentid-get-openapi.md
- name: Jira Cloud REST API - Update comment
  x-api-slug: api2issueissueidorkeycommentid-put
  description: Updates an existing comment using its JSON representation.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycommentid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycommentid-put-openapi.md
- name: Jira Cloud REST API - Delete comment
  x-api-slug: api2issueissueidorkeycommentid-delete
  description: Deletes an existing comment .
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycommentid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeycommentid-delete-openapi.md
- name: Jira Cloud REST API - Get edit issue meta
  x-api-slug: api2issueissueidorkeyeditmeta-get
  description: |-
    Returns the metadata for editing an issue.

    The fields returned by editmeta resource are the ones shown on the issue's Edit screen. Fields hidden from the screen will not be returned unless `overrideScreenSecurity` parameter is set to true.

    If an issue cannot be edited in Jira because of its workflow status (for example the issue is closed), then no fields will be returned, unless `overrideEditableFlag` is set to true.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyeditmeta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyeditmeta-get-openapi.md
- name: Jira Cloud REST API - Notify
  x-api-slug: api2issueissueidorkeynotify-post
  description: Sends an email notification to the list of users defined in the request
    body parameters.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeynotify-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeynotify-post-openapi.md
- name: Jira Cloud REST API - Get issue property keys
  x-api-slug: api2issueissueidorkeyproperties-get
  description: Returns the keys of all properties for the issue identified by the
    key or by the id.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyproperties-get-openapi.md
- name: Jira Cloud REST API - Get issue property
  x-api-slug: api2issueissueidorkeypropertiespropertykey-get
  description: Returns the value of the property with a given key from the issue identified
    by the key or by the id. The user who retrieves the property is required to have
    permissions to read the issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeypropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeypropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set issue property
  x-api-slug: api2issueissueidorkeypropertiespropertykey-put
  description: |-
    Sets the value of the specified issue's property.

    You can use this resource to store a custom data against the issue identified by the key or by the id. The user who stores the data is required to have permissions to edit the issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeypropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeypropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete issue property
  x-api-slug: api2issueissueidorkeypropertiespropertykey-delete
  description: Removes the property from the issue identified by the key or by the
    id. Ths user removing the property is required to have permissions to edit the
    issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeypropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeypropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get remote issue links
  x-api-slug: api2issueissueidorkeyremotelink-get
  description: Returns the remote issue links for the issue. This may be links to
    other Jira instances, web applications or web pages.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelink-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelink-get-openapi.md
- name: Jira Cloud REST API - Create or update remote issue link
  x-api-slug: api2issueissueidorkeyremotelink-post
  description: Creates or updates a remote issue link from a JSON representation.
    If a `globalId` is provided and a remote issue link exists with that globalId,
    the remote issue link is updated. Otherwise, the remote issue link is created.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelink-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelink-post-openapi.md
- name: Jira Cloud REST API - Delete remote issue link by global id
  x-api-slug: api2issueissueidorkeyremotelink-delete
  description: Deletes the issue's remote link with the given global ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelink-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelink-delete-openapi.md
- name: Jira Cloud REST API - Get remote issue link by id
  x-api-slug: api2issueissueidorkeyremotelinklinkid-get
  description: Returns the remote issue link by the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelinklinkid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelinklinkid-get-openapi.md
- name: Jira Cloud REST API - Update remote issue link
  x-api-slug: api2issueissueidorkeyremotelinklinkid-put
  description: Updates a remote issue link from a JSON representation. Sets all fields
    without values provided to null.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelinklinkid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelinklinkid-put-openapi.md
- name: Jira Cloud REST API - Delete remote issue link by id
  x-api-slug: api2issueissueidorkeyremotelinklinkid-delete
  description: Deletes the issue's remote link with the given ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelinklinkid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyremotelinklinkid-delete-openapi.md
- name: Jira Cloud REST API - Get transitions
  x-api-slug: api2issueissueidorkeytransitions-get
  description: |-
    Returns a list of transitions available for this issue for the current user.

    Specify `expand=transitions.fields` parameter to retrieve the fields required for a transition together with their types.

    Fields metadata corresponds to the fields available in a transition screen for a particular transition. Fields hidden from the screen will not be returned in the metadata.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeytransitions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeytransitions-get-openapi.md
- name: Jira Cloud REST API - Do transition
  x-api-slug: api2issueissueidorkeytransitions-post
  description: |-
    Performs the issue transition. While performing the transition you can modify other issue fields.

    The fields that can be set on transition, in either `fields` or `update` parameter can be determined using the **/rest/api/2/issue/{issueIdOrKey}/transitions?expand=transitions.fields** resource. If a field is not configured to appear on the transition screen, it will not be returned in the transition metadata. A field validation error will occur if such field is submitted in issue transition request.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeytransitions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeytransitions-post-openapi.md
- name: Jira Cloud REST API - Get votes
  x-api-slug: api2issueissueidorkeyvotes-get
  description: Returns voting data for an issue - whether the issue was voted for,
    total number of votes and users who voted for the issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyvotes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyvotes-get-openapi.md
- name: Jira Cloud REST API - Add vote
  x-api-slug: api2issueissueidorkeyvotes-post
  description: Adds a vote on the issue for a current user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyvotes-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyvotes-post-openapi.md
- name: Jira Cloud REST API - Remove vote
  x-api-slug: api2issueissueidorkeyvotes-delete
  description: Removes a current user's vote from an issue (aka "unvote").
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyvotes-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyvotes-delete-openapi.md
- name: Jira Cloud REST API - Get issue watchers
  x-api-slug: api2issueissueidorkeywatchers-get
  description: Returns the list of watchers for the issue with the given key.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeywatchers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeywatchers-get-openapi.md
- name: Jira Cloud REST API - Add watcher
  x-api-slug: api2issueissueidorkeywatchers-post
  description: Adds the user to the issue's watcher list.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeywatchers-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeywatchers-post-openapi.md
- name: Jira Cloud REST API - Remove watcher
  x-api-slug: api2issueissueidorkeywatchers-delete
  description: Removes the user from the issue's watcher list.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeywatchers-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeywatchers-delete-openapi.md
- name: Jira Cloud REST API - Get issue worklog
  x-api-slug: api2issueissueidorkeyworklog-get
  description: "Returns all work logs for an issue. The response is [paginated](#pagination)
    \ \n**Note:** Work logs won't be returned if the Log work field is hidden for
    the project."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklog-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklog-get-openapi.md
- name: Jira Cloud REST API - Add worklog
  x-api-slug: api2issueissueidorkeyworklog-post
  description: Adds a new worklog entry to an issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklog-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklog-post-openapi.md
- name: Jira Cloud REST API - Get worklog
  x-api-slug: api2issueissueidorkeyworklogid-get
  description: "Returns a specific worklog.  \n**Note:** The work log won't be returned
    if the Log work field is hidden for the project."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogid-get-openapi.md
- name: Jira Cloud REST API - Update worklog
  x-api-slug: api2issueissueidorkeyworklogid-put
  description: |-
    Updates an existing worklog entry.

    Note that:

    *   Fields possible for editing are: comment, visibility, started, timeSpent and timeSpentSeconds.
    *   Either timeSpent or timeSpentSeconds can be set.
    *   Fields which are not set will not be updated.
    *   For a request to be valid, it has to have at least one field change.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogid-put-openapi.md
- name: Jira Cloud REST API - Delete worklog
  x-api-slug: api2issueissueidorkeyworklogid-delete
  description: Deletes an existing worklog entry.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogid-delete-openapi.md
- name: Jira Cloud REST API - Get worklog property keys
  x-api-slug: api2issueissueidorkeyworklogworklogidproperties-get
  description: Returns the keys of all properties for the worklog identified by the
    key or by the id.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidproperties-get-openapi.md
- name: Jira Cloud REST API - Get worklog property
  x-api-slug: api2issueissueidorkeyworklogworklogidpropertiespropertykey-get
  description: Returns the value of the property with a given key from the worklog
    identified by the key or by the id. The user who retrieves the property is required
    to have permissions to read the worklog.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set worklog property
  x-api-slug: api2issueissueidorkeyworklogworklogidpropertiespropertykey-put
  description: |-
    Sets the value of the specified worklog's property.

    You can use this resource to store a custom data against the worklog identified by the key or by the id. The user who stores the data is required to have permissions to administer the worklog.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete worklog property
  x-api-slug: api2issueissueidorkeyworklogworklogidpropertiespropertykey-delete
  description: Removes the property from the worklog identified by the key or by the
    id. Ths user removing the property is required to have permissions to administer
    the worklog.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issueissueidorkeyworklogworklogidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Link issues
  x-api-slug: api2issuelink-post
  description: Creates an issue link between two issues. The user requires the link
    issue permission for the issue which will be linked to another issue. The specified
    link type in the request is used to create the link and will create a link from
    the first issue to the second issue using the outward description. It also create
    a link from the second issue to the first issue using the inward description of
    the issue link type. It will add the supplied comment to the first issue. The
    comment can have a restriction who can view it. If group is specified, only users
    of this group can view this comment, if roleLevel is specified only users who
    have the specified role can view this comment. The user who creates the issue
    link needs to belong to the specified group or have the specified role.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelink-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelink-post-openapi.md
- name: Jira Cloud REST API - Get issue link
  x-api-slug: api2issuelinklinkid-get
  description: Returns an issue link with the specified id.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinklinkid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinklinkid-get-openapi.md
- name: Jira Cloud REST API - Delete issue link
  x-api-slug: api2issuelinklinkid-delete
  description: Deletes an issue link with the specified id. To be able to delete an
    issue link you must be able to view both issues and must have the link issue permission
    for at least one of the issues.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinklinkid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinklinkid-delete-openapi.md
- name: Jira Cloud REST API - Get issue link types
  x-api-slug: api2issuelinktype-get
  description: Returns a list of available issue link types, if issue linking is enabled.
    Each issue link type has an id, a name and a label for the outward and inward
    link relationship.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktype-get-openapi.md
- name: Jira Cloud REST API - Create issue link type
  x-api-slug: api2issuelinktype-post
  description: Create a new issue link type.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktype-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktype-post-openapi.md
- name: Jira Cloud REST API - Get issue link type
  x-api-slug: api2issuelinktypeissuelinktypeid-get
  description: Returns for a given issue link type id all information about this issue
    link type.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktypeissuelinktypeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktypeissuelinktypeid-get-openapi.md
- name: Jira Cloud REST API - Update issue link type
  x-api-slug: api2issuelinktypeissuelinktypeid-put
  description: Update the specified issue link type.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktypeissuelinktypeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktypeissuelinktypeid-put-openapi.md
- name: Jira Cloud REST API - Delete issue link type
  x-api-slug: api2issuelinktypeissuelinktypeid-delete
  description: Delete the specified issue link type.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktypeissuelinktypeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuelinktypeissuelinktypeid-delete-openapi.md
- name: Jira Cloud REST API - Get issue security schemes
  x-api-slug: api2issuesecurityschemes-get
  description: Returns all issue security schemes that are defined.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuesecurityschemes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuesecurityschemes-get-openapi.md
- name: Jira Cloud REST API - Get issue security scheme
  x-api-slug: api2issuesecurityschemesid-get
  description: Returns the issue security scheme along with that are defined.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuesecurityschemesid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuesecurityschemesid-get-openapi.md
- name: Jira Cloud REST API - Get all issue types for user
  x-api-slug: api2issuetype-get
  description: Returns all issue types. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira, however, only issue types that are visible
    to the user are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetype-get-openapi.md
- name: Jira Cloud REST API - Create issue type
  x-api-slug: api2issuetype-post
  description: Creates an issue type and adds it to the default issue type scheme.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetype-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetype-post-openapi.md
- name: Jira Cloud REST API - Get issue type
  x-api-slug: api2issuetypeid-get
  description: |-
    Returns an issue type. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

    *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
    *   _Browse projects_ project permission to get the details of any issue type associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeid-get-openapi.md
- name: Jira Cloud REST API - Update issue type
  x-api-slug: api2issuetypeid-put
  description: Updates the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeid-put-openapi.md
- name: Jira Cloud REST API - Delete issue type
  x-api-slug: api2issuetypeid-delete
  description: Deletes the issue type. If the issue type is in use, all uses are updated
    with the alternative issue type (`alternativeIssueTypeId`). A list of alternative
    issue types can be obtained from the [Get alternative issue types](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-alternatives-get)
    resource. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeid-delete-openapi.md
- name: Jira Cloud REST API - Get alternative issue types
  x-api-slug: api2issuetypeidalternatives-get
  description: Returns a list of issue types that can be used to replace the issue
    type. The alternative issue types are those assigned to the same workflow scheme,
    field configuration scheme, and screen scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeidalternatives-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeidalternatives-get-openapi.md
- name: Jira Cloud REST API - Create issue type avatar
  x-api-slug: api2issuetypeidavatar2-post
  description: |-
    Creates an avatar for the issue type. Specify the avatar's local file location as binary data in the body of the request. Also, include the following headers:

    *   `X-Atlassian-Token: no-check`
    *   `Content-Type: image/_image type_` Valid image types are JPEG, GIF, or PNG.

    For example: `curl --request POST \ --user email@example.com: \ --header 'X-Atlassian-Token: no-check' \ --header 'Content-Type: image/< image_type>' \ --data-binary "" \ --url 'https://your-domain.atlassian.net/rest/api/2/issuetype/{issueTypeId}'This` The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image. The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size. After creating the avatar, use [Update issue type](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-put) to set it as the issue type's active avatar. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeidavatar2-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeidavatar2-post-openapi.md
- name: Jira Cloud REST API - Get issue type property keys
  x-api-slug: api2issuetypeissuetypeidproperties-get
  description: |-
    Returns all the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys of the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   _Administer Jira_ [global permission](href=) to get the property keys of any issue type.
    *   _Browse projects_ project permission to get the property keys of any issue types associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidproperties-get-openapi.md
- name: Jira Cloud REST API - Get issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-get
  description: |-
    Returns the key and value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:

    *   _Administer Jira_ [global permission](href=) to get the details of any issue type.
    *   _Browse projects_ project permission to get the details of any issue types associated with the projects the user has permission to browse.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-put
  description: Creates or updates the value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
    Use this resource to store and update data against an issue type. The value of
    the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty
    JSON blob. The maximum length of the property value is 32768 bytes. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete issue type property
  x-api-slug: api2issuetypeissuetypeidpropertiespropertykey-delete
  description: Deletes the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2issuetypeissuetypeidpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get auto complete
  x-api-slug: api2jqlautocompletedata-get
  description: Returns the auto complete data required for JQL searches.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2jqlautocompletedata-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2jqlautocompletedata-get-openapi.md
- name: Jira Cloud REST API - Get field auto complete for query string
  x-api-slug: api2jqlautocompletedatasuggestions-get
  description: Returns auto complete suggestions for JQL search.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2jqlautocompletedatasuggestions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2jqlautocompletedatasuggestions-get-openapi.md
- name: Jira Cloud REST API - Validate license
  x-api-slug: api2licensevalidator-post
  description: |-
    Validates a Jira license.

    Typically used by the setup phase of the Jira application. Returns an object with a list of errors as key, value pairs if the license is not valid.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2licensevalidator-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2licensevalidator-post-openapi.md
- name: Jira Cloud REST API - Get my permissions
  x-api-slug: api2mypermissions-get
  description: |-
    Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)

    If there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.

    If a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.

    If an issue context is provided, it will return whether or not the user has each permission in that specific issue.

    The above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.

    Global permissions work in the same way regardless of the scope.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypermissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypermissions-get-openapi.md
- name: Jira Cloud REST API - Get preference
  x-api-slug: api2mypreferences-get
  description: Returns preference of the currently logged in user. Preference key
    must be provided as input parameter (key). The value is returned exactly as it
    is.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferences-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferences-get-openapi.md
- name: Jira Cloud REST API - Set preference
  x-api-slug: api2mypreferences-put
  description: Sets preference of the currently logged in user. Preference key must
    be provided as input parameters (key). Value must be provided as POST body.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferences-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferences-put-openapi.md
- name: Jira Cloud REST API - Remove preference
  x-api-slug: api2mypreferences-delete
  description: Removes preference of the currently logged in user. Preference key
    must be provided as input parameters (key).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferences-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferences-delete-openapi.md
- name: Jira Cloud REST API - Get locale
  x-api-slug: api2mypreferenceslocale-get
  description: Returns the locale of the currently logged in user. If the user has
    no language preference explicitly set (the default setting), or is anonymous,
    this will be the browser locale detected by Jira. If browser detection is in effect,
    the "Accept-Language" browser header is used and falls back to the Jira site default
    locale if no match is found.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferenceslocale-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferenceslocale-get-openapi.md
- name: Jira Cloud REST API - Set locale
  x-api-slug: api2mypreferenceslocale-put
  description: Sets the locale of the currently logged in user. Locale JSON must be
    provided as PUT body.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferenceslocale-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferenceslocale-put-openapi.md
- name: Jira Cloud REST API - Delete locale
  x-api-slug: api2mypreferenceslocale-delete
  description: Deletes the set locale of the currently logged in user, resetting it
    to default.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferenceslocale-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2mypreferenceslocale-delete-openapi.md
- name: Jira Cloud REST API - Get current user
  x-api-slug: api2myself-get
  description: |-
    Returns currently logged user. This resource cannot be accessed anonymously.

    The resource accepts the `expand` param that is used to include, hidden by default, parts of response. This can be used to include:

    *   `groups` \- all groups, including nested groups, to which user belongs
    *   `applicationRoles` \- application roles defines to which application user has access
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2myself-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2myself-get-openapi.md
- name: Jira Cloud REST API - Get notification schemes paginated
  x-api-slug: api2notificationscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2notificationscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2notificationscheme-get-openapi.md
- name: Jira Cloud REST API - Get notification scheme
  x-api-slug: api2notificationschemeid-get
  description: |-
    Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with the requested notification scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2notificationschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2notificationschemeid-get-openapi.md
- name: Jira Cloud REST API - Get all permissions
  x-api-slug: api2permissions-get
  description: Returns all permissions that are present in the Jira instance - Global,
    Project and the global ones added by plugins
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissions-get-openapi.md
- name: Jira Cloud REST API - Get permitted projects
  x-api-slug: api2permissionsproject-post
  description: Returns all projects where currently logged in user was granted ALL
    requested project permissions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionsproject-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionsproject-post-openapi.md
- name: Jira Cloud REST API - Get all permission schemes
  x-api-slug: api2permissionscheme-get
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionscheme-get-openapi.md
- name: Jira Cloud REST API - Create permission scheme
  x-api-slug: api2permissionscheme-post
  description: Creates a new permission scheme. You can create a permission scheme
    with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionscheme-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionscheme-post-openapi.md
- name: Jira Cloud REST API - Get permission scheme
  x-api-slug: api2permissionschemeschemeid-get
  description: Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeid-get-openapi.md
- name: Jira Cloud REST API - Update permission scheme
  x-api-slug: api2permissionschemeschemeid-put
  description: |-
    Updates a permission scheme. Below are some important things to note when using this resource:

    *   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.
    *   If you want to update only the name and description, then do not send a permissions list in the request.
    *   Sending an empty list will remove all permission grants from the permission scheme.

    If you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeid-put-openapi.md
- name: Jira Cloud REST API - Delete permission scheme
  x-api-slug: api2permissionschemeschemeid-delete
  description: Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeid-delete-openapi.md
- name: Jira Cloud REST API - Get permission scheme grants
  x-api-slug: api2permissionschemeschemeidpermission-get
  description: Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermission-get-openapi.md
- name: Jira Cloud REST API - Create permission grant
  x-api-slug: api2permissionschemeschemeidpermission-post
  description: Creates a new permission grant in the given permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermission-post-openapi.md
- name: Jira Cloud REST API - Get permission scheme grant
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-get
  description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to log in to Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-get-openapi.md
- name: Jira Cloud REST API - Delete permission scheme entity
  x-api-slug: api2permissionschemeschemeidpermissionpermissionid-delete
  description: Deletes a permission grant from a permission scheme. See [About permission
    schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
    for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2permissionschemeschemeidpermissionpermissionid-delete-openapi.md
- name: Jira Cloud REST API - Get priorities
  x-api-slug: api2priority-get
  description: Returns a list of all issue priorities.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2priority-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2priority-get-openapi.md
- name: Jira Cloud REST API - Get priority
  x-api-slug: api2priorityid-get
  description: Returns an issue priority.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2priorityid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2priorityid-get-openapi.md
- name: Jira Cloud REST API - Get all projects
  x-api-slug: api2project-get
  description: |-
    Returns all projects visible to the currently logged in user. For projects to be visible, the authenticated user must be granted either _Browse projects_ or _Administer projects_ permissions. If no user is logged in, it returns all projects that are visible for anonymous users.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2project-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2project-get-openapi.md
- name: Jira Cloud REST API - Create project
  x-api-slug: api2project-post
  description: |-
    Creates a new project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2project-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2project-post-openapi.md
- name: Jira Cloud REST API - search
  x-api-slug: api2projectsearch-get
  description: Returns all projects visible to the currently logged in user, i.e.
    all projects the user has permission defined by the {@code action} parameter.
    If no user is logged in, all projects visible to anonymous users are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectsearch-get-openapi.md
- name: Jira Cloud REST API - Get all project types
  x-api-slug: api2projecttype-get
  description: |-
    Returns all [project types](https://confluence.atlassian.com/x/Var1Nw), whether or not the instance has a valid license for each type.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projecttype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projecttype-get-openapi.md
- name: Jira Cloud REST API - Get project type by key
  x-api-slug: api2projecttypeprojecttypekey-get
  description: |-
    Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projecttypeprojecttypekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projecttypeprojecttypekey-get-openapi.md
- name: Jira Cloud REST API - Get accessible project type by key
  x-api-slug: api2projecttypeprojecttypekeyaccessible-get
  description: |-
    Returns a [project type](https://confluence.atlassian.com/x/Var1Nw) if it is accessible to the logged in user.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projecttypeprojecttypekeyaccessible-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projecttypeprojecttypekeyaccessible-get-openapi.md
- name: Jira Cloud REST API - Get project
  x-api-slug: api2projectprojectidorkey-get
  description: |-
    Returns the [project details](https://confluence.atlassian.com/x/ahLpNw) for the specified project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkey-get-openapi.md
- name: Jira Cloud REST API - Update project
  x-api-slug: api2projectprojectidorkey-put
  description: |-
    Updates the [project details](https://confluence.atlassian.com/x/ahLpNw) of an existing project.

    All parameters are optional in the body of the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkey-put-openapi.md
- name: Jira Cloud REST API - Delete project
  x-api-slug: api2projectprojectidorkey-delete
  description: |-
    Deletes an existing project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkey-delete-openapi.md
- name: Jira Cloud REST API - Update project avatar
  x-api-slug: api2projectprojectidorkeyavatar-put
  description: ""
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatar-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatar-put-openapi.md
- name: Jira Cloud REST API - Delete project avatar
  x-api-slug: api2projectprojectidorkeyavatarid-delete
  description: Deletes an avatar of a single project. It is only possible to delete
    custom avatars.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatarid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatarid-delete-openapi.md
- name: Jira Cloud REST API - Create project avatar
  x-api-slug: api2projectprojectidorkeyavatar2-post
  description: Creates an avatar for a single project. Use it to upload an image to
    be be set as a project's avatar. The uploaded image will be cropped according
    to the crop parameters defined in the request. If no crop parameters are specified,
    the image will be cropped to a square. The square will originate at the top left
    of the image and the length of each side will be set to the smaller of the height
    or width of the image.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatar2-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatar2-post-openapi.md
- name: Jira Cloud REST API - Get all project avatars
  x-api-slug: api2projectprojectidorkeyavatars-get
  description: Returns all project avatars visible for the currently logged in user.
    The avatars are grouped into system avatars and custom avatars.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatars-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyavatars-get-openapi.md
- name: Jira Cloud REST API - Get project components paginated
  x-api-slug: api2projectprojectidorkeycomponent-get
  description: |-
    Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all components existing in a single project. See the [Get project components](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-components-get) resource if you want to get a full list of versions without pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeycomponent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeycomponent-get-openapi.md
- name: Jira Cloud REST API - Get project components
  x-api-slug: api2projectprojectidorkeycomponents-get
  description: |-
    Returns all components existing in a single project. See the [Get project components paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-component-get) resource if you want to get a full list of components with pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeycomponents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeycomponents-get-openapi.md
- name: Jira Cloud REST API - Get project property keys
  x-api-slug: api2projectprojectidorkeyproperties-get
  description: |-
    Returns all [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys for the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyproperties-get-openapi.md
- name: Jira Cloud REST API - Get project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-get
  description: |-
    Returns the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-put
  description: |-
    Sets the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). You can use project properties to store custom data against the project.

    The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 bytes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete project property
  x-api-slug: api2projectprojectidorkeypropertiespropertykey-delete
  description: |-
    Removes the [property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) from the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeypropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Get project roles for project
  x-api-slug: api2projectprojectidorkeyrole-get
  description: |-
    Returns a list of [project roles](https://confluence.atlassian.com/x/3odKLg) for the project.

    Note that all project roles are shared with all projects in Jira Cloud. See the [Get all project roles](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-get) resource for more information.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyrole-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyrole-get-openapi.md
- name: Jira Cloud REST API - Get project role for project
  x-api-slug: api2projectprojectidorkeyroleid-get
  description: |-
    Returns the project role's details and actors associated with the project. The list of actors is sorted by display name.

    If you would like to check to see whether a user belongs to a role based on their group memberships, use the [Get user](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-get) resource with the `groups` expand parameter selected. Then check whether the user keys and groups match with the actors returned for the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-get-openapi.md
- name: Jira Cloud REST API - Add actors to project role
  x-api-slug: api2projectprojectidorkeyroleid-post
  description: |-
    Adds additional actors to a project role for the project.

    If you want to replace all actors for the project, then use [Set actors for project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-put).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-post-openapi.md
- name: Jira Cloud REST API - Set actors for project role
  x-api-slug: api2projectprojectidorkeyroleid-put
  description: |-
    Associates actors with the project role for the project, replacing all existing actors.

    If you want to add actors to the project without overwriting the existing list, then use [Add actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-post).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-put-openapi.md
- name: Jira Cloud REST API - Delete actors from project role
  x-api-slug: api2projectprojectidorkeyroleid-delete
  description: |-
    Deletes actors from a project role for the project.

    If you want to remove default actors from the project role, see the [Delete default actors from project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-delete) resource.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroleid-delete-openapi.md
- name: Jira Cloud REST API - Get project role details
  x-api-slug: api2projectprojectidorkeyroledetails-get
  description: Returns all [project roles](https://confluence.atlassian.com/x/3odKLg)
    and the details for each role. Note that the list of project roles is common to
    all projects.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroledetails-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyroledetails-get-openapi.md
- name: Jira Cloud REST API - Get all statuses
  x-api-slug: api2projectprojectidorkeystatuses-get
  description: |-
    Returns the valid statuses for a project. The statuses are grouped by issue type, as each project has a set of valid issue types and each issue type has a set of valid statuses.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeystatuses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeystatuses-get-openapi.md
- name: Jira Cloud REST API - Update project type
  x-api-slug: api2projectprojectidorkeytypenewprojecttypekey-put
  description: |-
    Updates the [project type](https://confluence.atlassian.com/x/GwiiLQ).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeytypenewprojecttypekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeytypenewprojecttypekey-put-openapi.md
- name: Jira Cloud REST API - Get project versions paginated
  x-api-slug: api2projectprojectidorkeyversion-get
  description: |-
    Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all versions existing in a single project. See the [Get project versions](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-versions-get) resource if you want to get a full list of versions without pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyversion-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyversion-get-openapi.md
- name: Jira Cloud REST API - Get project versions
  x-api-slug: api2projectprojectidorkeyversions-get
  description: |-
    Returns all versions existing in a single project. The response is not paginated. Use [Get project versions paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-version-get) if you want to get the versions in a project with pagination.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyversions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectidorkeyversions-get-openapi.md
- name: Jira Cloud REST API - Get project issue security scheme
  x-api-slug: api2projectprojectkeyoridissuesecuritylevelscheme-get
  description: |-
    Returns the [issue security scheme](https://confluence.atlassian.com/x/J4lKLg) associated with the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or the _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridissuesecuritylevelscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridissuesecuritylevelscheme-get-openapi.md
- name: Jira Cloud REST API - Get project notification scheme
  x-api-slug: api2projectprojectkeyoridnotificationscheme-get
  description: |-
    Gets a [notification scheme](https://confluence.atlassian.com/x/8YdKLg) associated with the project. See the [Get notification scheme](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-id-get) resource for more information about notification schemes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridnotificationscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridnotificationscheme-get-openapi.md
- name: Jira Cloud REST API - Get assigned permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-get
  description: |-
    Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-get-openapi.md
- name: Jira Cloud REST API - Assign permission scheme
  x-api-slug: api2projectprojectkeyoridpermissionscheme-put
  description: |-
    Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridpermissionscheme-put-openapi.md
- name: Jira Cloud REST API - Get project issue security levels
  x-api-slug: api2projectprojectkeyoridsecuritylevel-get
  description: |-
    Returns all [issue security](https://confluence.atlassian.com/x/J4lKLg) levels for the project that the currently authenticated user has access to. If the user does not have permission to see an issue security level, then that level is not returned. If the user lacks the _Set Issue Security_ permission, then an empty list is returned.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Set Issue Security_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridsecuritylevel-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectprojectkeyoridsecuritylevel-get-openapi.md
- name: Jira Cloud REST API - Get all project categories
  x-api-slug: api2projectcategory-get
  description: Returns all project categories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategory-get-openapi.md
- name: Jira Cloud REST API - Create project category
  x-api-slug: api2projectcategory-post
  description: Create a project category via POST.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategory-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategory-post-openapi.md
- name: Jira Cloud REST API - Get project category by id
  x-api-slug: api2projectcategoryid-get
  description: Contains a representation of a project category in JSON format.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategoryid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategoryid-get-openapi.md
- name: Jira Cloud REST API - Update project category
  x-api-slug: api2projectcategoryid-put
  description: Modify a project category via PUT. Any fields present in the PUT will
    override existing values. As a convenience, if a field is not present, it is silently
    ignored.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategoryid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategoryid-put-openapi.md
- name: Jira Cloud REST API - Remove project category
  x-api-slug: api2projectcategoryid-delete
  description: Delete a project category.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategoryid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectcategoryid-delete-openapi.md
- name: Jira Cloud REST API - Validate project key
  x-api-slug: api2projectvalidatekey-get
  description: Validates a project key.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectvalidatekey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectvalidatekey-get-openapi.md
- name: Jira Cloud REST API - Get valid project key
  x-api-slug: api2projectvalidatevalidprojectkey-get
  description: Validates the project key and generated a valid project key if the
    supplied key is invalid.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectvalidatevalidprojectkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectvalidatevalidprojectkey-get-openapi.md
- name: Jira Cloud REST API - Get valid project name
  x-api-slug: api2projectvalidatevalidprojectname-get
  description: Validates a project name. If the name is invalid, an attempt is made
    to produce a valid name based on the supplied one. If no such valid name can be
    found, an empty string is returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectvalidatevalidprojectname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2projectvalidatevalidprojectname-get-openapi.md
- name: Jira Cloud REST API - Get resolutions
  x-api-slug: api2resolution-get
  description: Returns a list of all resolutions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2resolution-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2resolution-get-openapi.md
- name: Jira Cloud REST API - Get resolution
  x-api-slug: api2resolutionid-get
  description: Returns a resolution.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2resolutionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2resolutionid-get-openapi.md
- name: Jira Cloud REST API - Get all project roles
  x-api-slug: api2role-get
  description: |-
    Gets a list of all project roles, complete with project role details and default actors.

    ### About project roles

    [Project roles](https://confluence.atlassian.com/x/3odKLg) are a flexible way to to associate users and groups with projects. In Jira Cloud, the list of project roles is shared globally with all projects, but each project can have a different set of actors associated with it (unlike groups, which have the same membership throughout all Jira applications).

    Project roles can be used in [permission schemes](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-get), [email notification schemes](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-get), [issue security levels](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuesecurityschemes-get), [comment visibility](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-comment-list-post), and workflow conditions.

    #### Members and actors

    In the Jira REST API, a member of a project role is called an _actor_. An _actor_ is a group or user associated with a project role.

    Actors may be set as [default members](https://confluence.atlassian.com/x/3odKLg#Managingprojectroles-Specifying'defaultmembers'foraprojectrole) of the project role or set at the project level:

    *   Default actors: Users and groups that are assigned to the project role for all newly created projects. The default actors can be removed at the project level later if desired.
    *   Actors: Users and groups that are associated with a project role for a particular project, which may differ from the default actors. This allows you to assign a particular user to different roles in different projects.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2role-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2role-get-openapi.md
- name: Jira Cloud REST API - Create project role
  x-api-slug: api2role-post
  description: |-
    Creates a new project role with no [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get). You can use the [Add default actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-post) the project method to add default actors to the project role after creating it.

    _Note that although a new project role is available to all projects upon creation, any default actors that are associated with the project role are not added to projects that existed prior to the role being created._<

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2role-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2role-post-openapi.md
- name: Jira Cloud REST API - Get project role by ID
  x-api-slug: api2roleid-get
  description: |-
    Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-get-openapi.md
- name: Jira Cloud REST API - Partial update project role
  x-api-slug: api2roleid-post
  description: |-
    Update either the project role's name or its description.

    You cannot update both the name and description at the same time using this method. If you send a request with both a name and a description, then only the name will be updated, regardless of the order of appearance in the body of the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-post-openapi.md
- name: Jira Cloud REST API - Fully update project role
  x-api-slug: api2roleid-put
  description: |-
    Update the project role's name and description. You must include both a name and a description in the request.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-put-openapi.md
- name: Jira Cloud REST API - Delete project role
  x-api-slug: api2roleid-delete
  description: |-
    Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleid-delete-openapi.md
- name: Jira Cloud REST API - Get default actors for project role
  x-api-slug: api2roleidactors-get
  description: |-
    Returns the [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) for the project role.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleidactors-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleidactors-get-openapi.md
- name: Jira Cloud REST API - Add default actors to project role
  x-api-slug: api2roleidactors-post
  description: |-
    Adds [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) to the given role. You may add either groups or users, but you cannot add groups and users in the same request.

    Changing a project role's default actors does not affect project role members for projects already created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleidactors-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleidactors-post-openapi.md
- name: Jira Cloud REST API - Delete default actors from project role
  x-api-slug: api2roleidactors-delete
  description: |-
    Removes [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) from the project role. You may remove either a group or user, but you cannot remove a group and a user in the same request.

    Changing a project role's default actors does not affect project role members for projects already created.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleidactors-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2roleidactors-delete-openapi.md
- name: Jira Cloud REST API - Get all screens
  x-api-slug: api2screens-get
  description: Returns a [paginated](#pagination) list of all screens.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screens-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screens-get-openapi.md
- name: Jira Cloud REST API - Add field to default screen
  x-api-slug: api2screensaddtodefaultfieldid-post
  description: Adds field or custom field to the default tab
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensaddtodefaultfieldid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensaddtodefaultfieldid-post-openapi.md
- name: Jira Cloud REST API - Get available screen fields
  x-api-slug: api2screensscreenidavailablefields-get
  description: Gets available fields for screen. i.e ones that haven't already been
    added.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidavailablefields-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidavailablefields-get-openapi.md
- name: Jira Cloud REST API - Get all screen tabs
  x-api-slug: api2screensscreenidtabs-get
  description: Returns a list of all tabs for the given screen
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabs-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabs-get-openapi.md
- name: Jira Cloud REST API - Add screen tab
  x-api-slug: api2screensscreenidtabs-post
  description: Creates tab for given screen
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabs-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabs-post-openapi.md
- name: Jira Cloud REST API - Rename screen tab
  x-api-slug: api2screensscreenidtabstabid-put
  description: Renames tab on given screen
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabid-put-openapi.md
- name: Jira Cloud REST API - Delete screen tab
  x-api-slug: api2screensscreenidtabstabid-delete
  description: Deletes tab to give screen
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabid-delete-openapi.md
- name: Jira Cloud REST API - Get all screen tab fields
  x-api-slug: api2screensscreenidtabstabidfields-get
  description: Gets all fields for a given tab
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfields-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfields-get-openapi.md
- name: Jira Cloud REST API - Add screen tab field
  x-api-slug: api2screensscreenidtabstabidfields-post
  description: Adds field to the given tab.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfields-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfields-post-openapi.md
- name: Jira Cloud REST API - Remove screen tab field
  x-api-slug: api2screensscreenidtabstabidfieldsid-delete
  description: Removes field from given tab
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfieldsid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfieldsid-delete-openapi.md
- name: Jira Cloud REST API - Move screen tab field
  x-api-slug: api2screensscreenidtabstabidfieldsidmove-post
  description: Moves field on the given tab
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfieldsidmove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidfieldsidmove-post-openapi.md
- name: Jira Cloud REST API - Move screen tab
  x-api-slug: api2screensscreenidtabstabidmovepos-post
  description: Moves tab position
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidmovepos-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2screensscreenidtabstabidmovepos-post-openapi.md
- name: Jira Cloud REST API - Search for issues using JQL (GET)
  x-api-slug: api2search-get
  description: |-
    Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

    If the JQL query expression is too large to be encoded as a query parameter, use the [POST](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-post) version of this resource.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2search-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2search-get-openapi.md
- name: Jira Cloud REST API - Search for issues using JQL (POST)
  x-api-slug: api2search-post
  description: |-
    Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

    There is a [GET](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-get) version of this resource that can be used for smaller JQL query expressions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2search-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2search-post-openapi.md
- name: Jira Cloud REST API - Get issue security level
  x-api-slug: api2securitylevelid-get
  description: Returns a full representation of the security level that has the given
    id.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2securitylevelid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2securitylevelid-get-openapi.md
- name: Jira Cloud REST API - Get server info
  x-api-slug: api2serverinfo-get
  description: Returns general information about the current Jira server.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2serverinfo-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2serverinfo-get-openapi.md
- name: Jira Cloud REST API - Set base url
  x-api-slug: api2settingsbaseurl-put
  description: Sets the base URL that is configured for this Jira instance.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2settingsbaseurl-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2settingsbaseurl-put-openapi.md
- name: Jira Cloud REST API - Get issue navigator default columns
  x-api-slug: api2settingscolumns-get
  description: Returns the default system columns for issue navigator. Admin permission
    will be required.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2settingscolumns-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2settingscolumns-get-openapi.md
- name: Jira Cloud REST API - Set issue navigator default columns
  x-api-slug: api2settingscolumns-put
  description: Sets the default system columns for issue navigator. Admin permission
    will be required.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2settingscolumns-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2settingscolumns-put-openapi.md
- name: Jira Cloud REST API - Get statuses
  x-api-slug: api2status-get
  description: Returns a list of all statuses
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2status-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2status-get-openapi.md
- name: Jira Cloud REST API - Get status
  x-api-slug: api2statusidorname-get
  description: Returns a full representation of the Status having the given id or
    name. If there are two statuses with the same name, only the first found status
    will be returned. Therefore searching by id is encouraged.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2statusidorname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2statusidorname-get-openapi.md
- name: Jira Cloud REST API - Get status categories
  x-api-slug: api2statuscategory-get
  description: Returns a list of all status categories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2statuscategory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2statuscategory-get-openapi.md
- name: Jira Cloud REST API - Get status category
  x-api-slug: api2statuscategoryidorkey-get
  description: Returns a full representation of the StatusCategory having the given
    id or key
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2statuscategoryidorkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2statuscategoryidorkey-get-openapi.md
- name: Jira Cloud REST API - Get task
  x-api-slug: api2tasktaskid-get
  description: |-
    This endpoint is used to check the status of a [long-running asynchronous task](#async).

    When the task is finished, it will contain a **result**. The result may be arbitrary JSON, its shape different for each task type. Consult the documentation of the method that created the task for more details.

    To access a task, you need to be its creator or a Jira admin. Otherwise a 403 response will be returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2tasktaskid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2tasktaskid-get-openapi.md
- name: Jira Cloud REST API - Cancel task
  x-api-slug: api2tasktaskidcancel-post
  description: |-
    Requests that the task that corresponds to the given task id is cancelled.

    To cancel a task, you need to be its creator or a Jira admin. Otherwise a 403 response will be returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2tasktaskidcancel-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2tasktaskidcancel-post-openapi.md
- name: Jira Cloud REST API - Get avatars
  x-api-slug: api2universal-avatartypetypeownerentityid-get
  description: ""
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2universal-avatartypetypeownerentityid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2universal-avatartypetypeownerentityid-get-openapi.md
- name: Jira Cloud REST API - Store avatar
  x-api-slug: api2universal-avatartypetypeownerentityid-post
  description: Creates an avatar for a given entity, for the given entity ID and type
    of entity. For example, you can create an avatar for an issue type, given the
    issue type Id. Uploading an avatar is supported for different types of entities
    across the Jira products. However, it is supported for the "project" and "issuetype"
    entity types for all Jira products. The uploaded image will be cropped according
    to the crop parameters listed below. If no crop parameters are specified, the
    image will be cropped to a square. The square will originate at the top left of
    the image and the length of each side will be set to the smaller of the height
    or width of the image.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2universal-avatartypetypeownerentityid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2universal-avatartypetypeownerentityid-post-openapi.md
- name: Jira Cloud REST API - Delete avatar
  x-api-slug: api2universal-avatartypetypeownerowningobjectidavatarid-delete
  description: Deletes avatar
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2universal-avatartypetypeownerowningobjectidavatarid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2universal-avatartypetypeownerowningobjectidavatarid-delete-openapi.md
- name: Jira Cloud REST API - Get user
  x-api-slug: api2user-get
  description: Returns a user. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2user-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2user-get-openapi.md
- name: Jira Cloud REST API - Create user
  x-api-slug: api2user-post
  description: 'Creates a user. This resource is retained for legacy compatibility.
    As soon as a more suitable alternative is available this resource will be deprecated.
    The option is provided to set or generate a password for the user. When using
    the option to generate a password, by omitting `password` from the request, include
    `"notification": "true"` to ensure the user is sent an email advising them that
    their account has been created. This email includes a link for the user to set
    their password. If the notification isn''t sent for a generated password, the
    user will need to be sent a reset password request from Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=)'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2user-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2user-post-openapi.md
- name: Jira Cloud REST API - Delete user
  x-api-slug: api2user-delete
  description: Deletes a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Site administration (i.e., member of the site-admin [group](https://confluence.atlassian.com/display/Cloud/Manage+groups)).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2user-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2user-delete-openapi.md
- name: Jira Cloud REST API - Find users assignable to projects
  x-api-slug: api2userassignablemultiprojectsearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a string.
    *   they can be assigned issues in one or more projects.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userassignablemultiprojectsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userassignablemultiprojectsearch-get-openapi.md
- name: Jira Cloud REST API - Find users assignable to issues
  x-api-slug: api2userassignablesearch-get
  description: |-
    Returns a list of users that can be assigned to an issue. Use this method to find the list of users who can be assigned to:

    *   a new issue, by providing the `projectKeyOrId`.
    *   an updated issue, by providing the `issueKey`.
    *   to an issue during a transition (workflow action), by providing the `issueKey` and the transition id in `actionDescriptorId`. You can obtain the IDs of an issue's valid transitions using the `transitions` option in the `expand` parameter of [Get issue](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issue-issueIdOrKey-get).

    In all these cases, you can pass a username to determine if a user can be assigned to an issue. The user is returned in the response if they can be assigned to the issue or issue transition. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userassignablesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userassignablesearch-get-openapi.md
- name: Jira Cloud REST API - Bulk get users
  x-api-slug: api2userbulk-get
  description: Returns details of users specified in a list of usernames or keys.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
    Jira_ [global permission](href=). Users with permission to access Jira can call
    this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userbulk-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userbulk-get-openapi.md
- name: Jira Cloud REST API - Get user default columns
  x-api-slug: api2usercolumns-get
  description: |-
    Returns the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed in the request, the calling user's details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To get the column details for any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLgl).
    *   To get the calling user's column details: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usercolumns-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usercolumns-get-openapi.md
- name: Jira Cloud REST API - Set user default columns
  x-api-slug: api2usercolumns-put
  description: |-
    Sets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed. The parameters for this resource are expressed as HTML form data. For example, in curl: `curl -X PUT -d username= -d columns=summary -d columns=description ` **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set the calling user's columns: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usercolumns-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usercolumns-put-openapi.md
- name: Jira Cloud REST API - Reset user default columns
  x-api-slug: api2usercolumns-delete
  description: |-
    Resets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user to the system default. If a username is not passed, the calling user's default columns are reset. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set the calling user's columns: None
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usercolumns-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usercolumns-delete-openapi.md
- name: Jira Cloud REST API - Get user groups
  x-api-slug: api2usergroups-get
  description: Returns the groups to which a user belongs. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
    _Browse users and groups_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usergroups-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usergroups-get-openapi.md
- name: Jira Cloud REST API - Find users with permissions
  x-api-slug: api2userpermissionsearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have a set of permissions for a project or issue.

    If no search string is provided, a list of all users with the permissions is returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   Get users for any project, _Administer Jira_ [global permission](href=).
    *   Get users for a project, _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpermissionsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpermissionsearch-get-openapi.md
- name: Jira Cloud REST API - Find users for picker
  x-api-slug: api2userpicker-get
  description: Returns a list of users whose attributes match the query term. The
    returned object includes the `html` field where the matched query term is highlighted
    with the HTML strong tag. A list of usernames can be provided to exclude users
    from the results. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    _Browse users and groups_ [global permission](href=). Users with permission to
    access Jira can call this method, but will only get search results for an exact
    name match.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpicker-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpicker-get-openapi.md
- name: Jira Cloud REST API - Get user property keys
  x-api-slug: api2userproperties-get
  description: |-
    Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To access the calling user's property keys: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userproperties-get-openapi.md
- name: Jira Cloud REST API - Get user property
  x-api-slug: api2userpropertiespropertykey-get
  description: |-
    Returns the value of a user's property. If no property key is provided [Get user property keys](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-properties-get) is called. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To get a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To get a property from the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpropertiespropertykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpropertiespropertykey-get-openapi.md
- name: Jira Cloud REST API - Set user property
  x-api-slug: api2userpropertiespropertykey-put
  description: |-
    Sets the value of a user's property. Use this resource to store custom data against a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To set a property on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To set a property on the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpropertiespropertykey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpropertiespropertykey-put-openapi.md
- name: Jira Cloud REST API - Delete user property
  x-api-slug: api2userpropertiespropertykey-delete
  description: |-
    Deletes a property from a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To delete a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To delete a property from the calling user's record: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpropertiespropertykey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userpropertiespropertykey-delete-openapi.md
- name: Jira Cloud REST API - Find users
  x-api-slug: api2usersearch-get
  description: Returns a list of users that match the search string and property.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse
    users and groups_ [global permission](href=). Users with permission to access
    Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usersearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usersearch-get-openapi.md
- name: Jira Cloud REST API - Find users by query
  x-api-slug: api2usersearchquery-get
  description: |-
    Finds users using a structured query and returns user details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). The available queries statements are:

    `is assignee of PROJ` Returns the users that are assignees of at least one issue in project _PROJ_.*   `is assignee of (PROJ-1, PROJ-2)` Returns users that are assignees on the issues _PROJ-1_ or _PROJ-2_.
    *   `is reporter of (PROJ-1, PROJ-2)` Returns users that are reporters on the issues _PROJ-1_ or _PROJ-2_.
    *   `is watcher of (PROJ-1, PROJ-2)` Returns users that are watchers on the issues _PROJ-1_ or _PROJ-2_.
    *   `is voter of (PROJ-1, PROJ-2)` Returns users that are voters on the issues _PROJ-1_ or _PROJ-2_.
    *   `is commenter of (PROJ-1, PROJ-2)` Returns users that have posted a comment on the issues _PROJ-1_ or _PROJ-2_.
    *   `is transitioner of (PROJ-1, PROJ-2)` Returns users that have performed a transition on issues _PROJ-1_ or _PROJ-2_.
    *   `[propertyKey].entity.property.path is "property value"` Returns users with the entity property value.

    The list of issues can be extended as needed, as in _(PROJ-1, PROJ-2, ... PROJ-n)_. Statements can be combined using the `AND` and `OR` operators to form more complex queries, for example:

    `is assignee of PROJ AND [propertyKey].entity.property.path is "property value"`
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usersearchquery-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usersearchquery-get-openapi.md
- name: Jira Cloud REST API - Find user keys by query
  x-api-slug: api2usersearchquerykey-get
  description: |-
    Finds users using a structured query and returns a list of user keys. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). The available query statements are:

    *   `is assignee of PROJ` Returns the users that are assignees of at least one issue in project _PROJ_.
    *   `is assignee of (PROJ-1, PROJ-2)` Returns users that are assignees on the issues _PROJ-1_ or _PROJ-2_.
    *   `is reporter of (PROJ-1, PROJ-2)` Returns users that are reporters on the issues _PROJ-1_ or _PROJ-2_.
    *   `is watcher of (PROJ-1, PROJ-2)` Returns users that are watchers on the issues _PROJ-1_ or _PROJ-2_.
    *   `is voter of (PROJ-1, PROJ-2)` Returns users that are voters on the issues _PROJ-1_ or _PROJ-2_.
    *   `is commenter of (PROJ-1, PROJ-2)` Returns users that have posted a comment on the issues _PROJ-1_ or _PROJ-2_.
    *   `is transitioner of (PROJ-1, PROJ-2)` Returns users that have performed a transition on issues _PROJ-1_ or _PROJ-2_.
    *   `[propertyKey].entity.property.path is "property value"` Returns users with the entity property value.

    The list of issues can be extended as needed, as in _(PROJ-1, PROJ-2, ... PROJ-n)_. Statements can be combined using the `AND` and `OR` operators to form more complex queries, for example:

    `is assignee of PROJ AND [propertyKey].entity.property.path is "property value"`
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usersearchquerykey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2usersearchquerykey-get-openapi.md
- name: Jira Cloud REST API - Find users with browse permission
  x-api-slug: api2userviewissuesearch-get
  description: |-
    Returns a list of users who fulfill both of these criteria:

    *   their user attributes match a search string.
    *   they have permission to browse issues.

    Use this resource to find users who can browse:

    *   an issue, by providing the `issueKey`.
    *   any issue in a project, by providing the `projectKey`.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userviewissuesearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2userviewissuesearch-get-openapi.md
- name: Jira Cloud REST API - Create version
  x-api-slug: api2version-post
  description: Creates a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2version-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2version-post-openapi.md
- name: Jira Cloud REST API - Get remote version links
  x-api-slug: api2versionremotelink-get
  description: Returns the remote version links for a given global ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionremotelink-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionremotelink-get-openapi.md
- name: Jira Cloud REST API - Get version
  x-api-slug: api2versionid-get
  description: 'Returns a project version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required: _Browse projects_ project permission'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionid-get-openapi.md
- name: Jira Cloud REST API - Update version
  x-api-slug: api2versionid-put
  description: Modifies a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionid-put-openapi.md
- name: Jira Cloud REST API - Delete version
  x-api-slug: api2versionid-delete
  description: Deletes a project version. Deprecated, use [Delete and replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
    that supports swapping version values in custom fields, in addition to the swapping
    for `fixVersion` and `affectedVersion` provided in this resource. Alternative
    versions can be provided to update issues that use the deleted version in `fixVersion`
    or `affectedVersion`. If alternatives are not provided, occurrences of `fixVersion`
    and `affectedVersion` that contain the deleted version are cleared. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionid-delete-openapi.md
- name: Jira Cloud REST API - Merge versions
  x-api-slug: api2versionidmergetomoveissuesto-put
  description: Merges two project versions. The merge is completed by deleting the
    version specified in `id` and replacing any occurrences of its ID in `fixVersion`
    with the version ID specified in `moveIssuesTo`. Consider using [Delete and replace
    version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post)
    instead. This resource supports swapping version values in `fixVersion`, `affectedVersion`,
    and custom fields. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidmergetomoveissuesto-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidmergetomoveissuesto-put-openapi.md
- name: Jira Cloud REST API - Move version
  x-api-slug: api2versionidmove-post
  description: Modifies the version's sequence within the project, which affects the
    display order of the versions in Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidmove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidmove-post-openapi.md
- name: Jira Cloud REST API - Get version's related issues count
  x-api-slug: api2versionidrelatedissuecounts-get
  description: |-
    Returns the following counts for a version:

    *   Number of issues where the `fixVersion` is set to the version.
    *   Number of issues where the `affectedVersion` is set to the version.
    *   Number of issues where a version custom field is set to the version.

    [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ project permission
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidrelatedissuecounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidrelatedissuecounts-get-openapi.md
- name: Jira Cloud REST API - Delete and replace version
  x-api-slug: api2versionidremoveandswap-post
  description: Deletes a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
    or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
    Alternative versions can be provided to update issues that use the deleted version
    in `fixVersion`, `affectedVersion`, or any version picker custom fields. If alternatives
    are not provided, occurrences of `fixVersion`, `affectedVersion`, and any version
    picker custom field, that contain the deleted version, are cleared. Any replacement
    version must be in the same project as the version being deleted and cannot be
    the version being deleted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidremoveandswap-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidremoveandswap-post-openapi.md
- name: Jira Cloud REST API - Get version's unresolved issues count
  x-api-slug: api2versionidunresolvedissuecount-get
  description: 'Returns counts of the issues and unresolved issues for the project
    version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse
    projects_ project permission'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidunresolvedissuecount-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionidunresolvedissuecount-get-openapi.md
- name: Jira Cloud REST API - Get remote version links by version id
  x-api-slug: api2versionversionidremotelink-get
  description: Returns the remote version links associated with the given version
    ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelink-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelink-get-openapi.md
- name: Jira Cloud REST API - Create or update remote version link
  x-api-slug: api2versionversionidremotelink-post
  description: Create a remote version link via POST. The link's global ID will be
    taken from the JSON payload if provided; otherwise, it will be generated.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelink-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelink-post-openapi.md
- name: Jira Cloud REST API - Delete remote version links by version id
  x-api-slug: api2versionversionidremotelink-delete
  description: Delete all remote version links for a given version ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelink-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelink-delete-openapi.md
- name: Jira Cloud REST API - Get remote version link
  x-api-slug: api2versionversionidremotelinkglobalid-get
  description: A REST sub-resource representing a remote version link
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelinkglobalid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelinkglobalid-get-openapi.md
- name: Jira Cloud REST API - Create or update remote version link with global id
  x-api-slug: api2versionversionidremotelinkglobalid-post
  description: Create a remote version link via POST using the provided global ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelinkglobalid-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelinkglobalid-post-openapi.md
- name: Jira Cloud REST API - Delete remote version link
  x-api-slug: api2versionversionidremotelinkglobalid-delete
  description: Delete a specific remote version link with the given version ID and
    global ID.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelinkglobalid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2versionversionidremotelinkglobalid-delete-openapi.md
- name: Jira Cloud REST API - Get all workflows
  x-api-slug: api2workflow-get
  description: |-
    Returns all workflows in Jira or a single workflow.

    If the `workflowName` parameter is specified, a workflow will be returned as an object (not in an array). Otherwise, an array of workflow objects will be returned.

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflow-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflow-get-openapi.md
- name: Jira Cloud REST API - Get workflow transition properties
  x-api-slug: api2workflowtransitionstransitionidproperties-get
  description: |-
    Returns the properties on a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-get-openapi.md
- name: Jira Cloud REST API - Create workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-post
  description: |-
    Adds a property to a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-post-openapi.md
- name: Jira Cloud REST API - Update workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-put
  description: |-
    Updates a workflow transition by changing the property value. Trying to update a property that does not exist results in a new property being added to the transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-put-openapi.md
- name: Jira Cloud REST API - Delete workflow transition property
  x-api-slug: api2workflowtransitionstransitionidproperties-delete
  description: |-
    Deletes a property from a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).

    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowtransitionstransitionidproperties-delete-openapi.md
- name: Jira Cloud REST API - Create workflow scheme
  x-api-slug: api2workflowscheme-post
  description: |-
    Create a new workflow scheme.

    The body contains a representation of the new scheme. Values not passed are assumed to be set to their defaults.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowscheme-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowscheme-post-openapi.md
- name: Jira Cloud REST API - Get workflow scheme
  x-api-slug: api2workflowschemeid-get
  description: Returns the requested workflow scheme to the caller.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeid-get-openapi.md
- name: Jira Cloud REST API - Update workflow scheme
  x-api-slug: api2workflowschemeid-put
  description: |-
    Update the passed workflow scheme.

    The body of the request is a representation of the workflow scheme. Values not passed are assumed to indicate no change for that field.

    The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created and/or updated when the actual scheme cannot be edited (e.g. when the scheme is being used by a project). Values not appearing the body will not be touched.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeid-put-openapi.md
- name: Jira Cloud REST API - Delete workflow scheme
  x-api-slug: api2workflowschemeid-delete
  description: Delete the passed workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeid-delete-openapi.md
- name: Jira Cloud REST API - Create workflow scheme draft from parent
  x-api-slug: api2workflowschemeidcreatedraft-post
  description: Create a draft for the passed scheme. The draft will be a copy of the
    state of the parent.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidcreatedraft-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidcreatedraft-post-openapi.md
- name: Jira Cloud REST API - Get default workflow
  x-api-slug: api2workflowschemeiddefault-get
  description: Return the default workflow from the passed workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddefault-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddefault-get-openapi.md
- name: Jira Cloud REST API - Update default workflow
  x-api-slug: api2workflowschemeiddefault-put
  description: |-
    Set the default workflow for the passed workflow scheme.

    The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme cannot be edited.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddefault-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddefault-put-openapi.md
- name: Jira Cloud REST API - Delete default workflow
  x-api-slug: api2workflowschemeiddefault-delete
  description: Remove the default workflow from the passed workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddefault-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddefault-delete-openapi.md
- name: Jira Cloud REST API - Get workflow scheme draft
  x-api-slug: api2workflowschemeiddraft-get
  description: Returns the requested draft workflow scheme to the caller.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraft-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraft-get-openapi.md
- name: Jira Cloud REST API - Update workflow scheme draft
  x-api-slug: api2workflowschemeiddraft-put
  description: |-
    Update a draft workflow scheme. The draft will created if necessary.

    The body is a representation of the workflow scheme. Values not passed are assumed to indicate no change for that field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraft-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraft-put-openapi.md
- name: Jira Cloud REST API - Delete workflow scheme draft
  x-api-slug: api2workflowschemeiddraft-delete
  description: Delete the passed draft workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraft-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraft-delete-openapi.md
- name: Jira Cloud REST API - Get draft default workflow
  x-api-slug: api2workflowschemeiddraftdefault-get
  description: Return the default workflow from the passed draft workflow scheme to
    the caller.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftdefault-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftdefault-get-openapi.md
- name: Jira Cloud REST API - Update draft default workflow
  x-api-slug: api2workflowschemeiddraftdefault-put
  description: Set the default workflow for the passed draft workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftdefault-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftdefault-put-openapi.md
- name: Jira Cloud REST API - Delete draft default workflow
  x-api-slug: api2workflowschemeiddraftdefault-delete
  description: Remove the default workflow from the passed draft workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftdefault-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftdefault-delete-openapi.md
- name: Jira Cloud REST API - Get workflow scheme draft issue type
  x-api-slug: api2workflowschemeiddraftissuetypeissuetype-get
  description: Returns the issue type mapping for the passed draft workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftissuetypeissuetype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftissuetypeissuetype-get-openapi.md
- name: Jira Cloud REST API - Set workflow scheme draft issue type
  x-api-slug: api2workflowschemeiddraftissuetypeissuetype-put
  description: |-
    Set the issue type mapping for the passed draft scheme.

    The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme cannot be edited.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftissuetypeissuetype-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftissuetypeissuetype-put-openapi.md
- name: Jira Cloud REST API - Delete workflow scheme draft issue type
  x-api-slug: api2workflowschemeiddraftissuetypeissuetype-delete
  description: Remove the specified issue type mapping from the draft scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftissuetypeissuetype-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftissuetypeissuetype-delete-openapi.md
- name: Jira Cloud REST API - Get draft workflow
  x-api-slug: api2workflowschemeiddraftworkflow-get
  description: Returns the draft workflow mappings or requested mapping to the caller.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftworkflow-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftworkflow-get-openapi.md
- name: Jira Cloud REST API - Update draft workflow mapping
  x-api-slug: api2workflowschemeiddraftworkflow-put
  description: |-
    Update the draft scheme to include the passed mapping.

    The body is a representation of the workflow mapping. Values not passed are assumed to indicate no change for that field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftworkflow-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftworkflow-put-openapi.md
- name: Jira Cloud REST API - Delete draft workflow mapping
  x-api-slug: api2workflowschemeiddraftworkflow-delete
  description: Delete the passed workflow from the draft workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftworkflow-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeiddraftworkflow-delete-openapi.md
- name: Jira Cloud REST API - Get workflow scheme issue type
  x-api-slug: api2workflowschemeidissuetypeissuetype-get
  description: Returns the issue type mapping for the passed workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidissuetypeissuetype-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidissuetypeissuetype-get-openapi.md
- name: Jira Cloud REST API - Set workflow scheme issue type
  x-api-slug: api2workflowschemeidissuetypeissuetype-put
  description: |-
    Set the issue type mapping for the passed scheme.

    The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme cannot be edited.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidissuetypeissuetype-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidissuetypeissuetype-put-openapi.md
- name: Jira Cloud REST API - Delete workflow scheme issue type
  x-api-slug: api2workflowschemeidissuetypeissuetype-delete
  description: Remove the specified issue type mapping from the scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidissuetypeissuetype-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidissuetypeissuetype-delete-openapi.md
- name: Jira Cloud REST API - Get workflow
  x-api-slug: api2workflowschemeidworkflow-get
  description: Returns the workflow mappings or requested mapping to the caller for
    the passed scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidworkflow-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidworkflow-get-openapi.md
- name: Jira Cloud REST API - Update workflow mapping
  x-api-slug: api2workflowschemeidworkflow-put
  description: |-
    Update the scheme to include the passed mapping.

    The body is a representation of the workflow mapping. Values not passed are assumed to indicate no change for that field.

    The passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme cannot be edited.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidworkflow-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidworkflow-put-openapi.md
- name: Jira Cloud REST API - Delete workflow mapping
  x-api-slug: api2workflowschemeidworkflow-delete
  description: Delete the passed workflow from the workflow scheme.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidworkflow-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workflowschemeidworkflow-delete-openapi.md
- name: Jira Cloud REST API - Get IDs of deleted worklogs
  x-api-slug: api2worklogdeleted-get
  description: "Returns a list of IDs and delete timestamps for worklogs deleted after
    a date and time.  \n  \nThis resource is paginated, with a limit of 1000 worklogs
    per page. Each page lists worklogs from oldest to youngest. If the number of items
    in the date range exceeds 1000, `until` indicates the timestamp of the youngest
    item on the page. Also, `nextPage` provides the URL for the next page of worklogs.
    The `lastPage` parameter is set to true on the last page of worklogs.  \n  \nThis
    resource does not return worklogs deleted during the minute preceding the request.
    \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2worklogdeleted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2worklogdeleted-get-openapi.md
- name: Jira Cloud REST API - Get worklogs
  x-api-slug: api2workloglist-post
  description: "Returns worklog details for a list of worklog IDs.  \n  \nWorklogs
    can be set as viewable by:\n\n*   all users\n*   members of a project role or
    group\n\nFor a worklog to be returned, it must be set as _Viewable by All Users_
    or the calling user must be a member of the project role or group with permission
    to view the worklog.  \n  \nThe returned list of worklogs is limited to 1000 items.
    **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission
    to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workloglist-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2workloglist-post-openapi.md
- name: Jira Cloud REST API - Get IDs of updated worklogs
  x-api-slug: api2worklogupdated-get
  description: "Returns a list of IDs and update timestamps for worklogs updated after
    a date and time.  \n  \nThis resource is paginated, with a limit of 1000 worklogs
    per page. Each page lists worklogs from oldest to youngest. If the number of items
    in the date range exceeds 1000, `until` indicates the timestamp of the youngest
    item on the page. Also, `nextPage` provides the URL for the next page of worklogs.
    The `lastPage` parameter is set to true on the last page of worklogs.  \n  \nThis
    resource does not return worklogs updated during the minute preceding the request.
    \ \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
    Permission to access Jira."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2worklogupdated-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/api2worklogupdated-get-openapi.md
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auth1session-get-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Stride API - Get list of sites
  x-api-slug: site-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/site-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/site-get-openapi.md
- name: Stride API - Get a list of conversations
  x-api-slug: sitecloudidconversation-get
  description: The API returns the list of conversations the app has access to Authentication
    required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-get-openapi.md
- name: Stride API - Create conversation
  x-api-slug: sitecloudidconversation-post
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-post-openapi.md
- name: Stride API - Get a direct conversation of a user
  x-api-slug: sitecloudidconversationuseruserid-get
  description: Get a direct conversation of a user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruserid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruserid-get-openapi.md
- name: Stride API - Send message to a user
  x-api-slug: sitecloudidconversationuseruseridmessage-post
  description: Send message to a user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessage-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessage-post-openapi.md
- name: Stride API - Edit a message in a direct conversation
  x-api-slug: sitecloudidconversationuseruseridmessagemessageid-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-put-openapi.md
- name: Stride API - Delete a message in a direct conversation
  x-api-slug: sitecloudidconversationuseruseridmessagemessageid-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-delete-openapi.md
- name: Stride API - Get conversation details
  x-api-slug: sitecloudidconversationconversationid-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-get-openapi.md
- name: Stride API - Update conversation
  x-api-slug: sitecloudidconversationconversationid-patch
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-patch-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-patch-openapi.md
- name: Stride API - Get a list of chat:actionTarget modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatactiontarget-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontarget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontarget-get-openapi.md
- name: Stride API - Create or update a chat:actionTarget module
  x-api-slug: sitecloudidconversationconversationidappmodulechatactiontargetkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-put-openapi.md
- name: Stride API - Delete a chat:actionTarget module
  x-api-slug: sitecloudidconversationconversationidappmodulechatactiontargetkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-delete-openapi.md
- name: Stride API - Get a list of chat:bot modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatbot-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbot-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbot-get-openapi.md
- name: Stride API - Create or update a chat:bot module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-put-openapi.md
- name: Stride API - Delete a chat:bot module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-delete-openapi.md
- name: Stride API - Get a list of chat:bot:messages modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotmessages-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessages-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessages-get-openapi.md
- name: Stride API - Create or update a chat:bot:messages module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotmessageskey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-put-openapi.md
- name: Stride API - Delete a chat:bot:messages module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotmessageskey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-delete-openapi.md
- name: Stride API - Update the chat:configuration state
  x-api-slug: sitecloudidconversationconversationidappmodulechatconfigurationkeystate-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatconfigurationkeystate-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatconfigurationkeystate-put-openapi.md
- name: Stride API - Get a list of chat:dialog modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatdialog-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialog-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialog-get-openapi.md
- name: Stride API - Create or update a chat:dialog module
  x-api-slug: sitecloudidconversationconversationidappmodulechatdialogkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-put-openapi.md
- name: Stride API - Delete a chat:dialog module
  x-api-slug: sitecloudidconversationconversationidappmodulechatdialogkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-delete-openapi.md
- name: Stride API - Get a list of chat:externalPage modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatexternalpage-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpage-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpage-get-openapi.md
- name: Stride API - Create or update a chat:externalPage module
  x-api-slug: sitecloudidconversationconversationidappmodulechatexternalpagekey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-put-openapi.md
- name: Stride API - Delete a chat:externalPage module
  x-api-slug: sitecloudidconversationconversationidappmodulechatexternalpagekey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-delete-openapi.md
- name: Stride API - Get a list of chat:glance modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatglance-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglance-get-openapi.md
- name: Stride API - Create or update a chat:glance module
  x-api-slug: sitecloudidconversationconversationidappmodulechatglancekey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-put-openapi.md
- name: Stride API - Delete a chat:glance module
  x-api-slug: sitecloudidconversationconversationidappmodulechatglancekey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-delete-openapi.md
- name: Stride API - Update the chat:glance state
  x-api-slug: sitecloudidconversationconversationidappmodulechatglancekeystate-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekeystate-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekeystate-put-openapi.md
- name: Stride API - Get a list of chat:sidebar modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatsidebar-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebar-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebar-get-openapi.md
- name: Stride API - Create or update a chat:sidebar module
  x-api-slug: sitecloudidconversationconversationidappmodulechatsidebarkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-put-openapi.md
- name: Stride API - Delete a chat:sidebar module
  x-api-slug: sitecloudidconversationconversationidappmodulechatsidebarkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-delete-openapi.md
- name: Stride API - Get a list of chat:webhook modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatwebhook-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhook-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhook-get-openapi.md
- name: Stride API - Create or update a chat:webhook module
  x-api-slug: sitecloudidconversationconversationidappmodulechatwebhookkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-put-openapi.md
- name: Stride API - Delete a chat:webhook module
  x-api-slug: sitecloudidconversationconversationidappmodulechatwebhookkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-delete-openapi.md
- name: Stride API - Archive conversation
  x-api-slug: sitecloudidconversationconversationidarchive-put
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidarchive-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidarchive-put-openapi.md
- name: Stride API - Upload a file
  x-api-slug: sitecloudidconversationconversationidmedia-post
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmedia-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmedia-post-openapi.md
- name: Stride API - Get a file
  x-api-slug: sitecloudidconversationconversationidmediamediaid-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-get-openapi.md
- name: Stride API - Delete a file
  x-api-slug: sitecloudidconversationconversationidmediamediaid-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-delete-openapi.md
- name: Stride API - Get conversation history
  x-api-slug: sitecloudidconversationconversationidmessage-get
  description: "Authentication required, with scope participate:conversation This
    method returns messages after/before a given messageIDs or/and timestamps. If
    these parameters are omitted the method returns conversation\u2019s latest messages.
    Max number of messages returned is 75."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-get-openapi.md
- name: Stride API - Send a message to a conversation
  x-api-slug: sitecloudidconversationconversationidmessage-post
  description: Send a message to a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-post-openapi.md
- name: Stride API - Get latest messages for conversation
  x-api-slug: sitecloudidconversationconversationidmessagerecent-get
  description: Authentication required, with scope participate:conversation Max number
    of messages returned is 75.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagerecent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagerecent-get-openapi.md
- name: Stride API - Get Message by id
  x-api-slug: sitecloudidconversationconversationidmessagemessageid-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-get-openapi.md
- name: Stride API - Edit a message in a conversation
  x-api-slug: sitecloudidconversationconversationidmessagemessageid-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-put-openapi.md
- name: Stride API - Delete a message in a conversation
  x-api-slug: sitecloudidconversationconversationidmessagemessageid-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-delete-openapi.md
- name: Stride API - Get conversation history contextually
  x-api-slug: sitecloudidconversationconversationidmessagemessageidcontext-get
  description: Authentication required, with scope participate:conversation This method
    returns messages after and/or before a given messageID including the message itself.
    Default value for 'after' and 'before' query parameters is 0. Max number of messages
    returned is 75.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageidcontext-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageidcontext-get-openapi.md
- name: Stride API - Get conversation roster
  x-api-slug: sitecloudidconversationconversationidroster-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-get-openapi.md
- name: Stride API - Update a conversation roster
  x-api-slug: sitecloudidconversationconversationidroster-patch
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-patch-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-patch-openapi.md
- name: Stride API - Unarchive conversation
  x-api-slug: sitecloudidconversationconversationidunarchive-put
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidunarchive-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidunarchive-put-openapi.md
- name: Stride API - Get list of sites
  x-api-slug: site-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/site-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/site-get-openapi.md
- name: Stride API - Get a list of conversations
  x-api-slug: sitecloudidconversation-get
  description: The API returns the list of conversations the app has access to Authentication
    required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-get-openapi.md
- name: Stride API - Create conversation
  x-api-slug: sitecloudidconversation-post
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversation-post-openapi.md
- name: Stride API - Get a direct conversation of a user
  x-api-slug: sitecloudidconversationuseruserid-get
  description: Get a direct conversation of a user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruserid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruserid-get-openapi.md
- name: Stride API - Send message to a user
  x-api-slug: sitecloudidconversationuseruseridmessage-post
  description: Send message to a user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessage-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessage-post-openapi.md
- name: Stride API - Edit a message in a direct conversation
  x-api-slug: sitecloudidconversationuseruseridmessagemessageid-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-put-openapi.md
- name: Stride API - Delete a message in a direct conversation
  x-api-slug: sitecloudidconversationuseruseridmessagemessageid-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationuseruseridmessagemessageid-delete-openapi.md
- name: Stride API - Get conversation details
  x-api-slug: sitecloudidconversationconversationid-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-get-openapi.md
- name: Stride API - Update conversation
  x-api-slug: sitecloudidconversationconversationid-patch
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-patch-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationid-patch-openapi.md
- name: Stride API - Get a list of chat:actionTarget modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatactiontarget-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontarget-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontarget-get-openapi.md
- name: Stride API - Create or update a chat:actionTarget module
  x-api-slug: sitecloudidconversationconversationidappmodulechatactiontargetkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-put-openapi.md
- name: Stride API - Delete a chat:actionTarget module
  x-api-slug: sitecloudidconversationconversationidappmodulechatactiontargetkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatactiontargetkey-delete-openapi.md
- name: Stride API - Get a list of chat:bot modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatbot-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbot-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbot-get-openapi.md
- name: Stride API - Create or update a chat:bot module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-put-openapi.md
- name: Stride API - Delete a chat:bot module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotkey-delete-openapi.md
- name: Stride API - Get a list of chat:bot:messages modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotmessages-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessages-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessages-get-openapi.md
- name: Stride API - Create or update a chat:bot:messages module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotmessageskey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-put-openapi.md
- name: Stride API - Delete a chat:bot:messages module
  x-api-slug: sitecloudidconversationconversationidappmodulechatbotmessageskey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatbotmessageskey-delete-openapi.md
- name: Stride API - Update the chat:configuration state
  x-api-slug: sitecloudidconversationconversationidappmodulechatconfigurationkeystate-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatconfigurationkeystate-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatconfigurationkeystate-put-openapi.md
- name: Stride API - Get a list of chat:dialog modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatdialog-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialog-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialog-get-openapi.md
- name: Stride API - Create or update a chat:dialog module
  x-api-slug: sitecloudidconversationconversationidappmodulechatdialogkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-put-openapi.md
- name: Stride API - Delete a chat:dialog module
  x-api-slug: sitecloudidconversationconversationidappmodulechatdialogkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatdialogkey-delete-openapi.md
- name: Stride API - Get a list of chat:externalPage modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatexternalpage-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpage-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpage-get-openapi.md
- name: Stride API - Create or update a chat:externalPage module
  x-api-slug: sitecloudidconversationconversationidappmodulechatexternalpagekey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-put-openapi.md
- name: Stride API - Delete a chat:externalPage module
  x-api-slug: sitecloudidconversationconversationidappmodulechatexternalpagekey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatexternalpagekey-delete-openapi.md
- name: Stride API - Get a list of chat:glance modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatglance-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglance-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglance-get-openapi.md
- name: Stride API - Create or update a chat:glance module
  x-api-slug: sitecloudidconversationconversationidappmodulechatglancekey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-put-openapi.md
- name: Stride API - Delete a chat:glance module
  x-api-slug: sitecloudidconversationconversationidappmodulechatglancekey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekey-delete-openapi.md
- name: Stride API - Update the chat:glance state
  x-api-slug: sitecloudidconversationconversationidappmodulechatglancekeystate-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekeystate-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatglancekeystate-put-openapi.md
- name: Stride API - Get a list of chat:sidebar modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatsidebar-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebar-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebar-get-openapi.md
- name: Stride API - Create or update a chat:sidebar module
  x-api-slug: sitecloudidconversationconversationidappmodulechatsidebarkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-put-openapi.md
- name: Stride API - Delete a chat:sidebar module
  x-api-slug: sitecloudidconversationconversationidappmodulechatsidebarkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatsidebarkey-delete-openapi.md
- name: Stride API - Get a list of chat:webhook modules
  x-api-slug: sitecloudidconversationconversationidappmodulechatwebhook-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhook-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhook-get-openapi.md
- name: Stride API - Create or update a chat:webhook module
  x-api-slug: sitecloudidconversationconversationidappmodulechatwebhookkey-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-put-openapi.md
- name: Stride API - Delete a chat:webhook module
  x-api-slug: sitecloudidconversationconversationidappmodulechatwebhookkey-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidappmodulechatwebhookkey-delete-openapi.md
- name: Stride API - Archive conversation
  x-api-slug: sitecloudidconversationconversationidarchive-put
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidarchive-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidarchive-put-openapi.md
- name: Stride API - Upload a file
  x-api-slug: sitecloudidconversationconversationidmedia-post
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmedia-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmedia-post-openapi.md
- name: Stride API - Get a file
  x-api-slug: sitecloudidconversationconversationidmediamediaid-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-get-openapi.md
- name: Stride API - Delete a file
  x-api-slug: sitecloudidconversationconversationidmediamediaid-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmediamediaid-delete-openapi.md
- name: Stride API - Get conversation history
  x-api-slug: sitecloudidconversationconversationidmessage-get
  description: "Authentication required, with scope participate:conversation This
    method returns messages after/before a given messageIDs or/and timestamps. If
    these parameters are omitted the method returns conversation\u2019s latest messages.
    Max number of messages returned is 75."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-get-openapi.md
- name: Stride API - Send a message to a conversation
  x-api-slug: sitecloudidconversationconversationidmessage-post
  description: Send a message to a conversation.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessage-post-openapi.md
- name: Stride API - Get latest messages for conversation
  x-api-slug: sitecloudidconversationconversationidmessagerecent-get
  description: Authentication required, with scope participate:conversation Max number
    of messages returned is 75.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagerecent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagerecent-get-openapi.md
- name: Stride API - Get Message by id
  x-api-slug: sitecloudidconversationconversationidmessagemessageid-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-get-openapi.md
- name: Stride API - Edit a message in a conversation
  x-api-slug: sitecloudidconversationconversationidmessagemessageid-put
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-put-openapi.md
- name: Stride API - Delete a message in a conversation
  x-api-slug: sitecloudidconversationconversationidmessagemessageid-delete
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageid-delete-openapi.md
- name: Stride API - Get conversation history contextually
  x-api-slug: sitecloudidconversationconversationidmessagemessageidcontext-get
  description: Authentication required, with scope participate:conversation This method
    returns messages after and/or before a given messageID including the message itself.
    Default value for 'after' and 'before' query parameters is 0. Max number of messages
    returned is 75.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageidcontext-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidmessagemessageidcontext-get-openapi.md
- name: Stride API - Get conversation roster
  x-api-slug: sitecloudidconversationconversationidroster-get
  description: Authentication required, with scope participate:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-get-openapi.md
- name: Stride API - Update a conversation roster
  x-api-slug: sitecloudidconversationconversationidroster-patch
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-patch-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidroster-patch-openapi.md
- name: Stride API - Unarchive conversation
  x-api-slug: sitecloudidconversationconversationidunarchive-put
  description: Authentication required, with scope manage:conversation
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidunarchive-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/atlassian/master/_listings/atlassian/sitecloudidconversationconversationidunarchive-put-openapi.md
x-common:
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/platform/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/confluence/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/software/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/service-desk/swagger.v3.json
- type: x-website
  url: http://atlassian.com/
- type: x-website
  url: http://www.atlassian.com
- type: x-api-gallery
  url: http://att.dev.program.api.gallery.streamdata.io
- type: x-api-stack
  url: http://atlassian.stack.network
- type: x-blog
  url: http://blogs.atlassian.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/atlassian
- type: x-crunchbase
  url: http://www.crunchbase.com/company/atlassian
- type: x-email
  url: copyright@atlassian.com
- type: x-email
  url: trademarks@atlassian.com
- type: x-email
  url: sales@atlassian.com
- type: x-email
  url: ar_enterprise@atlassian.com
- type: x-email
  url: privacy@atlassian.com
- type: x-email
  url: eudatarep@atlassian.com
- type: x-email
  url: experts@atlassian.com
- type: x-email
  url: remittance@atlassian.com
- type: x-email
  url: ap@atlassian.com
- type: x-email
  url: procurement@atlassian.com
- type: x-github
  url: https://github.com/atlassian
- type: x-privacy-policy
  url: https://www.atlassian.com/legal/privacy-policy?_ga=2.188884514.868776184.1519225620-845241124.1519225620
- type: x-twitter
  url: https://twitter.com/atlassian
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---