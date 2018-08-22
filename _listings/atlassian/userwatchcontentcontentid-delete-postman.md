{
  "info": {
    "name": "Confluence Cloud API Remove content watcher",
    "_postman_id": "8ac5b631-11f9-4fff-9bf1-bdcafe035996",
    "description": "Removes a user as a watcher from a piece of content. Choose the user by \ndoing one of the following:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Audit",
      "item": [
        {
          "id": "61ffbd86-76e1-4ff7-9fff-282943e2a8a6",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.getAuditRecords_get",
          "request": {
            "url": "{{default}}/audit?endDate=%7B%7D&limit=%7B%7D&searchString=%7B%7D&start=%7B%7D&startDate=%7B%7D",
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
            "description": "Returns all records in the audit log, optionally for a certain date range. \nThis contains information about events like space exports, group membership \nchanges, app installations, etc. For more information, see \n[Audit log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html) \nin the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "98e0ebe9-a86e-4fa1-83c2-073e7f783f7b"
            }
          ]
        },
        {
          "id": "5b9676c2-1031-4185-8628-2225550e1757",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.createAuditRecord_post",
          "request": {
            "url": "{{default}}/audit",
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
            "description": "Creates a record in the audit log. \n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d50163e3-b1f1-450c-88bb-14537f10af7d"
            }
          ]
        },
        {
          "id": "01f82291-37f3-4212-9f19-b885fcd865fd",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.getAuditRecordsForTimePeriod_get",
          "request": {
            "url": "{{default}}/audit/since?limit=%7B%7D&number=%7B%7D&searchString=%7B%7D&start=%7B%7D&units=%7B%7D",
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
            "description": "Returns records from the audit log, for a time period back from the current \ndate. For example, you can use this method to get the last 3 months of records.\n\nThis contains information about events like space exports, group membership \nchanges, app installations, etc. For more information, see \n[Audit log](https://confluence.atlassian.com/confcloud/audit-log-802164269.html) \nin the Confluence administrator's guide.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bff39fba-cddb-4b34-9f47-5083d607556b"
            }
          ]
        }
      ]
    },
    {
      "name": "Export",
      "item": [
        {
          "id": "3b779519-fb2c-40a3-9e99-5edc041ce643",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.exportAuditRecords_get",
          "request": {
            "url": "{{default}}/audit/export?endDate=%7B%7D&format=%7B%7D&searchString=%7B%7D&startDate=%7B%7D",
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
            "description": "Exports audit records as a CSV file or ZIP file.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4e285d6-ec99-4d73-9dfa-b4bf9948bb50"
            }
          ]
        }
      ]
    },
    {
      "name": "Retention",
      "item": [
        {
          "id": "4f6b5afe-27d5-4e08-955b-d40fd0bf511c",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.getRetentionPeriod_get",
          "request": {
            "url": "{{default}}/audit/retention",
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
            "description": "Returns the retention period for records in the audit log. The retention \nperiod is how long an audit record is kept for, from creation date until \nit is deleted.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "17ea52fa-7351-4d56-97fe-bc025304ee9e"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "da3d4d07-153c-4a1e-91ea-38cd7e087527",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AuditResource.setRetentionPeriod_put",
          "request": {
            "url": "{{default}}/audit/retention",
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
            "description": "Sets the retention period for records in the audit log. The retention period \ncan be set to a maximum of 20 years.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "749c0069-4a8f-4c8e-a54d-a3bed650afa0"
            }
          ]
        },
        {
          "id": "98269603-066b-4bae-a72c-0e05f1cf6ced",
          "name": "com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.setLookAndFeelSettings_put",
          "request": {
            "url": "{{default}}/settings/lookandfeel/selected?spaceKey=%7B%7D",
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
            "description": "Sets the look and feel settings to either the default settings or the\ncustom settings, for the site or a single space. Note, the default \nspace settings are inherited from the current global settings.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ed5ddbeb-d56d-4121-8ddb-cb29548e9282"
            }
          ]
        },
        {
          "id": "a2dc2b41-6a05-4723-8608-e686b6e21ca7",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.setSpaceTheme_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/theme"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Sets the theme for a space. Note, if you want to reset the space theme to \nthe default Confluence theme, use the 'Reset space theme' method instead \nof this method.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "db8f9c5f-71e3-40e9-b2b1-93fb24766c8b"
            }
          ]
        }
      ]
    },
    {
      "name": "Content",
      "item": [
        {
          "id": "01ba1a9a-c4fd-4d42-843a-49a0a2b2025e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.getContent_get",
          "request": {
            "url": "{{default}}/content?expand=%7B%7D&limit=%7B%7D&orderby=%7B%7D&postingDay=%7B%7D&spaceKey=%7B%7D&start=%7B%7D&status=%7B%7D&title=%7B%7D&trigger=%7B%7D&type=%7B%7D",
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
            "description": "Returns all content in a Confluence instance.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission). \nOnly content that the user has permission to view will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5a31e2b6-e9d4-4cda-a77a-d1d932bf0ef3"
            }
          ]
        },
        {
          "id": "50beba23-a738-46ef-9c61-5cc1af2f7c57",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.createContent_post",
          "request": {
            "url": "{{default}}/content?expand=%7B%7D&status=%7B%7D",
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
            "description": "Creates a new piece of content or publishes an existing draft. \n\nTo publish a draft, add the `id` and `status` properties to the body of the request. \nSet the `id` to the ID of the draft and set the `status` to 'current'. When the \nrequest is sent, a new piece of content will be created and the metadata from the \ndraft will be transferred into it.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'Add' permission for the \nspace that the content will be created in, and permission to view the draft if publishing a draft."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6019f5eb-8241-42bd-8f79-af979c26bea3"
            }
          ]
        },
        {
          "id": "7a305587-c548-4060-a0ce-70daca3740d3",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.getContentById_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id"
              ],
              "query": [
                {
                  "key": "embeddedContentRender",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "trigger",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "version",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Returns a single piece of content, like a page or a blog post.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3ed3e285-ecc5-48aa-87c2-4c5eed00069b"
            }
          ]
        },
        {
          "id": "7998d1ff-07a4-4ea2-a7ae-1124cd71ed37",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.updateContent_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id"
              ],
              "query": [
                {
                  "key": "conflictPolicy",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Updates a piece of content. Use this method to update the title or body \nof a piece of content, change the status, change the parent page, and more.\n\nNote, updating draft content is currently not supported.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b073f278-f482-45bc-ae83-e5ff11e3044b"
            }
          ]
        },
        {
          "id": "7771711a-8536-4c2e-be4c-9b9f44b5c353",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.deleteContent_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Moves a piece of content to the space's trash or purges it from the trash, \ndepending on the content's type and status:\n\n- If the content's type is `page` or `blogpost` and its status is `current`, \nit will be trashed.\n- If the content's type is `page` or `blogpost` and its status is `trashed`, \nthe content will be purged from the trash and deleted permanently. Note, \nyou must also set the `status` query parameter to `trashed` in your request.\n- If the content's type is `comment` or `attachment`, it will be deleted \npermanently without being trashed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Delete' permission for the space that the content is in, and permission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5bcfe356-6c78-4b17-90f7-8f60f86c5a6a"
            }
          ]
        },
        {
          "id": "07ac87b2-3034-4dfa-bb4d-455b9dc600ec",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentChildren_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "parentVersion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Returns a map of the direct children of a piece of content. A piece of content \nhas different types of child content, depending on its type. These are \nthe default parent-child content type relationships:\n\n- `page`: child content is `page`, `comment`, `attachment`\n- `blogpost`: child content is `comment`, `attachment`\n- `attachment`: child content is `comment`\n- `comment`: child content is `attachment`\n\nApps can override these default relationships. Apps can also introduce \nnew content types that create new parent-child content relationships.\n\nNote, the map will always include all child content types that are valid \nfor the content. However, if the content has no instances of a child content \ntype, the map will contain an empty array for that child content type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'View' permission for the space, \nand permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "84ce7374-fa81-4738-993b-2cbabca5e753"
            }
          ]
        },
        {
          "id": "592d4eb2-bc5f-4987-9980-6c91f9056042",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentComments_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/comment"
              ],
              "query": [
                {
                  "key": "depth",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "location",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "parentVersion",
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
                  "id": "id",
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
            "description": "Returns the comments on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'View' permission for the space, \nand permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dc0e4cdf-de8d-41e6-ad4c-cbaa30e57ccc"
            }
          ]
        },
        {
          "id": "4d70b2d6-1531-4a91-a58c-7e87bd7f9524",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ChildContentResource.getContentChildrenByType_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/:type"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "parentVersion",
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
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "type",
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
            "description": "Returns all children of a given type, for a piece of content. \nA piece of content has different types of child content, depending on its type:\n\n- `page`: child content is `page`, `comment`, `attachment`\n- `blogpost`: child content is `comment`, `attachment`\n- `attachment`: child content is `comment`\n- `comment`: child content is `attachment`\n\nCustom content types that are provided by apps can also be returned.\n\nNote, this method only returns direct children. To return children at all \nlevels, use [Get descendants by type](#api-content-id-descendant-type-get).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: 'View' permission for the space, \nand permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "564f42f9-c8ca-45a3-8398-8609b8d1c58c"
            }
          ]
        },
        {
          "id": "b3a71866-0fa2-40db-861e-14391c64d83a",
          "name": "com.atlassian.confluence.plugins.restapi.resources.DescendantContentResource.getContentDescendants_g",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/descendant"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Returns a map of the descendants of a piece of content. This is similar \nto [Get content children](#api-content-id-child-get), except that this \nmethod returns child pages at all levels, rather than just the direct \nchild pages.\n\nA piece of content has different types of descendants, depending on its type:\n\n- `page`: descendant is `page`, `comment`, `attachment`\n- `blogpost`: descendant is `comment`, `attachment`\n- `attachment`: descendant is `comment`\n- `comment`: descendant is `attachment`\n\nThe map will always include all descendant types that are valid for the content. \nHowever, if the content has no instances of a descendant type, the map will \ncontain an empty array for that descendant type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it \nis a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d06f80af-9ef7-4a49-be3b-76710e4e5428"
            }
          ]
        },
        {
          "id": "f60669e1-18a2-4c4a-8aa7-07bd7160b189",
          "name": "com.atlassian.confluence.plugins.restapi.resources.DescendantContentResource.descendantsOfType_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/descendant/:type"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "type",
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
            "description": "Returns all descendants of a given type, for a piece of content. This is \nsimilar to [Get content children by type](#api-content-id-child-type-get), \nexcept that this method returns child pages at all levels, rather than just \nthe direct child pages.\n\nA piece of content has different types of descendants, depending on its type:\n\n- `page`: descendant is `page`, `comment`, `attachment`\n- `blogpost`: descendant is `comment`, `attachment`\n- `attachment`: descendant is `comment`\n- `comment`: descendant is `attachment`\n\nCustom content types that are provided by apps can also be returned.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it \nis a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "10924194-cca2-435c-bea6-47f963a97aca"
            }
          ]
        },
        {
          "id": "27a3a9d6-d574-4556-a734-7441d95ba169",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.getContentProperties_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "id",
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
            "description": "Returns the properties for a piece of content. For more information \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b9441130-d048-453c-a4be-ed4d02545292"
            }
          ]
        },
        {
          "id": "64b7cbca-00dc-4f94-9aa6-2fd426c71926",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.createContentProperty_pos",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property"
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Creates a property for an existing piece of content. For more information \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis is the same as [Create content property for key](#api-content-id-property-key-post) \nexcept that the key is specified in the request body instead of as a \npath parameter.\n\nContent properties can also be added when creating a new piece of content \nby including them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31985457-43c2-41c1-8b5c-dd9c78eb1a05"
            }
          ]
        },
        {
          "id": "b401c2ee-5bed-4018-88f4-5a16bd673ab1",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.getContentProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Returns a content property for a piece of content. For more information, see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space, and permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d86319df-6a32-4cee-a043-082546d5773c"
            }
          ]
        },
        {
          "id": "c93ff614-042a-462b-8bf0-4c0a19234b27",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.updateContentProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Updates an existing content property. This method will also create a new \nproperty for a piece of content, if the property key does not exist and \nthe property version is 1. For more information about content properties, see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5fa99d7d-df58-4db0-9982-6fac96e42795"
            }
          ]
        },
        {
          "id": "ecd1e367-8e49-4f0b-8aea-9ec2f219266d",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.createContentPropertyForK",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Creates a property for an existing piece of content. For more information \nabout content properties, see [Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\nThis is the same as [Create content property](#api-content-id-property-post) \nexcept that the key is specified as a path parameter instead of in the \nrequest body.\n\nContent properties can also be added when creating a new piece of content \nby including them in the `metadata.properties` of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e334ebb9-9c00-4d6e-8be3-dd3a1acf5f9a"
            }
          ]
        },
        {
          "id": "88ab215f-fee0-4fb1-b65e-ddca9d969c7b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentPropertyResource.deleteContentProperty_del",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/property/:key"
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Deletes a content property. For more information about content properties, see \n[Content properties in the REST API](https://developer.atlassian.com/cloud/confluence/content-properties/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "580df2a1-b38f-41ea-b4c4-ad912babf06e"
            }
          ]
        },
        {
          "id": "26602889-9e8b-47dc-b89b-a7d9b5e5d754",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getContentRestrictionS",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/group/:groupName"
              ],
              "variable": [
                {
                  "id": "groupName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
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
            "description": "Returns whether the specified content restriction applies to a group. \nFor example, if the 'admins' group has permission to read a page with an \nID of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/group/admins`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3feadd9e-1489-475e-89a6-a850673f8726"
            }
          ]
        },
        {
          "id": "5f71faed-8778-4f33-9c22-39ad3bee5fef",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getContentRestrictionS",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/user"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "userName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
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
            "description": "Returns whether the specified content restriction applies to a user. \nFor example, if the user 'admin' has permission to read a page with an \nID of 123, then the following request will return true:\n\n`https://your-domain.atlassian.net/wiki/rest/api/content/123/restriction/byOperation/read/user?username=admin`\n\nOne of `key`, `username`, or `accountId` must be specified as a query \nparameter to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca7c79c6-0321-4904-a561-d611ce266edf"
            }
          ]
        },
        {
          "id": "c3fbc8a8-728d-449b-a1b6-d377fa2f17ec",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.getContentVersions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/version"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "id",
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
            "description": "Returns the versions for a piece of content in descending order.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8af99015-d66b-4274-bd26-e3f187fcb53d"
            }
          ]
        },
        {
          "id": "0e4b8c5f-4120-4ef9-b633-cbee51f4ebe4",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.getContentVersion_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/version/:versionNumber"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "versionNumber",
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
            "description": "Returns a version for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0e5dc0cf-474c-4dc8-826d-da2c266ccf43"
            }
          ]
        },
        {
          "id": "9c7da04d-b7ac-46ec-8ad5-0a38ca3606ea",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.deleteContentVersion_delet",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/version/:versionNumber"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "versionNumber",
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
            "description": "Delete a historical version. This does not delete the changes made to the \ncontent in that version, rather the changes for the deleted version are \nrolled up into the next version. Note, you cannot delete the current version.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9aecb72d-9964-47cd-a160-09305a053d23"
            }
          ]
        },
        {
          "id": "81196a65-66c7-40a0-8663-24233e1ee2cc",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getContentByTypeForSpace_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/content/:type"
              ],
              "query": [
                {
                  "key": "depth",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "spaceKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "type",
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
            "description": "Returns all content of a given type, in a space. The returned content is\nordered by content ID in ascending order.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'View' permission for the space. Note, the returned list will only\ncontain content that the current user has permission to view."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9759bc6c-fb0a-4d81-9e9b-1333d93d9f31"
            }
          ]
        },
        {
          "id": "8a56a0b9-4efb-4af6-bff1-27d59c9d5d4c",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.updateContentTemplate_put",
          "request": {
            "url": "{{default}}/template",
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
            "description": "Updates a content template. Note, blueprint templates cannot be updated\nvia the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to create a space template or 'Confluence Administrator' \nglobal permission to create a global template."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1c36c09e-f676-4cb8-94c3-a4660cb3113d"
            }
          ]
        },
        {
          "id": "ca0e8c8c-7802-4f3a-b7b8-f543b6b4bac3",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.createContentTemplate_post",
          "request": {
            "url": "{{default}}/template",
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
            "description": "Creates a new content template. Note, blueprint templates cannot be created via the REST API.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to create a space template or 'Confluence Administrator' \nglobal permission to create a global template."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ac54f8d0-b75b-434a-ab43-dbcc67636691"
            }
          ]
        },
        {
          "id": "91ff592c-5a57-4c8e-b33c-73fc244fbbae",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getContentTemplates_get",
          "request": {
            "url": "{{default}}/template/page?expand=%7B%7D&limit=%7B%7D&spaceKey=%7B%7D&start=%7B%7D",
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
            "description": "Returns all content templates. Use this method to retrieve all global\ncontent templates or all content templates in a space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to view space templates and 'Confluence \nAdministrator' global permission to view global templates."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a160f7e8-b0f6-45ae-870f-159a893a6221"
            }
          ]
        },
        {
          "id": "2a62d20c-7b9c-4aa2-b097-873c1c6c84ff",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getContentTemplate_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "template/:contentTemplateId"
              ],
              "variable": [
                {
                  "id": "contentTemplateId",
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
            "description": "Returns a content template. This includes information about template, \nlike the name, the space or blueprint that the template is in, the body \nof the template, and more.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space to view space templates and 'Confluence \nAdministrator' global permission to view global templates."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f12c135e-29d3-4d0b-9124-8677a54b5859"
            }
          ]
        },
        {
          "id": "a0630a60-a702-4480-bf92-a32ba4b0720b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.getContentWatchStatus_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "user/watch/content/:contentId"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "username",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contentId",
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
            "description": "Returns whether a user is watching a piece of content. Choose the user by \ndoing one of the following:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "815aa970-2654-4be3-a291-7880c65b37d2"
            }
          ]
        },
        {
          "id": "668fbf28-0a86-478a-8e4e-069e8436f53f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.addContentWatcher_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "user/watch/content/:contentId"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "username",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contentId",
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
            "description": "Adds a user as a watcher to a piece of content. Choose the user by doing \none of the following:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\nNote, you must add the `X-Atlassian-Token: no-check` header when making a \nrequest, as this operation has XSRF protection.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec7ae7cb-3e3c-4987-9e9c-ce9c5e831fc3"
            }
          ]
        }
      ]
    },
    {
      "name": "Publish",
      "item": [
        {
          "id": "e5e13344-364b-4802-8865-f50caca3576c",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentBlueprintResource.publishSharedDraft_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/blueprint/instance/:draftId"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "draftId",
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
            "description": "Publishes a shared draft of a page created from a blueprint.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the draft and 'Add' permission for the space that \nthe content will be created in."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca9e1ba2-9634-43cc-898a-ad1315151e1b"
            }
          ]
        },
        {
          "id": "430ed419-222c-4921-8216-c9f91f7ce4a7",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentBlueprintResource.publishLegacyDraft_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/blueprint/instance/:draftId"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "draftId",
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
            "description": "Publishes a legacy draft of a page created from a blueprint. Legacy drafts \nwill eventually be removed in favour of shared drafts. For now, this method \nworks the same as [Publish shared draft](#api-content-blueprint-instance-draftId-put).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the draft and 'Add' permission for the space that \nthe content will be created in."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "71f88bc2-fc3d-4b71-bb30-0a3f792d041b"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "85080b21-735a-47d3-8dcc-8ed19ee31967",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.searchContentByCQL_get",
          "request": {
            "url": "{{default}}/content/search?cql=%7B%7D&cqlcontext=%7B%7D&expand=%7B%7D&limit=%7B%7D&start=%7B%7D",
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
            "description": "Returns the list of content that matches a Confluence Query Language \n(CQL) query. For information on CQL, see: \n[Advanced searching using CQL](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission). \nOnly content that the user has permission to view will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a37bd8f5-ff0d-4e6c-958b-71e4ed411ab3"
            }
          ]
        },
        {
          "id": "1568c315-c239-4633-b563-c5c6c6f00860",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SearchResource.search_get",
          "request": {
            "url": "{{default}}/search?cql=%7B%7D&cqlcontext=%7B%7D&includeArchivedSpaces=%7B%7D&limit=%7B%7D&start=%7B%7D",
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
            "description": "Searches for content using the \n[Confluence Query Language (CQL)](https://developer.atlassian.com/cloud/confluence/advanced-searching-using-cql/)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the entities. Note, only entities that the user has \npermission to view will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e369d86c-68cc-4871-925c-288f3c560e95"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachments",
      "item": [
        {
          "id": "fdd8a276-397b-430c-b32b-028343522aa7",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.getAttachments_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "filename",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "mediaType",
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
                  "id": "id",
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
            "description": "Returns the attachments for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content. If the content is a blog post, 'View' permission \nfor the space is required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ab84d8d6-770a-4146-8f96-c87964ce4b0c"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "9c8cbab2-11bd-4001-ac6d-3e8920073e93",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.createOrUpdateAttachments_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Adds an attachment to a piece of content. If the attachment already exists \nfor the content, then the attachment is updated (i.e. a new version of the \nattachment is created).\n\nNote, you must set a `X-Atlassian-Token: nocheck` header on the request \nfor this method, otherwise it will be blocked. This protects against XSRF \nattacks, which is necessary as this method accepts multipart/form-data.\n\nThe media type 'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client libraries have classes that make it easier to implement \nmultipart posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) \nJava class provided by Apache HTTP Components.\n\nExample: This curl command attaches a file ('example.txt') to a piece of \ncontent (id='123') with a comment and `minorEdits`=true. If the 'example.txt' \nfile already exists, it will update it with a new version of the attachment.\n\n``` bash\ncurl -D- \\\n  -u admin:admin \\\n  -X PUT \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "38f9e5cf-49b8-40eb-89b9-93ac1ff29362"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "5ac85a6a-d753-430d-9007-2ffef9e64765",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.createAttachments_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment"
              ],
              "query": [
                {
                  "key": "status",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Adds an attachment to a piece of content. This method only adds a new \nattachment. If you want to update an existing attachment, use \n[Create or update attachments](#api-content-id-child-attachment-put).\n\nNote, you must set a `X-Atlassian-Token: nocheck` header on the request \nfor this method, otherwise it will be blocked. This protects against XSRF \nattacks, which is necessary as this method accepts multipart/form-data.\n\nThe media type 'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client libraries have classes that make it easier to implement \nmultipart posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) \nJava class provided by Apache HTTP Components.\n\nExample: This curl command attaches a file ('example.txt') to a container \n(id='123') with a comment and `minorEdits`=true.\n\n``` bash\ncurl -D- \\\n  -u admin:admin \\\n  -X POST \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2f71fb0e-d51b-4fc6-9e40-af8b4f9b7c4a"
            }
          ]
        },
        {
          "id": "c59e0857-03a3-44bd-a766-74d4eabfd755",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.updateAttachmentProperties_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment/:attachmentId"
              ],
              "variable": [
                {
                  "id": "attachmentId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
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
            "description": "Updates the attachment properties, i.e. the non-binary data of an attachment \nlike the filename, media-type, comment, and parent container.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c74d483b-8638-414b-b209-e7cffbc9385f"
            }
          ]
        },
        {
          "id": "edcadca7-a919-4a32-bfff-79fa4b3e28c0",
          "name": "com.atlassian.confluence.plugins.restapi.resources.AttachmentResource.updateAttachmentData_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/child/attachment/:attachmentId/data"
              ],
              "variable": [
                {
                  "id": "attachmentId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
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
            "description": "Updates the binary data of an attachment, given the attachment ID, and \noptionally the comment and the minor edit field.\n\nThis method is essentially the same as [Create or update attachments](#api-content-id-child-attachment-put), \nexcept that it matches the attachment ID rather than the name.\n\nNote, you must set a `X-Atlassian-Token: nocheck` header on the request \nfor this method, otherwise it will be blocked. This protects against XSRF \nattacks, which is necessary as this method accepts multipart/form-data.\n\nThe media type 'multipart/form-data' is defined in [RFC 1867](https://www.ietf.org/rfc/rfc1867.txt). \nMost client libraries have classes that make it easier to implement \nmultipart posts, like the [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) \nJava class provided by Apache HTTP Components.\n\nExample: This curl command updates an attachment (id='att456') that is attached  \nto a piece of content (id='123') with a comment and `minorEdits`=true. \n\n``` bash\ncurl -D- \\\n  -u admin:admin \\\n  -X POST \\\n  -H \"X-Atlassian-Token: nocheck\" \\\n  -F \"file=@example.txt\" \\\n  -F \"minorEdit=true\" \\\n  -F \"comment=Example attachment comment\" \\\n  http://myhost/rest/api/content/123/child/attachment/att456/data\n```\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f6b77820-632d-4400-b204-056eb6e02fc4"
            }
          ]
        }
      ]
    },
    {
      "name": "Historycontent",
      "item": [
        {
          "id": "359e49d9-11fc-4b49-bc30-735983a4a834",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.getHistoryForContent_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/history"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Returns the most recent update for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: Permission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c43cc27-e276-427a-b380-1c6f7427b24f"
            }
          ]
        }
      ]
    },
    {
      "name": "Macro",
      "item": [
        {
          "id": "ce322931-a2b5-4684-904a-afff19353bcc",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentResource.getMacroBodyByMacroId_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/history/:version/macro/id/:macroId"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "macroId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "version",
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
            "description": "Returns the body of a macro in storage format, for the given macro ID. \nThis includes information like the name of the macro, the body of the macro, \nand any macro parameters. This method is mainly used by Cloud apps.\n\nAbout the macro ID: When a macro is created in a new version of content, \nConfluence will generate a random ID for it, unless an ID is specified \n(by an app). The macro ID will look similar to this: '50884bd9-0cb8-41d5-98be-f80943c14f96'. \nThe ID is then persisted as new versions of content are created, and is \nonly modified by Confluence if there are conflicting IDs.\n\nNote, to preserve backwards compatibility this resource will also match on \nthe hash of the macro body, even if a macro ID is found. This check will \neventually become redundant, as macro IDs are generated for pages and \ntransparently propagate out to all instances.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content that the macro is in."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "614b079a-2805-451b-af88-98d5e85c05ab"
            }
          ]
        }
      ]
    },
    {
      "name": "Labelscontent",
      "item": [
        {
          "id": "46c3b110-6d67-4614-903d-702d9b989ea5",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.getLabelsForContent_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/label"
              ],
              "query": [
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "prefix",
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
                  "id": "id",
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
            "description": "Returns the labels on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'View' permission for the space and permission to view the content if it is a page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3e00f094-58ff-4feb-ba41-785536b49480"
            }
          ]
        }
      ]
    },
    {
      "name": "Labels",
      "item": [
        {
          "id": "854a9647-cc6e-4ced-9931-95891eb75d0d",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.addLabelsToContent_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/label"
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Adds labels to a piece of content. Does not modify the existing labels.\n\nNotes:\n\n- Labels can also be added when creating content ([Create content](#api-content-post)).\n- Labels can be updated when updating content ([Update content](#api-content-id-put)). \nThis will delete the existing labels and replace them with the labels in \nthe request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b29ea2ee-d1b2-4aa0-ba88-0ed23cad051d"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "2c7e8061-3c2d-4b0d-aeae-403cbafb7d7f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.removeLabelFromContentUsing",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/label"
              ],
              "query": [
                {
                  "key": "name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Removes a label from a piece of content. This is similar to \n[Remove label from content](#api-content-id-label-label-delete) \nexcept that the label name is specified via a query parameter. \n\nUse this method if the label name has \"/\" characters, as \n[Remove label from content using query parameter](#api-content-id-label-delete) \ndoes not accept \"/\" characters for the label name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "11a72a86-9aa6-45a8-9adc-3d48039de8a5"
            }
          ]
        },
        {
          "id": "0e8be83f-96c6-4f94-bc81-1e357dec1244",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentLabelsResource.removeLabelFromContent_dele",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/label/:label"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "label",
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
            "description": "Removes a label from a piece of content. This is similar to \n[Remove label from content using query parameter](#api-content-id-label-delete) \nexcept that the label name is specified via a path parameter. \n\nUse this method if the label name does not have \"/\" characters, as the path \nparameter does not accept \"/\" characters for security reasons. Otherwise, \nuse [Remove label from content using query parameter](#api-content-id-label-delete).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5f6163f0-b810-4536-b2db-7b13c4cf9325"
            }
          ]
        },
        {
          "id": "d839f944-9f6e-456b-a8a0-48d365628440",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.removeGroupFromContent",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/group/:groupName"
              ],
              "variable": [
                {
                  "id": "groupName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
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
            "description": "Removes a group from a content restriction. That is, remove read or update \npermission for the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "264307ee-1e2d-4a3d-8200-917ba8bd4e58"
            }
          ]
        },
        {
          "id": "0cb7629e-4e1d-446f-b6f9-bb58b693674c",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.removeUserFromContentR",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/user"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "userName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
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
            "description": "Removes a group from a content restriction. That is, remove read or update \npermission for the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aeee2b20-0c99-4ee1-bfa0-c18e007b3ad6"
            }
          ]
        },
        {
          "id": "1e1c8e08-dd6b-4af7-9dce-0dabd2266eb1",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.removeTemplate_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "template/:contentTemplateId"
              ],
              "variable": [
                {
                  "id": "contentTemplateId",
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
            "description": "Deletes a template. This results in different actions depending on the \ntype of template:\n\n- If the template is a content template, it is deleted.\n- If the template is a modified space-level blueprint template, it reverts \nto the template inherited from the global-level blueprint template.\n- If the template is a modified global-level blueprint template, it reverts \nto the default global-level blueprint template.\n\n Note, unmodified blueprint templates cannot be deleted."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "35df76aa-49b1-46bf-a70b-296d0ca6ca6f"
            }
          ]
        },
        {
          "id": "073ad639-632a-485d-9caa-b8233ac839a0",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserWatchResource.removeContentWatcher_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "user/watch/content/:contentId"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "username",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contentId",
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
            "description": "Removes a user as a watcher from a piece of content. Choose the user by \ndoing one of the following:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "09ec5e24-7828-4b5f-98d7-04b6b08a7655"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchespage",
      "item": [
        {
          "id": "2727f277-8d9f-4fe9-9d18-0859d7689477",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentNotificationsResource.getWatchesForPage_ge",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/notification/child-created"
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
                  "id": "id",
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
            "description": "Returns the watches for a page. A user that watches a page will receive \nreceive notifications when the page is updated.\n\nIf you want to manage watches for a page, use the following `user` methods:\n\n- [Get content watch status for user](#api-user-watch-content-contentId-get)\n- [Add content watch](#api-user-watch-content-contentId-post)\n- [Remove content watch](#api-user-watch-content-contentId-delete)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3750fb12-9903-4872-99a6-29de702d579e"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchesspace",
      "item": [
        {
          "id": "2462db3b-3e8f-4a4e-8eb7-1932ac04f64b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentNotificationsResource.getWatchesForSpace_g",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/notification/created"
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
                  "id": "id",
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
            "description": "Returns all space watches for the space that the content is in. A user that \nwatches a space will receive receive notifications when any content in the \nspace is updated.\n\nIf you want to manage watches for a space, use the following `user` methods:\n\n- [Get space watch status for user](#api-user-watch-space-spaceKey-get)\n- [Add space watch](#api-user-watch-space-spaceKey-post)\n- [Remove space watch](#api-user-watch-space-spaceKey-delete)\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b9b94c7-b3d2-45ed-b49b-2df758e5a1b2"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "bfb0554f-3ed3-4ea6-8d49-eaecd7b325a8",
          "name": "com.atlassian.confluence.plugins.restapi.resources.PageHierarchyResource.copyPageHierarchy_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/pagehierarchy/copy"
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Copy page hierarchy allows the copying of an entire hierarchy of pages and their associated properties, permissions and attachments.\n The id path parameter refers to the content id of the page to copy, and the new parent of this copied page is defined using the destinationPageId in the request body.\n The titleOptions object defines the rules of renaming page titles during the copy;\n for example, search and replace can be used in conjunction to rewrite the copied page titles.\n\n Response example:\n <pre><code>\n {\n      \"id\" : \"1180606\",\n      \"links\" : {\n           \"status\" : \"/rest/api/longtask/1180606\"\n      }\n }\n </code></pre>\n Use the /longtask/<taskId> REST API to get the copy task status."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1908ec79-cf1c-4107-b74e-552e93f1b5f5"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictions",
      "item": [
        {
          "id": "12345640-0eda-4094-8f70-096e566d986b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getRestrictions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "id",
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
            "description": "Returns the restrictions on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "214edb1d-68a3-40a7-a7e8-f8c4968e418c"
            }
          ]
        },
        {
          "id": "0bacee93-6eb6-407e-9c92-761294430283",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.updateRestrictions_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Updates restrictions for a piece of content. This removes the existing \nrestrictions and replaces them with the restrictions in the request.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ffb16374-e1ea-4c53-9041-142510b84771"
            }
          ]
        },
        {
          "id": "c57ecd51-2c02-47fd-8e29-017c308e90f1",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.addRestrictions_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Adds restrictions to a piece of content. Note, this does not change any \nexisting restrictions on the content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5230962b-f3d5-4680-9cab-dcc33c089a9d"
            }
          ]
        },
        {
          "id": "52931383-9ee0-432f-b6b7-f49aa74de27c",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.deleteRestrictions_del",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Removes all restrictions (read and update) on a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "392434c8-38d5-41fe-ab23-d38c38c9f6a9"
            }
          ]
        },
        {
          "id": "20ee37f2-606c-481f-9b87-0a803138d63b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getRestrictionsByOpera",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Returns restrictions on a piece of content by operation. This method is \nsimilar to [Get restrictions](#api-content-id-restriction-get) except that \nthe operations are properties of the return object, rather than items in \na results array. \n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a50f38d0-787f-4bfd-bc82-1157576dda49"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictionsoperation",
      "item": [
        {
          "id": "915608fa-6818-4bff-a542-d9645bf27e55",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.getRestrictionsForOper",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
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
            "description": "Returns the restictions on a piece of content for a given operation (read \nor update).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c393de0c-8271-4718-9efa-2bca3afc39cb"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "efd134c4-0bd8-4873-895f-2390bbecab48",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.addGroupToContentRestr",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/group/:groupName"
              ],
              "variable": [
                {
                  "id": "groupName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
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
            "description": "Adds a group to a content restriction. That is, grant read or update \npermission to the group for a piece of content.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2134c5d4-e62d-4e80-abc4-224977ce77ef"
            }
          ]
        },
        {
          "id": "fcf94b5b-916a-48c2-b832-5498b521f10f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.GroupResource.getGroup_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "group/:groupName"
              ],
              "variable": [
                {
                  "id": "groupName",
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
            "description": "Returns a user group for a given group name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "77f823f1-f046-498f-9cde-797d75698251"
            }
          ]
        },
        {
          "id": "da38756a-d7e7-4da9-b11b-ad89fb68a623",
          "name": "com.atlassian.confluence.plugins.restapi.resources.GroupResource.getGroupMembers_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "group/:groupName/member"
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
                  "id": "groupName",
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
            "description": "Returns the users that are members of a group.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f9d191b-850d-4aa5-8ee4-7965fbb47f18"
            }
          ]
        },
        {
          "id": "cada433e-dfe4-45dd-a98e-2e2288bb9d3b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserResource.getGroupMembershipsForUser_get",
          "request": {
            "url": "{{default}}/user/memberof?accountId=%7B%7D&key=%7B%7D&limit=%7B%7D&start=%7B%7D&username=%7B%7D",
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
            "description": "Returns the groups that a user is a member of.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c6ba4a7-0f21-40c2-a311-eb005f8ae04b"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "dfd5ec56-d97e-473f-a3e4-e7650f693fff",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentRestrictionResource.addUserToContentRestri",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/restriction/byOperation/:operationKey/user"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "userName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "operationKey",
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
            "description": "Adds a user to a content restriction. That is, grant read or update \npermission to the user for a piece of content.\n\nOne of `key`, `username`, or `accountId` must be specified as a query \nparameter to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to edit the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "908d5719-90b1-4d72-b3fe-1fdedcdc9cc5"
            }
          ]
        },
        {
          "id": "bbfff498-56b8-4668-8dc3-9d9d03196fdf",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserResource.getUser_get",
          "request": {
            "url": "{{default}}/user?accountId=%7B%7D&expand=%7B%7D&key=%7B%7D&username=%7B%7D",
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
            "description": "Returns a user. This includes information about the user, like the\ndisplay name, userKey, account ID, profile picture, and more.\n\nThe `username`, `key`, or `accountId` parameter must be specified, in \norder to identify the user.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4c13e193-9a64-444e-8aab-d41e633d8ff8"
            }
          ]
        }
      ]
    },
    {
      "name": "Restore",
      "item": [
        {
          "id": "34cf436f-1aa3-4827-be21-bf074ca0f170",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentVersionResource.restoreContentVersion_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "content/:id/version"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Restores a historical version to be the latest version. That is, a new version \nis created with the content of the historical version.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to update the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "330059bc-c127-47a3-bce1-ed34d3f4fa30"
            }
          ]
        }
      ]
    },
    {
      "name": "Convert",
      "item": [
        {
          "id": "694a4267-3cc5-4058-be98-49972efa417f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ContentBodyResource.convertContentBody_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "contentbody/convert/:to"
              ],
              "query": [
                {
                  "key": "contentIdContext",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "embeddedContentRender",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "spaceKeyContext",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "to",
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
            "description": "Converts a content body from one format to another format.\n\nSupported conversions:\n\n- storage: view, export_view, styled_view, editor\n- editor: storage\n- view: none\n- export_view: none\n- styled_view: none\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nIf request specifies 'contentIdContext', 'View' permission for the space, and permission to view the content."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4b6457c3-85b3-4486-8209-747e75e621ec"
            }
          ]
        }
      ]
    },
    {
      "name": "Groups",
      "item": [
        {
          "id": "978a7620-4a5b-472d-ae90-ca312e10dd71",
          "name": "com.atlassian.confluence.plugins.restapi.resources.GroupResource.getGroups_get",
          "request": {
            "url": "{{default}}/group?limit=%7B%7D&start=%7B%7D",
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
            "description": "Returns all user groups. The returned groups are ordered alphabetically in\nascending order by group name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "16d3fe1b-c208-4bbd-8e89-7879ba84ef44"
            }
          ]
        }
      ]
    },
    {
      "name": "Long-running",
      "item": [
        {
          "id": "b9bc92bb-9910-43ff-b58a-25200c5f3f4d",
          "name": "com.atlassian.confluence.plugins.restapi.resources.LongTaskResource.getTasks_get",
          "request": {
            "url": "{{default}}/longtask?limit=%7B%7D&start=%7B%7D",
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
            "description": "Returns information about all active long-running tasks (e.g. space export), \nsuch as how long each task has been running and the percentage of each task \nthat has completed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "76e871f7-e32b-4460-a497-bceda232a406"
            }
          ]
        },
        {
          "id": "7ef041fd-3aec-40fc-9b30-0f14dba266f3",
          "name": "com.atlassian.confluence.plugins.restapi.resources.LongTaskResource.getTask_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "longtask/:id"
              ],
              "variable": [
                {
                  "id": "id",
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
            "description": "Returns information about an active long-running task (e.g. space export), \nsuch as how long it has been running and the percentage of the task that \nhas completed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5497e96-51b9-4d67-9670-abc54d639ead"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "f6ab11fa-ec50-4a3a-94ea-024b6a16c285",
          "name": "com.atlassian.confluence.plugins.restapi.resources.RelationResource.findTargetFromSource_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "relation/:relationName/from/:sourceType/:sourceKey/to/:targetType"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceVersion",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetVersion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "relationName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceType",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetType",
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
            "description": "Returns all target entities that have a particular relationship to the \nsource entity. Note, relationships are one way.\n\nFor example, the following method finds all content that the current user \nhas an 'ignore' relationship with:\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/ignore/from/user/current/to/content`\nNote, 'ignore' is an example custom relationship type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view both the target entity and source entity."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4652b8df-357f-4f50-8469-448655a3bfda"
            }
          ]
        },
        {
          "id": "0ba5e96b-f721-4907-9658-d5cc4343ce2e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.RelationResource.GetRelationship_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "relation/:relationName/from/:sourceType/:sourceKey/to/:targetType/:targetKey"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceVersion",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetVersion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "relationName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceType",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetType",
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
            "description": "Find whether a particular type of relationship exists from a source \nentity to a target entity. Note, relationships are one way.\n\nFor example, you can use this method to find whether the current user has \nselected a particular page as a favorite (i.e. 'save for later'):\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/favourite/from/user/current/to/content/123`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view both the target entity and source entity."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1857ccef-4e01-4e7f-9e0a-211541ece562"
            }
          ]
        },
        {
          "id": "2d1a6a2b-3941-40bb-9649-b46deaf77f2f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.RelationResource.findSourcesForTarget_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "relation/:relationName/to/:targetType/:targetKey/from/:sourceType"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "limit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceVersion",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetVersion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "relationName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceType",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetType",
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
            "description": "Returns all target entities that have a particular relationship to the \nsource entity. Note, relationships are one way.\n\nFor example, the following method finds all users that have a 'collaborator' \nrelationship to a piece of content with an ID of '1234':\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/collaborator/to/content/1234/from/user`\nNote, 'collaborator' is an example custom relationship type.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to view both the target entity and source entity."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ddb10005-a597-497c-ba6a-01e4c2940d71"
            }
          ]
        }
      ]
    },
    {
      "name": "Relationship",
      "item": [
        {
          "id": "d8cacd4b-cf21-4dec-ba9f-44c9db6aed67",
          "name": "com.atlassian.confluence.plugins.restapi.resources.RelationResource.createRelationship_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "relation/:relationName/from/:sourceType/:sourceKey/to/:targetType/:targetKey"
              ],
              "query": [
                {
                  "key": "sourceStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceVersion",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetVersion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "relationName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceType",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetType",
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
            "description": "Creates a relationship between two entities (user, space, content). The \n'favourite' relationship is supported by default, but you can use this method \nto create any type of relationship between two entities.\n\nFor example, the following method creates a 'sibling' relationship between \ntwo pieces of content:\n`GET https://your-domain.atlassian.net/wiki/rest/api/relation/sibling/from/content/123/to/content/456`\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d018bd5d-6a5e-40e7-916c-548dfb91d14e"
            }
          ]
        }
      ]
    },
    {
      "name": "Folder",
      "item": [
        {
          "id": "0d4f40d6-8859-4fca-9a1b-3eb0716ef656",
          "name": "com.atlassian.confluence.plugins.restapi.resources.RelationResource.delete_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "relation/:relationName/from/:sourceType/:sourceKey/to/:targetType/:targetKey"
              ],
              "query": [
                {
                  "key": "sourceStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sourceVersion",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetStatus",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "targetVersion",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "relationName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "sourceType",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "targetType",
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
            "description": "Deletes a relationship between two entities (user, space, content).\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission). \nFor favourite relationships, the current user can only delete their own \nfavourite relationships. A space administrator can delete favourite \nrelationships for any user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3edc86eb-e08d-4444-acf7-662688194541"
            }
          ]
        }
      ]
    },
    {
      "name": "Look",
      "item": [
        {
          "id": "b594bb07-9a0e-424a-b855-5ec5bfa35bae",
          "name": "com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.getLookAndFeelSettings_get",
          "request": {
            "url": "{{default}}/settings/lookandfeel?spaceKey=%7B%7D",
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
            "description": "Returns the look and feel settings for the site or a single space. This \nincludes attributes such as the color scheme, padding, and border radius.\n\nThe look and feel settings for a space can be inherited from the global \nlook and feel settings or provided by a theme.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nNone"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cfcd3ac0-e9b6-4b57-8d9e-ee4aca619039"
            }
          ]
        },
        {
          "id": "9d707c91-eae6-41e2-9d88-988fb46a6376",
          "name": "com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.updateLookAndFeelSettings_pos",
          "request": {
            "url": "{{default}}/settings/lookandfeel/custom?spaceKey=%7B%7D",
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
            "description": "Updates the look and feel settings for the site or for a single space.\nIf custom settings exist, they are updated. If no custom settings exist, \nthen a set of custom settings is created.\n\nNote, if a theme is selected for a space, the space look and feel settings \nare provided by the theme and cannot be overridden.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d3d2d716-0c2a-4440-bb03-85fc082b6ae9"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "e76a54a7-971b-437c-b7a3-86b383530cf8",
          "name": "com.atlassian.confluence.plugins.restapi.resources.LookAndFeelResource.resetLookAndFeelSettings_dele",
          "request": {
            "url": "{{default}}/settings/lookandfeel/custom?spaceKey=%7B%7D",
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
            "description": "Resets the custom look and feel settings for the site or a single space.\nThis changes the values of the custom settings to be the same as the \ndefault settings. It does not change which settings (default or custom) \nare selected. Note, the default space settings are inherited from the \ncurrent global settings.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "07e5ba29-7fdd-4db0-b101-6f4f0f96fba7"
            }
          ]
        },
        {
          "id": "56a7555a-d8a6-4459-89bb-8936821d2638",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.resetSpaceTheme_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/theme"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Resets the space theme. This means that the space will inherit the \nglobal look and feel settings\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f87b5dea-94e7-4d92-98c3-a226e3402b93"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "37aeaa3a-d8b6-4db4-905a-a1de8630aa76",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SystemInfoResource.getSystemInfo_get",
          "request": {
            "url": "{{default}}/settings/systemInfo",
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
            "description": "Returns the system information for the Confluence Cloud tenant. This\ninformation is used by Atlassian.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "00d6c1aa-6059-4bce-b3b0-b9bb6ed83920"
            }
          ]
        }
      ]
    },
    {
      "name": "Themes",
      "item": [
        {
          "id": "2d2ee331-e3bc-4585-b027-200ed35dc93e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ThemeResource.getThemes_get",
          "request": {
            "url": "{{default}}/settings/theme?limit=%7B%7D&start=%7B%7D",
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
            "description": "Returns all themes, not including the default theme.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7709f9bc-fb72-435f-b389-3cc8a25b13fa"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "e90906f6-c0ea-45ee-8485-76e19d699241",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ThemeResource.getGlobalTheme_get",
          "request": {
            "url": "{{default}}/settings/theme/selected",
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
            "description": "Returns the globally assigned theme.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2d678d6e-25f1-4e1d-931e-6f76510b4447"
            }
          ]
        }
      ]
    },
    {
      "name": "Theme",
      "item": [
        {
          "id": "36e907bb-311d-4c68-95ce-2f5f0a1564d3",
          "name": "com.atlassian.confluence.plugins.restapi.resources.ThemeResource.getTheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "settings/theme/:themeKey"
              ],
              "variable": [
                {
                  "id": "themeKey",
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
            "description": "Returns a theme. This includes information about the theme name,\ndescription, and icon.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: None"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be572d29-0a0b-4ac0-848d-c70137b89208"
            }
          ]
        }
      ]
    },
    {
      "name": "Spaces",
      "item": [
        {
          "id": "bc50ba64-eed4-4fd7-b1da-0ba146448eb7",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpaces_get",
          "request": {
            "url": "{{default}}/space?expand=%7B%7D&favourite=%7B%7D&favouriteUserKey=%7B%7D&label=%7B%7D&limit=%7B%7D&spaceKey=%7B%7D&start=%7B%7D&status=%7B%7D&type=%7B%7D",
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
            "description": "Returns all spaces. The returned spaces are ordered alphabetically in\nascending order by space key.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission).\nNote, the returned list will only contain spaces that the current user\nhas permission to view."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ecb952cc-0345-4af5-b0b8-689639b1f1b9"
            }
          ]
        }
      ]
    },
    {
      "name": "Space",
      "item": [
        {
          "id": "e105a054-6e05-42f7-9c79-a4ab75b32fec",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.createSpace_post",
          "request": {
            "url": "{{default}}/space",
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
            "description": "Creates a new space. Note, currently you cannot set space labels when\ncreating a space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Create Space(s)' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "780bb91b-a409-4b7b-b824-63d70aba662c"
            }
          ]
        },
        {
          "id": "98900bb8-dd7a-4f03-b101-1384ae29c55b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpace_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Returns a space. This includes information like the name, description,\nand permissions, but not the content in the space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'View' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9a2a4b49-abc8-42d9-9794-e4d410c625d9"
            }
          ]
        },
        {
          "id": "cfa1f4ee-30d0-4ba0-9a4a-559a4d255677",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.updateSpace_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Updates the name, description, or homepage of a space.\n\n-   For security reasons, permissions cannot be updated via the API and\nmust be changed via the user interface instead.\n-   Currently you cannot set space labels when updating a space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "76e24fc6-e7d1-4dcf-b637-4e00d2f84a1c"
            }
          ]
        },
        {
          "id": "05f45d27-7710-4aa3-8aa7-f591a65ad39e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.deleteSpace_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Deletes a space. Note, the space will be deleted in a long running task.\nTherefore, the space may not be deleted yet when this method has\nreturned. Clients should poll the status link that is returned in the\nresponse until the task completes.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e5d1b594-443e-4ef9-98eb-8aae9313698b"
            }
          ]
        },
        {
          "id": "db6aba1b-540e-4738-9ce3-80e3081ec07b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.getSpaceProperties_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/property"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "spaceKey",
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
            "description": "Returns all properties for the given space. Space properties are a key-value storage associated with a space.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’ permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4d5c9fb4-e0f3-41b2-ae54-64c91b5b3cc7"
            }
          ]
        },
        {
          "id": "332eb340-5dd1-4bf8-8a10-49b7b956f30a",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.createSpaceProperty_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/property"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Creates a new space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n‘Admin’ permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a62848f1-d4eb-478e-8373-8362c02483e6"
            }
          ]
        },
        {
          "id": "741bdfd9-c0fe-4187-a7e7-fab732345020",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.getSpaceProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/property/:key"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "spaceKey",
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
            "description": "Returns a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’ permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3e41fdea-5267-446a-846a-f2af7c53885e"
            }
          ]
        },
        {
          "id": "414fadb2-c97b-4f83-b776-c1401f4231aa",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.updateSpaceProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/property/:key"
              ],
              "variable": [
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "spaceKey",
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
            "description": "Updates a space property. Note, you cannot update the key of a space\nproperty, only the value.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n‘Admin’ permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "10ebf776-ea1b-4e27-90f1-50079646e2df"
            }
          ]
        },
        {
          "id": "612f3805-9f25-40f6-b38c-b18598902a1f",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.createSpacePropertyForKey_p",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/property/:key"
              ],
              "variable": [
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "spaceKey",
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
            "description": "Creates a new space property. This is the same as `POST\n/space/{spaceKey}/property` but the key for the property is passed as a\npath parameter, rather than in the request body.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n‘Admin’ permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56398a7d-31f8-47cb-bd0a-6617b642a25a"
            }
          ]
        },
        {
          "id": "ccb9cda9-cb12-4253-bfaa-f044a8683721",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpacePropertyResource.deleteSpaceProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/property/:key"
              ],
              "variable": [
                {
                  "id": "key",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "spaceKey",
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
            "description": "Deletes a space property.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**:\n‘Admin’ permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0394afee-151a-444c-a379-80009a19c599"
            }
          ]
        },
        {
          "id": "fd07e4a7-ab52-465d-a6fb-1621666dbe46",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpaceSettings_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/settings"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Returns the settings of a space. Currently only the\n`routeOverrideEnabled` setting can be returned.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'View' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c5063fca-76e9-4204-bbff-41d5b78fd615"
            }
          ]
        },
        {
          "id": "79850a30-fa51-4256-a601-00023fd78b24",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.updateSpaceSettings_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/settings"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Updates the settings for a space. Currently only the\n`routeOverrideEnabled` setting can be updated.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Admin' permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31cdf855-c099-4d60-9a91-15754ff0a280"
            }
          ]
        },
        {
          "id": "cde1c492-931b-46ec-96f7-f15a60ae88df",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceThemeResource.getSpaceTheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/theme"
              ],
              "variable": [
                {
                  "id": "spaceKey",
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
            "description": "Returns the theme selected for a space, if one is set. If no space \ntheme is set, this means that the space is inheriting the global look \nand feel settings.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’ permission for the space."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6534ee7d-bce2-42a5-b04e-5cfc0d3305af"
            }
          ]
        }
      ]
    },
    {
      "name": "Private",
      "item": [
        {
          "id": "c5f5efb0-18c1-4b0c-8baa-e48a56bf307e",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.createPrivateSpace_post",
          "request": {
            "url": "{{default}}/space/_private",
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
            "description": "Creates a new space that is only visible to the creator. This method is\nthe same as the [Create space](#api-space-post) method with permissions\nset to the current user only. Note, currently you cannot set space\nlabels when creating a space.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'Create Space(s)' global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "75c8f2d8-0e00-41e7-9557-b5854c44ab49"
            }
          ]
        }
      ]
    },
    {
      "name": "Contentspace",
      "item": [
        {
          "id": "ad65d99e-0d25-4edb-8c93-2e0481c1004b",
          "name": "com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getContentForSpace_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "space/:spaceKey/content"
              ],
              "query": [
                {
                  "key": "depth",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
                  "id": "spaceKey",
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
            "description": "Returns all content in a space. The returned content is grouped by type\n(pages then blogposts), then ordered by content ID in ascending order.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\n'View' permission for the space. Note, the returned list will only\ncontain content that the current user has permission to view."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "061b2ac7-d2a5-4f44-a899-f67fc1b61a80"
            }
          ]
        }
      ]
    },
    {
      "name": "Blueprint",
      "item": [
        {
          "id": "53d7d2f5-ae9d-4e11-aeca-bbb24f83f9cb",
          "name": "com.atlassian.confluence.plugins.restapi.resources.TemplateResource.getBlueprintTemplates_get",
          "request": {
            "url": "{{default}}/template/blueprint?expand=%7B%7D&limit=%7B%7D&spaceKey=%7B%7D&start=%7B%7D",
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
            "description": "Returns all templates provided by blueprints. Use this method to retrieve \nall global blueprint templates or all blueprint templates in a space.\n\nNote, all global blueprints are inherited by each space. Space blueprints \ncan be customised without affecting the global blueprints.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e3982514-f362-4811-ba86-5a4c2154e8c6"
            }
          ]
        }
      ]
    },
    {
      "name": "Anonymous",
      "item": [
        {
          "id": "a8119f6b-5028-4bcd-8d43-6c864457dec7",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserResource.getAnonymousUser_get",
          "request": {
            "url": "{{default}}/user/anonymous?expand=%7B%7D",
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
            "description": "Returns information about how anonymous users are represented, like the\nprofile picture and display name.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "58b2cc4b-f898-40ed-950c-647147b5f250"
            }
          ]
        }
      ]
    },
    {
      "name": "Current",
      "item": [
        {
          "id": "0dd63f7a-5096-477d-8e23-5fa9a0084fe0",
          "name": "com.atlassian.confluence.plugins.restapi.resources.UserResource.getCurrentUser_get",
          "request": {
            "url": "{{default}}/user/current?expand=%7B%7D",
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
            "description": "Returns the currently logged-in user. This includes information about\nthe user, like the display name, userKey, account ID, profile picture,\nand more.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \nPermission to access the Confluence site ('Can use' global permission)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d021fdad-786a-4464-92e4-2ece64ecad15"
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