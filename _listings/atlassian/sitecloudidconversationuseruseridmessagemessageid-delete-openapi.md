---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Software Cloud API Delete a message in a direct conversation
  description: Authentication required, with scope participate:conversation
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
    post:
      summary: Create conversation
      description: Authentication required, with scope manage:conversation
      operationId: ConversationPostHandler
      x-api-path-slug: sitecloudidconversation-post
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      responses:
        200:
          description: OK
      tags:
      - Conversation
  /site/{cloudId}/conversation/user/{userId}:
    get:
      summary: Get a direct conversation of a user
      description: Get a direct conversation of a user.
      operationId: ConversationUserGetHandler
      x-api-path-slug: sitecloudidconversationuseruserid-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: userId
        description: The user Id
      responses:
        200:
          description: OK
      tags:
      - Direct
      - Conversation
      - Of
      - User
  /site/{cloudId}/conversation/user/{userId}/message:
    post:
      summary: Send message to a user
      description: Send message to a user.
      operationId: UserMessagePostHandler
      x-api-path-slug: sitecloudidconversationuseruseridmessage-post
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: userId
        description: The user Id
      responses:
        200:
          description: OK
      tags:
      - Send
      - Message
      - To
      - User
  /site/{cloudId}/conversation/user/{userId}/message/{messageId}:
    put:
      summary: Edit a message in a direct conversation
      description: Authentication required, with scope participate:conversation
      operationId: UserMessagePutHandler
      x-api-path-slug: sitecloudidconversationuseruseridmessagemessageid-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: messageId
        description: The ID of the message
      - in: path
        name: userId
        description: The user Id
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Message
      - In
      - Direct
      - Conversation
    delete:
      summary: Delete a message in a direct conversation
      description: Authentication required, with scope participate:conversation
      operationId: UserMessageDeleteHandler
      x-api-path-slug: sitecloudidconversationuseruseridmessagemessageid-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: messageId
        description: The ID of the message
      - in: path
        name: userId
        description: The user Id
      responses:
        200:
          description: OK
      tags:
      - Message
      - In
      - Direct
      - Conversation
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