{
  "info": {
    "name": "Confluence Cloud API Get long-running tasks",
    "_postman_id": "aca81d64-fe93-4ff3-92e8-0af61fac23af",
    "description": "Returns information about all active long-running tasks (e.g. space export), \nsuch as how long each task has been running and the percentage of each task \nthat has completed.\n\n**[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:\nPermission to access the Confluence site ('Can use' global permission).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Audit",
      "item": [
        {
          "id": "6bf83132-d678-4781-ab17-c1323a0ad838",
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
              "id": "75ba1bc5-462f-412c-9ae1-eeb4759487f3"
            }
          ]
        },
        {
          "id": "aa2ef422-d36c-42d3-aa5e-decb11a489c3",
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
              "id": "adda52bb-cff1-4b09-8a14-88c4e2ac60e7"
            }
          ]
        },
        {
          "id": "a003010a-6029-4478-a803-bb63d5de6b65",
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
              "id": "d6d6e0eb-c66b-401e-a04b-f26fffeab48e"
            }
          ]
        }
      ]
    },
    {
      "name": "Export",
      "item": [
        {
          "id": "7a707d2b-b344-4b0a-bfb9-790385da93fb",
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
              "id": "c9e0a22b-4e29-4767-b1d2-a01c6f655891"
            }
          ]
        }
      ]
    },
    {
      "name": "Retention",
      "item": [
        {
          "id": "da67208c-d297-46a2-931c-62288ebeacfc",
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
              "id": "5eeb4c19-9316-4df9-8261-a4bc1544cecf"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "07d5956e-1652-4392-9b26-a424c95ee9b4",
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
              "id": "854f683e-8289-47ad-843c-cecdf111e175"
            }
          ]
        }
      ]
    },
    {
      "name": "Content",
      "item": [
        {
          "id": "ea789ca0-cd7e-4fee-84b2-513c74936397",
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
              "id": "c5374e62-e0e2-4fe0-a74b-76f4d05c8abe"
            }
          ]
        },
        {
          "id": "9acdd21c-5ef3-44b6-9725-ee9aa871e7f2",
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
              "id": "c9af7ba2-c4d6-48e1-8913-7b2dd2041f2b"
            }
          ]
        },
        {
          "id": "20bc01af-26e1-427e-a34f-3b42b1c02065",
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
              "id": "495f1608-2470-4ef4-a62e-a6256e5e6222"
            }
          ]
        },
        {
          "id": "10ec67d0-c957-409b-8c3d-e987d52eeb76",
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
              "id": "b55290e7-9000-4781-807f-52ebc75e97a1"
            }
          ]
        },
        {
          "id": "a516dfab-a5c1-492c-9f11-03c7e4d32ec2",
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
              "id": "8c5f9cae-a15f-46c6-859b-a5d09e7f2185"
            }
          ]
        },
        {
          "id": "27c803b4-bb05-429f-b851-35a138c5bc9a",
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
              "id": "2a32fd0f-15a5-47b2-9f16-86c517539ae3"
            }
          ]
        },
        {
          "id": "0884810b-9fc8-41e2-a0b0-74e966d7e395",
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
              "id": "0093405c-47a8-461a-acfe-0fcf7ceddd43"
            }
          ]
        },
        {
          "id": "7667e56d-7154-49c3-bbbf-f459a3948af7",
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
              "id": "8c860d0a-1b25-4d75-8f82-d117c1d78560"
            }
          ]
        },
        {
          "id": "3fca0f2c-2a48-4a41-b629-decd7e926312",
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
              "id": "ec5f0da2-26fe-4ca5-9a88-ac6a427d46da"
            }
          ]
        },
        {
          "id": "d24cda4e-8a27-494f-9cb0-64331becd9b9",
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
              "id": "8ab1ac48-2061-4a30-a865-76adc6293831"
            }
          ]
        },
        {
          "id": "ff1faa00-27df-4b3a-93f9-0b01496f73c0",
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
              "id": "493696de-a18d-431f-b288-0fe305136448"
            }
          ]
        },
        {
          "id": "0c4c3594-20b1-4c2b-b9d3-6667cb838a7a",
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
              "id": "5a8f57f1-31d5-4dbd-b1d4-e88b8a4299f5"
            }
          ]
        },
        {
          "id": "96b37b0f-f7c4-4c99-94dc-fb507128bbad",
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
              "id": "9af2eb4c-d6f0-4f74-87c1-15f687f7650f"
            }
          ]
        },
        {
          "id": "6c858849-d548-4bd0-8239-5dcf6bbf521c",
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
              "id": "76af0ba5-eec7-4c71-a2d6-95d5e0e0e19b"
            }
          ]
        },
        {
          "id": "85395ec3-b696-4890-83c9-ad9b49a78a26",
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
              "id": "2925143d-cf92-4a52-8537-368f48c82689"
            }
          ]
        },
        {
          "id": "6b1299b5-e0cd-4907-8e34-c15e2af891e1",
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
              "id": "7f7a5730-6067-490a-9127-59464e9620bf"
            }
          ]
        },
        {
          "id": "20be0ed1-708a-4ca4-bf5f-4b7c94de5911",
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
              "id": "eaf7b6b0-db25-488e-a34c-318e3356c25b"
            }
          ]
        },
        {
          "id": "7913fd93-35b3-4e3c-a8b0-c57decd5deaa",
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
              "id": "8632c6b4-384e-4b57-aa14-662814682945"
            }
          ]
        },
        {
          "id": "14c2df23-c243-4e29-aa58-0caadaadfaa7",
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
              "id": "1ca2c545-96d2-432a-8bbb-819868fc28f7"
            }
          ]
        },
        {
          "id": "7627c1cc-8310-490e-808a-923b6897b397",
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
              "id": "bd048c88-65da-48b8-b1cf-ea1f08c03870"
            }
          ]
        },
        {
          "id": "96720a4b-d8df-420a-b567-41313b48396c",
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
              "id": "8bd8d134-c0f6-485f-973d-30a34f0a8ca7"
            }
          ]
        }
      ]
    },
    {
      "name": "Publish",
      "item": [
        {
          "id": "8bb62639-65c8-4ee1-a28a-fe7d79f9be47",
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
              "id": "6f27e7e2-1df2-4ec9-9112-04f9d8ab491b"
            }
          ]
        },
        {
          "id": "44cec016-39d2-4184-a515-a09e7e6e8920",
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
              "id": "94e84181-5862-4409-9831-855ceb78ab44"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "2fb477b2-d806-43fc-a3b4-57eae8fd3845",
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
              "id": "d54c24b1-706e-47bf-8a69-c8e8af59db3e"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachments",
      "item": [
        {
          "id": "6b92bbfe-5031-40af-b6b3-bed279e3321a",
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
              "id": "6c12727d-560f-4333-9a28-36f3f6830d12"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "cf428e88-e0a5-4433-85d3-1bea37877696",
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
              "id": "8ec2c126-a53b-4f37-b8de-76e6b125f0b5"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "3ecb47d0-3b71-4692-a33d-835395acb62b",
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
              "id": "3f749fa0-73da-4ab5-8a6f-c755c9211587"
            }
          ]
        },
        {
          "id": "b7b75ec8-e1d3-488f-a7c3-279b39be6324",
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
              "id": "0f0b3a96-27f0-4db1-8f4a-4df17856928b"
            }
          ]
        },
        {
          "id": "a97b6384-1d73-4f1c-b1c1-742354e65e60",
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
              "id": "b01660cc-3e28-4da5-8058-d2b77cb5076b"
            }
          ]
        }
      ]
    },
    {
      "name": "Historycontent",
      "item": [
        {
          "id": "4d9230fb-32b9-4b8f-af01-14bc454fd470",
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
              "id": "5b145959-b2ec-4225-81dd-329fc5195b49"
            }
          ]
        }
      ]
    },
    {
      "name": "Macro",
      "item": [
        {
          "id": "b833c101-98bc-4834-befa-83f96081be49",
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
              "id": "99a19ff4-31e8-4cde-857a-f209a173e500"
            }
          ]
        }
      ]
    },
    {
      "name": "Labelscontent",
      "item": [
        {
          "id": "5c2c144a-ae51-4a11-a3de-f9618c30d241",
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
              "id": "41c7ddf1-641d-444f-b87e-55588b2af87a"
            }
          ]
        }
      ]
    },
    {
      "name": "Labels",
      "item": [
        {
          "id": "41e1c0af-02a6-4571-9962-ca2bc5d9b11f",
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
              "id": "711d2141-fb4a-40b2-9750-7891ddc12057"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "4d9d16d5-363c-4e4e-b9cb-43edba9b63c5",
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
              "id": "549c390c-ce51-4307-bc01-0045bc695754"
            }
          ]
        },
        {
          "id": "e4367fa1-730a-459c-b496-069ebc5fdccd",
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
              "id": "cad90131-5ce5-42b6-a2ac-b7d1a4d3fc0e"
            }
          ]
        },
        {
          "id": "87e63d6e-4fc0-4517-ad85-f1b5325fc508",
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
              "id": "94dd5504-d887-4c24-91f1-ae189755db65"
            }
          ]
        },
        {
          "id": "02edc794-b2f0-4d90-904f-753c9fbcd64c",
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
              "id": "018da639-d62e-4c63-b1b1-5a99fbb33c75"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchespage",
      "item": [
        {
          "id": "10f1656a-d9ea-4b48-8364-41c5a5ef9a6a",
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
              "id": "2eefc794-2102-4162-9216-72c867e62646"
            }
          ]
        }
      ]
    },
    {
      "name": "Watchesspace",
      "item": [
        {
          "id": "530aab90-044f-4c7e-84ca-49351def7432",
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
              "id": "44d3acac-4e03-4c78-b67e-fdf13969d3c8"
            }
          ]
        }
      ]
    },
    {
      "name": "Copy",
      "item": [
        {
          "id": "59f17265-31ad-4b10-9e9d-ef87bb1130f2",
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
              "id": "d29f2e5c-3b06-4efd-a00c-e6112e241497"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictions",
      "item": [
        {
          "id": "e6bfef7c-4745-483c-bba0-92c306538d5a",
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
              "id": "b73c2c77-d6ab-4c45-9f2e-93e9d1a851c5"
            }
          ]
        },
        {
          "id": "7c8db3d6-35b6-45d7-bc8e-6ec6d1d6099e",
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
              "id": "2ddc4e48-3f00-4143-b870-d2bd2b5d4dac"
            }
          ]
        },
        {
          "id": "91c5c2e3-2e05-45bc-af9c-48ec8ba544ba",
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
              "id": "c2ff8750-6c25-43b6-a520-90ef03090c81"
            }
          ]
        },
        {
          "id": "f1cb7890-ed65-47ab-a6d2-172b5bfb1aab",
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
              "id": "8ca9925e-370e-43c7-9257-893322faacee"
            }
          ]
        },
        {
          "id": "d87198bf-86a5-47cd-891e-832182a32903",
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
              "id": "62886561-05cc-4b4b-a715-8b801468afb6"
            }
          ]
        }
      ]
    },
    {
      "name": "Restrictionsoperation",
      "item": [
        {
          "id": "37036022-fa6b-4ac1-a951-ee11c5865380",
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
              "id": "6ec974b6-ffac-46db-ba79-ff7ff55cf63d"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "fa996af8-1072-4848-a4dc-8b7f921e4f03",
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
              "id": "afa51947-bbd5-4ca3-b1c0-468c2e233942"
            }
          ]
        },
        {
          "id": "cd74b389-4821-4db1-9c15-770967b43944",
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
              "id": "615e191f-dbe2-4449-992a-c3265bcaaa7f"
            }
          ]
        },
        {
          "id": "9c5a1968-3a6b-4b49-941b-7e4e2e0084b8",
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
              "id": "5986265e-d544-488c-89c9-4b447aba4fd2"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "c96f8163-838d-4a92-a92d-98685ae95c5f",
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
              "id": "08d12d5c-b255-4f46-b1df-8290a45b48db"
            }
          ]
        }
      ]
    },
    {
      "name": "Restore",
      "item": [
        {
          "id": "7599cb52-4855-470c-a369-ac21936ab361",
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
              "id": "a2ce1b47-e5a8-4dd1-9b0f-e7247ecc6bc2"
            }
          ]
        }
      ]
    },
    {
      "name": "Convert",
      "item": [
        {
          "id": "4b11c545-4e4a-4035-942d-c1ad2cfd49ae",
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
              "id": "1b7d0338-0fef-4a31-820e-e72f3aaa1e99"
            }
          ]
        }
      ]
    },
    {
      "name": "Groups",
      "item": [
        {
          "id": "eb2d72dd-0794-4242-8f41-af1f4180d16e",
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
              "id": "1d53ca49-5e89-44bb-96ef-94b2d17f0278"
            }
          ]
        }
      ]
    },
    {
      "name": "Long-running",
      "item": [
        {
          "id": "b72899fd-af98-4f15-9d8e-a61b0cae9893",
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
              "id": "a60dc58b-9f1a-4b0c-831c-751fcad51d52"
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