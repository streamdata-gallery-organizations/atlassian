---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Software Cloud API Get Message by id
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
  /site/{cloudId}/conversation/{conversationId}:
    get:
      summary: Get conversation details
      description: Authentication required, with scope participate:conversation
      operationId: ConversationGetHandler
      x-api-path-slug: sitecloudidconversationconversationid-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      responses:
        200:
          description: OK
      tags:
      - Conversation
      - Details
    patch:
      summary: Update conversation
      description: Authentication required, with scope manage:conversation
      operationId: ConversationPatchHandler
      x-api-path-slug: sitecloudidconversationconversationid-patch
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      responses:
        200:
          description: OK
      tags:
      - Conversation
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:actionTarget:
    get:
      summary: Get a list of chat:actionTarget modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatActionTargetGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatactiontarget-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:actionTarget
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:actionTarget/{key}:
    put:
      summary: Create or update a chat:actionTarget module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatActionTargetPutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatactiontargetkey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:actionTarget
      - Module
    delete:
      summary: Delete a chat:actionTarget module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatActionTargetDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatactiontargetkey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:actionTarget
      - Module
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:bot:
    get:
      summary: Get a list of chat:bot modules
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbot-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:bot
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:bot/{key}:
    put:
      summary: Create or update a chat:bot module
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotPutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbotkey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:bot
      - Module
    delete:
      summary: Delete a chat:bot module
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbotkey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:bot
      - Module
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:bot:messages:
    get:
      summary: Get a list of chat:bot:messages modules
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotMessageGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbotmessages-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:bot:messages
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:bot:messages/{key}:
    put:
      summary: Create or update a chat:bot:messages module
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotMessagePutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbotmessageskey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:bot:messages
      - Module
    delete:
      summary: Delete a chat:bot:messages module
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatBotMessageDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatbotmessageskey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:bot:messages
      - Module
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:configuration/{key}/state:
    put:
      summary: Update the chat:configuration state
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatConfigurationPutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatconfigurationkeystate-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: Key of the configuration module
      responses:
        200:
          description: OK
      tags:
      - Chat:configuration
      - State
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:dialog:
    get:
      summary: Get a list of chat:dialog modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatDialogGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatdialog-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:dialog
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:dialog/{key}:
    put:
      summary: Create or update a chat:dialog module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatDialogPutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatdialogkey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:dialog
      - Module
    delete:
      summary: Delete a chat:dialog module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatDialogDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatdialogkey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:dialog
      - Module
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:externalPage:
    get:
      summary: Get a list of chat:externalPage modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatExternalPageGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatexternalpage-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:externalPage
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:externalPage/{key}:
    put:
      summary: Create or update a chat:externalPage module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatExternalPagePutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatexternalpagekey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:externalPage
      - Module
    delete:
      summary: Delete a chat:externalPage module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatExternalPageDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatexternalpagekey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:externalPage
      - Module
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:glance:
    get:
      summary: Get a list of chat:glance modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatGlanceGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatglance-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:glance
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:glance/{key}:
    put:
      summary: Create or update a chat:glance module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatGlancePutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatglancekey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:glance
      - Module
    delete:
      summary: Delete a chat:glance module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatGlanceDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatglancekey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:glance
      - Module
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:glance/{key}/state:
    put:
      summary: Update the chat:glance state
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatGlanceStatePutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatglancekeystate-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: Key of the glance
      responses:
        200:
          description: OK
      tags:
      - Chat:glance
      - State
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:sidebar:
    get:
      summary: Get a list of chat:sidebar modules
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatSidebarGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatsidebar-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:sidebar
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:sidebar/{key}:
    put:
      summary: Create or update a chat:sidebar module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatSidebarPutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatsidebarkey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:sidebar
      - Module
    delete:
      summary: Delete a chat:sidebar module
      description: Authentication required, with scope participate:conversation
      operationId: AppModuleChatSidebarDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatsidebarkey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:sidebar
      - Module
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:webhook:
    get:
      summary: Get a list of chat:webhook modules
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatWebhookGetAllHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatwebhook-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: A maximum number of modules to return per call
      - in: query
        name: start
        description: Offset for the query
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Chat:webhook
      - Modules
  /site/{cloudId}/conversation/{conversationId}/app/module/chat:webhook/{key}:
    put:
      summary: Create or update a chat:webhook module
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatWebhookPutHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatwebhookkey-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Update
      - Chat:webhook
      - Module
    delete:
      summary: Delete a chat:webhook module
      description: Authentication required, with scope participate:conversation
      operationId: AppWebhookChatWebhookDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidappmodulechatwebhookkey-delete
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: key
        description: The key to identify the resource
      responses:
        200:
          description: OK
      tags:
      - Chat:webhook
      - Module
  /site/{cloudId}/conversation/{conversationId}/archive:
    put:
      summary: Archive conversation
      description: Authentication required, with scope manage:conversation
      operationId: ConversationArchivePutHandler
      x-api-path-slug: sitecloudidconversationconversationidarchive-put
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      responses:
        200:
          description: OK
      tags:
      - Archive
      - Conversation
  /site/{cloudId}/conversation/{conversationId}/media:
    post:
      summary: Upload a file
      description: Authentication required, with scope participate:conversation
      operationId: ConversationMediaPostHandler
      x-api-path-slug: sitecloudidconversationconversationidmedia-post
      parameters:
      - in: path
        name: cloudId
        description: Cloud ID
      - in: path
        name: conversationId
        description: Conversation ID
      - in: query
        name: name
        description: File name
      responses:
        200:
          description: OK
      tags:
      - Upload
      - File
  /site/{cloudId}/conversation/{conversationId}/media/{mediaId}:
    get:
      summary: Get a file
      description: Authentication required, with scope participate:conversation
      operationId: ConversationMediaGetHandler
      x-api-path-slug: sitecloudidconversationconversationidmediamediaid-get
      parameters:
      - in: path
        name: cloudId
        description: Cloud ID
      - in: path
        name: conversationId
        description: Conversation ID
      - in: path
        name: mediaId
        description: Media ID
      responses:
        200:
          description: OK
      tags:
      - File
    delete:
      summary: Delete a file
      description: Authentication required, with scope participate:conversation
      operationId: ConversationMediaDeleteHandler
      x-api-path-slug: sitecloudidconversationconversationidmediamediaid-delete
      parameters:
      - in: path
        name: cloudId
        description: Cloud ID
      - in: path
        name: conversationId
        description: Conversation ID
      - in: path
        name: mediaId
        description: Media ID
      responses:
        200:
          description: OK
      tags:
      - File
  /site/{cloudId}/conversation/{conversationId}/message:
    get:
      summary: Get conversation history
      description: "Authentication required, with scope participate:conversation This
        method returns messages after/before a given messageIDs or/and timestamps.
        If these parameters are omitted the method returns conversation\u2019s latest
        messages. Max number of messages returned is 75."
      operationId: ConversationMessagesGetHandler
      x-api-path-slug: sitecloudidconversationconversationidmessage-get
      parameters:
      - in: query
        name: afterMessage
        description: Returns at most 75 latest messages after a provided messageID
      - in: query
        name: afterTimestamp
        description: Returns at most 75 latest messages after a provided RFC3339 timestamp
          (2006-01-02T15:04:05+07:00)
      - in: query
        name: beforeMessage
        description: Returns at most 75 messages before a provided messageID
      - in: query
        name: beforeTimestamp
        description: Returns at most 75 messages before a provided RFC3339 timestamp
          (2006-01-02T15:04:05+07:00)
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: The maximum number of results
      responses:
        200:
          description: OK
      tags:
      - Conversation
      - History
    post:
      summary: Send a message to a conversation
      description: Send a message to a conversation.
      operationId: ConversationMessagePostHandler
      x-api-path-slug: sitecloudidconversationconversationidmessage-post
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      responses:
        200:
          description: OK
      tags:
      - Send
      - Message
      - To
      - Conversation
  /site/{cloudId}/conversation/{conversationId}/message/recent:
    get:
      summary: Get latest messages for conversation
      description: Authentication required, with scope participate:conversation Max
        number of messages returned is 75.
      operationId: ConversationMessagesRecentGetHandler
      x-api-path-slug: sitecloudidconversationconversationidmessagerecent-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: query
        name: limit
        description: The maximum number of results
      responses:
        200:
          description: OK
      tags:
      - Latest
      - Messagesconversation
  /site/{cloudId}/conversation/{conversationId}/message/{messageId}:
    get:
      summary: Get Message by id
      description: Authentication required, with scope participate:conversation
      operationId: ConversationMessageGetHandler
      x-api-path-slug: sitecloudidconversationconversationidmessagemessageid-get
      parameters:
      - in: path
        name: cloudId
        description: The id of the site (cloudId)
      - in: path
        name: conversationId
        description: The conversation id
      - in: path
        name: messageId
        description: The ID of the Message to retrieve
      responses:
        200:
          description: OK
      tags:
      - Message
      - By
      - Id
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