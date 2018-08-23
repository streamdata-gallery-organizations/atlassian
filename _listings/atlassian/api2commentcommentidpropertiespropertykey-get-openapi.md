---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get comment property
  description: Returns the value of the property with a given key from the comment
    identified by the key or by the id. The user who retrieves the property is required
    to have permissions to read the comment.
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