---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Get share permissions
  description: Returns the share permissions for a filter. A filter can be shared
    with groups, projects, all logged-in users, or the public. Sharing with all logged-in
    users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None, however the calling user must have permission to view the filter.
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