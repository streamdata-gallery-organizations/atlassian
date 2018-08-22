---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Software Cloud API Get a list of conversations
  description: The API returns the list of conversations the app has access to Authentication
    required, with scope participate:conversation
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /site/:
    get:
      summary: Get list of sites
      description: Authentication required, with scope participate:conversation
      operationId: GetAllHandler
      x-api-path-slug: site-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Sites
  /site/{cloudId}/conversation:
    get:
      summary: Get a list of conversations
      description: The API returns the list of conversations the app has access to
        Authentication required, with scope participate:conversation
      operationId: ConversationGetAllHandler
      x-api-path-slug: sitecloudidconversation-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: query
        name: cursor
        description: The cursor is a string, that you can use to scroll through the
          data set to get more results
      - in: query
        name: exclude-direct
        description: Exclude direct messages from a response
      - in: query
        name: include-archived
        description: Include archived conversations into response
      - in: query
        name: include-private
        description: Include private conversations into response
      - in: query
        name: limit
        description: A maximum number of conversations to return per call
      - in: query
        name: query
        description: A string containing full or part of conversations name
      - in: query
        name: sort
        description: A sort order of the conversations lists
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Conversations
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