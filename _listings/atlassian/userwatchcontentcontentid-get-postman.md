{
  "info": {
    "name": "Confluence Cloud API Get content watch status",
    "_postman_id": "ce1c570e-3531-44dc-bf96-7fc2c67df00d",
    "description": "Returns whether a user is watching a piece of content. Choose the user by \ndoing one of the following:\n\n- Specify a user via a query parameter: Use the `username`, `key`, or `accountId` \nto identify the user. The user making the request must be a Confluence administrator.\n- Do not specify a user: The currently logged-in user will be used.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**: \n'Confluence Administrator' global permission if specifying a user, otherwise \npermission to access the Confluence site ('Can use' global permission).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Audit",
      "item": [
        {
          "id": "c716d1dc-269d-4da2-b033-23f7053df73d",
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
              "id": "8c3c46dd-67a1-4304-a61e-f11ed4d9c7b9"
            }
          ]
        },
        {
          "id": "87c798bb-d583-43e2-8ecc-62946ac91da0",
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
              "id": "9866ce67-4c4d-49e5-9945-117c05cfb99f"
            }
          ]
        },
        {
          "id": "20e357df-36ef-48d9-8d64-2cae24fee420",
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
              "id": "3463f352-f710-4d67-bd7e-c3581badb0c8"
            }
          ]
        }
      ]
    },
    {
      "name": "Export",
      "item": [
        {
          "id": "799889d4-cd85-4a8d-aaf9-c1a8866371b5",
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
              "id": "5c4d4e98-0307-4a43-be89-6f9cac135320"
            }
          ]
        }
      ]
    },
    {
      "name": "Retention",
      "item": [
        {
          "id": "2d88fcfb-975c-4151-854a-6dc21bf2cdc8",
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
              "id": "0ceb9480-9506-46cf-ab2f-cf56dfc2f3ea"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "77a6bf92-833c-4579-9cb2-a23dbf85dbaf",
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
              "id": "654932a1-d9e1-4dde-b7f3-b3c04372f677"
            }
          ]
        },
        {
          "id": "c9d357d4-635a-4a14-b62b-47207019ab66",
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
              "id": "208d15c2-8265-46fc-a1d1-13ccdfe315fd"
            }
          ]
        },
        {
          "id": "2d770c3a-442d-4a75-8bcb-4c7bd06764aa",
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
              "id": "1a2c3aaf-f870-49c3-a84e-c51c50662dcb"
            }
          ]
        }
      ]
    },
    {
      "name": "Content",
      "item": [
        {
          "id": "df7ab516-5cd4-4fd2-8d73-71efcba3a165",
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
              "id": "8cf5412b-22db-43cb-ab22-f5f1baa30bec"
            }
          ]
        },
        {
          "id": "016f5837-3e30-4bf7-bb64-65bbd218e4c6",
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
              "id": "a6f92151-c2de-448f-bc18-327b8165f6eb"
            }
          ]
        },
        {
          "id": "1b070f3f-3121-4d80-85af-cc11cb2d58dd",
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
              "id": "bf996cee-4d05-4edc-a1b9-7e28e8871db6"
            }
          ]
        },
        {
          "id": "7dcd7953-39b9-4cd9-b584-b129b751b507",
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
              "id": "5f551a6c-6060-45f6-ae16-fae63f8a1839"
            }
          ]
        },
        {
          "id": "05cc47f7-e57d-4bd8-860e-3fa159ecac44",
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
              "id": "6022a184-fa7d-4ec4-91ca-282acbd1881b"
            }
          ]
        },
        {
          "id": "e57bd685-91e6-447d-80a3-9d40c980f45c",
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
              "id": "0b3e158a-51b0-4b65-a52e-dd41bf39c7ce"
            }
          ]
        },
        {
          "id": "6416e187-f9e6-42a5-9537-4a542c977bcb",
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
              "id": "ba4b40f0-689d-4e49-88c0-a9db57160356"
            }
          ]
        },
        {
          "id": "f2cc8a86-814a-487e-8b39-0e5bd2dc16e6",
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
              "id": "88bc0264-ccc0-4bd2-a405-c5a3eca2a91e"
            }
          ]
        },
        {
          "id": "a9ae61d3-9944-4c6f-842f-30a75e7d40ba",
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
              "id": "e56bf559-5fbc-4a22-934d-247c07451869"
            }
          ]
        },
        {
          "id": "201450d4-a287-4f47-88f6-9462c787bdbf",
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
              "id": "5d93812b-f20d-4a9b-8609-654805bf00d8"
            }
          ]
        },
        {
          "id": "417f2305-23fa-4d9c-aeb2-0a7bad12056c",
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
              "id": "4c5bda36-7963-437f-a84f-bd898519a9ba"
            }
          ]
        },
        {
          "id": "7654f2e7-89fb-4b8e-a6b9-b7fab84b9be3",
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
              "id": "a3800fda-a875-4421-8320-5266decfe2ac"
            }
          ]
        },
        {
          "id": "674dbf3b-533f-434a-8b68-7bfc35e14d03",
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
              "id": "2deae079-b9a2-4313-b6fd-3a6744b5a77c"
            }
          ]
        },
        {
          "id": "ca62092c-8964-4427-8a42-60bef10c27de",
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
              "id": "c512470c-a003-4521-a76b-46db0b291986"
            }
          ]
        },
        {
          "id": "492cce0f-0824-48d9-afb7-15e82b14fe43",
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
              "id": "962c3853-d76c-49ae-b272-2641aedd78f0"
            }
          ]
        },
        {
          "id": "348d24a3-a3c4-4b55-8ffc-33b9e4f18583",
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
              "id": "e381d1c5-8b83-45e7-93a9-d351e156d4b3"
            }
          ]
        },
        {
          "id": "7d138b53-1253-4f39-becc-8616d3aa445d",
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
              "id": "29570c5c-a798-49bc-93c6-fe25fd3ca6f9"
            }
          ]
        },
        {
          "id": "295442f4-7ead-4a94-b351-2a4c0efe1da3",
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
              "id": "f8cef8a8-9256-4097-a140-48ad82bf4920"
            }
          ]
        },
        {
          "id": "8f4954aa-da18-47b4-860a-4e48bfe806c2",
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
              "id": "93dfab00-fc4e-44bc-8892-5a403f09fa25"
            }
          ]
        },
        {
          "id": "2fb42be9-445a-43af-8b72-8e9d6dfffb2a",
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
              "id": "3446d22b-7611-4600-8df7-9d66ac71e059"
            }
          ]
        },
        {
          "id": "b5ee8d5b-6d0c-465f-b37e-b3c22f21d980",
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
              "id": "9adb9d6f-1faa-43eb-b720-58ad50295511"
            }
          ]
        },
        {
          "id": "238d5f64-0c74-4ee9-9e12-b56918d8afd7",
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
              "id": "d0224041-4a12-400a-91ee-aee24833eea5"
            }
          ]
        },
        {
          "id": "f4e14556-9fef-42cb-996d-7bdbb98919d0",
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
              "id": "20d9a222-e3b4-43d4-853f-5a9819c524d0"
            }
          ]
        },
        {
          "id": "90a798c1-16ae-48fb-ad69-beb5607b1ca1",
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
              "id": "03a80f5c-c869-4510-ada0-308debe6bd5a"
            }
          ]
        },
        {
          "id": "ef150a37-6bd7-4d42-b403-b10a7944b97e",
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
              "id": "c3033b25-b77d-4608-afa9-8314935270e6"
            }
          ]
        },
        {
          "id": "c1f65df9-adb1-4681-9a62-625ac418fdc6",
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
              "id": "8454a309-5650-426c-805d-90338e546b04"
            }
          ]
        },
        {
          "id": "0c4863df-a0b8-469f-9301-8efd0e216f66",
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
              "id": "186baedd-4142-45ae-a088-448232ef9935"
            }
          ]
        }
      ]
    },
    {
      "name": "Publish",
      "item": [
        {
          "id": "536d5432-2e51-4a6c-bbca-419ce0479cdd",
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
              "id": "cd002dea-8414-4301-87d3-070185115b25"
            }
          ]
        },
        {
          "id": "df830db9-5b07-43ab-8297-9520d344d7ef",
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
              "id": "44526860-15f7-4864-b44b-d939c179ffe3"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "d3409666-5da7-4b2c-9ae7-ea1793c58541",
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
              "id": "71cd2d99-9155-4f14-81fd-7bba2c462480"
            }
          ]
        },
        {
          "id": "8ddf7ac7-7898-47f9-8806-6fd2d6fce7ae",
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
              "id": "b0e38d8a-7f62-4d42-a401-c4f055e30fca"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachments",
      "item": [
        {
          "id": "97efe39a-16bc-46b5-b6c7-4e10fd0bdfc1",
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
              "id": "27381b69-0c19-44a9-ab45-8bb557cefa11"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "b67d32ab-d6b6-4cb6-88a0-f589fe0facc0",
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
              "id": "af0b5534-1e63-4f38-9231-2e2b908eb62b"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "1abfb757-afe9-4250-8e41-bea0b211a7df",
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
              "id": "be3669af-cea6-461c-abed-f6995aece481"
            }
          ]
        },
        {
          "id": "a57bc861-bfed-4ef6-8f99-4a6ea31a1174",
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
              "id": "c5426634-f3e7-46ef-89cc-1b8ac47e7518"
            }
          ]
        },
        {
          "id": "ef1abad1-122a-42b9-9a0b-13b9e7735715",
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
              "id": "73ecaa0a-1b03-499d-99c9-0be3b77f2118"
            }
          ]
        }
      ]
    },
    {
      "name": "Historycontent",
      "item": [
        {
          "id": "846dd623-b9f6-4dbc-bbb1-5c4808998489",
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
              "id": "3dfea904-6fd0-4366-a3b6-27e43baf4315"
            }
          ]
        }
      ]
    },
    {
      "name": "Macro",
      "item": [
        {
          "id": "9874aa0b-035d-44d0-a627-3ac20390c150",
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
              "id": "6383f2fe-9804-44e5-9cb6-b516f0a14bc8"
            }
          ]
        }
      ]
    },
    {
      "name": "Labelscontent",
      "item": [
        {
          "id": "f7d19986-6017-4774-90df-cd66e65c0687",
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
              "id": "100199ff-f3a0-4cea-8998-ce060487cbdb"
            }
          ]
        }
      ]
    },
    {
      "name": "Labels",
      "item": [
        {
          "id": "4da6b8d6-2365-4bd5-99f3-41a8b1f93604",
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
              "id": "591bedff-d5fe-45f6-949c-cea92674deb4"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "93fa9b6e-4dba-4e6b-b2f7-0ff66f5e6382",
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
              "id": "558511e8-8473-4001-a005-cd1142dbd2b7"
            }
          ]
        },
        {
          "id": "c36628d6-cd1f-4519-9bf4-ee47082763e8",
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
              "id": "f490d09b-7858-4686-97ef-e6e68f5ffbab"
            }
          ]
        },
        {
          "id": "92c47eba-148b-49c0-8d4e-4bf8fbd13a73",
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
              "id": "1dd406fa-db6a-4662-92f7-6012102bdf4f"
            }
          ]
        },
        {
          "id": "a5bfe0ed-b296-499f-9f9f-262cb5cf8349",
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
              "id": "41a82b60-90d4-44b0-b8f9-f42048ddb514"
            }
          ]
        },
        {
          "id": "ca26fb5a-dc2d-4130-b47c-c9d4718c81aa",
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
              "id": "0f714dba-f757-495c-9781-2322660d7c20"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchespage",
      "item": [
        {
          "id": "88fc9937-7db7-4768-bbc8-feffddb2f460",
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
              "id": "82e59031-8131-4568-817d-b7240de10955"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchesspace",
      "item": [
        {
          "id": "2454cad4-36d8-4c6d-a3c2-b39c9c4b2e43",
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
              "id": "7d08c921-c08e-406c-9be0-4d775a6047e7"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "e0c43d14-d76f-46be-b2f3-dc8db26a1a4c",
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
              "id": "2ee2218d-d2c8-46b4-add1-0f28fedd26c4"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictions",
      "item": [
        {
          "id": "06231aac-11dc-4296-bb15-662a3f2d1ac8",
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
              "id": "ad636db1-f160-41ad-88d5-b9cd6ddb5864"
            }
          ]
        },
        {
          "id": "afc3c780-bd80-4a97-82d5-6879c46bbeaa",
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
              "id": "49100620-a76c-48b1-9b47-d61dbf341f57"
            }
          ]
        },
        {
          "id": "a2ae6285-4487-4cd4-8ee7-c7cd9d784823",
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
              "id": "87916cbc-99aa-4b0f-af2c-bdcda5f04759"
            }
          ]
        },
        {
          "id": "5968470e-5c68-4f92-99d3-02544d1a43b9",
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
              "id": "2ae1a04d-2350-497e-977c-dd96b063b155"
            }
          ]
        },
        {
          "id": "9671bd20-e519-40d7-ac7b-dec7c8a0b1ee",
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
              "id": "75446148-5824-4efc-ba5f-da84ef0360c6"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictionsoperation",
      "item": [
        {
          "id": "4049dc6d-6056-4327-8bf0-bfbd0ebe6d98",
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
              "id": "4a9e36fe-2959-44fc-a15d-2abe5d5a7ab1"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "fdcbaaa4-a680-44f7-9355-e12ba83c5542",
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
              "id": "d24b185b-7d5c-44b1-a1c1-b5f680c57ca0"
            }
          ]
        },
        {
          "id": "bb3ca67a-009f-4603-8c86-3a6b241a86b1",
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
              "id": "1c38323d-f672-430f-941c-19ca7fbcd795"
            }
          ]
        },
        {
          "id": "62139604-1994-44e8-8ca6-d49c57602853",
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
              "id": "a26c7ef4-6403-4eb2-9945-52c0a2c096d3"
            }
          ]
        },
        {
          "id": "25f2d72d-b91c-4d18-8da1-e40fbaa0a74c",
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
              "id": "bf64111c-d883-434e-9d7c-7b09968b3be7"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "e668e643-d277-4ba7-9dbd-e11ecc1045e9",
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
              "id": "dd14623f-3c5d-4df7-86d6-a715b3d1d535"
            }
          ]
        },
        {
          "id": "5d7abf20-5739-4d5c-8502-dd97a974a9a8",
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
              "id": "11be5fc5-7f30-4926-a7f8-b8440f1e24e0"
            }
          ]
        }
      ]
    },
    {
      "name": "Restore",
      "item": [
        {
          "id": "3410f6a4-4025-4320-89ba-25d253921033",
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
              "id": "e70359ac-85ef-47c6-8fe8-45b59393391e"
            }
          ]
        }
      ]
    },
    {
      "name": "Convert",
      "item": [
        {
          "id": "c143e747-02bd-463b-9025-fbab11ced5e1",
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
              "id": "cda9334f-0378-40d3-98c6-4a84263b1bba"
            }
          ]
        }
      ]
    },
    {
      "name": "Groups",
      "item": [
        {
          "id": "8e60bce2-9ba0-4c31-af3b-b39519eaa188",
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
              "id": "6c25252a-3567-4145-bda2-9a7158ae6a75"
            }
          ]
        }
      ]
    },
    {
      "name": "Long-running",
      "item": [
        {
          "id": "a358925f-699e-4df8-82d2-00a9f3dc832b",
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
              "id": "29178f1c-df52-4036-9361-deb4bc7168b7"
            }
          ]
        },
        {
          "id": "1be88add-095c-4d19-8470-1590fb67f8dc",
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
              "id": "f3bcac34-c2a9-45d1-95ef-d50d56e475a8"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "3bfb02db-dc0d-422a-9916-e6b6451b6646",
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
              "id": "e91f15af-e827-48f8-99b9-cb800a1b4f6c"
            }
          ]
        },
        {
          "id": "88552fab-71a3-4939-b0ca-85664a14a0e4",
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
              "id": "37f95ed8-fe34-49e9-a55e-207507c43b8f"
            }
          ]
        },
        {
          "id": "ab26d7d8-03a3-4cc5-880f-bab98da80ee9",
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
              "id": "2c7c3ccb-3838-4ed9-b1e2-e5f8d114a1c1"
            }
          ]
        }
      ]
    },
    {
      "name": "Relationship",
      "item": [
        {
          "id": "cde42bde-a8af-4b1f-81fc-5e778e084d30",
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
              "id": "d137903f-751c-4167-9099-a866ee43f133"
            }
          ]
        }
      ]
    },
    {
      "name": "Folder",
      "item": [
        {
          "id": "ef67b053-0834-4ebb-86c3-382874a7d678",
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
              "id": "640b1786-aabb-4623-b8d4-1072e6d5b426"
            }
          ]
        }
      ]
    },
    {
      "name": "Look",
      "item": [
        {
          "id": "6c8083ff-88a5-4aa2-894d-91cb504b145d",
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
              "id": "19afc711-b09a-4d5c-b685-6b59a5b22b2f"
            }
          ]
        },
        {
          "id": "4f9b4f56-a329-4013-9356-d6f24edcd68b",
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
              "id": "183f76da-8208-4b1e-8879-717517e2a0d5"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "16a88023-aa64-410e-a633-e13819cb742b",
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
              "id": "4c3ba235-ec93-409c-ba88-71c5fc67040d"
            }
          ]
        },
        {
          "id": "4cb1fa9a-1442-42bc-b25b-58efe3aaa390",
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
              "id": "c146f996-932b-409f-bdb9-533356d23bb0"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "d33db7a5-f6f5-4833-bb9e-2f7361904099",
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
              "id": "9050b3c8-0d8e-43ff-bae5-6f3f44dded7a"
            }
          ]
        }
      ]
    },
    {
      "name": "Themes",
      "item": [
        {
          "id": "7c3a3fca-8619-43ea-9227-bc5dbd66b1d7",
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
              "id": "5ab6ca8a-89d5-4e29-a66a-1d80754f339d"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "0bac3fb7-b6c0-4a4b-b757-cec095c226d1",
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
              "id": "e4da959e-18d2-48bb-9827-b75d9a7185b8"
            }
          ]
        }
      ]
    },
    {
      "name": "Theme",
      "item": [
        {
          "id": "f4ab0765-b9f4-45c0-b07d-3947b6c28c48",
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
              "id": "9c58f285-96b4-4765-821f-c18d29b204c8"
            }
          ]
        }
      ]
    },
    {
      "name": "Spaces",
      "item": [
        {
          "id": "57c71124-74c5-4257-b53c-ed04027e089a",
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
              "id": "27db22e7-2848-4fbb-90de-4212d6e97a8b"
            }
          ]
        }
      ]
    },
    {
      "name": "Space",
      "item": [
        {
          "id": "d268a64f-0e52-455e-833f-797091f44395",
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
              "id": "31cd0e6e-f70e-435a-85e7-2f5847bc26ee"
            }
          ]
        },
        {
          "id": "b3582629-4f0b-4760-acab-858fd4a8ef4b",
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
              "id": "04d4dc55-31a4-4b7e-83ef-f3dca0334261"
            }
          ]
        },
        {
          "id": "47478ec5-adc7-457c-b6c4-1235d897d99a",
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
              "id": "454d46fd-9e65-4444-818d-b8a32bfd38cc"
            }
          ]
        },
        {
          "id": "9e02f09e-3d98-491d-8499-ac2eb41089d2",
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
              "id": "cdcec69b-596e-41d2-930e-d2c7e64f93e3"
            }
          ]
        },
        {
          "id": "78ae6d15-74e2-4901-b84c-a4b6871d7322",
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
              "id": "64616884-8a6d-456f-9cc0-bbb34e442d42"
            }
          ]
        },
        {
          "id": "8ec09881-750c-4bd3-8de1-edaddce82459",
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
              "id": "0382b40f-fe04-421d-880d-5bffa97d440b"
            }
          ]
        },
        {
          "id": "98ff2390-1d84-4f43-9e57-eb7c86588db4",
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
              "id": "9d49c7ec-b6b7-4a83-815c-9b446a2cfcda"
            }
          ]
        },
        {
          "id": "73b7f318-899a-4d90-8dff-1a9ddcefb3f2",
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
              "id": "88d12e6d-8cef-4156-86cb-c5640c9db5c7"
            }
          ]
        },
        {
          "id": "714734e6-3498-4d0e-beba-935d6c9dd17f",
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
              "id": "fa32fd47-5e9e-4c60-aff4-104b20655c72"
            }
          ]
        },
        {
          "id": "b94181cc-d097-4a04-90b8-21c80d677a82",
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
              "id": "b73fc651-2bf1-410f-957e-0a4a5227f2e3"
            }
          ]
        },
        {
          "id": "3fde3ff3-d187-484d-bba0-304c8a97c215",
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
              "id": "fdd4e158-b255-4310-91ed-9d99501565eb"
            }
          ]
        },
        {
          "id": "359e4e0d-d403-445b-9e28-ba111eb32951",
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
              "id": "25cb93e0-f035-49f2-91c1-178bf40ec8d8"
            }
          ]
        },
        {
          "id": "077da62d-6257-48cb-b703-dd97e2c6fc8a",
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
              "id": "243e91c8-c5b2-4798-a063-1b3a3ed1012a"
            }
          ]
        }
      ]
    },
    {
      "name": "Private",
      "item": [
        {
          "id": "9bc72d6f-bab8-4e3b-a663-b4ebc67cd0b1",
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
              "id": "6b84bb33-32e7-4330-9833-761fa8641db5"
            }
          ]
        }
      ]
    },
    {
      "name": "Contentspace",
      "item": [
        {
          "id": "3abb37c0-8057-4132-8e5b-fba6c9bf3b66",
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
              "id": "62b1d20b-2bc8-4cb4-be5e-9ec2ddec68c1"
            }
          ]
        }
      ]
    },
    {
      "name": "Blueprint",
      "item": [
        {
          "id": "f1dd38d6-fcb4-4a9b-823e-da4d07559ffb",
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
              "id": "63a3ab34-2e49-4155-ae68-18a11a8dc4ca"
            }
          ]
        }
      ]
    },
    {
      "name": "Anonymous",
      "item": [
        {
          "id": "f1d7c9ac-e513-4c04-8141-a8eb88e007b8",
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
              "id": "541c0d7f-403f-4f55-ad8e-94957dcc1fc1"
            }
          ]
        }
      ]
    },
    {
      "name": "Current",
      "item": [
        {
          "id": "9db570de-83a8-4b09-a1cc-5ddbe14cca40",
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
              "id": "93671448-da10-49cc-b0d7-9571bdd6ebf2"
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