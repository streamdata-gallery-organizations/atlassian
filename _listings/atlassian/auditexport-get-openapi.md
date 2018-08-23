---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Confluence Cloud API Export audit records
  description: "Exports audit records as a CSV file or ZIP file.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw)
    required**: \n'Confluence Administrator' global permission."
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