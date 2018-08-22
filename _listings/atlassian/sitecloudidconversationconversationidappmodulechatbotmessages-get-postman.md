{
  "info": {
    "name": "Jira Software Cloud API Get a list of chat:bot:messages modules",
    "_postman_id": "e34234bd-5106-4109-a2f0-03943b13bb3f",
    "description": "Authentication required, with scope participate:conversation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "6ef2321c-2e47-459e-9445-69b1a541b288",
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
              "id": "f0d7c50a-70a1-4355-a1c2-e4027f6130a4"
            }
          ]
        },
        {
          "id": "63b728f5-c284-413c-a51d-f7c5c266e9c0",
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
              "id": "5066360b-7015-4fb8-9dce-5f3648765cb6"
            }
          ]
        },
        {
          "id": "cae138ac-839a-4766-bb85-0d4c3ab582e3",
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
              "id": "8bcc2fcc-5449-470e-8934-66652c3e1bcc"
            }
          ]
        },
        {
          "id": "10010487-d506-441a-91e1-0c5425ed0c87",
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
              "id": "a11b34ac-a0b3-4f7f-b9b8-d4425650cca1"
            }
          ]
        },
        {
          "id": "bfe3805e-d288-40ab-b19e-d50a352e0989",
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
              "id": "5b9bd1e4-3053-4012-b431-7091421dae9f"
            }
          ]
        }
      ]
    },
    {
      "name": "Conversation",
      "item": [
        {
          "id": "61e92528-1722-46c4-a1ab-48f993d55d8b",
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
              "id": "e3047809-904e-494c-843e-92f6b56f4ab1"
            }
          ]
        },
        {
          "id": "ff18d142-12a8-4e18-a83f-fd576ca5200a",
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
              "id": "f009fd42-5489-4e44-8ee2-cd36213f8c5a"
            }
          ]
        },
        {
          "id": "a04367ea-38e5-4a33-9087-7a3e1b97fb20",
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
              "id": "33856161-47fe-4957-ac90-2cd2dc427ea4"
            }
          ]
        }
      ]
    },
    {
      "name": "Direct",
      "item": [
        {
          "id": "439a3fea-3a96-49ee-bfb4-546e1e19816e",
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
              "id": "2bd21405-0c60-4051-9709-fad7f7f6237a"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "ae7ae095-90c4-4675-9aa5-9eb67665ea81",
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
              "id": "cd51a2f1-a002-4062-9253-96b63e382402"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "84d62964-ff51-42d5-87bc-87c7c96d5b4f",
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
              "id": "fae695d4-1380-44dd-a37c-affa83887bc5"
            }
          ]
        }
      ]
    },
    {
      "name": "Message",
      "item": [
        {
          "id": "8b24367a-765f-4b21-9e01-cde37ff7218b",
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
              "id": "95b42750-7f0b-4b38-ad09-fa9c3ac4f9a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "d0e46901-a666-419d-8f59-b3930a4f62c9",
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
              "id": "a44d1104-2903-4fac-95a1-87fe144dade1"
            }
          ]
        },
        {
          "id": "da294849-2b9f-48cd-8002-e265e79ac449",
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
              "id": "9b379716-72ea-416b-9bea-cd577f14d450"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:actionTarget",
      "item": [
        {
          "id": "d5deeac0-6cea-4476-ad45-c0238d3723bf",
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
              "id": "310f1d25-99e8-4297-984a-cbd7dfbec547"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:bot",
      "item": [
        {
          "id": "b5687158-1fec-4771-92d9-c3e8b0d6693d",
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
              "id": "ff82650a-883c-4d0d-b5a8-74a4815127c7"
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