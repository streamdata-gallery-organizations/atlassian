{
  "info": {
    "name": "Jira Software Cloud API Get a list of chat:glance modules",
    "_postman_id": "27e9c756-ab61-475e-8093-1b747bef78ba",
    "description": "Authentication required, with scope participate:conversation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "1f65f9b3-46f8-414f-a6ed-42c72b746aee",
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
              "id": "19048fc1-1307-47a1-a193-3cda8a24d011"
            }
          ]
        },
        {
          "id": "5395f175-8a92-4586-8a9e-9b2fa175ddcf",
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
              "id": "7543ede9-b2c2-4436-a7c8-040c1bc63245"
            }
          ]
        },
        {
          "id": "0a33c33d-bc83-4340-90a7-913e1923245d",
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
              "id": "d8f0a80b-b195-40ec-ae54-eca80ecfe0a0"
            }
          ]
        },
        {
          "id": "0d626cb5-d03c-4975-94d4-b2bf7dd69268",
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
              "id": "a4a2c645-59d9-44e7-a757-e955a6e55170"
            }
          ]
        },
        {
          "id": "d4deb744-d0b7-48cb-af70-5986a358ed99",
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
              "id": "e330b9ce-88b8-4aa0-a2d9-6cd467990805"
            }
          ]
        },
        {
          "id": "6ac7d22d-4478-40cf-8356-c9cb4625132d",
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
              "id": "20605c24-bf7f-471c-951a-db652bb842f1"
            }
          ]
        },
        {
          "id": "5c1d01a6-a5d6-4261-9c02-775b486e98b1",
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
              "id": "422cadbe-74a1-4edc-b8ed-ec4f2901600b"
            }
          ]
        },
        {
          "id": "ddedd73f-995c-406f-a40f-de9ed1e25cff",
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
              "id": "7526d1fe-d28e-412f-a115-83aa941069aa"
            }
          ]
        }
      ]
    },
    {
      "name": "Conversation",
      "item": [
        {
          "id": "4988cb9a-d9e7-41e0-92b0-5a6329b63844",
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
              "id": "62aa1c03-f489-4a4d-8972-c058abd373a3"
            }
          ]
        },
        {
          "id": "a0085c11-1204-4bd3-9d4c-d3563fda587e",
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
              "id": "43a38526-881a-4e02-ad7f-ebc9f4ec260c"
            }
          ]
        },
        {
          "id": "c7b2173a-4460-4567-928d-d7849552af29",
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
              "id": "24fdd418-1bdd-4348-878f-684137f0fd45"
            }
          ]
        }
      ]
    },
    {
      "name": "Direct",
      "item": [
        {
          "id": "5fffd260-2d1f-4eee-be9d-d58ada236e3a",
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
              "id": "0096bea4-ca40-4a3c-b746-57b4dccd53f4"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "ea0f9efd-092e-4bd9-a634-c90eebc6046a",
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
              "id": "cc565c4d-37fd-4a63-ba4f-dc5ec3fb757c"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "985adb0d-8e06-4708-941e-29cd8d8531de",
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
              "id": "50e7d123-5d00-4716-be60-fdf483c46dc5"
            }
          ]
        }
      ]
    },
    {
      "name": "Message",
      "item": [
        {
          "id": "5c31d8df-d323-4211-b639-4f56778344f6",
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
              "id": "58d380cf-5285-4851-ab81-eeed2ad0205a"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "4c9b5075-909a-4d5d-bd1e-acf3249415a1",
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
              "id": "23531f01-1be3-488a-ac28-6e1b4de84d15"
            }
          ]
        },
        {
          "id": "2e9a47e2-7999-485c-ad57-77cd18ee0c98",
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
              "id": "6ee4a2b2-c36e-4785-83bf-511187e669d1"
            }
          ]
        },
        {
          "id": "cd0051e1-a235-44d5-84c8-a0a9c0bcbe69",
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
              "id": "e8c83d4a-400b-4f48-a2f4-59f55cc2ff2e"
            }
          ]
        },
        {
          "id": "c8524f0c-5793-4ff8-b346-61c378a60923",
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
              "id": "d9f41ee0-5be7-48a5-be71-24319aa9e962"
            }
          ]
        },
        {
          "id": "d652d0e7-a3cf-4357-bddb-5b364cd74746",
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
              "id": "6f785185-095d-42da-9a52-462b7028243c"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:actionTarget",
      "item": [
        {
          "id": "4a25fc7e-787d-4d93-a8a4-3488ad26d29c",
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
              "id": "b1cb57e8-d34c-45c4-87c2-f4e64136ede6"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:bot",
      "item": [
        {
          "id": "cd8f1ea1-4002-4a95-adca-1d6daed3e491",
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
              "id": "e1e31618-4876-4e15-b3c4-79df0139f6a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:bot:messages",
      "item": [
        {
          "id": "b07ddd40-dc73-4d0d-b6e6-9c8f80158988",
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
              "id": "5c84d71f-e98f-41e2-b295-80a32723e32c"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:configuration",
      "item": [
        {
          "id": "db25967e-61d9-4ad6-8dab-e025d67d2e9a",
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
              "id": "4e0730f7-684e-47f2-aeec-b6a7e946a271"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:dialog",
      "item": [
        {
          "id": "47bcb6f8-59ad-4d96-b9cb-ab8b75e3c8ea",
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
              "id": "d4851f3d-87e1-45cc-a0dd-87fa60fcdabf"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:externalPage",
      "item": [
        {
          "id": "46cd911e-b0a0-47ce-a8ce-8146bb3c72be",
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
              "id": "51fdfab1-d36d-46ea-bfda-dd34782861ba"
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