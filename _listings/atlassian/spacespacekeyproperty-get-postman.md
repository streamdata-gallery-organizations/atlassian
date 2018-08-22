{
  "info": {
    "name": "Confluence Cloud API Get space properties",
    "_postman_id": "eb58d2c3-73f9-44a6-be5a-db3c874889ce",
    "description": "Returns all properties for the given space. Space properties are a key-value storage associated with a space.\n\n**[Permissions required](https://confluence.atlassian.com/x/_AozKw)**: ‘View’ permission for the space.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Audit",
      "item": [
        {
          "id": "813fb92e-1e33-41fa-8ab0-dc76f30211ee",
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
              "id": "6b8b50a0-1fa4-4369-bbee-511ffe03a704"
            }
          ]
        },
        {
          "id": "c96272d8-37fe-4122-83ff-47f00c6eb24e",
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
              "id": "3340b951-05d6-4f09-b20f-8be3f4e6e273"
            }
          ]
        },
        {
          "id": "b807c55e-b11d-4f30-b13c-9cb9e8d23089",
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
              "id": "7405c005-cfe9-44a8-bad8-a4d6aa724832"
            }
          ]
        }
      ]
    },
    {
      "name": "Export",
      "item": [
        {
          "id": "3fc0c5c0-c400-40dd-8418-302b3b7760b3",
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
              "id": "f363236b-0f97-4e42-8299-2d8359330f93"
            }
          ]
        }
      ]
    },
    {
      "name": "Retention",
      "item": [
        {
          "id": "66a8191b-99d4-448b-b3f1-9e9053deb5ee",
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
              "id": "d7e971b2-9d9e-4bec-b744-54de6d439e77"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "5921288c-01ce-4f9e-98b4-70d4b90d639c",
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
              "id": "382c818b-d06b-4dad-8359-55d4826d83c2"
            }
          ]
        },
        {
          "id": "87a45cc2-2820-4afe-8a57-26ffb89f9e79",
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
              "id": "cebf3cfe-1f7a-4020-a0d0-c62fd021a25f"
            }
          ]
        }
      ]
    },
    {
      "name": "Content",
      "item": [
        {
          "id": "7fb1e356-a857-42c4-8c35-76b200944fde",
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
              "id": "851d3c95-4d51-4006-88ea-f06f3e762620"
            }
          ]
        },
        {
          "id": "7162d544-4a62-47e5-a914-b0d385d7b271",
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
              "id": "c8f7b47e-67c4-43f2-b8e6-f45690302790"
            }
          ]
        },
        {
          "id": "825c00d9-b14f-4b89-80a3-e17de08180b2",
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
              "id": "bf3b6fb5-7278-4521-bbb3-ae339c799ddd"
            }
          ]
        },
        {
          "id": "9750006d-b351-47e6-81eb-55b7821b3451",
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
              "id": "766e8563-4f32-4265-8124-5016ccf2525d"
            }
          ]
        },
        {
          "id": "8945881d-321a-4012-9765-e19100132045",
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
              "id": "a8cb8e11-2eb4-41e5-98b1-9a558c62a5a1"
            }
          ]
        },
        {
          "id": "5f58a817-aee8-4bbe-9b62-32d33c02417d",
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
              "id": "d8ff08f8-df99-47af-bc50-c21e63794415"
            }
          ]
        },
        {
          "id": "00fa3da5-3bbb-40ef-88a7-3f30b052fbc4",
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
              "id": "e600df9a-d4fe-4ec5-9249-20640c976462"
            }
          ]
        },
        {
          "id": "61946f2e-194e-4e29-86e8-f0db2885a512",
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
              "id": "a39925a6-0bd8-4b4d-bd2e-e2d8a9ecfeb5"
            }
          ]
        },
        {
          "id": "462aab31-14c9-4570-920a-63442dd9adc5",
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
              "id": "13afc80a-4712-4a1b-86c5-812b72dee564"
            }
          ]
        },
        {
          "id": "0076e946-d723-40ca-845a-e6cb9cbbefbc",
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
              "id": "6dff655a-c53c-4983-85dd-bdc78474834d"
            }
          ]
        },
        {
          "id": "841fe0f4-461e-4049-8c8d-d5891ca3bc1d",
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
              "id": "5bb6d2d2-4399-404d-9707-16f5f9234d0a"
            }
          ]
        },
        {
          "id": "6218595a-1258-44cf-acc7-37ce22a1f017",
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
              "id": "4d7df8ed-5031-4d20-b442-1e880b2b610e"
            }
          ]
        },
        {
          "id": "dac9be4b-917e-40ec-85f3-7832b1f5c300",
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
              "id": "e5eb0bef-bfb8-4841-bd1d-afd13c426bcb"
            }
          ]
        },
        {
          "id": "69fab495-68dc-4783-b223-c05bec71f178",
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
              "id": "18ca66e6-b404-4a8e-9acd-0411b852858b"
            }
          ]
        },
        {
          "id": "595ab56d-191a-48b9-bea7-d688874e3fdc",
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
              "id": "fc9fe54a-4b5e-49cc-9cc7-5e4c56d96564"
            }
          ]
        },
        {
          "id": "83d278f7-2c38-41f2-9a1a-12033befcd20",
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
              "id": "89c4348e-3f77-41a4-be39-b1040746a44b"
            }
          ]
        },
        {
          "id": "bb63e832-fafe-48d9-be97-cc5081503c0c",
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
              "id": "5ef5ef6b-3a3d-474b-b082-c9bf00029dde"
            }
          ]
        },
        {
          "id": "0bd98326-af93-4797-bfc5-ba50c53d932c",
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
              "id": "4f31cb41-c236-48b1-b41d-dec13346217e"
            }
          ]
        },
        {
          "id": "3c00d2fb-5ac5-4778-befc-7976ba75df28",
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
              "id": "f85a7816-3f18-47e4-8cf7-4a5df49337f8"
            }
          ]
        },
        {
          "id": "6e3fc29a-7a75-4864-b4b0-1c0b4f35ffb3",
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
              "id": "40f5f7cd-dc8f-49f2-83fe-2e54700492a0"
            }
          ]
        },
        {
          "id": "447bd456-5458-495c-b9d4-9f5f922735ee",
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
              "id": "6cc53b19-ea9c-4106-84c3-4f363a93644d"
            }
          ]
        },
        {
          "id": "24a57ffa-cb9f-43e0-97a2-bc9db7018762",
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
              "id": "e4e7977f-f0fd-4b64-9698-21f3524c9003"
            }
          ]
        }
      ]
    },
    {
      "name": "Publish",
      "item": [
        {
          "id": "eabb6553-d71b-41f7-838c-c7221fa01b2a",
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
              "id": "a776a9f6-a098-4a3f-aca8-bac4bf109b76"
            }
          ]
        },
        {
          "id": "35337f81-30a3-48ea-a4a5-cf4a8be24e16",
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
              "id": "d9c6eaf8-42e8-4d50-aed5-84cf58caf402"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "b51e2382-e832-4d1d-af67-b5b8bd3107c7",
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
              "id": "2aaf01d7-a0ee-4bd1-ab22-953a0c7ace49"
            }
          ]
        },
        {
          "id": "cb647e0c-fdee-4126-ae7c-203a9ca83407",
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
              "id": "719fb046-86b9-473f-8cef-bd630624c519"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachments",
      "item": [
        {
          "id": "fbb6e5f7-3dd0-41f1-a704-b648ca762e0a",
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
              "id": "2392b2d8-cc8e-4012-8ead-24e255e2c283"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "0cca0354-6d93-4886-a21b-75b929c4c343",
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
              "id": "f3f52d91-1f53-4f91-9587-8a6d899d5c37"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "9f884afb-911b-4567-ad3f-6a68cb664540",
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
              "id": "feafaec0-e046-4482-a51b-dee97d739810"
            }
          ]
        },
        {
          "id": "e01cb22f-a8fc-4cb2-b22f-38475eae9720",
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
              "id": "2ad4ae27-707a-429c-b2de-dae482a1f32d"
            }
          ]
        },
        {
          "id": "c0f23c49-b126-49c8-9586-fc65b918c099",
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
              "id": "383228d8-674a-4320-af64-fc40c949c751"
            }
          ]
        }
      ]
    },
    {
      "name": "Historycontent",
      "item": [
        {
          "id": "1e2819ac-4a22-4190-8871-de301ad8ef2e",
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
              "id": "60cf1d86-6e63-417b-9cd4-d420a90f37de"
            }
          ]
        }
      ]
    },
    {
      "name": "Macro",
      "item": [
        {
          "id": "2328ba44-27cd-4a40-bb60-8ce2c74665bd",
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
              "id": "a8e01408-75d0-4c6c-b76b-e8bbe33d5c30"
            }
          ]
        }
      ]
    },
    {
      "name": "Labelscontent",
      "item": [
        {
          "id": "8da8b131-d272-45da-a7b7-b99334656161",
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
              "id": "8bb07c5e-2632-46db-89af-3810e1cf858b"
            }
          ]
        }
      ]
    },
    {
      "name": "Labels",
      "item": [
        {
          "id": "7b8924d4-2716-44f5-a8ca-8d4283d931c5",
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
              "id": "fd5465a0-d78a-45ac-9a77-2853ec3217b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "51d26dba-d189-4045-8bbb-a93024478040",
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
              "id": "dbc2948e-6954-4e12-b8f6-36c21ba3842b"
            }
          ]
        },
        {
          "id": "9aa75e30-d310-496e-8cd6-351501c1d6b8",
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
              "id": "0d680f10-0b81-4f33-ae7b-1a1c4c6fb6af"
            }
          ]
        },
        {
          "id": "b75e7851-f06f-4eab-b932-8dc886b8e8d1",
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
              "id": "fdab0204-23a6-46a4-9ee9-97d9552b855e"
            }
          ]
        },
        {
          "id": "fc8fd20f-a1be-441c-a7f8-0448291d3f04",
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
              "id": "c53c9537-2216-42b4-a074-9c18561e1b8e"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchespage",
      "item": [
        {
          "id": "68e5435d-694c-4574-a1ae-3b91666adf65",
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
              "id": "22be1082-2bec-420a-9576-6802553918c5"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchesspace",
      "item": [
        {
          "id": "afca2661-c5e8-4896-9079-d032b9f7ad12",
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
              "id": "aa4ee9ca-799c-43ef-ac23-49ae70ac87cd"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "aa4372dd-5507-46fa-a3e0-9f637b1c8df6",
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
              "id": "d3e8b039-7ad4-4db3-9b31-a479cdfedd41"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictions",
      "item": [
        {
          "id": "7a0b11d5-d5ab-4c8c-a1a4-461be6051c6f",
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
              "id": "973d4ed4-be7c-41f8-aa07-ec167ebef254"
            }
          ]
        },
        {
          "id": "f9876876-c3f6-4e7b-adad-8224b7a0049c",
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
              "id": "a5e05225-3cdf-4f2e-8f2d-f84da6a10143"
            }
          ]
        },
        {
          "id": "189031b3-2ae7-4990-8cb7-2d8621dd0a4e",
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
              "id": "8af5fdac-2ffc-4921-bd4f-207c012669a2"
            }
          ]
        },
        {
          "id": "b61fabe1-2bb9-4701-a326-7d9dcb54ce9c",
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
              "id": "fc07f6d0-623a-435f-826e-1706c3568b4f"
            }
          ]
        },
        {
          "id": "c83687cc-29f3-41a4-a572-e9d4220bf5ae",
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
              "id": "f1d4d1e5-1470-4b39-bc85-83d82e0cd56b"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictionsoperation",
      "item": [
        {
          "id": "9e64af85-de23-4983-9fc1-843a55da34e9",
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
              "id": "a1f04a2a-24c7-46ac-b2b2-02be83bb8442"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "0ba9bf8f-5f85-42c6-8abd-ffea0926b1d0",
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
              "id": "55a6a2c9-a072-4787-bd20-7c62eb71c7c2"
            }
          ]
        },
        {
          "id": "20ccf309-424b-458e-a8e4-19d6aff6fc42",
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
              "id": "47dae41a-df67-4d0a-a134-43d7a0a1c10e"
            }
          ]
        },
        {
          "id": "fb19aba6-3656-496c-b7fb-bff4adda43de",
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
              "id": "f3651134-7497-4cef-a81c-13a444c7d633"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "0cfa63e5-7273-4d1f-8d0b-10d0af25d65f",
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
              "id": "50348bc2-3b11-4cc5-b80b-006a6d978463"
            }
          ]
        }
      ]
    },
    {
      "name": "Restore",
      "item": [
        {
          "id": "c6b48a33-95e2-4615-857e-9f6aaed6b1bd",
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
              "id": "7bcd7539-5be6-4ae4-92ca-e9f8357023c1"
            }
          ]
        }
      ]
    },
    {
      "name": "Convert",
      "item": [
        {
          "id": "b20d4425-da03-41e9-a215-de97a12b168d",
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
              "id": "10d6b7d8-acf8-492f-982c-23032be42ad8"
            }
          ]
        }
      ]
    },
    {
      "name": "Groups",
      "item": [
        {
          "id": "b3572eeb-737f-4eac-a052-7ca2734f6a6b",
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
              "id": "64e9fa6c-3b06-40f6-a403-1f50c98618bf"
            }
          ]
        }
      ]
    },
    {
      "name": "Long-running",
      "item": [
        {
          "id": "bb60f694-abd7-45a2-a6a6-c8cbab7ddee1",
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
              "id": "da9f6159-cf14-45e5-98d8-187a7c42729a"
            }
          ]
        },
        {
          "id": "42bb32d8-2ad9-4641-b9c4-c6d125360b56",
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
              "id": "8c2d9313-e762-43c1-a55a-34a1fb71f173"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "44c676d4-366e-42e0-b62d-da09e8b5614b",
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
              "id": "0fabc87b-303c-44bb-aada-d0f7fa576d4c"
            }
          ]
        },
        {
          "id": "54977dbe-c515-40d6-b235-a9fdd029bf5a",
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
              "id": "268f1866-9719-4161-b2c8-1b9870e4bf5f"
            }
          ]
        },
        {
          "id": "56811024-3603-4d1e-88cd-742c5cab9b44",
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
              "id": "a76ad8dc-a7a4-4f5a-b5a5-b9c67c22e7cf"
            }
          ]
        }
      ]
    },
    {
      "name": "Relationship",
      "item": [
        {
          "id": "3291e2a8-2da6-4d59-ab17-5167a4c9d8af",
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
              "id": "81cf33aa-ce40-4b34-96bc-52771df42085"
            }
          ]
        }
      ]
    },
    {
      "name": "Folder",
      "item": [
        {
          "id": "bb87fd67-8675-4cb5-b0f2-58c14fdc70d3",
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
              "id": "5a8ede65-5566-438c-9d0c-d703849769d7"
            }
          ]
        }
      ]
    },
    {
      "name": "Look",
      "item": [
        {
          "id": "924dbf80-f9c6-41b7-9f90-57702cdd4460",
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
              "id": "a9a1cda7-67de-4ac8-a6b2-91598fcff99c"
            }
          ]
        },
        {
          "id": "6b0ce007-81af-404c-a6d6-963e1c1cfe53",
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
              "id": "8a558640-0940-47d6-9a2b-03d3fbdedf61"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "e9de9619-cdd2-4bf7-b4c1-f544465e843c",
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
              "id": "566e2ba7-8b1c-4406-9823-195fb235670c"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "40a6d97e-2c2b-47ee-97b3-219acd74f2d2",
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
              "id": "c52a46b1-4da6-48f2-9e72-c771a521b89c"
            }
          ]
        }
      ]
    },
    {
      "name": "Themes",
      "item": [
        {
          "id": "8b79a7ab-7d1e-42b8-8c6f-b050e9bf0321",
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
              "id": "34e3e539-c8bc-4eb2-9a90-e1f7680b2e42"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "55c1f864-6f4c-4405-b475-9949d34342e3",
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
              "id": "e8b0c389-c3a3-44c8-88fd-7ef40c1bf9ec"
            }
          ]
        }
      ]
    },
    {
      "name": "Theme",
      "item": [
        {
          "id": "86fd6c51-aa31-4d0f-985e-02f1625b03f9",
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
              "id": "4a59c1ae-2b64-488b-8655-dfcc6b5ce34e"
            }
          ]
        }
      ]
    },
    {
      "name": "Spaces",
      "item": [
        {
          "id": "1dc86228-4fa5-48ac-b796-b0c8c9225479",
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
              "id": "a3317a85-ddca-4c41-98ba-7ab69a87e0a2"
            }
          ]
        }
      ]
    },
    {
      "name": "Space",
      "item": [
        {
          "id": "a9094dcc-f892-4769-b63e-29cedfa4f5d0",
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
              "id": "f3c97744-c145-408d-8751-9b9513bc9a57"
            }
          ]
        },
        {
          "id": "cecfde11-71f1-4805-958f-b658b5dcde91",
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
              "id": "2620273d-d4e7-45f1-a7a5-580d362ee193"
            }
          ]
        },
        {
          "id": "6e831551-20c5-40bf-a4b1-7c5860d2ae97",
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
              "id": "d45ef400-8913-4909-b7be-63134e927630"
            }
          ]
        },
        {
          "id": "7f106340-c8cb-4c45-82f7-8b6c75779751",
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
              "id": "93254098-9e48-43cd-8091-b41f6490c922"
            }
          ]
        },
        {
          "id": "4b590926-c826-4434-bece-76208b58ceda",
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
              "id": "6fefe403-2d2c-4e7b-86a6-f04a356a15cf"
            }
          ]
        }
      ]
    },
    {
      "name": "Private",
      "item": [
        {
          "id": "222d3cc9-1033-49ae-ae9a-046de8b2706a",
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
              "id": "37f1ee6d-b750-4586-a0e7-ba4b37e489fd"
            }
          ]
        }
      ]
    },
    {
      "name": "Contentspace",
      "item": [
        {
          "id": "45c62e53-f187-4641-8e96-aa0acbd4c103",
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
              "id": "cc8feb1d-0e91-4b21-8bf6-c093965ba894"
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