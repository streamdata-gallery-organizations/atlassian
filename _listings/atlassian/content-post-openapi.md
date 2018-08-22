---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Create content
  description: "Creates a new piece of content or publishes an existing draft. \n\nTo
    publish a draft, add the `id` and `status` properties to the body of the request.
    \nSet the `id` to the ID of the draft and set the `status` to 'current'. When
    the \nrequest is sent, a new piece of content will be created and the metadata
    from the \ndraft will be transferred into it.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: 'Add' permission for the \nspace that the content will be created
    in, and permission to view the draft if publishing a draft."
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