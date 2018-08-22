---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get global attachment settings
  description: "Returns the global attachment settings, that is, whether attachments
    are enabled and the maximum attachment size allowed.  \n  \nNote that there are
    also [project permissions](https://confluence.atlassian.com/x/yodKLg) that restrict
    whether users can create and delete attachments or not.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None."
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