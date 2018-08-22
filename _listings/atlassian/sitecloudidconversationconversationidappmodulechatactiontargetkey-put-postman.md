{
  "info": {
    "name": "Jira Software Cloud API Create or update a chat:actionTarget module",
    "_postman_id": "79ebe481-5937-4b6e-b75b-06bf765d4b17",
    "description": "Authentication required, with scope participate:conversation",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "e8783a90-3295-4d78-82fa-8b91a5c4af34",
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
              "id": "431ed896-1e5c-431f-940c-4e47f0b623e2"
            }
          ]
        },
        {
          "id": "8c9db219-c203-46e4-8e31-f4ec4d67ee95",
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
              "id": "143aa0f5-ffbf-434a-8b37-2d1da74f234f"
            }
          ]
        },
        {
          "id": "859055db-6167-42d0-9549-9963fdda583d",
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
              "id": "bf323f70-1d1d-456f-87de-13145027f626"
            }
          ]
        }
      ]
    },
    {
      "name": "Conversation",
      "item": [
        {
          "id": "7f725df8-83ab-491a-9e11-28d42b8bf6f7",
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
              "id": "4535ce88-d88a-473e-9c10-dddfa01a4e25"
            }
          ]
        },
        {
          "id": "0064cb6f-906b-41f2-8c59-e5b0d5e71edd",
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
              "id": "784c3368-2028-4eb4-b940-60be4f8a4377"
            }
          ]
        },
        {
          "id": "12ea9f4f-1db3-439c-b4e3-93082d79d5a2",
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
              "id": "6eb83f4b-23f8-4f77-a824-a82acdcb7de0"
            }
          ]
        }
      ]
    },
    {
      "name": "Direct",
      "item": [
        {
          "id": "f9c0f68d-9bda-43db-83a7-3a36f1416473",
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
              "id": "ba6896d8-095a-4527-b044-4528534e188c"
            }
          ]
        }
      ]
    },
    {
      "name": "Send",
      "item": [
        {
          "id": "71f76533-042a-4f9a-8d78-8e9cc6e7f6ff",
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
              "id": "510cab37-5c07-4439-9018-a9188d7dd9c3"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "ed2c4278-0a3f-4759-979a-95a41787c820",
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
              "id": "3f61dc4e-f830-46ff-9001-76e4cf264f0d"
            }
          ]
        }
      ]
    },
    {
      "name": "Message",
      "item": [
        {
          "id": "74034b1b-0184-45d9-8b4c-9fcf768e7dbc",
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
              "id": "b1cc737a-e52c-431d-b0a1-e31ccaef426a"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "065d102e-b0db-41bd-b8c3-bf051a163b62",
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
              "id": "527595ab-1a92-46f2-8f68-f5d85b3ea718"
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