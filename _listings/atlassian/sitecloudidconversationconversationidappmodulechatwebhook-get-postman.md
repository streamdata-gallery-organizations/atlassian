{
  "info": {
    "name": "Jira Software Cloud API Get a list of chat:webhook modules",
    "_postman_id": "9cb779b0-da2c-4cc2-9989-be4edebf7efc",
    "description": "Authentication required, with scope participate:conversation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "5f19136c-5be2-4cb7-aa98-3355180ff3d5",
          "name": "GetAllHandler",
          "request": {
            "url": "{{default}}/site/",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9135cba9-c9d2-448c-a0f1-740ab7ce52ff"
            }
          ]
        },
        {
          "id": "ac1c6efa-ca47-4bf3-918f-a039c71ad74c",
          "name": "ConversationGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation"
              ],
              "query": [
                {
                  "key": "cursor",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "exclude-direct",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include-archived",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "include-private",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "query",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "The API returns the list of conversations the app has access to Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "51b9e8e9-7c50-4d40-a6ff-63005863f3e8"
            }
          ]
        },
        {
          "id": "6331f1db-596f-47e3-8a6c-ae9424ba6460",
          "name": "AppModuleChatActionTargetGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:actionTarget"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "93e9d426-7bb5-41a8-aa52-f8ac2aac0f6d"
            }
          ]
        },
        {
          "id": "fd359fb0-6617-4f74-8d9d-af7aa3cddc6b",
          "name": "AppWebhookChatBotGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:bot"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "958fbf7b-f244-43a5-82ba-9196bdebae60"
            }
          ]
        },
        {
          "id": "e6888066-9023-4108-bc14-7907ff9b305a",
          "name": "AppWebhookChatBotMessageGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:bot:messages"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "23c7eb26-6602-4e9e-a7d4-560b609ae15b"
            }
          ]
        },
        {
          "id": "b1a9c8bb-1d26-4d9e-9484-c8a259c7e9f5",
          "name": "AppModuleChatDialogGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:dialog"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "40debab2-6e60-4932-af77-f264acbb7de2"
            }
          ]
        },
        {
          "id": "939fc13d-426f-4755-b662-c86b9ae63a2a",
          "name": "AppModuleChatExternalPageGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:externalPage"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "01f4a64b-e854-4293-98f9-e6f6671d330a"
            }
          ]
        },
        {
          "id": "c20b2189-7e0d-497d-9b67-4ab3fca637c7",
          "name": "AppModuleChatGlanceGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:glance"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "80831b61-a498-4d27-b020-9e08f1acd0ea"
            }
          ]
        },
        {
          "id": "296baed9-e849-4a71-b34b-3a93e3defc8a",
          "name": "AppModuleChatSidebarGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:sidebar"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ac242cc3-306f-4d21-975e-97ac7a121769"
            }
          ]
        },
        {
          "id": "40c14da1-8b5e-4be8-9216-c89ed6a98be5",
          "name": "AppWebhookChatWebhookGetAllHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:webhook"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f964ef83-c4c5-4ec4-88c6-acac2aeb2d8f"
            }
          ]
        }
      ]
    },
    {
      "name": "Conversation",
      "item": [
        {
          "id": "299faa36-f3d7-4ab7-82fd-cfaf4f3aef16",
          "name": "ConversationPostHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope manage:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "edcdc2f9-d825-47ec-993f-388ce2d781cc"
            }
          ]
        },
        {
          "id": "79064424-a9ee-417c-a28d-96b09ce0da3a",
          "name": "ConversationGetHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1ba991b-0861-49c9-b1c9-b0e8387dc9d4"
            }
          ]
        },
        {
          "id": "96ab9b04-4793-4222-862d-7d10373e5f95",
          "name": "ConversationPatchHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PATCH",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope manage:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b90b0c0b-5381-4f54-acc7-8dda856b1f3e"
            }
          ]
        }
      ]
    },
    {
      "name": "Direct",
      "item": [
        {
          "id": "831a610e-bf98-4426-bbc4-cfda3ac7e5d9",
          "name": "ConversationUserGetHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/user/:userId"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "userId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a direct conversation of a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ee81931-141c-4562-ad7b-b2a355d72de0"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "74b96a54-7c56-41be-9042-f91cea326f1f",
          "name": "UserMessagePostHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/user/:userId/message"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "userId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Send message to a user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1fec8bac-f852-4fcb-860b-43c1907aec5a"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "7b156a62-571c-4019-835f-0dbb145cb8ad",
          "name": "UserMessagePutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/user/:userId/message/:messageId"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "messageId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "userId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ed9d361-9837-4db8-86c8-b7c67fa11a3a"
            }
          ]
        }
      ]
    },
    {
      "name": "Message",
      "item": [
        {
          "id": "ae3358a2-ce79-4403-9849-bfd2e299ef4c",
          "name": "UserMessageDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/user/:userId/message/:messageId"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "messageId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "userId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9475ff64-bade-4eed-a0cc-993f6534592d"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "5e5247cd-47b0-4d71-8964-c0080e82e21a",
          "name": "AppModuleChatActionTargetPutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:actionTarget/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2da70d26-d373-477f-bbae-bc159909b895"
            }
          ]
        },
        {
          "id": "67669ff7-4806-4ead-bd1d-43622fdd3eee",
          "name": "AppWebhookChatBotPutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:bot/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "26874122-aed7-49a1-a065-b4f0e4f618ed"
            }
          ]
        },
        {
          "id": "fa003429-a156-4164-be94-c5d0079db48a",
          "name": "AppWebhookChatBotMessagePutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:bot:messages/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "608b55ab-73a8-4ac0-95ef-6ff0f29d78bb"
            }
          ]
        },
        {
          "id": "4f0f2dbf-bb07-4eb9-8a4b-e4b7403575ef",
          "name": "AppModuleChatDialogPutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:dialog/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3c513e7-8510-4a6a-86f6-eca8792994f9"
            }
          ]
        },
        {
          "id": "4df127b3-1c01-439e-8fc9-ea6504a9adbd",
          "name": "AppModuleChatExternalPagePutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:externalPage/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b96cb8dc-3959-4b4e-863d-1f9412b981e2"
            }
          ]
        },
        {
          "id": "5edcc5c7-a345-4f66-bd33-1816ca297ef0",
          "name": "AppModuleChatGlancePutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:glance/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a2c01a15-420b-43d8-93c2-7da43e26eac1"
            }
          ]
        },
        {
          "id": "755720ba-7b7f-4ec9-ba36-9780c35845c6",
          "name": "AppModuleChatSidebarPutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:sidebar/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "52792055-2c33-4a83-b721-ab25dd9a98e4"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:actionTarget",
      "item": [
        {
          "id": "8da60416-4088-41db-b8c2-4e16a9a92222",
          "name": "AppModuleChatActionTargetDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:actionTarget/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d802103c-2ea1-428b-99f6-8197052ee0c0"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:bot",
      "item": [
        {
          "id": "03b40b51-10ea-41ae-9d56-ca601dbdbf06",
          "name": "AppWebhookChatBotDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:bot/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2b62acb5-5360-42cf-a123-0eca0a660b31"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:bot:messages",
      "item": [
        {
          "id": "551846ec-a1ac-4a07-9cc3-d05d2637d687",
          "name": "AppWebhookChatBotMessageDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:bot:messages/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ea940162-99dc-4f2c-9b5d-118d349e47b2"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:configuration",
      "item": [
        {
          "id": "1c1b2f35-ce14-45df-ac26-49474f009f42",
          "name": "AppModuleChatConfigurationPutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:configuration/:key/state"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3cb75b43-d0d6-41a3-9654-19efa07ee815"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:dialog",
      "item": [
        {
          "id": "d8518887-0d25-4738-a899-119f6e6028c4",
          "name": "AppModuleChatDialogDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:dialog/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c5246d31-127f-4622-bffc-f58b6591a4ba"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:externalPage",
      "item": [
        {
          "id": "ca24b5a7-9a5a-4be5-ae44-b6be5eb2fbff",
          "name": "AppModuleChatExternalPageDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:externalPage/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "85f6f888-a08c-4614-9ef4-c5058e358e7c"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:glance",
      "item": [
        {
          "id": "46038b64-3c9c-49a6-bf85-1f4ca4d38b8c",
          "name": "AppModuleChatGlanceDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:glance/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2bf1203a-31c7-4f8f-b2c3-ef22d02eead1"
            }
          ]
        },
        {
          "id": "990e0f3f-a14a-4452-a710-74d86f152899",
          "name": "AppModuleChatGlanceStatePutHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:glance/:key/state"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "16b20827-8067-4b56-89a9-da0438701dfb"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:sidebar",
      "item": [
        {
          "id": "06930607-bd57-4f26-b290-5d1647202b74",
          "name": "AppModuleChatSidebarDeleteHandler",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "site/:cloudId/conversation/:conversationId/app/module/chat:sidebar/:key"
              ],
              "variable": [
                {
                  "id": "cloudId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "conversationId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Authentication required, with scope participate:conversation"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e353f264-159c-424f-a55a-dec8794edc3d"
            }
          ]
        }
      ]
    }
  ],
  "variable": [
    {
      "key": "default",
      "value": "http://www.example.com/"
    }
  ]
}