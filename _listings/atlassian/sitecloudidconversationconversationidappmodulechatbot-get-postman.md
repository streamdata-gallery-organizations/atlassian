{
  "info": {
    "name": "Jira Software Cloud API Get a list of chat:bot modules",
    "_postman_id": "76a16bce-dba1-4d85-974b-9af59355e881",
    "description": "Authentication required, with scope participate:conversation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "41eb75f2-f62c-40b0-ac72-3a17b42c7f1e",
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
              "id": "0f043ef8-a77f-4a37-ab02-4e974e369dbf"
            }
          ]
        },
        {
          "id": "2c08e193-3716-4fc7-86da-af6227f9de4f",
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
              "id": "548edeec-d03d-481a-8cf2-f5fae7a21a8c"
            }
          ]
        },
        {
          "id": "849783c8-96a8-4bdd-bdbe-5c22f52fbb23",
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
              "id": "a9e26bd2-3d1c-4bbd-82a8-678a002dbd34"
            }
          ]
        },
        {
          "id": "5a515dac-0e8b-463f-bd34-19480d3c77d0",
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
              "id": "5090b51a-90be-4bb4-b84f-938dc96cb5e2"
            }
          ]
        }
      ]
    },
    {
      "name": "Conversation",
      "item": [
        {
          "id": "e9a52863-b9a7-4d08-ac30-e1cf25b54dc1",
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
              "id": "cd1f97d0-d547-475b-ad23-633e133263b7"
            }
          ]
        },
        {
          "id": "a4c20bb7-8803-4d74-b264-6660e6c5be0e",
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
              "id": "945fa04d-18b0-41ab-86ea-45cb5f63d432"
            }
          ]
        },
        {
          "id": "b2e9e95c-71ad-488a-ae74-b1c687b639ed",
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
              "id": "66925b79-bf04-496e-9c98-56d9327ab31b"
            }
          ]
        }
      ]
    },
    {
      "name": "Direct",
      "item": [
        {
          "id": "87a3be9a-c122-47b9-9fe6-1b0d28e2f044",
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
              "id": "c8589fdb-3286-478f-acf4-d02e0114cd3e"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "70d40c8d-00c2-4bdb-89fa-af9f5e835c1b",
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
              "id": "aba6ee09-af27-4a60-8415-36ec62460c07"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "59f64d8a-95ff-422a-b4d6-46759dcf9d6a",
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
              "id": "56ecb4a0-fc15-4a13-8562-2b22a30a9ccd"
            }
          ]
        }
      ]
    },
    {
      "name": "Message",
      "item": [
        {
          "id": "1bbd135d-2718-4bda-a7bd-6f65ddaa2c88",
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
              "id": "81c5b5ea-0982-4f5b-bf70-7040f3e98b50"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "56225e21-cb4c-4458-a0d2-9f7efdce21bd",
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
              "id": "4068f4cc-8ed8-4035-adc8-745bc60b2a0d"
            }
          ]
        }
      ]
    },
    {
      "name": "Chat:actionTarget",
      "item": [
        {
          "id": "1185c824-3f3c-4697-b0fc-18fc351efb8f",
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
              "id": "6074d2cd-b72f-4da8-8548-492040b42dd8"
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