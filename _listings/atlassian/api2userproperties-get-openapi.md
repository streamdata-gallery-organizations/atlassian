---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get user property keys
  description: |-
    Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

    *   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
    *   To access the calling user's property keys: None

    Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
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
    post:
      summary: Create permission grant
      description: Creates a new permission grant in the given permission scheme.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.createPermissionGrant_pos
      x-api-path-slug: api2permissionschemeschemeidpermission-post
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: schemeId
        description: The ID of the permission scheme in which to create a new permission
          grant
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Grant
  /api/2/permissionscheme/{schemeId}/permission/{permissionId}:
    get:
      summary: Get permission scheme grant
      description: Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to log in to Jira.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrant_
      x-api-path-slug: api2permissionschemeschemeidpermissionpermissionid-get
      parameters:
      - in: query
        name: expand
        description: Use expand to include additional information in the response
      - in: path
        name: permissionId
        description: The ID of the permission grant (e
      - in: path
        name: schemeId
        description: The ID of the permission scheme (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Grant
    delete:
      summary: Delete permission scheme entity
      description: Deletes a permission grant from a permission scheme. See [About
        permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes)
        for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionSchemeEnt
      x-api-path-slug: api2permissionschemeschemeidpermissionpermissionid-delete
      parameters:
      - in: path
        name: permissionId
        description: The ID of the permission grant to delete (e
      - in: path
        name: schemeId
        description: The ID of the permission scheme to delete the permission grant
          from (e
      responses:
        200:
          description: OK
      tags:
      - Permission
      - Scheme
      - Entity
  /api/2/priority:
    get:
      summary: Get priorities
      description: Returns a list of all issue priorities.
      operationId: com.atlassian.jira.rest.v2.issue.PriorityResource.getPriorities_get
      x-api-path-slug: api2priority-get
      responses:
        200:
          description: OK
      tags:
      - Priorities
  /api/2/priority/{id}:
    get:
      summary: Get priority
      description: Returns an issue priority.
      operationId: com.atlassian.jira.rest.v2.issue.PriorityResource.getPriority_get
      x-api-path-slug: api2priorityid-get
      parameters:
      - in: path
        name: id
        description: a String containing the priority id
      responses:
        200:
          description: OK
      tags:
      - Priority
  /api/2/project:
    get:
      summary: Get all projects
      description: |-
        Returns all projects visible to the currently logged in user. For projects to be visible, the authenticated user must be granted either _Browse projects_ or _Administer projects_ permissions. If no user is logged in, it returns all projects that are visible for anonymous users.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getAllProjects_get
      x-api-path-slug: api2project-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: recent
        description: Returns the most recently accessed projects for the current user
      responses:
        200:
          description: OK
      tags:
      - Projects
    post:
      summary: Create project
      description: |-
        Creates a new project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.createProject_post
      x-api-path-slug: api2project-post
      parameters:
      - in: header
        name: force-account-id
      responses:
        200:
          description: OK
      tags:
      - Project
  /api/2/project/search:
    get:
      summary: search
      description: Returns all projects visible to the currently logged in user, i.e.
        all projects the user has permission defined by the {@code action} parameter.
        If no user is logged in, all projects visible to anonymous users are returned.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.searchProjects_get
      x-api-path-slug: api2projectsearch-get
      parameters:
      - in: query
        name: action
        description: Type of the project action
      - in: query
        name: categoryId
        description: Project category filter
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: maxResults
        description: Maximum number of items to return per page
      - in: query
        name: orderBy
        description: Ordering of the results by a given field from the following:*   `name`*   `key`*   `type`*   `category`*   `owner`Prefix
          it with + for ascending and - for descending order
      - in: query
        name: query
        description: A string used to filter the results; only projects with key or
          name containing the string will be returned (case insensitive)
      - in: query
        name: startAt
        description: Page offset, i
      - in: query
        name: typeKey
        description: Projects type key filter
      responses:
        200:
          description: OK
      tags:
      - Search
  /api/2/project/type:
    get:
      summary: Get all project types
      description: |-
        Returns all [project types](https://confluence.atlassian.com/x/Var1Nw), whether or not the instance has a valid license for each type.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getAllProjectTypes_get
      x-api-path-slug: api2projecttype-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Types
  /api/2/project/type/{projectTypeKey}:
    get:
      summary: Get project type by key
      description: |-
        Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getProjectTypeByKey_get
      x-api-path-slug: api2projecttypeprojecttypekey-get
      parameters:
      - in: path
        name: projectTypeKey
        description: The key of the project type
      responses:
        200:
          description: OK
      tags:
      - Project
      - Type
      - By
      - Key
  /api/2/project/type/{projectTypeKey}/accessible:
    get:
      summary: Get accessible project type by key
      description: |-
        Returns a [project type](https://confluence.atlassian.com/x/Var1Nw) if it is accessible to the logged in user.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)).
      operationId: com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getAccessibleProjectTypeByKey_get
      x-api-path-slug: api2projecttypeprojecttypekeyaccessible-get
      parameters:
      - in: path
        name: projectTypeKey
        description: The key of the project type
      responses:
        200:
          description: OK
      tags:
      - Accessible
      - Project
      - Type
      - By
      - Key
  /api/2/project/{projectIdOrKey}:
    get:
      summary: Get project
      description: |-
        Returns the [project details](https://confluence.atlassian.com/x/ahLpNw) for the specified project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProject_get
      x-api-path-slug: api2projectprojectidorkey-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
    put:
      summary: Update project
      description: |-
        Updates the [project details](https://confluence.atlassian.com/x/ahLpNw) of an existing project.

        All parameters are optional in the body of the request.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.updateProject_put
      x-api-path-slug: api2projectprojectidorkey-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: header
        name: force-account-id
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
    delete:
      summary: Delete project
      description: |-
        Deletes an existing project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.deleteProject_delete
      x-api-path-slug: api2projectprojectidorkey-delete
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
  /api/2/project/{projectIdOrKey}/avatar:
    put:
      summary: Update project avatar
      description: ""
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.updateProjectAvatar_put
      x-api-path-slug: api2projectprojectidorkeyavatar-put
      parameters:
      - in: path
        name: projectIdOrKey
      responses:
        200:
          description: OK
      tags:
      - Project
      - Avatar
  /api/2/project/{projectIdOrKey}/avatar/{id}:
    delete:
      summary: Delete project avatar
      description: Deletes an avatar of a single project. It is only possible to delete
        custom avatars.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.deleteProjectAvatar_delete
      x-api-path-slug: api2projectprojectidorkeyavatarid-delete
      parameters:
      - in: path
        name: id
        description: ID of the avatar
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Avatar
  /api/2/project/{projectIdOrKey}/avatar2:
    post:
      summary: Create project avatar
      description: Creates an avatar for a single project. Use it to upload an image
        to be be set as a project's avatar. The uploaded image will be cropped according
        to the crop parameters defined in the request. If no crop parameters are specified,
        the image will be cropped to a square. The square will originate at the top
        left of the image and the length of each side will be set to the smaller of
        the height or width of the image.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.createProjectAvatar_post
      x-api-path-slug: api2projectprojectidorkeyavatar2-post
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: query
        name: size
        description: (optional) Length of each side of the crop region
      - in: query
        name: x
        description: (optional) X coordinate of the top-left corner of the crop region
      - in: query
        name: "y"
        description: (optional) Y coordinate of the top-left corner of the crop region
      responses:
        200:
          description: OK
      tags:
      - Project
      - Avatar
  /api/2/project/{projectIdOrKey}/avatars:
    get:
      summary: Get all project avatars
      description: Returns all project avatars visible for the currently logged in
        user. The avatars are grouped into system avatars and custom avatars.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getAllProjectAvatars_get
      x-api-path-slug: api2projectprojectidorkeyavatars-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Avatars
  /api/2/project/{projectIdOrKey}/component:
    get:
      summary: Get project components paginated
      description: |-
        Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all components existing in a single project. See the [Get project components](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-components-get) resource if you want to get a full list of versions without pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectComponentsPaginated_get
      x-api-path-slug: api2projectprojectidorkeycomponent-get
      parameters:
      - in: query
        name: maxResults
        description: The maximum number of components to return per page
      - in: query
        name: orderBy
        description: '[Order](https://developer'
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: query
        name: query
        description: Filter the results using a literal string
      - in: query
        name: startAt
        description: The starting index of the returned list of components
      responses:
        200:
          description: OK
      tags:
      - Project
      - Components
      - Paginated
  /api/2/project/{projectIdOrKey}/components:
    get:
      summary: Get project components
      description: |-
        Returns all components existing in a single project. See the [Get project components paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-component-get) resource if you want to get a full list of components with pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectComponents_get
      x-api-path-slug: api2projectprojectidorkeycomponents-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Components
  /api/2/project/{projectIdOrKey}/properties:
    get:
      summary: Get project property keys
      description: |-
        Returns all [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys for the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.getProjectPropertyKeys_get
      x-api-path-slug: api2projectprojectidorkeyproperties-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Property
      - Keys
  /api/2/project/{projectIdOrKey}/properties/{propertyKey}:
    get:
      summary: Get project property
      description: |-
        Returns the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.getProjectProperty_get
      x-api-path-slug: api2projectprojectidorkeypropertiespropertykey-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: path
        name: propertyKey
        description: The project property key
      responses:
        200:
          description: OK
      tags:
      - Project
      - Property
    put:
      summary: Set project property
      description: |-
        Sets the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). You can use project properties to store custom data against the project.

        The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 bytes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.setProjectProperty_put
      x-api-path-slug: api2projectprojectidorkeypropertiespropertykey-put
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: path
        name: propertyKey
        description: The key of the project property
      responses:
        200:
          description: OK
      tags:
      - Set
      - Project
      - Property
    delete:
      summary: Delete project property
      description: |-
        Removes the [property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) from the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.deleteProjectProperty_delete
      x-api-path-slug: api2projectprojectidorkeypropertiespropertykey-delete
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: path
        name: propertyKey
        description: The project property key
      responses:
        200:
          description: OK
      tags:
      - Project
      - Property
  /api/2/project/{projectIdOrKey}/role:
    get:
      summary: Get project roles for project
      description: |-
        Returns a list of [project roles](https://confluence.atlassian.com/x/3odKLg) for the project.

        Note that all project roles are shared with all projects in Jira Cloud. See the [Get all project roles](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-get) resource for more information.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.getProjectRoles_get
      x-api-path-slug: api2projectprojectidorkeyrole-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Rolesproject
  /api/2/project/{projectIdOrKey}/role/{id}:
    get:
      summary: Get project role for project
      description: |-
        Returns the project role's details and actors associated with the project. The list of actors is sorted by display name.

        If you would like to check to see whether a user belongs to a role based on their group memberships, use the [Get user](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-get) resource with the `groups` expand parameter selected. Then check whether the user keys and groups match with the actors returned for the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.getProjectRole_get
      x-api-path-slug: api2projectprojectidorkeyroleid-get
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Roleproject
    post:
      summary: Add actors to project role
      description: |-
        Adds additional actors to a project role for the project.

        If you want to replace all actors for the project, then use [Set actors for project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-put).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.addActorUsers_post
      x-api-path-slug: api2projectprojectidorkeyroleid-post
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Actors
      - To
      - Project
      - Role
    put:
      summary: Set actors for project role
      description: |-
        Associates actors with the project role for the project, replacing all existing actors.

        If you want to add actors to the project without overwriting the existing list, then use [Add actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-post).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.setActors_put
      x-api-path-slug: api2projectprojectidorkeyroleid-put
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Set
      - Actorsproject
      - Role
    delete:
      summary: Delete actors from project role
      description: |-
        Deletes actors from a project role for the project.

        If you want to remove default actors from the project role, see the [Delete default actors from project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-delete) resource.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.deleteActor_delete
      x-api-path-slug: api2projectprojectidorkeyroleid-delete
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: group
        description: The name of the group to remove from the project role
      - in: path
        name: id
        description: The ID of the project role
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: query
        name: user
        description: The user account ID of the user to remove from the project role
      responses:
        200:
          description: OK
      tags:
      - Actors
      - From
      - Project
      - Role
  /api/2/project/{projectIdOrKey}/roledetails:
    get:
      summary: Get project role details
      description: Returns all [project roles](https://confluence.atlassian.com/x/3odKLg)
        and the details for each role. Note that the list of project roles is common
        to all projects.
      operationId: com.atlassian.jira.rest.v2.issue.project.ProjectRoleDetailsResource.getProjectRoleDetails_get
      x-api-path-slug: api2projectprojectidorkeyroledetails-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
      - Details
  /api/2/project/{projectIdOrKey}/statuses:
    get:
      summary: Get all statuses
      description: |-
        Returns the valid statuses for a project. The statuses are grouped by issue type, as each project has a set of valid issue types and each issue type has a set of valid statuses.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getAllStatuses_get
      x-api-path-slug: api2projectprojectidorkeystatuses-get
      parameters:
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Statuses
  /api/2/project/{projectIdOrKey}/type/{newProjectTypeKey}:
    put:
      summary: Update project type
      description: |-
        Updates the [project type](https://confluence.atlassian.com/x/GwiiLQ).

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.updateProjectType_put
      x-api-path-slug: api2projectprojectidorkeytypenewprojecttypekey-put
      parameters:
      - in: path
        name: newProjectTypeKey
        description: The key of the new project type
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Type
  /api/2/project/{projectIdOrKey}/version:
    get:
      summary: Get project versions paginated
      description: |-
        Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all versions existing in a single project. See the [Get project versions](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-versions-get) resource if you want to get a full list of versions without pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectVersionsPaginated_get
      x-api-path-slug: api2projectprojectidorkeyversion-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: maxResults
        description: The maximum number of versions to return per page
      - in: query
        name: orderBy
        description: '[Order](https://developer'
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      - in: query
        name: query
        description: Filter the results using a literal string
      - in: query
        name: startAt
        description: The starting index of the returned list of versions (page offset)
      - in: query
        name: status
        description: A comma separated string used to filter the results by version
          status
      responses:
        200:
          description: OK
      tags:
      - Project
      - Versions
      - Paginated
  /api/2/project/{projectIdOrKey}/versions:
    get:
      summary: Get project versions
      description: |-
        Returns all versions existing in a single project. The response is not paginated. Use [Get project versions paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-version-get) if you want to get the versions in a project with pagination.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectVersions_get
      x-api-path-slug: api2projectprojectidorkeyversions-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectIdOrKey
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Versions
  /api/2/project/{projectKeyOrId}/issuesecuritylevelscheme:
    get:
      summary: Get project issue security scheme
      description: |-
        Returns the [issue security scheme](https://confluence.atlassian.com/x/J4lKLg) associated with the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or the _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ProjectIssueSecurityLevelSchemeResource.getIssueSecurityScheme_get
      x-api-path-slug: api2projectprojectkeyoridissuesecuritylevelscheme-get
      parameters:
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Issue
      - Security
      - Scheme
  /api/2/project/{projectKeyOrId}/notificationscheme:
    get:
      summary: Get project notification scheme
      description: |-
        Gets a [notification scheme](https://confluence.atlassian.com/x/8YdKLg) associated with the project. See the [Get notification scheme](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-id-get) resource for more information about notification schemes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.notification.ProjectNotificationSchemeResource.getNotificationScheme_get
      x-api-path-slug: api2projectprojectkeyoridnotificationscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Notification
      - Scheme
  /api/2/project/{projectKeyOrId}/permissionscheme:
    get:
      summary: Get assigned permission scheme
      description: |-
        Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.getAssignedPermissionScheme_ge
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assigned
      - Permission
      - Scheme
    put:
      summary: Assign permission scheme
      description: |-
        Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)
      operationId: com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.assignPermissionScheme_put
      x-api-path-slug: api2projectprojectkeyoridpermissionscheme-put
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Permission
      - Scheme
  /api/2/project/{projectKeyOrId}/securitylevel:
    get:
      summary: Get project issue security levels
      description: |-
        Returns all [issue security](https://confluence.atlassian.com/x/J4lKLg) levels for the project that the currently authenticated user has access to. If the user does not have permission to see an issue security level, then that level is not returned. If the user lacks the _Set Issue Security_ permission, then an empty list is returned.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Set Issue Security_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.securitylevel.ProjectSecurityLevelResource.getSecurityLevelsForProject_ge
      x-api-path-slug: api2projectprojectkeyoridsecuritylevel-get
      parameters:
      - in: path
        name: projectKeyOrId
        description: The project ID or project key (case sensitive)
      responses:
        200:
          description: OK
      tags:
      - Project
      - Issue
      - Security
      - Levels
  /api/2/projectCategory:
    get:
      summary: Get all project categories
      description: Returns all project categories
      operationId: com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.getAllProjectCategories_get
      x-api-path-slug: api2projectcategory-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Categories
    post:
      summary: Create project category
      description: Create a project category via POST.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.createProjectCategory_post
      x-api-path-slug: api2projectcategory-post
      responses:
        200:
          description: OK
      tags:
      - Project
      - Category
  /api/2/projectCategory/{id}:
    get:
      summary: Get project category by id
      description: Contains a representation of a project category in JSON format.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.getProjectCategoryById_get
      x-api-path-slug: api2projectcategoryid-get
      parameters:
      - in: path
        name: id
        description: project category id
      responses:
        200:
          description: OK
      tags:
      - Project
      - Category
      - By
      - Id
    put:
      summary: Update project category
      description: Modify a project category via PUT. Any fields present in the PUT
        will override existing values. As a convenience, if a field is not present,
        it is silently ignored.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.updateProjectCategory_put
      x-api-path-slug: api2projectcategoryid-put
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Project
      - Category
    delete:
      summary: Remove project category
      description: Delete a project category.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.removeProjectCategory_delete
      x-api-path-slug: api2projectcategoryid-delete
      parameters:
      - in: path
        name: id
        description: Id of the project category to delete
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Project
      - Category
  /api/2/projectvalidate/key:
    get:
      summary: Validate project key
      description: Validates a project key.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectValidateResource.validateProjectKey_get
      x-api-path-slug: api2projectvalidatekey-get
      parameters:
      - in: query
        name: key
        description: the project key
      responses:
        200:
          description: OK
      tags:
      - Validate
      - Project
      - Key
  /api/2/projectvalidate/validProjectKey:
    get:
      summary: Get valid project key
      description: Validates the project key and generated a valid project key if
        the supplied key is invalid.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectValidateResource.getValidProjectKey_get
      x-api-path-slug: api2projectvalidatevalidprojectkey-get
      parameters:
      - in: query
        name: key
        description: the project key
      responses:
        200:
          description: OK
      tags:
      - Valid
      - Project
      - Key
  /api/2/projectvalidate/validProjectName:
    get:
      summary: Get valid project name
      description: Validates a project name. If the name is invalid, an attempt is
        made to produce a valid name based on the supplied one. If no such valid name
        can be found, an empty string is returned.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectValidateResource.getValidProjectName_get
      x-api-path-slug: api2projectvalidatevalidprojectname-get
      parameters:
      - in: query
        name: name
        description: the project name
      responses:
        200:
          description: OK
      tags:
      - Valid
      - Project
      - Name
  /api/2/resolution:
    get:
      summary: Get resolutions
      description: Returns a list of all resolutions.
      operationId: com.atlassian.jira.rest.v2.issue.ResolutionResource.getResolutions_get
      x-api-path-slug: api2resolution-get
      responses:
        200:
          description: OK
      tags:
      - Resolutions
  /api/2/resolution/{id}:
    get:
      summary: Get resolution
      description: Returns a resolution.
      operationId: com.atlassian.jira.rest.v2.issue.ResolutionResource.getResolution_get
      x-api-path-slug: api2resolutionid-get
      parameters:
      - in: path
        name: id
        description: a String containing the resolution id
      responses:
        200:
          description: OK
      tags:
      - Resolution
  /api/2/role:
    get:
      summary: Get all project roles
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
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.getAllProjectRoles_get
      x-api-path-slug: api2role-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Roles
    post:
      summary: Create project role
      description: |-
        Creates a new project role with no [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get). You can use the [Add default actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-post) the project method to add default actors to the project role after creating it.

        _Note that although a new project role is available to all projects upon creation, any default actors that are associated with the project role are not added to projects that existed prior to the role being created._<

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.createProjectRole_post
      x-api-path-slug: api2role-post
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
  /api/2/role/{id}:
    get:
      summary: Get project role by ID
      description: |-
        Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.getProjectRoleById_get
      x-api-path-slug: api2roleid-get
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
      - By
      - ID
    post:
      summary: Partial update project role
      description: |-
        Update either the project role's name or its description.

        You cannot update both the name and description at the same time using this method. If you send a request with both a name and a description, then only the name will be updated, regardless of the order of appearance in the body of the request.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.partialUpdateProjectRole_post
      x-api-path-slug: api2roleid-post
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Partial
      - Update
      - Project
      - Role
    put:
      summary: Fully update project role
      description: |-
        Update the project role's name and description. You must include both a name and a description in the request.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.fullyUpdateProjectRole_put
      x-api-path-slug: api2roleid-put
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Fully
      - Update
      - Project
      - Role
    delete:
      summary: Delete project role
      description: |-
        Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.deleteProjectRole_delete
      x-api-path-slug: api2roleid-delete
      parameters:
      - in: path
        name: id
        description: The ID of the project role to delete
      - in: query
        name: swap
        description: The ID of the project role that will replace the one being deleted
      responses:
        200:
          description: OK
      tags:
      - Project
      - Role
  /api/2/role/{id}/actors:
    get:
      summary: Get default actors for project role
      description: |-
        Returns the [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) for the project role.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.getProjectRoleActorsForRole_get
      x-api-path-slug: api2roleidactors-get
      parameters:
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Default
      - Actorsproject
      - Role
    post:
      summary: Add default actors to project role
      description: |-
        Adds [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) to the given role. You may add either groups or users, but you cannot add groups and users in the same request.

        Changing a project role's default actors does not affect project role members for projects already created.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.addProjectRoleActorsToRole_post
      x-api-path-slug: api2roleidactors-post
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
        description: The ID of the project role
      responses:
        200:
          description: OK
      tags:
      - Default
      - Actors
      - To
      - Project
      - Role
    delete:
      summary: Delete default actors from project role
      description: |-
        Removes [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) from the project role. You may remove either a group or user, but you cannot remove a group and a user in the same request.

        Changing a project role's default actors does not affect project role members for projects already created.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
      operationId: com.atlassian.jira.rest.v2.issue.project.RoleResource.deleteProjectRoleActorsFromRole_delete
      x-api-path-slug: api2roleidactors-delete
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: group
        description: The group name of the group to be removed as a default actor
      - in: path
        name: id
        description: The ID of the project role
      - in: query
        name: user
        description: The user account ID of the user to remove as a default actor
      responses:
        200:
          description: OK
      tags:
      - Default
      - Actors
      - From
      - Project
      - Role
  /api/2/screens:
    get:
      summary: Get all screens
      description: Returns a [paginated](#pagination) list of all screens.
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.getAllScreens_get
      x-api-path-slug: api2screens-get
      parameters:
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
      - Screens
  /api/2/screens/addToDefault/{fieldId}:
    post:
      summary: Add field to default screen
      description: Adds field or custom field to the default tab
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.addFieldToDefaultScreen_post
      x-api-path-slug: api2screensaddtodefaultfieldid-post
      parameters:
      - in: path
        name: fieldId
        description: id of field / custom field
      responses:
        200:
          description: OK
      tags:
      - Field
      - To
      - Default
      - Screen
  /api/2/screens/{screenId}/availableFields:
    get:
      summary: Get available screen fields
      description: Gets available fields for screen. i.e ones that haven't already
        been added.
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.getAvailableScreenFields_get
      x-api-path-slug: api2screensscreenidavailablefields-get
      parameters:
      - in: path
        name: screenId
        description: id of screen
      responses:
        200:
          description: OK
      tags:
      - Available
      - Screen
      - Fields
  /api/2/screens/{screenId}/tabs:
    get:
      summary: Get all screen tabs
      description: Returns a list of all tabs for the given screen
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.getAllScreenTabs_get
      x-api-path-slug: api2screensscreenidtabs-get
      parameters:
      - in: query
        name: projectKey
        description: the key of the project; this parameter is optional
      - in: path
        name: screenId
        description: id of screen
      responses:
        200:
          description: OK
      tags:
      - Screen
      - Tabs
    post:
      summary: Add screen tab
      description: Creates tab for given screen
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.addScreenTab_post
      x-api-path-slug: api2screensscreenidtabs-post
      parameters:
      - in: path
        name: screenId
        description: id of screen
      responses:
        200:
          description: OK
      tags:
      - Screen
      - Tab
  /api/2/screens/{screenId}/tabs/{tabId}:
    put:
      summary: Rename screen tab
      description: Renames tab on given screen
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.renameScreenTab_put
      x-api-path-slug: api2screensscreenidtabstabid-put
      parameters:
      - in: path
        name: screenId
        description: id of screen
      - in: path
        name: tabId
      responses:
        200:
          description: OK
      tags:
      - Rename
      - Screen
      - Tab
    delete:
      summary: Delete screen tab
      description: Deletes tab to give screen
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.deleteScreenTab_delete
      x-api-path-slug: api2screensscreenidtabstabid-delete
      parameters:
      - in: path
        name: screenId
        description: id of screen
      - in: path
        name: tabId
        description: id of tab
      responses:
        200:
          description: OK
      tags:
      - Screen
      - Tab
  /api/2/screens/{screenId}/tabs/{tabId}/fields:
    get:
      summary: Get all screen tab fields
      description: Gets all fields for a given tab
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.getAllScreenTabFields_get
      x-api-path-slug: api2screensscreenidtabstabidfields-get
      parameters:
      - in: query
        name: projectKey
        description: the key of the project; this parameter is optional
      - in: path
        name: screenId
        description: id of screen
      - in: path
        name: tabId
        description: id of tab
      responses:
        200:
          description: OK
      tags:
      - Screen
      - Tab
      - Fields
    post:
      summary: Add screen tab field
      description: Adds field to the given tab.
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.addScreenTabField_post
      x-api-path-slug: api2screensscreenidtabstabidfields-post
      parameters:
      - in: path
        name: screenId
        description: id of screen
      - in: path
        name: tabId
        description: id of tab
      responses:
        200:
          description: OK
      tags:
      - Screen
      - Tab
      - Field
  /api/2/screens/{screenId}/tabs/{tabId}/fields/{id}:
    delete:
      summary: Remove screen tab field
      description: Removes field from given tab
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.removeScreenTabField_delete
      x-api-path-slug: api2screensscreenidtabstabidfieldsid-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: screenId
        description: id of screen
      - in: path
        name: tabId
        description: id of tab
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Screen
      - Tab
      - Field
  /api/2/screens/{screenId}/tabs/{tabId}/fields/{id}/move:
    post:
      summary: Move screen tab field
      description: Moves field on the given tab
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.moveScreenTabField_post
      x-api-path-slug: api2screensscreenidtabstabidfieldsidmove-post
      parameters:
      - in: path
        name: id
      - in: path
        name: screenId
        description: id of screen
      - in: path
        name: tabId
        description: id of tab
      responses:
        200:
          description: OK
      tags:
      - Move
      - Screen
      - Tab
      - Field
  /api/2/screens/{screenId}/tabs/{tabId}/move/{pos}:
    post:
      summary: Move screen tab
      description: Moves tab position
      operationId: com.atlassian.jira.rest.v2.issue.ScreensResource.moveScreenTab_post
      x-api-path-slug: api2screensscreenidtabstabidmovepos-post
      parameters:
      - in: path
        name: pos
        description: position of tab
      - in: path
        name: screenId
        description: id of screen
      - in: path
        name: tabId
        description: id of tab
      responses:
        200:
          description: OK
      tags:
      - Move
      - Screen
      - Tab
  /api/2/search:
    get:
      summary: Search for issues using JQL (GET)
      description: |-
        Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

        If the JQL query expression is too large to be encoded as a query parameter, use the [POST](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-post) version of this resource.
      operationId: com.atlassian.jira.rest.v2.search.SearchResource.searchForIssuesUsingJql_get
      x-api-path-slug: api2search-get
      parameters:
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: query
        name: fields
        description: A comma-separated list of fields to return for each issue, use
          it to retrieve a subset of fields
      - in: query
        name: fieldsByKeys
        description: Reference fields by their key (rather than ID)
      - in: query
        name: jql
        description: A [JQL](https://confluence
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: properties
        description: A comma-separated list of up to 5 issue properties to include
          in the results
      - in: query
        name: startAt
        description: The index of the first item to return in the page of results
          (page offset)
      - in: query
        name: validateQuery
        description: Determines how to validate the JQL query and treat the validation
          results
      responses:
        200:
          description: OK
      tags:
      - Searchissues
      - Using
      - JQL
      - (GET)
    post:
      summary: Search for issues using JQL (POST)
      description: |-
        Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.

        There is a [GET](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-get) version of this resource that can be used for smaller JQL query expressions.
      operationId: com.atlassian.jira.rest.v2.search.SearchResource.searchForIssuesUsingJql_post
      x-api-path-slug: api2search-post
      responses:
        200:
          description: OK
      tags:
      - Searchissues
      - Using
      - JQL
      - (POST)
  /api/2/securitylevel/{id}:
    get:
      summary: Get issue security level
      description: Returns a full representation of the security level that has the
        given id.
      operationId: com.atlassian.jira.rest.v2.issue.IssueSecurityLevelResource.getIssueSecurityLevel_get
      x-api-path-slug: api2securitylevelid-get
      parameters:
      - in: path
        name: id
        description: a String containing an issue security level id
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Security
      - Level
  /api/2/serverInfo:
    get:
      summary: Get server info
      description: Returns general information about the current Jira server.
      operationId: com.atlassian.jira.rest.v2.ServerInfoResource.getServerInfo_get
      x-api-path-slug: api2serverinfo-get
      responses:
        200:
          description: OK
      tags:
      - Server
      - Info
  /api/2/settings/baseUrl:
    put:
      summary: Set base url
      description: Sets the base URL that is configured for this Jira instance.
      operationId: com.atlassian.jira.rest.v2.admin.SettingsResource.setBaseURL_put
      x-api-path-slug: api2settingsbaseurl-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Base
      - Url
  /api/2/settings/columns:
    get:
      summary: Get issue navigator default columns
      description: Returns the default system columns for issue navigator. Admin permission
        will be required.
      operationId: com.atlassian.jira.rest.v2.admin.SettingsResource.getIssueNavigatorDefaultColumns_get
      x-api-path-slug: api2settingscolumns-get
      responses:
        200:
          description: OK
      tags:
      - Issue
      - Navigator
      - Default
      - Columns
    put:
      summary: Set issue navigator default columns
      description: Sets the default system columns for issue navigator. Admin permission
        will be required.
      operationId: com.atlassian.jira.rest.v2.admin.SettingsResource.setIssueNavigatorDefaultColumns_put
      x-api-path-slug: api2settingscolumns-put
      responses:
        200:
          description: OK
      tags:
      - Set
      - Issue
      - Navigator
      - Default
      - Columns
  /api/2/status:
    get:
      summary: Get statuses
      description: Returns a list of all statuses
      operationId: com.atlassian.jira.rest.v2.issue.StatusResource.getStatuses_get
      x-api-path-slug: api2status-get
      responses:
        200:
          description: OK
      tags:
      - Statuses
  /api/2/status/{idOrName}:
    get:
      summary: Get status
      description: Returns a full representation of the Status having the given id
        or name. If there are two statuses with the same name, only the first found
        status will be returned. Therefore searching by id is encouraged.
      operationId: com.atlassian.jira.rest.v2.issue.StatusResource.getStatus_get
      x-api-path-slug: api2statusidorname-get
      parameters:
      - in: path
        name: idOrName
        description: a numeric Status id or a status name
      responses:
        200:
          description: OK
      tags:
      - Status
  /api/2/statuscategory:
    get:
      summary: Get status categories
      description: Returns a list of all status categories
      operationId: com.atlassian.jira.rest.v2.issue.StatusCategoryResource.getStatusCategories_get
      x-api-path-slug: api2statuscategory-get
      responses:
        200:
          description: OK
      tags:
      - Status
      - Categories
  /api/2/statuscategory/{idOrKey}:
    get:
      summary: Get status category
      description: Returns a full representation of the StatusCategory having the
        given id or key
      operationId: com.atlassian.jira.rest.v2.issue.StatusCategoryResource.getStatusCategory_get
      x-api-path-slug: api2statuscategoryidorkey-get
      parameters:
      - in: path
        name: idOrKey
        description: a numeric StatusCategory id or a status category key
      responses:
        200:
          description: OK
      tags:
      - Status
      - Category
  /api/2/task/{taskId}:
    get:
      summary: Get task
      description: |-
        This endpoint is used to check the status of a [long-running asynchronous task](#async).

        When the task is finished, it will contain a **result**. The result may be arbitrary JSON, its shape different for each task type. Consult the documentation of the method that created the task for more details.

        To access a task, you need to be its creator or a Jira admin. Otherwise a 403 response will be returned.
      operationId: com.atlassian.jira.rest.v2.task.TaskResource.getTask_get
      x-api-path-slug: api2tasktaskid-get
      parameters:
      - in: path
        name: taskId
      responses:
        200:
          description: OK
      tags:
      - Task
  /api/2/task/{taskId}/cancel:
    post:
      summary: Cancel task
      description: |-
        Requests that the task that corresponds to the given task id is cancelled.

        To cancel a task, you need to be its creator or a Jira admin. Otherwise a 403 response will be returned.
      operationId: com.atlassian.jira.rest.v2.task.TaskResource.cancelTask_post
      x-api-path-slug: api2tasktaskidcancel-post
      parameters:
      - in: path
        name: taskId
      responses:
        200:
          description: OK
      tags:
      - Cancel
      - Task
  /api/2/universal_avatar/type/{type}/owner/{entityId}:
    get:
      summary: Get avatars
      description: ""
      operationId: com.atlassian.jira.rest.v2.issue.UniversalAvatarResource.getAvatars_get
      x-api-path-slug: api2universal-avatartypetypeownerentityid-get
      parameters:
      - in: path
        name: entityId
      - in: path
        name: type
      responses:
        200:
          description: OK
      tags:
      - Avatars
    post:
      summary: Store avatar
      description: Creates an avatar for a given entity, for the given entity ID and
        type of entity. For example, you can create an avatar for an issue type, given
        the issue type Id. Uploading an avatar is supported for different types of
        entities across the Jira products. However, it is supported for the "project"
        and "issuetype" entity types for all Jira products. The uploaded image will
        be cropped according to the crop parameters listed below. If no crop parameters
        are specified, the image will be cropped to a square. The square will originate
        at the top left of the image and the length of each side will be set to the
        smaller of the height or width of the image.
      operationId: com.atlassian.jira.rest.v2.issue.UniversalAvatarResource.storeAvatar_post
      x-api-path-slug: api2universal-avatartypetypeownerentityid-post
      parameters:
      - in: path
        name: entityId
        description: The Id of the entity that you want to update the avatar of
      - in: query
        name: size
        description: (optional) The length of each side of the crop region
      - in: path
        name: type
        description: The type of the entity that you want to update the avatar of
      - in: query
        name: x
        description: (optional) The X coordinate of the top-left corner of the crop
          region
      - in: query
        name: "y"
        description: (optional) The Y coordinate of the top-left corner of the crop
          region
      responses:
        200:
          description: OK
      tags:
      - Store
      - Avatar
  /api/2/universal_avatar/type/{type}/owner/{owningObjectId}/avatar/{id}:
    delete:
      summary: Delete avatar
      description: Deletes avatar
      operationId: com.atlassian.jira.rest.v2.issue.UniversalAvatarResource.deleteAvatar_delete
      x-api-path-slug: api2universal-avatartypetypeownerowningobjectidavatarid-delete
      parameters:
      - in: path
        name: id
        description: database id for avatar
      - in: path
        name: owningObjectId
      - in: path
        name: type
        description: Project id or project key
      responses:
        200:
          description: OK
      tags:
      - Avatar
  /api/2/user:
    get:
      summary: Get user
      description: Returns a user. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
        None.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.getUser_get
      x-api-path-slug: api2user-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: query
        name: expand
        description: Use [expand](https://developer
      - in: header
        name: force-account-id
      - in: query
        name: key
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
    post:
      summary: Create user
      description: 'Creates a user. This resource is retained for legacy compatibility.
        As soon as a more suitable alternative is available this resource will be
        deprecated. The option is provided to set or generate a password for the user.
        When using the option to generate a password, by omitting `password` from
        the request, include `"notification": "true"` to ensure the user is sent an
        email advising them that their account has been created. This email includes
        a link for the user to set their password. If the notification isn''t sent
        for a generated password, the user will need to be sent a reset password request
        from Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**
        _Administer Jira_ [global permission](href=)'
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.createUser_post
      x-api-path-slug: api2user-post
      responses:
        200:
          description: OK
      tags:
      - User
    delete:
      summary: Delete user
      description: Deletes a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Site administration (i.e., member of the site-admin [group](https://confluence.atlassian.com/display/Cloud/Manage+groups)).
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.removeUser_delete
      x-api-path-slug: api2user-delete
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      - in: query
        name: key
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
  /api/2/user/assignable/multiProjectSearch:
    get:
      summary: Find users assignable to projects
      description: |-
        Returns a list of users who fulfill both of these criteria:

        *   their user attributes match a string.
        *   they can be assigned issues in one or more projects.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findBulkAssignableUsers_get
      x-api-path-slug: api2userassignablemultiprojectsearch-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: projectKeys
        description: A comma-separated list of project keys (case sensitive)
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: The search string
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Assignable
      - To
      - Projects
  /api/2/user/assignable/search:
    get:
      summary: Find users assignable to issues
      description: |-
        Returns a list of users that can be assigned to an issue. Use this method to find the list of users who can be assigned to:

        *   a new issue, by providing the `projectKeyOrId`.
        *   an updated issue, by providing the `issueKey`.
        *   to an issue during a transition (workflow action), by providing the `issueKey` and the transition id in `actionDescriptorId`. You can obtain the IDs of an issue's valid transitions using the `transitions` option in the `expand` parameter of [Get issue](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issue-issueIdOrKey-get).

        In all these cases, you can pass a username to determine if a user can be assigned to an issue. The user is returned in the response if they can be assigned to the issue or issue transition. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findAssignableUsers_get
      x-api-path-slug: api2userassignablesearch-get
      parameters:
      - in: query
        name: actionDescriptorId
        description: The ID of the transition
      - in: header
        name: force-account-id
      - in: query
        name: issueKey
        description: The key of the issue
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: project
        description: The project ID or project key (case sensitive)
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Assignable
      - To
      - Issues
  /api/2/user/bulk:
    get:
      summary: Bulk get users
      description: Returns details of users specified in a list of usernames or keys.
        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer
        Jira_ [global permission](href=). Users with permission to access Jira can
        call this method, but empty search results are returned.
      operationId: com.atlassian.jira.rest.v2.user.UserBulkResource.bulkGetUsers_get
      x-api-path-slug: api2userbulk-get
      parameters:
      - in: query
        name: key
        description: Comma-separated list of user keys
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: Comma-separated list of usernames
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Get
      - Users
  /api/2/user/columns:
    get:
      summary: Get user default columns
      description: |-
        Returns the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed in the request, the calling user's details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To get the column details for any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLgl).
        *   To get the calling user's column details: None
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.getUserDefaultColumns_get
      x-api-path-slug: api2usercolumns-get
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Default
      - Columns
    put:
      summary: Set user default columns
      description: |-
        Sets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed. The parameters for this resource are expressed as HTML form data. For example, in curl: `curl -X PUT -d username= -d columns=summary -d columns=description ` **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To set the calling user's columns: None
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.setUserColumns_put
      x-api-path-slug: api2usercolumns-put
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      responses:
        200:
          description: OK
      tags:
      - Set
      - User
      - Default
      - Columns
    delete:
      summary: Reset user default columns
      description: |-
        Resets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user to the system default. If a username is not passed, the calling user's default columns are reset. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To set the calling user's columns: None
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.resetUserColumns_delete
      x-api-path-slug: api2usercolumns-delete
      parameters:
      - in: query
        name: accountId
        description: the account ID
      - in: header
        name: force-account-id
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - Reset
      - User
      - Default
      - Columns
  /api/2/user/groups:
    get:
      summary: Get user groups
      description: Returns the groups to which a user belongs. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):**
        _Browse users and groups_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.getUserGroups_get
      x-api-path-slug: api2usergroups-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: query
        name: key
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Groups
  /api/2/user/permission/search:
    get:
      summary: Find users with permissions
      description: |-
        Returns a list of users who fulfill both of these criteria:

        *   their user attributes match a search string.
        *   they have a set of permissions for a project or issue.

        If no search string is provided, a list of all users with the permissions is returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   Get users for any project, _Administer Jira_ [global permission](href=).
        *   Get users for a project, _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg) for the project.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findUsersWithAllPermissions_get
      x-api-path-slug: api2userpermissionsearch-get
      parameters:
      - in: header
        name: force-account-id
      - in: query
        name: issueKey
        description: The issue key for the issue
      - in: query
        name: maxResults
        description: The maximum number of items to return per page
      - in: query
        name: permissions
        description: A comma-separated list of permissions
      - in: query
        name: projectKey
        description: The project key for the project (case sensitive)
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: startAt
        description: The index of the first item to return in a page of results (page
          offset)
      - in: query
        name: username
        description: The search string
      responses:
        200:
          description: OK
      tags:
      - Find
      - Users
      - Permissions
  /api/2/user/picker:
    get:
      summary: Find users for picker
      description: Returns a list of users whose attributes match the query term.
        The returned object includes the `html` field where the matched query term
        is highlighted with the HTML strong tag. A list of usernames can be provided
        to exclude users from the results. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Browse users and groups_ [global permission](href=). Users with
        permission to access Jira can call this method, but will only get search results
        for an exact name match.
      operationId: com.atlassian.jira.rest.v2.issue.UserResource.findUsersForPicker_get
      x-api-path-slug: api2userpicker-get
      parameters:
      - in: query
        name: exclude
        description: A comma-separated list of usernames to exclude from the search
          results
      - in: query
        name: excludeAccountIds
        description: A comma-separated list of user accountIds to exclude from the
          search results
      - in: header
        name: force-account-id
      - in: query
        name: maxResults
        description: The maximum number of items to return
      - in: query
        name: query
        description: A search input that is matched against appropriate user attributes
          to find relevant users
      - in: query
        name: showAvatar
        description: Include the URI to the users avatar
      responses:
        200:
          description: OK
      tags:
      - Find
      - Userspicker
  /api/2/user/properties:
    get:
      summary: Get user property keys
      description: |-
        Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**

        *   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).
        *   To access the calling user's property keys: None

        Note: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI.
      operationId: com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.getUserPropertyKeys_get
      x-api-path-slug: api2userproperties-get
      parameters:
      - in: query
        name: accountId
        description: The account ID of the user
      - in: header
        name: force-account-id
      - in: query
        name: userKey
        description: The key of the user
      - in: query
        name: username
        description: The username of the user
      responses:
        200:
          description: OK
      tags:
      - User
      - Property
      - Keys
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