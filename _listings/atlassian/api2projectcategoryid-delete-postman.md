{
  "info": {
    "name": "Jira Cloud API Remove project category",
    "_postman_id": "db8af739-7fb6-48a3-bab8-fe06402e43ba",
    "description": "Delete a project category.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "88c07cd2-e40d-4873-949c-de425cd385a1",
          "name": "com.atlassian.jira.rest.v2.admin.ApplicationPropertiesResource.getApplicationProperty_get",
          "request": {
            "url": "{{default}}/api/2/application-properties?key=%7B%7D&keyFilter=%7B%7D&permissionLevel=%7B%7D",
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
            "description": "Returns an application property."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "01ac9e13-86dc-45b0-a5aa-724f9511e94d"
            }
          ]
        },
        {
          "id": "98155c8f-094a-4f3a-88c6-236a0c0a356c",
          "name": "com.atlassian.jira.rest.v2.admin.applicationrole.ApplicationRoleResource.getAllApplicationRoles_get",
          "request": {
            "url": "{{default}}/api/2/applicationrole",
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
            "description": "Returns all ApplicationRoles in the system. Will also return an ETag header containing a version hash of the collection of ApplicationRoles."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0611297b-0d99-4fcb-b8eb-5467228e7e67"
            }
          ]
        },
        {
          "id": "388d9d0c-5897-4eb5-b764-da864cdec1a1",
          "name": "com.atlassian.jira.rest.v2.admin.applicationrole.ApplicationRoleResource.getApplicationRole_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/applicationrole/:key"
              ],
              "variable": [
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
            "description": "Returns the ApplicationRole with passed key if it exists."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d843f63-5e2a-422d-9cec-9fa88d952af8"
            }
          ]
        }
      ]
    },
    {
      "name": "Advanced",
      "item": [
        {
          "id": "3c1b7f92-20c2-453a-b40a-242bf621fa82",
          "name": "com.atlassian.jira.rest.v2.admin.ApplicationPropertiesResource.getAdvancedSettings_get",
          "request": {
            "url": "{{default}}/api/2/application-properties/advanced-settings",
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
            "description": "Returns the properties that are displayed on the General Configuration Advanced Settings page."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d426abcb-a5b2-44f9-b4d7-5cccb1acb3f9"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "30ef084e-124c-4929-b676-dfe06edfcf3a",
          "name": "com.atlassian.jira.rest.v2.admin.ApplicationPropertiesResource.setApplicationProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/application-properties/:id"
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
            "description": "Modify an application property via PUT. The \"value\" field present in the PUT will override the existing value."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7f2b8d4a-f1b4-418e-84a9-b49d1aeeae07"
            }
          ]
        },
        {
          "id": "d0eebac0-e2c9-45ad-a1ea-23ec6aebf02a",
          "name": "com.atlassian.jira.rest.v2.issue.CommentPropertyResource.setCommentProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/comment/:commentId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "commentId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Sets the value of the specified comment's property.\n\nYou can use this resource to store a custom data against the comment identified by the key or by the id. The user who stores the data is required to have permissions to administer the comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eb9eeb63-469e-4de0-a775-b1e3cd13adf8"
            }
          ]
        },
        {
          "id": "6aa4a72d-40ce-4fab-a47b-29c54398edc6",
          "name": "com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.setSharedTimeTrackingConfiguratio",
          "request": {
            "url": "{{default}}/api/2/configuration/timetracking/options",
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
            "description": "Sets the time tracking settings.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f0aaad55-5cd9-4801-86fe-3c40093debd4"
            }
          ]
        },
        {
          "id": "0816e38d-5368-4021-9db6-19ec7193bdb6",
          "name": "com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.setDashboardItemProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/dashboard/:dashboardId/items/:itemId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "dashboardId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "itemId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Sets the value of a dashboard item property. Use this resource in apps to store custom data against a dashboard item.  \n  \nA dashboard item enables an app to add user-specific information to a user dashboard. Dashboard items are exposed to users as gadgets that users can add to their dashboards. For more information on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).  \n  \nWhen an app creates a dashboard item it registers a callback to receive the dashboard item ID. The callback fires whenever the item is rendered or, where the item is configurable, the user edits the item. The app then uses this resource to store the item's content or configuration details. For more information on working with dashboard items, see [Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/) and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/) documentation.  \n  \nThere is no resource to set or get dashboard items.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira. However, to set a dashboard item property the user must be the owner of the dashboard. Note, users with the _Administer Jira_ [global permission](href=) are considered owners of the System dashboard.  \n  \nThe value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 bytes."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3093305b-72ad-46d7-82db-d7fd83b55687"
            }
          ]
        },
        {
          "id": "3392d5c0-ed41-4696-82f1-bd02687839e3",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.setDefaultShareScope_put",
          "request": {
            "url": "{{default}}/api/2/filter/defaultShareScope",
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
            "description": "Sets the default sharing for new filters and dashboards for a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "22b3b47f-ae98-4900-807e-6dd1b38910b7"
            }
          ]
        },
        {
          "id": "b77fd017-bd28-4977-b3d7-c00685a62d2c",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.setColumns_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/columns"
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
            "description": "Sets the columns for a filter. Only navigable fields can be set as columns. Use [Get fields](https://developer.atlassian.com/cloud/jira/platform/rest#api-api-2-field-get) to get the list fields in Jira. A navigable field has `navigable` set to `true`. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)) and permission to view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c60916c-ba01-4a04-ab44-e4f3b52b11e0"
            }
          ]
        },
        {
          "id": "3dee07f9-bcc1-49b2-bd33-2ac1d63911d3",
          "name": "com.atlassian.jira.rest.v2.issue.IssuePropertyResource.setIssueProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Sets the value of the specified issue's property.\n\nYou can use this resource to store a custom data against the issue identified by the key or by the id. The user who stores the data is required to have permissions to edit the issue."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "52144856-822c-47c8-b5d7-b8c7e68606cf"
            }
          ]
        },
        {
          "id": "4e77f163-ad39-41a2-8bfb-49248a10084c",
          "name": "com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.setWorklogProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog/:worklogId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "worklogId",
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
            "description": "Sets the value of the specified worklog's property.\n\nYou can use this resource to store a custom data against the worklog identified by the key or by the id. The user who stores the data is required to have permissions to administer the worklog."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bfff8aa0-a8c7-4e75-a927-011b21b7822e"
            }
          ]
        },
        {
          "id": "7464f7d9-7531-44ca-b0c5-8d0377724cad",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.setIssueTypeProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:issueTypeId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueTypeId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Creates or updates the value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). Use this resource to store and update data against an issue type. The value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length of the property value is 32768 bytes. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3befed15-e487-4e53-a75b-98e3252f0212"
            }
          ]
        },
        {
          "id": "0ad17410-ced9-4307-9b55-c66d7a7f315b",
          "name": "com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.setPreference_put",
          "request": {
            "url": "{{default}}/api/2/mypreferences?key=%7B%7D",
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
            "description": "Sets preference of the currently logged in user. Preference key must be provided as input parameters (key). Value must be provided as POST body."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c3e3123b-fd83-48f3-a0fa-cbd9db48aa8f"
            }
          ]
        },
        {
          "id": "ddf31dfd-0e4c-41f0-8dd4-6bc736f8f5b9",
          "name": "com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.setLocale_put",
          "request": {
            "url": "{{default}}/api/2/mypreferences/locale",
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
            "description": "Sets the locale of the currently logged in user. Locale JSON must be provided as PUT body."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e414b381-155f-4ea6-b843-de8c53873f1f"
            }
          ]
        },
        {
          "id": "00e4f95e-6cbb-4a49-a164-97edc8e6b841",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.setProjectProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Sets the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). You can use project properties to store custom data against the project.\n\nThe value of the request body must be a [valid](http://tools.ietf.org/html/rfc4627), non-empty JSON blob. The maximum length is 32768 bytes.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1b481191-9f36-4a17-8bd1-f726dc858f76"
            }
          ]
        },
        {
          "id": "bc0d270d-9c3a-4417-8492-e4c3fbd63be4",
          "name": "com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.setActors_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/role/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "projectIdOrKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Associates actors with the project role for the project, replacing all existing actors.\n\nIf you want to add actors to the project without overwriting the existing list, then use [Add actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-post).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4446e8dd-d58d-4524-a654-986dde4d15d4"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "8766271f-a03d-4e4d-bcdd-476c4e38810a",
          "name": "com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.getAttachmentMeta_get",
          "request": {
            "url": "{{default}}/api/2/attachment/meta",
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
            "description": "Returns the global attachment settings, that is, whether attachments are enabled and the maximum attachment size allowed.  \n  \nNote that there are also [project permissions](https://confluence.atlassian.com/x/yodKLg) that restrict whether users can create and delete attachments or not.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3c917d4f-50d3-48b5-a55e-01833ffdc744"
            }
          ]
        },
        {
          "id": "ee785a89-ec09-4041-b65e-15a6c951001c",
          "name": "com.atlassian.jira.rest.v2.admin.ConfigurationResource.getConfiguration_get",
          "request": {
            "url": "{{default}}/api/2/configuration",
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
            "description": "Returns the [global settings](https://confluence.atlassian.com/x/qYXKM) in Jira. These settings determine whether optional features (for example, sub-tasks, time tracking, and others) are enabled. If time tracking is enabled, this method also returns the time tracking configuration.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "068d4ac5-8bc6-44c4-bd0a-7544eae17ce1"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "ceb4e77a-0494-4d9b-a5a8-06600e7c1316",
          "name": "com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.getAttachment_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/attachment/:id"
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
            "description": "Returns the metadata for an attachment. Note that the attachment itself is not returned.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the calling user must have permission to view the issue that the attachment belongs to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "40c43ae5-3af6-46ab-b9f4-2e1fa3e2261e"
            }
          ]
        },
        {
          "id": "478f9d82-0df9-4034-bf16-4656aa4dbd52",
          "name": "com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.removeAttachment_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/attachment/:id"
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
            "description": "Deletes an attachment from an issue.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Any of the following permissions in the project that the issue is in:\n\n*   _Delete own attachments_ [project permission](https://confluence.atlassian.com/x/yodKLg) to delete an attachment created by the calling user.\n*   _Delete all attachments_ [project permission](https://confluence.atlassian.com/x/yodKLg) to delete an attachment created by any user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7073cddb-66b0-4828-b113-de829ff55b54"
            }
          ]
        },
        {
          "id": "4a29fce5-d62a-49f1-b4eb-6840df5f745b",
          "name": "com.atlassian.jira.rest.v2.issue.IssueAttachmentsResource.addAttachment_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/attachments"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Add one or more attachments to an issue.\n\nThis resource expects a multipart post. The media-type multipart/form-data is defined in RFC 1867. Most client libraries have classes that make dealing with multipart posts simple. For instance, in Java the Apache HTTP Components library provides a [MultiPartEntity](http://hc.apache.org/httpcomponents-client-ga/httpmime/apidocs/org/apache/http/entity/mime/MultipartEntity.html) that makes it simple to submit a multipart POST.\n\nIn order to protect against XSRF attacks, because this method accepts multipart/form-data, it has XSRF protection on it. This means you must submit a header of X-Atlassian-Token: no-check with the request, otherwise it will be blocked.\n\nThe name of the multipart/form-data parameter that contains attachments must be \"file\"\n\nA simple example to upload a file called \"myfile.txt\" to issue REST-123:\n\ncurl -D- -u admin:admin -X POST -H \"X-Atlassian-Token: no-check\" -F \"file=@myfile.txt\" http://myhost/rest/api/2/issue/TEST-123/attachments"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "356729be-7e44-4018-aff5-1c7d2e59d734"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadataan",
      "item": [
        {
          "id": "bec27a13-e887-4e52-985f-fd4cf5d5985e",
          "name": "com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.expandAttachmentForHumans_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/attachment/:id/expand/human"
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
            "description": "Returns the metadata for the contents of an attachment, if it is an archive, and metadata for the attachment itself. For example, if the attachment is a ZIP archive, then information about the files in the archive is returned and metadata for the ZIP archive. Currently, only the ZIP archive format is supported.  \n  \nUse this method to retrieve data that is presented in the UI, as this method returns the metadata for the attachment itself, such as the attachment's ID and name. Otherwise, use [Get contents metadata for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-raw-get), which only returns the metadata for the attachment's contents.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the calling user must have permission to view the issue that the attachment belongs to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f6d39491-ace8-430d-8cb6-62dc7f512f7b"
            }
          ]
        }
      ]
    },
    {
      "name": "Contents",
      "item": [
        {
          "id": "5fba65b3-ae89-41e9-b601-6650ad671803",
          "name": "com.atlassian.jira.rest.v2.issue.attachment.AttachmentResource.expandAttachmentForMachines_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/attachment/:id/expand/raw"
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
            "description": "Returns the metadata for the contents of an attachment, if it is an archive. For example, if the attachment is a ZIP archive, then information about the files in the archive is returned. Currently, only the ZIP archive format is supported.  \n  \nUse this method if you are processing the data without presenting it in the UI, as this method only returns the metadata for the contents of the attachment. Otherwise, to retrieve data to present in the UI, use [Get all metadata for an expanded attachment](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-attachment-id-expand-human-get) which also returns the metadata for the attachment itself, such as the attachment's ID and name.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the calling user must have permission to view the issue that the attachment belongs to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3af4c7b7-9e84-4f85-9f0c-a895ffb5f9b5"
            }
          ]
        }
      ]
    },
    {
      "name": "Audit",
      "item": [
        {
          "id": "3f44c0eb-bedb-4909-849c-82e10677ba6b",
          "name": "com.atlassian.jira.rest.v2.admin.auditing.AuditingResource.getAuditRecords_get",
          "request": {
            "url": "{{default}}/api/2/auditing/record?filter=%7B%7D&from=%7B%7D&limit=%7B%7D&offset=%7B%7D&to=%7B%7D",
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
            "description": "Returns auditing records filtered using provided parameters"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d1c707a9-ba92-40f6-96ec-86782dc5031a"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "2308a08e-a7a7-4346-ba38-faaf239afed6",
          "name": "com.atlassian.jira.rest.v2.issue.AvatarResource.getAllSystemAvatars_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/avatar/:type/system"
              ],
              "variable": [
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
            "description": "Returns all system avatars of the given type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6dc11243-5602-42c5-875a-ebfbf1809c75"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "5b81af82-2612-4970-9cca-92b939700295",
          "name": "com.atlassian.jira.rest.v2.issue.IssueCommentListResource.getCommentsByIds_post",
          "request": {
            "url": "{{default}}/api/2/comment/list?expand=%7B%7D",
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
            "description": "Returns comments for given comments ids. Only comments to which the user has permissions, will be included in the result. The returned set of comments is limited to 1000 elements."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7cd3c24f-6907-4c2d-8109-92ee5737c6e8"
            }
          ]
        },
        {
          "id": "70ed9bd4-c278-4519-98e2-d7c1e9e5dd8e",
          "name": "com.atlassian.jira.rest.v2.issue.IssueCommentResource.getComments_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/comment"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "orderBy",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns all comments for an issue.\n\nResults can be ordered by the \"created\" field which means the date a comment was added."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18676d93-baed-4a40-af3f-6d99d5835336"
            }
          ]
        }
      ]
    },
    {
      "name": "Comment",
      "item": [
        {
          "id": "1c291ea2-20b1-4020-b052-78e5e38cdd4a",
          "name": "com.atlassian.jira.rest.v2.issue.CommentPropertyResource.getCommentPropertyKeys_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/comment/:commentId/properties"
              ],
              "variable": [
                {
                  "id": "commentId",
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
            "description": "Returns the keys of all properties for the comment identified by the key or by the id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f089e959-1109-4861-a209-8f6251ff59ed"
            }
          ]
        },
        {
          "id": "68fddb48-060a-42ab-a3e2-55b262c386be",
          "name": "com.atlassian.jira.rest.v2.issue.CommentPropertyResource.getCommentProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/comment/:commentId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "commentId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Returns the value of the property with a given key from the comment identified by the key or by the id. The user who retrieves the property is required to have permissions to read the comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1fd19b32-4678-4dc4-b648-8b7697cbe126"
            }
          ]
        },
        {
          "id": "3779f087-7b97-4bc9-977f-3b67e7e02d75",
          "name": "com.atlassian.jira.rest.v2.issue.CommentPropertyResource.deleteCommentProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/comment/:commentId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "commentId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Removes the property from the comment identified by the key or by the id. Ths user removing the property is required to have permissions to administer the comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57addda2-624f-4a82-a66b-0970b43fd170"
            }
          ]
        },
        {
          "id": "1d3e4c07-f9fc-4ce4-aac1-8e93f0baf4eb",
          "name": "com.atlassian.jira.rest.v2.issue.IssueCommentResource.addComment_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/comment"
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
                  "id": "issueIdOrKey",
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
            "description": "Adds a new comment to an issue."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5e6e546-0617-497a-b66c-056a451ab326"
            }
          ]
        },
        {
          "id": "32cca105-dbf5-428c-bd59-fd6d37fdec57",
          "name": "com.atlassian.jira.rest.v2.issue.IssueCommentResource.getComment_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/comment/:id"
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
                  "id": "issueIdOrKey",
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
            "description": "Returns a single comment."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9cf8008b-558b-458e-b1fe-c19a245f82a7"
            }
          ]
        },
        {
          "id": "d22a73df-9807-41a6-895d-82027a8b92d7",
          "name": "com.atlassian.jira.rest.v2.issue.IssueCommentResource.updateComment_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/comment/:id"
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
                  "id": "issueIdOrKey",
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
            "description": "Updates an existing comment using its JSON representation."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "07865262-1cf4-4553-95c8-ec29b2e83f47"
            }
          ]
        },
        {
          "id": "133e7ba3-afb9-4717-b06d-04d97b3f9ccc",
          "name": "com.atlassian.jira.rest.v2.issue.IssueCommentResource.deleteComment_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/comment/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "issueIdOrKey",
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
            "description": "Deletes an existing comment ."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3296784f-3992-47df-801a-a2c6ebf54d3d"
            }
          ]
        }
      ]
    },
    {
      "name": "Component",
      "item": [
        {
          "id": "bd497b5b-6a96-4dbd-8527-0a25a12a9a41",
          "name": "com.atlassian.jira.rest.v2.issue.ComponentResource.createComponent_post",
          "request": {
            "url": "{{default}}/api/2/component",
            "method": "POST",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a component. Use components to provide containers for issues within a project. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:\n\n*   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).\n*   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cde9c729-637a-48ef-bf99-f03fd7579a2c"
            }
          ]
        },
        {
          "id": "d13f8ccf-c650-4eb8-8bb4-dd441b593a50",
          "name": "com.atlassian.jira.rest.v2.issue.ComponentResource.getComponent_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/component/:id"
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
            "description": "Returns a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "85a52535-5c09-434a-8a3d-ce27011d1c92"
            }
          ]
        },
        {
          "id": "92243b3f-c161-447b-acde-2d976b3f86a2",
          "name": "com.atlassian.jira.rest.v2.issue.ComponentResource.updateComponent_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/component/:id"
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
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string (\"\") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:\n\n*   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).\n*   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de86c96f-abec-4e7b-8195-6b3779137772"
            }
          ]
        },
        {
          "id": "190d5408-9202-4f92-8db2-dcdc4bc54b97",
          "name": "com.atlassian.jira.rest.v2.issue.ComponentResource.deleteComponent_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/component/:id"
              ],
              "query": [
                {
                  "key": "moveIssuesTo",
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
            "description": "Deletes a component. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:\n\n*   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).\n*   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "907ef53b-4869-4c9d-9293-fa7c3206129f"
            }
          ]
        },
        {
          "id": "d0ba2988-4ca4-4b83-8b91-7f23953587cc",
          "name": "com.atlassian.jira.rest.v2.issue.ComponentResource.getComponentRelatedIssues_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/component/:id/relatedIssueCounts"
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
            "description": "Returns the counts of issues assigned to the component. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aa119afa-2130-4bba-86bc-b42823592002"
            }
          ]
        }
      ]
    },
    {
      "name": "Selected",
      "item": [
        {
          "id": "c3461e6e-29a0-472f-931d-c649d8129495",
          "name": "com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getSelectedTimeTrackingImplementa",
          "request": {
            "url": "{{default}}/api/2/configuration/timetracking",
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
            "description": "Returns the time tracking provider that is currently selected. Note that if time tracking is disabled, then a successful but empty response is returned.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1877720b-101e-4f37-a52f-bfda3f4e60ed"
            }
          ]
        }
      ]
    },
    {
      "name": "Select",
      "item": [
        {
          "id": "0ee61587-b246-4140-9473-d0eb4252b51b",
          "name": "com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.selectTimeTrackingImplementation_",
          "request": {
            "url": "{{default}}/api/2/configuration/timetracking",
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
            "description": "Selects a time tracking provider.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "583b34e8-af7c-4101-8d81-efe34efad6ee"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "87100b71-f07f-49af-8f8d-433f13c742c6",
          "name": "com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.disableTimeTracking_delete",
          "request": {
            "url": "{{default}}/api/2/configuration/timetracking",
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
            "description": "Disables time tracking.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "80f3a3ce-9e23-4e82-a02f-a155df0e27ed"
            }
          ]
        }
      ]
    },
    {
      "name": "Time",
      "item": [
        {
          "id": "7ca31439-e41a-43ef-ba0e-4d9910d1d782",
          "name": "com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getAvailableTimeTrackingImplement",
          "request": {
            "url": "{{default}}/api/2/configuration/timetracking/list",
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
            "description": "Returns all time tracking providers. By default, Jira only has one time tracking provider: _JIRA provided time tracking_. However, you can install other time tracking providers via apps from the Atlassian Marketplace. For more information on time tracking providers, see the documentation for the [Time Tracking Provider](https://developer.atlassian.com/cloud/jira/platform/modules/time-tracking-provider/) module.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "353bad6e-1ec7-468a-ba2c-6f640c79e37a"
            }
          ]
        },
        {
          "id": "13dc53ed-207e-4225-aece-b1e90d9461bb",
          "name": "com.atlassian.jira.rest.v2.admin.timetracking.TimeTrackingResource.getSharedTimeTrackingConfiguratio",
          "request": {
            "url": "{{default}}/api/2/configuration/timetracking/options",
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
            "description": "Returns the time tracking settings. This includes settings such as the time format, default time unit, and others. For more information, see [Configuring time tracking](https://confluence.atlassian.com/x/qoXKM).  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** Jira administration (that is, member of the _administrators_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c251a81d-e827-4655-aeac-655b88e5f84f"
            }
          ]
        }
      ]
    },
    {
      "name": "Custom",
      "item": [
        {
          "id": "f45d74d9-e933-48e0-a7f8-007452dada77",
          "name": "com.atlassian.jira.rest.v2.issue.customfield.CustomFieldOptionResource.getCustomFieldOption_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/customFieldOption/:id"
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
            "description": "Returns a custom field option. For example, an option in a cascading select list.  \n  \n**[Permissions](https://developer.atlassian.com/cloud/jira/platform/rest/#permissions) required:** None."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0e533cc5-76e8-488a-821d-782fe4ccc3c6"
            }
          ]
        },
        {
          "id": "6a49f05f-0a60-4ff1-82ab-ab5aef33ef50",
          "name": "com.atlassian.jira.rest.v2.issue.FieldResource.createCustomField_post",
          "request": {
            "url": "{{default}}/api/2/field",
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
            "description": "Creates a custom field.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec25438e-2877-48b7-afd8-27dd1058d3df"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboards",
      "item": [
        {
          "id": "28cdcf2c-8efa-470a-a494-291e61df3e14",
          "name": "com.atlassian.jira.rest.v2.dashboard.DashboardResource.getAllDashboards_get",
          "request": {
            "url": "{{default}}/api/2/dashboard?filter=%7B%7D&maxResults=%7B%7D&startAt=%7B%7D",
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
            "description": "Returns a list of dashboards owned by or shared with the user. The list may be filtered to include only favorite or owned dashboards.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7de05c93-ef63-47bf-aeef-c864886a5742"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboard",
      "item": [
        {
          "id": "1d2ec803-c40f-4fc1-89b9-29b2cfddb490",
          "name": "com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.getDashboardItemPropertyKeys_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/dashboard/:dashboardId/items/:itemId/properties"
              ],
              "variable": [
                {
                  "id": "dashboardId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "itemId",
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
            "description": "Returns the keys of all properties for a dashboard item.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira. However, to get the property keys the user must be the owner of the dashboard or be shared the dashboard. Note, users with the _Administer Jira_ [global permission](href=) are considered owners of the System dashboard. The System dashboard is considered to be shared with all other users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "125b316c-ab5c-4d12-b4a5-0cb84ba82259"
            }
          ]
        },
        {
          "id": "3b92125a-08aa-4653-9cb9-ee6144020534",
          "name": "com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.getDashboardItemProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/dashboard/:dashboardId/items/:itemId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "dashboardId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "itemId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Returns the key and value of a dashboard item property.  \n  \nA dashboard item enables an app to add user-specific information to a user dashboard. Dashboard items are exposed to users as gadgets that users can add to their dashboards. For more information on how users do this, see [Adding and customizing gadgets](https://confluence.atlassian.com/x/7AeiLQ).  \n  \nWhen an app creates a dashboard item it registers a callback to receive the dashboard item ID. The callback fires whenever the item is rendered or, where the item is configurable, the user edits the item. The app then uses this resource to store the item's content or configuration details. For more information on working with dashboard items, see [Building a dashboard item for a JIRA Connect add-on](https://developer.atlassian.com/server/jira/platform/guide-building-a-dashboard-item-for-a-jira-connect-add-on-33746254/) and the [Dashboard Item](https://developer.atlassian.com/cloud/jira/platform/modules/dashboard-item/) documentation.  \n  \nThere is no resource to set or get dashboard items.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira. However, to get a dashboard item property the user must be the owner of the dashboard or be shared the dashboard. Note, users with the _Administer Jira_ [global permission](href=) are considered owners of the System dashboard. The System dashboard is considered to be shared with all other users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e182c42e-50d5-40d9-ba47-8e3eeb3768fa"
            }
          ]
        },
        {
          "id": "82bc31a5-c4c5-4719-8918-b89ac06eac51",
          "name": "com.atlassian.jira.rest.v2.dashboard.DashboardItemPropertyResource.deleteDashboardItemProperty_delet",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/dashboard/:dashboardId/items/:itemId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "dashboardId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "itemId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Deletes a dashboard item property.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira. However, to delete a dashboard item property the user must be the owner of the dashboard. Note, users with the _Administer Jira_ [global permission](href=) are considered owners of the System dashboard."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e4a9599-a4b0-4acc-8cde-7cd1b18a3ff9"
            }
          ]
        },
        {
          "id": "ef9b4ad8-9083-4e31-824e-0019c9963b18",
          "name": "com.atlassian.jira.rest.v2.dashboard.DashboardResource.getDashboard_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/dashboard/:id"
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
            "description": "Returns a dashboard.  \n  \n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira. However, to get a dashboard, the dashboard must be shared with the user or the user must own it. Note, users with the _Administer Jira_ [global permission](href=) are considered owners of the System dashboard. The System dashboard is considered to be shared with all other users."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "93243aaf-314e-4e09-a25a-aec0c1be5767"
            }
          ]
        }
      ]
    },
    {
      "name": "Evaluate",
      "item": [
        {
          "id": "19f9f4fb-c38b-4cac-980e-40c78e8da31c",
          "name": "com.atlassian.jira.rest.v2.expression.JiraExpressionsResource.evaluateJiraExpression_post",
          "request": {
            "url": "{{default}}/api/2/expression/eval?expand=%7B%7D",
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
            "description": "Evaluates a Jira expression and returns its value. Jira expressions is the name of a domain-specific language for Jira that can be used to evaluate expressions in the context of Jira entities."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89e75d66-edba-4ee9-9fc1-763ffef1d1f0"
            }
          ]
        }
      ]
    },
    {
      "name": "Fields",
      "item": [
        {
          "id": "f41c86f6-5a48-498e-aed3-a787fa76c685",
          "name": "com.atlassian.jira.rest.v2.issue.FieldResource.getFields_get",
          "request": {
            "url": "{{default}}/api/2/field",
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
            "description": "Returns all issue fields in Jira, both system and custom fields.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the following rules apply:\n\n*   Fields that cannot be added to the issue navigator are always returned.\n*   Fields that cannot be placed on an issue screen are always returned.\n*   Fields that depend on global Jira settings are only returned if the setting is enabled. That is, timetracking fields, subtasks, votes, and watches.\n*   For all other fields, this method only returns the fields that the current user has permission to see (that is, the field can be used in at least one project that the user can see)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b3c5a18-c275-4726-81a2-3c5a9d662ab6"
            }
          ]
        }
      ]
    },
    {
      "name": "Issue",
      "item": [
        {
          "id": "317948da-cbd0-47d9-9de4-ba77c97d78e9",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getAllIssueFieldOptions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option"
              ],
              "query": [
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fieldKey",
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
            "description": "Returns all options defined for a select list issue field. A select list issue field is a type of [issue field](https://developer.atlassian.com/cloud/jira/platform/modules/issue-field/) that allows a user to select an value from a list of options.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f53ad0b-f2e0-4261-b18e-f0e159fd8e2e"
            }
          ]
        },
        {
          "id": "f253aaad-ca71-46f6-9565-44a7c4fe56b6",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.createIssueFieldOption_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option"
              ],
              "variable": [
                {
                  "id": "fieldKey",
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
            "description": "Creates an option for a select list issue field.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "72bcdff7-e12b-4b9f-9781-19e85f3b19bd"
            }
          ]
        },
        {
          "id": "1d783ba0-afb6-47ff-8f61-6cd00ab2a24c",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getIssueFieldOption_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option/:optionId"
              ],
              "variable": [
                {
                  "id": "fieldKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "optionId",
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
            "description": "Returns an option from a select list issue field.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18572f35-8ab1-41f6-94de-762f9ea3de30"
            }
          ]
        },
        {
          "id": "fe186f56-4c5d-46a4-a22e-e544ec1851fd",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.updateIssueFieldOption_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option/:optionId"
              ],
              "variable": [
                {
                  "id": "fieldKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "optionId",
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
            "description": "Updates an option for a select list issue field. If the option does not exist, a new option is created.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bcb72ee8-9bdf-4243-94ad-ac6dbae07298"
            }
          ]
        },
        {
          "id": "472ee40f-74f6-4ebe-b538-d9757366e9d8",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.deleteIssueFieldOption_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option/:optionId"
              ],
              "variable": [
                {
                  "id": "fieldKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "optionId",
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
            "description": "Deletes an option from a select list issue field.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cdd374d4-1f83-4df0-921d-d4ec1713a638"
            }
          ]
        },
        {
          "id": "a31473ec-1f63-4b43-80ca-b658cce5bc87",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.createIssue_post",
          "request": {
            "url": "{{default}}/api/2/issue?updateHistory=%7B%7D",
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
            "description": "Creates an issue or a sub-task from a JSON representation.\n\nYou can provide two parameters in request's body: `update` or `fields`. The fields, that can be set on an issue create operation, can be determined using the **/rest/api/2/issue/createmeta** resource. If a particular field is not configured to appear on the issue's Create screen, then it will not be returned in the createmeta response. A field validation error will occur if such field is submitted in request.\n\nCreating a sub-task is similar to creating an issue with the following differences:\n\n*   `issueType` field must be set to a sub-task issue type (use `/issue/createmeta` to find sub-task issue types), and\n*   You must provide a `parent` field with the ID or key of the parent issue."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4a803205-3bb6-485f-8a13-ffa4d24198be"
            }
          ]
        },
        {
          "id": "f0710efd-151d-4737-97e9-4e1c949f7497",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getIssuePickerResource_get",
          "request": {
            "url": "{{default}}/api/2/issue/picker?currentIssueKey=%7B%7D&currentJQL=%7B%7D&currentProjectId=%7B%7D&query=%7B%7D&showSubTaskParent=%7B%7D&showSubTasks=%7B%7D",
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
            "description": "Returns a list of suggested issues matching the auto-completion query for the user executing this request. This REST method checks the user's history and browsing context to return issue suggestions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "152ed53c-9769-4501-a558-4386741f4ea4"
            }
          ]
        },
        {
          "id": "2b727b93-0605-4352-a4a1-b3d6253b73c5",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getIssue_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "fieldsByKeys",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "properties",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "updateHistory",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns a full representation of the issue for the given issue key.\n\nThe issue JSON consists of the issue key and a collection of fields. Additional information like links to workflow transition sub-resources, or HTML rendered values of the fields supporting HTML rendering can be retrieved with `expand` request parameter specified.\n\nThe `fields` request parameter accepts a comma-separated list of fields to include in the response. It can be used to retrieve a subset of fields. By default all fields are returned in the response. A particular field can be excluded from the response if prefixed with a \"-\" (minus) sign. Parameter can be provided multiple times on a single request.\n\nBy default, all fields are returned in the response. Note: this is different from a JQL search - only navigable fields are returned by default (`*navigable`)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8e7c5f76-6d55-4f50-a9e5-3c8772845276"
            }
          ]
        },
        {
          "id": "f5e22fab-30dd-4c17-8c9c-2df75d3dbd6b",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.deleteIssue_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey"
              ],
              "query": [
                {
                  "key": "deleteSubtasks",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Deletes an individual issue.\n\nIf the issue has sub-tasks you must set the `deleteSubtasks=true` parameter to delete the issue. You cannot delete an issue without deleting its sub-tasks."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "dfef032c-cfca-4223-9d72-b09ff129504c"
            }
          ]
        },
        {
          "id": "6139dd06-9d79-42cd-9300-3c269c6b508e",
          "name": "com.atlassian.jira.rest.v2.issue.IssuePropertyResource.getIssuePropertyKeys_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/properties"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns the keys of all properties for the issue identified by the key or by the id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b53b9c0b-0774-4153-a4c8-0fffcc670411"
            }
          ]
        },
        {
          "id": "0c3160e6-6b79-43b6-91b6-3333edcd8013",
          "name": "com.atlassian.jira.rest.v2.issue.IssuePropertyResource.getIssueProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Returns the value of the property with a given key from the issue identified by the key or by the id. The user who retrieves the property is required to have permissions to read the issue."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "797869b4-2e6b-497b-a0c5-f5369eed2bcc"
            }
          ]
        },
        {
          "id": "a3c9810a-82de-4dff-8254-8bc319ad1e8f",
          "name": "com.atlassian.jira.rest.v2.issue.IssuePropertyResource.deleteIssueProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Removes the property from the issue identified by the key or by the id. Ths user removing the property is required to have permissions to edit the issue."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "795f3f28-a5de-4a11-8466-72a28c92113e"
            }
          ]
        },
        {
          "id": "da578186-02ed-46c3-95f3-aae5435b270c",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getIssueWatchers_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/watchers"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns the list of watchers for the issue with the given key."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b11571f-356d-41fa-9205-0748a7cc49bb"
            }
          ]
        },
        {
          "id": "ae2a41ad-73ca-4fec-8069-bf5090fd6b9d",
          "name": "com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.getIssueWorklog_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns all work logs for an issue. The response is [paginated](#pagination)  \n**Note:** Work logs won't be returned if the Log work field is hidden for the project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "78166c2f-dfc1-4ca5-bb55-a8b4536949e9"
            }
          ]
        },
        {
          "id": "40fc4542-ccbb-4e38-9709-d4046290113c",
          "name": "com.atlassian.jira.rest.v2.issue.LinkIssueResource.getIssueLink_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issueLink/:linkId"
              ],
              "variable": [
                {
                  "id": "linkId",
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
            "description": "Returns an issue link with the specified id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31398afa-e81c-4a0f-9aaf-4700a30a0317"
            }
          ]
        },
        {
          "id": "e7f93ccc-8101-4398-abec-ec7b5aa42e4c",
          "name": "com.atlassian.jira.rest.v2.issue.LinkIssueResource.deleteIssueLink_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issueLink/:linkId"
              ],
              "variable": [
                {
                  "id": "linkId",
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
            "description": "Deletes an issue link with the specified id. To be able to delete an issue link you must be able to view both issues and must have the link issue permission for at least one of the issues."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9eda2752-d5a5-4ada-8aeb-7544d01f4fff"
            }
          ]
        },
        {
          "id": "e80e0bf0-a671-4328-82df-f3db1a898e62",
          "name": "com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.getIssueLinkTypes_get",
          "request": {
            "url": "{{default}}/api/2/issueLinkType",
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
            "description": "Returns a list of available issue link types, if issue linking is enabled. Each issue link type has an id, a name and a label for the outward and inward link relationship."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b45ff1a5-def1-4b90-8ddb-970be2fcfdf5"
            }
          ]
        },
        {
          "id": "bc9504f0-fc0d-4dcc-bba7-0e4a7d1299cc",
          "name": "com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.createIssueLinkType_post",
          "request": {
            "url": "{{default}}/api/2/issueLinkType",
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
            "description": "Create a new issue link type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8be1f0d4-929a-4e0b-8622-c3a644161d67"
            }
          ]
        },
        {
          "id": "2d8a99ad-25df-4e30-8cbf-78d7ba1a4fde",
          "name": "com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.getIssueLinkType_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issueLinkType/:issueLinkTypeId"
              ],
              "variable": [
                {
                  "id": "issueLinkTypeId",
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
            "description": "Returns for a given issue link type id all information about this issue link type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "659763f6-6402-4e9b-85c5-9698e2536c6b"
            }
          ]
        },
        {
          "id": "713a01d7-48ae-480c-9a76-664e151d5084",
          "name": "com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.updateIssueLinkType_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issueLinkType/:issueLinkTypeId"
              ],
              "variable": [
                {
                  "id": "issueLinkTypeId",
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
            "description": "Update the specified issue link type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f3a68c1-0c32-4302-9333-c4983f9bc77d"
            }
          ]
        },
        {
          "id": "6cfc42cd-8569-490c-b861-67538c267c67",
          "name": "com.atlassian.jira.rest.v2.issue.IssueLinkTypeResource.deleteIssueLinkType_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issueLinkType/:issueLinkTypeId"
              ],
              "variable": [
                {
                  "id": "issueLinkTypeId",
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
            "description": "Delete the specified issue link type."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57cf6521-0e9a-4325-a74f-4f0d88a7b7dd"
            }
          ]
        },
        {
          "id": "c1c01f9a-5172-406b-a090-40d5c889afe5",
          "name": "com.atlassian.jira.rest.v2.issue.IssueSecuritySchemeResource.getIssueSecuritySchemes_get",
          "request": {
            "url": "{{default}}/api/2/issuesecurityschemes",
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
            "description": "Returns all issue security schemes that are defined."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3c921d31-e26d-4b17-bd61-7ee7750b98b6"
            }
          ]
        },
        {
          "id": "fce13435-d0bc-4fef-96bc-f85406ac482a",
          "name": "com.atlassian.jira.rest.v2.issue.IssueSecuritySchemeResource.getIssueSecurityScheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuesecurityschemes/:id"
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
            "description": "Returns the issue security scheme along with that are defined."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd44b973-1a85-4b34-8134-8fc42b3681ee"
            }
          ]
        },
        {
          "id": "d63d7bf7-b687-4ed9-b396-58649ab3ff4e",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypeResource.getIssueAllTypes_get",
          "request": {
            "url": "{{default}}/api/2/issuetype",
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
            "description": "Returns all issue types. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira, however, only issue types that are visible to the user are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8cbe5b6-509d-4082-ae14-da755e463179"
            }
          ]
        },
        {
          "id": "fec37ecc-fb80-4640-baae-7bbecd7d70e2",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypeResource.createIssueType_post",
          "request": {
            "url": "{{default}}/api/2/issuetype",
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
            "description": "Creates an issue type and adds it to the default issue type scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "64e276cc-7ba2-4c7f-ac8c-10a581d96720"
            }
          ]
        },
        {
          "id": "5ff1b0d8-88d3-45ed-8536-429461883238",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypeResource.getIssueType_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:id"
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
            "description": "Returns an issue type. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:\n\n*   _Administer Jira_ [global permission](href=) to get the details of any issue type.\n*   _Browse projects_ project permission to get the details of any issue type associated with the projects the user has permission to browse."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "166fc48d-09ae-4410-8ac2-51e70cd8718b"
            }
          ]
        },
        {
          "id": "8e21e08c-abaf-41b9-8cfd-82d58d2db7c0",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypeResource.updateIssueType_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:id"
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
            "description": "Updates the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "335d3160-124c-4028-96b1-385d1f4265bd"
            }
          ]
        },
        {
          "id": "0ab0fe59-2556-404b-b57b-b61c2261182a",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypeResource.deleteIssueType_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:id"
              ],
              "query": [
                {
                  "key": "alternativeIssueTypeId",
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
            "description": "Deletes the issue type. If the issue type is in use, all uses are updated with the alternative issue type (`alternativeIssueTypeId`). A list of alternative issue types can be obtained from the [Get alternative issue types](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-alternatives-get) resource. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "90b5cf2b-ede1-4ecb-aa7c-18c6cdecaa77"
            }
          ]
        },
        {
          "id": "afd9a275-4048-4d03-9bef-aa5329ab42c3",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypeResource.createIssueTypeAvatar_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:id/avatar2"
              ],
              "query": [
                {
                  "key": "size",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "x",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "y",
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
            "description": "Creates an avatar for the issue type. Specify the avatar's local file location as binary data in the body of the request. Also, include the following headers:\n\n*   `X-Atlassian-Token: no-check`\n*   `Content-Type: image/_image type_` Valid image types are JPEG, GIF, or PNG.\n\nFor example: `curl --request POST \\ --user email@example.com: \\ --header 'X-Atlassian-Token: no-check' \\ --header 'Content-Type: image/< image_type>' \\ --data-binary \"\" \\ --url 'https://your-domain.atlassian.net/rest/api/2/issuetype/{issueTypeId}'This` The avatar is cropped to a square. If no crop parameters are specified, the square originates at the top left of the image. The length of the square's sides is set to the smaller of the height or width of the image. The cropped image is then used to create avatars of 16x16, 24x24, 32x32, and 48x48 in size. After creating the avatar, use [Update issue type](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuetype-id-put) to set it as the issue type's active avatar. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a86382e3-7373-4e82-85df-da324a24d34f"
            }
          ]
        },
        {
          "id": "361de592-a7d4-4ca9-8d9f-be6132628213",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.getIssueTypePropertyKeys_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:issueTypeId/properties"
              ],
              "variable": [
                {
                  "id": "issueTypeId",
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
            "description": "Returns all the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys of the issue type. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   _Administer Jira_ [global permission](href=) to get the property keys of any issue type.\n*   _Browse projects_ project permission to get the property keys of any issue types associated with the projects the user has permission to browse."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f6ba356-3c13-448b-a041-e64b2e331a31"
            }
          ]
        },
        {
          "id": "30b7d49d-8155-4960-ad6d-116fcf614453",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.getIssueTypeProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:issueTypeId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueTypeId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Returns the key and value of the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:\n\n*   _Administer Jira_ [global permission](href=) to get the details of any issue type.\n*   _Browse projects_ project permission to get the details of any issue types associated with the projects the user has permission to browse."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5896ed06-ed63-4188-83f5-5e13d057f207"
            }
          ]
        },
        {
          "id": "82865c94-8311-4630-aa09-ecaf4cc7043a",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypePropertyResource.deleteIssueTypeProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:issueTypeId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueTypeId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Deletes the [issue type property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "077b1b2f-095a-4171-9e42-05ec7db6f306"
            }
          ]
        }
      ]
    },
    {
      "name": "Selectable",
      "item": [
        {
          "id": "83f76eba-d1f0-477f-8534-140b31321375",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getSelectableIssueFieldOptions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option/suggestions/edit"
              ],
              "query": [
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "projectId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fieldKey",
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
            "description": "Returns options defined for a select list issue field that can be viewed and selected by the currently logged in user.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c16a91ae-65f2-46f1-b57b-c44495ada3b1"
            }
          ]
        }
      ]
    },
    {
      "name": "Visible",
      "item": [
        {
          "id": "26a0679b-16d0-4ccb-b6fa-99246ed1d12c",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.getVisibleIssueFieldOptions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option/suggestions/search"
              ],
              "query": [
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "projectId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fieldKey",
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
            "description": "Returns options defined for a select list issue field that can be viewed by the currently logged in user.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca957b3e-9164-4781-8ccc-e4d7140957ad"
            }
          ]
        }
      ]
    },
    {
      "name": "Replace",
      "item": [
        {
          "id": "b399789c-014e-47c9-a1ce-62ec891caf24",
          "name": "com.atlassian.jira.rest.v2.issue.field.IssueFieldOptionResource.replaceIssueFieldOption_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/field/:fieldKey/option/:optionId/issue"
              ],
              "query": [
                {
                  "key": "jql",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "replaceWith",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "fieldKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "optionId",
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
            "description": "Deselects a select list issue field option in all issues that it has been selected in. A different option can be selected to replace the deselected option. The update can also be limited to a smaller set of issues by using a JQL query.\n\nThis is an [asynchronous method](#async). The response object will contain a link to the long-running task. For example, _https://your-domain.atlassian.net/rest/api/2/task/10127_.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission. Jira permissions are not required for the app providing the field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b3477401-4441-44d7-b6ac-402293251348"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "8e156cee-e7d7-46f0-b0e1-2d818610e90d",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getFilters_get",
          "request": {
            "url": "{{default}}/api/2/filter?expand=%7B%7D",
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
            "description": "Returns all filters. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned:\n\n*   Filters owned by the user.\n*   Filters shared with a group that the user is a member of.\n*   Filters shared with a private project that the user can browse.\n*   Filters shared with a public project, even if the user is anonymous.\n*   Filters shared with the public, even if the user is anonymous."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "48d3e9b5-e8b3-4e49-ba18-8c1fc66d15b2"
            }
          ]
        }
      ]
    },
    {
      "name": "Filter",
      "item": [
        {
          "id": "e4f39ed7-a461-41cf-82dd-a90343c8b0f0",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.createFilter_post",
          "request": {
            "url": "{{default}}/api/2/filter?expand=%7B%7D",
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
            "description": "Creates a new filter. The new filter is not shared and not selected as a favorite. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "29b2f9a2-8173-4359-9574-c8f2d231a029"
            }
          ]
        },
        {
          "id": "e21d94ec-e00b-4df3-a5fd-ba15739a5981",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getFilter_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id"
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
            "description": "Returns a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the calling user must have permission view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b5de80b6-d95a-459b-bddc-cb0e6a2c7576"
            }
          ]
        },
        {
          "id": "22bc624e-28cc-40a9-a63e-e37f9ff6c58d",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.updateFilter_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id"
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
            "description": "Updates an existing filter. Use this method to update a filter's name, description, JQL, or sharing. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can update:\n\n*   Private filters (i.e., not shared) can only be updated by the creator of the filter.\n*   Shared filters can only be updated by the creator of the filter or a Jira administrator."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "975b1565-51df-4208-b451-773cefc36530"
            }
          ]
        },
        {
          "id": "19a0d452-74f5-43c1-b4ce-cfd897fcc8ce",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.deleteFilter_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id"
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
            "description": "Delete a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira, however the following rules govern what a user can delete:\n\n*   Private filters (i.e., not shared) can only be deleted by the creator of the filter.\n*   Shared filters can only be deleted by the creator of the filter or a Jira administrator."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43cf1f17-73a4-43b5-8057-9a99022b793a"
            }
          ]
        },
        {
          "id": "c0bdb2ff-b857-4ed3-a77b-6466ed3f007e",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.setFavouriteForFilter_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/favourite"
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
            "description": "Add a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)) and permission to view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de8f29b9-6848-4a06-b9d9-d764f4f3a397"
            }
          ]
        }
      ]
    },
    {
      "name": "Default",
      "item": [
        {
          "id": "3087ef44-fed1-40c0-ac9b-282387fac00b",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getDefaultShareScope_get",
          "request": {
            "url": "{{default}}/api/2/filter/defaultShareScope",
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
            "description": "Returns the default sharing settings for new filters and dashboards for a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bfcd9531-a93f-4460-93d9-cea36a44646a"
            }
          ]
        }
      ]
    },
    {
      "name": "Favourite",
      "item": [
        {
          "id": "82afd365-382a-4b2d-b712-efa26d7c3319",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getFavouriteFilters_get",
          "request": {
            "url": "{{default}}/api/2/filter/favourite?expand=%7B%7D",
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
            "description": "Returns the favorite filters of the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e72de696-a94d-46e0-a76a-bbb3de4ccffa"
            }
          ]
        }
      ]
    },
    {
      "name": "My",
      "item": [
        {
          "id": "3a5a8586-bee1-4418-8bff-98bc959b8bd1",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getMyFilters_get",
          "request": {
            "url": "{{default}}/api/2/filter/my?expand=%7B%7D&includeFavourites=%7B%7D",
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
            "description": "Returns the filters owned by the calling user. If `includeFavourites` is `true`, the user's favorite filters are also returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "69316d7a-6d24-484b-92de-04a9367c9a30"
            }
          ]
        },
        {
          "id": "5abe185f-d12e-4fbd-b308-f6dfdda90252",
          "name": "com.atlassian.jira.rest.v2.permission.PermissionsResource.getMyPermissions_get",
          "request": {
            "url": "{{default}}/api/2/mypermissions?issueId=%7B%7D&issueKey=%7B%7D&permissions=%7B%7D&projectId=%7B%7D&projectKey=%7B%7D",
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
            "description": "Checks whether the current user has the given permissions. You can optionally provide a specific context to get permissions for (`projectKey` OR `projectId` OR `issueKey` OR `issueId`)\n\nIf there is no context provided, then the project related permissions will return true if the user has that permission in ANY project.\n\nIf a project context is provided, project related permissions will return true if the user has the permissions in the specified project. For permissions that are determined using issue data (e.g Current Assignee), true will be returned if the user meets the permission criteria in ANY issue in that project.\n\nIf an issue context is provided, it will return whether or not the user has each permission in that specific issue.\n\nThe above means that for issue-level permissions (EDIT_ISSUE for example), hasPermission may be true when no context is provided, or when a project context is provided, **but** may be false for any given (or all) issues. This would occur (for example) if Reporters were given the EDIT_ISSUE permission. This is because any user could be a reporter, except in the context of a concrete issue, where the reporter is known.\n\nGlobal permissions work in the same way regardless of the scope."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "35ea4961-ffa2-463a-9888-65650e26748c"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchfilters",
      "item": [
        {
          "id": "aeb9041e-4bf0-441b-b9c2-a6d09d3cdcf9",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getFiltersPaginated_get",
          "request": {
            "url": "{{default}}/api/2/filter/search?accountId=%7B%7D&expand=%7B%7D&filterName=%7B%7D&groupname=%7B%7D&maxResults=%7B%7D&orderBy=%7B%7D&owner=%7B%7D&projectId=%7B%7D&startAt=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Search for filters. This method is similar to [Get filters](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-get) except that you can refine the results to include filters that have specific attributes. For example, filters with a particular name. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however only the following filters are returned (if no search parameters are set):\n\n*   Filters owned by the user.\n*   Filters shared with a group that the user is a member of.\n*   Filters shared with a private project that the user can browse.\n*   Filters shared with a public project, even if the user is anonymous.\n*   Filters shared with the public, even if the user is anonymous."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f54f8f05-fe25-4228-b3e4-f5f650e49442"
            }
          ]
        }
      ]
    },
    {
      "name": "Columns",
      "item": [
        {
          "id": "3b9d9cf6-5024-44fb-b795-f04e6ba571fe",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getColumns_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/columns"
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
            "description": "Returns the columns configured for a filter. The column configuration is used when the filter's results are viewed in _List View_ with the _Columns_ set to _Filter_. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the calling user must have permission to view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4f14e34e-193d-4591-b0c0-c67df534a480"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "b4a8f585-6b36-4274-9e0e-a0a9ec72c694",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.resetColumns_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/columns"
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
            "description": "Reset the user's column configuration for the filter to the default. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)) and permission to view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "78c8afeb-7d05-49d4-979e-0d03a8e7268b"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "77de7ede-5e85-4c95-be77-3c88ef1b6cc0",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.deleteFavouriteForFilter_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/favourite"
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
            "description": "Removes a filter as a favorite for the calling user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)) and permission to view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a9820f84-1106-4b50-879c-15dc5bc515a8"
            }
          ]
        },
        {
          "id": "e5d0f0f0-0d3c-49f2-8ec8-e0c34fe7c78c",
          "name": "com.atlassian.jira.rest.v2.issue.GroupResource.removeGroup_delete",
          "request": {
            "url": "{{default}}/api/2/group?groupname=%7B%7D&swapGroup=%7B%7D",
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
            "description": "Deletes a group.\n\n**[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0f78f56f-9fe8-4620-8462-7ae4b69668cc"
            }
          ]
        },
        {
          "id": "c97a2791-c92c-4f2b-99b4-ad2c9435974d",
          "name": "com.atlassian.jira.rest.v2.issue.GroupResource.removeUserFromGroup_delete",
          "request": {
            "url": "{{default}}/api/2/group/user?accountid=%7B%7D&groupname=%7B%7D&username=%7B%7D",
            "method": "DELETE",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Removes a user from a group. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8cc2dea-0138-4c36-8775-f0016a5d2901"
            }
          ]
        },
        {
          "id": "a0d93f5c-d40b-4b20-a44e-16409d83d92f",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.removeVote_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/votes"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Removes a current user's vote from an issue (aka \"unvote\")."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7e551783-54a7-4440-b065-dfc7750e309c"
            }
          ]
        },
        {
          "id": "bddb2835-0faa-4d89-9318-52fa163f9dd5",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.removeWatcher_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/watchers"
              ],
              "query": [
                {
                  "key": "accountId",
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
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Removes the user from the issue's watcher list."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89e9e291-998b-4d71-ad4e-72e95450a74c"
            }
          ]
        },
        {
          "id": "7f62855e-cf1d-430a-ab01-03d7d00dac0b",
          "name": "com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.removePreference_delete",
          "request": {
            "url": "{{default}}/api/2/mypreferences?key=%7B%7D",
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
            "description": "Removes preference of the currently logged in user. Preference key must be provided as input parameters (key)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cf882446-1925-4577-93e6-d5e7024919bc"
            }
          ]
        },
        {
          "id": "ddbc3ec2-91f0-4af3-a6b5-047440b327a0",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.removeProjectCategory_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/projectCategory/:id"
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
            "description": "Delete a project category."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d136afa8-4824-4294-9020-47457e7dfe69"
            }
          ]
        }
      ]
    },
    {
      "name": "Share",
      "item": [
        {
          "id": "ade9b0ee-1ef3-448d-96c6-419362275b50",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getSharePermissions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/permission"
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
            "description": "Returns the share permissions for a filter. A filter can be shared with groups, projects, all logged-in users, or the public. Sharing with all logged-in users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the calling user must have permission to view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30a331bf-d6df-4c8b-b875-98ec9301f1be"
            }
          ]
        },
        {
          "id": "5a43788e-1b1e-47ac-bde3-abadd5d75067",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.addSharePermission_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/permission"
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
            "description": "Add a share permissions to a filter. If you add a global share permission (i.e., all logged-in users or the public) it will overwrite all share permissions for the filter.  \nBe aware that this method uses different objects for updating share permissions compared to [Update filter](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-filter-id-put). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Share dashboards and filters_ [global permission](https://confluence.atlassian.com/x/x4dKLg) and the calling user must own the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a58486e-cccc-4352-9288-c9a5c3f326e2"
            }
          ]
        },
        {
          "id": "4929519b-8d82-4585-9c79-2649c8d6e297",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.getSharePermission_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/permission/:permissionId"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "permissionId",
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
            "description": "Returns a share permission for a filter. A filter can be shared with groups, projects, all logged-in users, or the public. Sharing with all logged-in users or the public is known as a global share permission. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the calling user must have permission to view the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e339a593-57e8-4783-8f9b-106819d3aebf"
            }
          ]
        },
        {
          "id": "7883f3e4-9ea2-4232-899b-c5b99238eeef",
          "name": "com.atlassian.jira.rest.v2.search.FilterResource.deleteSharePermission_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/filter/:id/permission/:permissionId"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "permissionId",
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
            "description": "Deletes a share permission from a filter. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (i.e., member of the _users_ [group](https://confluence.atlassian.com/x/24xjL)) and the calling user must own the filter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "20ccd695-2e27-4a36-8de1-2b1fc1a94c42"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "6d40d296-ac35-4ed7-a340-f8b6dc7755b5",
          "name": "com.atlassian.jira.rest.v2.issue.GroupResource.getGroup_get",
          "request": {
            "url": "{{default}}/api/2/group?expand=%7B%7D&groupname=%7B%7D",
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
            "description": "This resource is deprecated, use [`group/member`](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-group-member-get).\n\nReturns all users in a group.\n\n**[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "75e86c69-8258-4f2a-bdb7-1fa212ae3ceb"
            }
          ]
        },
        {
          "id": "106adb71-a9cf-419a-8379-9b69448cc7c8",
          "name": "com.atlassian.jira.rest.v2.issue.GroupResource.createGroup_post",
          "request": {
            "url": "{{default}}/api/2/group",
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
            "description": "Creates a group.\n\n**[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3b527608-e254-42fa-974e-8ecddb772953"
            }
          ]
        }
      ]
    },
    {
      "name": "Users",
      "item": [
        {
          "id": "0b7aadae-f6f6-49f8-8731-5e5577592db2",
          "name": "com.atlassian.jira.rest.v2.issue.GroupResource.getUsersFromGroup_get",
          "request": {
            "url": "{{default}}/api/2/group/member?groupname=%7B%7D&includeInactiveUsers=%7B%7D&maxResults=%7B%7D&startAt=%7B%7D",
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
            "description": "Returns all users in a group. Users are ordered by username.\n\n**[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c5ba4d07-e9d6-43b2-819e-40fc84b76405"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "96349019-1764-45b3-b55d-44929d4fde49",
          "name": "com.atlassian.jira.rest.v2.issue.GroupResource.addUserToGroup_post",
          "request": {
            "url": "{{default}}/api/2/group/user?groupname=%7B%7D",
            "method": "POST",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Adds a user to a group.\n\n**[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c956393-c6ce-4053-a36d-e7b65c8ecc19"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "2b9f32e5-ecd9-494c-9a93-be2cd2dc61d5",
          "name": "com.atlassian.jira.rest.v2.issue.GroupPickerResource.findGroups_get",
          "request": {
            "url": "{{default}}/api/2/groups/picker?accountId=%7B%7D&exclude=%7B%7D&maxResults=%7B%7D&query=%7B%7D&userName=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns groups with substrings matching a given query. This is mainly for use with the group picker, so the returned groups contain html to be used as picker suggestions. The groups are also wrapped in a single response object that also contains a header for use in the picker, specifically _Showing X of Y matching groups_.\n\nThe number of groups returned is limited by the system property \"jira.ajax.autocomplete.limit\"\n\nThe groups will be unique and sorted."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4bb9e7f-5f48-48a9-9298-f42a4789b623"
            }
          ]
        },
        {
          "id": "a4519b20-56d9-4af1-a441-99ac31211481",
          "name": "com.atlassian.jira.rest.v2.issue.GroupAndUserPickerResource.findUsersAndGroups_get",
          "request": {
            "url": "{{default}}/api/2/groupuserpicker?avatarSize=%7B%7D&caseInsensitive=%7B%7D&excludeConnectAddons=%7B%7D&fieldId=%7B%7D&issueTypeId=%7B%7D&maxResults=%7B%7D&projectId=%7B%7D&query=%7B%7D&showAvatar=%7B%7D",
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
            "description": "Returns a list of users and groups matching query with highlighting. This resource cannot be accessed anonymously."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "23465766-c2eb-4c55-b9f1-d64569ab8509"
            }
          ]
        }
      ]
    },
    {
      "name": "Issues",
      "item": [
        {
          "id": "a511453f-1d1e-45b1-b7d9-0419be7e4c0f",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.createIssues_post",
          "request": {
            "url": "{{default}}/api/2/issue/bulk",
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
            "description": "Creates multiple issues or sub-tasks from a JSON representation, in a single bulk operation.\n\nCreating a sub-task is similar to creating an issue - check Create issue section for details: {@link IssueResource#createIssue(boolean, IssueUpdateBean)}}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "662f2502-1c42-4b74-bf46-d65b6ce39926"
            }
          ]
        }
      ]
    },
    {
      "name": "Create",
      "item": [
        {
          "id": "9be446b3-5c3b-4140-9a94-79fd97d90763",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getCreateIssueMeta_get",
          "request": {
            "url": "{{default}}/api/2/issue/createmeta?issuetypeIds=%7B%7D&issuetypeNames=%7B%7D&projectIds=%7B%7D&projectKeys=%7B%7D",
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
            "description": "Returns the metadata for creating issues. This includes the available projects, issue types, fields (with information whether those fields are required) and field types. Projects, in which the user does not have permission to create issues, will not be returned.\n\nThe fields in the createmeta response correspond to the fields on the issue's Create screen for the specific project/issuetype. Fields hidden from the screen will not be returned in the createmeta response.\n\nFields will only be returned if `expand=projects.issuetypes.fields` is set.\n\nThe results can be filtered by project and/or issue type, controlled by the query parameters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8c75b914-c1cf-4df5-b25d-2c75b9b13fd2"
            }
          ]
        }
      ]
    },
    {
      "name": "Bulk",
      "item": [
        {
          "id": "1fcab5ec-edd5-40f9-ab24-127a1d823054",
          "name": "com.atlassian.jira.rest.v2.property.IssuePropertyBulkUpdateResource.bulkSetIssueProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "propertyKey",
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
            "description": "Allows to set a property for all issues identified by a given filter. Only entities the user has permissions to edit will be updated.\n\nCurrently the following filters are available:\n\n*   **entityIds** \\- A list of issues to update. Only issues with ids from this list will be considered for updating. This is an optional filter, if not provided, then any editable issue that matches all other filters will be updated.\n*   **currentValue** \\- If provided, then only issues with the property currently set to that value will be updated.\n*   **hasProperty** \\- If true, then only existing properties will be updated. If false, then only issues that do not have any value associated with this property will be updated. If omitted, the property will be set on all issues, regardless of whether it previously existed or not.\n\nIf more than one filter is given, then they are all joined with the logical \"and\", that is: only issues that satisfy all filters are updated. If no filters are provided at all, then the property will be updated on _all_ issues editable by the caller (i.e. issues in projects with the EDIT_ISSUES permission).\n\nIf an invalid combination of filters is provided, an error will be returned by the API. For example, specifying the current value and \"hasProperty\" to \"false\" would never match any issues (as it would mean: update this property if the current value is something, oh, but only if there is no value at all) and is therefore not allowed.\n\nThis method is [asynchronous](#async), meaning that it will not return the results immediately, instead creating a task to perform the requested update operation (unless preliminary validation, e.g. of the provided filter, fails).\n\nThe operation is transactional: either all eligible issues are updated, or none (if there are any errors)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec2be356-cce3-4624-a1f6-4b56d9425ef3"
            }
          ]
        },
        {
          "id": "553e195a-0f27-4f69-ba6e-e7f592d4c655",
          "name": "com.atlassian.jira.rest.v2.property.IssuePropertyBulkUpdateResource.bulkDeleteIssueProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "propertyKey",
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
            "description": "Allows to delete a property from all issues identified by a given filter. Only entities the user has permissions to edit will be updated. See the [issue property bulk set endpoint documentation](#api-api-2-issue-properties-propertyKey-put) for more details."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5873a217-7617-4119-a697-ef46980ab1ca"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "19003d49-2e34-4a19-84ce-60787cfc5de9",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.editIssue_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey"
              ],
              "query": [
                {
                  "key": "notifyUsers",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "overrideEditableFlag",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "overrideScreenSecurity",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Edits the issue from a JSON representation.\n\nThe fields available for update can be determined using the **/rest/api/2/issue/{issueIdOrKey}/editmeta** resource.  \nIf a field is hidden from the Edit screen then it will not be returned by the editmeta resource. A field validation error will occur if such field is submitted in an edit request. However connect add-on with admin scope may override a screen security configuration.\n\nIf an issue cannot be edited in Jira because of its workflow status (for example the issue is closed), then you will not be able to edit it with this resource.\n\nField to be updated should appear either in `fields` or `update` request's body parameter, but not in both.  \nTo update a single sub-field of a complex field (e.g. timetracking) please use the `update` parameter of the edit operation. Using a `\"field_id\": field_value` construction in the `fields` parameter is a shortcut of \"set\" operation in the `update` parameter."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "91822682-1eb0-4240-90a1-c3839b531815"
            }
          ]
        },
        {
          "id": "9406edfe-d0ce-459f-a037-af6fee1e6940",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getEditIssueMeta_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/editmeta"
              ],
              "query": [
                {
                  "key": "overrideEditableFlag",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "overrideScreenSecurity",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns the metadata for editing an issue.\n\nThe fields returned by editmeta resource are the ones shown on the issue's Edit screen. Fields hidden from the screen will not be returned unless `overrideScreenSecurity` parameter is set to true.\n\nIf an issue cannot be edited in Jira because of its workflow status (for example the issue is closed), then no fields will be returned, unless `overrideEditableFlag` is set to true."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ee0059a-7ac2-4c5a-8dc1-f2fc45864d19"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "8ec47573-da3f-4933-bf84-abe0e6573002",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.assignIssue_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/assignee"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Assigns the issue to the user. Use this resource to assign issues for the users having \"Assign Issue\" permission, and not having the \"Edit Issue\" permission. If `name` body parameter is set to \"-1\" then automatic issue assignee is used. A `name` set to `null` will remove the assignee."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e6dca751-5e79-4077-bc7b-dcd2a9d1648a"
            }
          ]
        },
        {
          "id": "fc73142b-2f43-4f59-a02d-c49e91f608bd",
          "name": "com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.assignPermissionScheme_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectKeyOrId/permissionscheme"
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
                  "id": "projectKeyOrId",
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
            "description": "Associates a permission scheme with a particular project. See [Managing project permissions](https://confluence.atlassian.com/x/yodKLg) for more information about permission schemes.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5d0f435-bcce-4078-bf0e-33caecdfa24c"
            }
          ]
        }
      ]
    },
    {
      "name": "Change",
      "item": [
        {
          "id": "e058f4b6-367a-4eaa-bfab-e3d9da96a22e",
          "name": "com.atlassian.jira.rest.v2.issue.IssueChangelogResource.getChangeLogs_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/changelog"
              ],
              "query": [
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns a [paginated](#pagination) list of all updates of an issue, sorted by date, starting from the oldest."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97630269-18ad-403b-ae95-274fc52f18e8"
            }
          ]
        }
      ]
    },
    {
      "name": "Notify",
      "item": [
        {
          "id": "c26a406e-2633-4752-9407-57bcf9cc72dc",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.notify_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/notify"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Sends an email notification to the list of users defined in the request body parameters."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "12477c67-136c-40ea-8db8-4b6c81e06589"
            }
          ]
        }
      ]
    },
    {
      "name": "Remote",
      "item": [
        {
          "id": "b43e7948-532f-4d5c-ba42-999f99a67519",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getRemoteIssueLinks_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/remotelink"
              ],
              "query": [
                {
                  "key": "globalId",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns the remote issue links for the issue. This may be links to other Jira instances, web applications or web pages."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be75de21-d3e5-474e-836f-58328fee4334"
            }
          ]
        },
        {
          "id": "bfcba428-f843-4705-a50b-8603185ae7bc",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.deleteRemoteIssueLinkByGlobalId_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/remotelink"
              ],
              "query": [
                {
                  "key": "globalId",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Deletes the issue's remote link with the given global ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fff4ca24-7a1a-4ba5-99b6-318ee6b3b6c8"
            }
          ]
        },
        {
          "id": "0a396f33-89e3-4a81-94c3-8c3a14b2e47c",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getRemoteIssueLinkById_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/remotelink/:linkId"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "linkId",
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
            "description": "Returns the remote issue link by the given ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6793143d-a67d-4524-b796-a32b4162e541"
            }
          ]
        },
        {
          "id": "a85269d2-0b74-4b25-b706-573cacff776a",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.updateRemoteIssueLink_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/remotelink/:linkId"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "linkId",
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
            "description": "Updates a remote issue link from a JSON representation. Sets all fields without values provided to null."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5627e764-7bf3-4d82-a7b9-1d491b51a2ff"
            }
          ]
        },
        {
          "id": "93b8e3e0-a974-43c8-9d68-84e5225c8762",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.deleteRemoteIssueLinkById_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/remotelink/:linkId"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "linkId",
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
            "description": "Deletes the issue's remote link with the given ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bfeba147-83dd-4ef4-a505-3b22179aeb9d"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "f481e465-7e75-4f3e-bbac-0c5f4bcd42a1",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.createOrUpdateRemoteIssueLink_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/remotelink"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Creates or updates a remote issue link from a JSON representation. If a `globalId` is provided and a remote issue link exists with that globalId, the remote issue link is updated. Otherwise, the remote issue link is created."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c693aa27-d694-40e3-94ff-6d981920c961"
            }
          ]
        }
      ]
    },
    {
      "name": "Transitions",
      "item": [
        {
          "id": "1e1eb467-bb1f-4112-b691-f9a1a43538b8",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getTransitions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/transitions"
              ],
              "query": [
                {
                  "key": "skipRemoteOnlyCondition",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "transitionId",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns a list of transitions available for this issue for the current user.\n\nSpecify `expand=transitions.fields` parameter to retrieve the fields required for a transition together with their types.\n\nFields metadata corresponds to the fields available in a transition screen for a particular transition. Fields hidden from the screen will not be returned in the metadata."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "164c6a33-af23-485e-8f50-bfd817bb1e35"
            }
          ]
        }
      ]
    },
    {
      "name": "Do",
      "item": [
        {
          "id": "11ae345d-b92f-4108-92b4-5981f6a3cf1f",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.doTransition_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/transitions"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Performs the issue transition. While performing the transition you can modify other issue fields.\n\nThe fields that can be set on transition, in either `fields` or `update` parameter can be determined using the **/rest/api/2/issue/{issueIdOrKey}/transitions?expand=transitions.fields** resource. If a field is not configured to appear on the transition screen, it will not be returned in the transition metadata. A field validation error will occur if such field is submitted in issue transition request."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "64d104ec-203b-461e-9aa2-68397e3af1ba"
            }
          ]
        }
      ]
    },
    {
      "name": "Votes",
      "item": [
        {
          "id": "3cd506aa-040b-4986-af36-8f72a07376d8",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.getVotes_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/votes"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Returns voting data for an issue - whether the issue was voted for, total number of votes and users who voted for the issue."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59f52a61-ef5d-497a-a35b-0261dbd7528f"
            }
          ]
        }
      ]
    },
    {
      "name": "Vote",
      "item": [
        {
          "id": "5e0f0c37-ba94-4965-a6b0-4e3a00967456",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.addVote_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/votes"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Adds a vote on the issue for a current user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b758694c-272d-45e1-b4fa-1dc31daf9ff8"
            }
          ]
        }
      ]
    },
    {
      "name": "Watcher",
      "item": [
        {
          "id": "9762dc01-956c-4283-8174-9a78231218d5",
          "name": "com.atlassian.jira.rest.v2.issue.IssueResource.addWatcher_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/watchers"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Adds the user to the issue's watcher list."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2743061f-bc30-4f4c-86fe-3747b67a9b8a"
            }
          ]
        }
      ]
    },
    {
      "name": "Worklog",
      "item": [
        {
          "id": "b20a34b9-34ab-486a-98f5-d3de0326f846",
          "name": "com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.addWorklog_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog"
              ],
              "query": [
                {
                  "key": "adjustEstimate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "newEstimate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "notifyUsers",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "overrideEditableFlag",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "reduceBy",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
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
            "description": "Adds a new worklog entry to an issue."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4623e333-2e85-49e5-94f5-4aa04b16703f"
            }
          ]
        },
        {
          "id": "dc4deccf-943b-40d6-8cef-8c897d2dce71",
          "name": "com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.getWorklog_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog/:id"
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
                  "id": "issueIdOrKey",
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
            "description": "Returns a specific worklog.  \n**Note:** The work log won't be returned if the Log work field is hidden for the project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cc7c7679-93f0-45c1-9d38-9b4d5b1ebbc8"
            }
          ]
        },
        {
          "id": "5ccc461f-5517-4c69-a8dc-f506b80453ac",
          "name": "com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.updateWorklog_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog/:id"
              ],
              "query": [
                {
                  "key": "adjustEstimate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "newEstimate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "notifyUsers",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "overrideEditableFlag",
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
                  "id": "issueIdOrKey",
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
            "description": "Updates an existing worklog entry.\n\nNote that:\n\n*   Fields possible for editing are: comment, visibility, started, timeSpent and timeSpentSeconds.\n*   Either timeSpent or timeSpentSeconds can be set.\n*   Fields which are not set will not be updated.\n*   For a request to be valid, it has to have at least one field change."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "57e3d6a9-194a-4f53-a5db-fdcca5511699"
            }
          ]
        },
        {
          "id": "4aeb941f-74c9-4abd-8481-64cb64f86835",
          "name": "com.atlassian.jira.rest.v2.issue.IssueWorklogsResource.deleteWorklog_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog/:id"
              ],
              "query": [
                {
                  "key": "adjustEstimate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "increaseBy",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "newEstimate",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "notifyUsers",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "overrideEditableFlag",
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
                  "id": "issueIdOrKey",
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
            "description": "Deletes an existing worklog entry."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fd1d87be-9788-4dcb-956e-5e108cb3e3ba"
            }
          ]
        },
        {
          "id": "03547cb6-14c7-47cf-b40f-de1f17cbf8bf",
          "name": "com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.getWorklogPropertyKeys_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog/:worklogId/properties"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "worklogId",
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
            "description": "Returns the keys of all properties for the worklog identified by the key or by the id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d3c9f02e-4eb9-4461-b1b8-f56f254877b7"
            }
          ]
        },
        {
          "id": "95d455e1-652e-4c20-9005-57d45e42c912",
          "name": "com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.getWorklogProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog/:worklogId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "worklogId",
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
            "description": "Returns the value of the property with a given key from the worklog identified by the key or by the id. The user who retrieves the property is required to have permissions to read the worklog."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2a73190f-9a7d-4d5f-b9b0-7867cbf8e361"
            }
          ]
        },
        {
          "id": "2dcc9bae-737e-446e-b5f3-a47dad89d5e1",
          "name": "com.atlassian.jira.rest.v2.issue.WorklogPropertyResource.deleteWorklogProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issue/:issueIdOrKey/worklog/:worklogId/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "issueIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "worklogId",
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
            "description": "Removes the property from the worklog identified by the key or by the id. Ths user removing the property is required to have permissions to administer the worklog."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e9ee960e-005e-46e2-b147-9c618192907f"
            }
          ]
        }
      ]
    },
    {
      "name": "Link",
      "item": [
        {
          "id": "bc492e78-a35a-40b5-ae29-c6a3002da7cc",
          "name": "com.atlassian.jira.rest.v2.issue.LinkIssueResource.linkIssues_post",
          "request": {
            "url": "{{default}}/api/2/issueLink",
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
            "description": "Creates an issue link between two issues. The user requires the link issue permission for the issue which will be linked to another issue. The specified link type in the request is used to create the link and will create a link from the first issue to the second issue using the outward description. It also create a link from the second issue to the first issue using the inward description of the issue link type. It will add the supplied comment to the first issue. The comment can have a restriction who can view it. If group is specified, only users of this group can view this comment, if roleLevel is specified only users who have the specified role can view this comment. The user who creates the issue link needs to belong to the specified group or have the specified role."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "34ef18d7-1aa4-40fe-85b5-eb7cb1947e81"
            }
          ]
        }
      ]
    },
    {
      "name": "Alternative",
      "item": [
        {
          "id": "790df0a8-3a11-4f89-9568-58a4db061350",
          "name": "com.atlassian.jira.rest.v2.issue.IssueTypeResource.getAlternativeIssueTypes_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/issuetype/:id/alternatives"
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
            "description": "Returns a list of issue types that can be used to replace the issue type. The alternative issue types are those assigned to the same workflow scheme, field configuration scheme, and screen scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "097900b8-ed99-4399-8f5d-e56c6cab19c9"
            }
          ]
        }
      ]
    },
    {
      "name": "Auto",
      "item": [
        {
          "id": "1bcb633e-bfbe-4546-b603-ecc0a8235e96",
          "name": "com.atlassian.jira.rest.v2.search.SearchAutoCompleteResource.getAutoComplete_get",
          "request": {
            "url": "{{default}}/api/2/jql/autocompletedata",
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
            "description": "Returns the auto complete data required for JQL searches."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8eb36e6e-4568-4ade-b635-19710842277b"
            }
          ]
        }
      ]
    },
    {
      "name": "Field",
      "item": [
        {
          "id": "7c757e99-f2a5-40bf-8644-d996ee6ebe47",
          "name": "com.atlassian.jira.rest.v2.search.SearchAutoCompleteResource.getFieldAutoCompleteForQueryString_get",
          "request": {
            "url": "{{default}}/api/2/jql/autocompletedata/suggestions?fieldName=%7B%7D&fieldValue=%7B%7D&predicateName=%7B%7D&predicateValue=%7B%7D",
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
            "description": "Returns auto complete suggestions for JQL search."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7c2ab74e-ec8e-4743-80fd-8b5ae647dbe9"
            }
          ]
        }
      ]
    },
    {
      "name": "Validate",
      "item": [
        {
          "id": "ffe6d015-9160-4855-96cb-12a5cf11af51",
          "name": "com.atlassian.jira.rest.v2.license.LicenceValidator.validateLicense_post",
          "request": {
            "url": "{{default}}/api/2/licenseValidator",
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
            "description": "Validates a Jira license.\n\nTypically used by the setup phase of the Jira application. Returns an object with a list of errors as key, value pairs if the license is not valid."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2c703fd4-ae25-4ddb-8a45-42d4ac106005"
            }
          ]
        }
      ]
    },
    {
      "name": "Preference",
      "item": [
        {
          "id": "0473e6fa-0c73-4c93-93ac-edfb634a41e4",
          "name": "com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.getPreference_get",
          "request": {
            "url": "{{default}}/api/2/mypreferences?key=%7B%7D",
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
            "description": "Returns preference of the currently logged in user. Preference key must be provided as input parameter (key). The value is returned exactly as it is."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70362a1d-426a-49f7-8a9a-79eb2d9bc7fd"
            }
          ]
        }
      ]
    },
    {
      "name": "Locale",
      "item": [
        {
          "id": "0b28bfae-c58b-434b-a074-76bbb29279db",
          "name": "com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.getLocale_get",
          "request": {
            "url": "{{default}}/api/2/mypreferences/locale",
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
            "description": "Returns the locale of the currently logged in user. If the user has no language preference explicitly set (the default setting), or is anonymous, this will be the browser locale detected by Jira. If browser detection is in effect, the \"Accept-Language\" browser header is used and falls back to the Jira site default locale if no match is found."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a9f6ffb-bf20-4add-9903-cf45a0bb0324"
            }
          ]
        },
        {
          "id": "5995e90d-79fe-4f9a-9ac9-0bdf79e40ce8",
          "name": "com.atlassian.jira.rest.v2.preference.CurrentUserPreferencesResource.deleteLocale_delete",
          "request": {
            "url": "{{default}}/api/2/mypreferences/locale",
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
            "description": "Deletes the set locale of the currently logged in user, resetting it to default."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a5670f24-31fd-481b-b0d0-27df34b5135f"
            }
          ]
        }
      ]
    },
    {
      "name": "Current",
      "item": [
        {
          "id": "2479e34f-a99f-4095-99bc-e48ea688bd2b",
          "name": "com.atlassian.jira.rest.v2.issue.CurrentUserResource.getCurrentUser_get",
          "request": {
            "url": "{{default}}/api/2/myself",
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
            "description": "Returns currently logged user. This resource cannot be accessed anonymously.\n\nThe resource accepts the `expand` param that is used to include, hidden by default, parts of response. This can be used to include:\n\n*   `groups` \\- all groups, including nested groups, to which user belongs\n*   `applicationRoles` \\- application roles defines to which application user has access"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d1a6ced-43f8-4ac4-9924-7e6914533a76"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "c76323be-48a0-4cdf-931c-d8ecb1374707",
          "name": "com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationSchemes_get",
          "request": {
            "url": "{{default}}/api/2/notificationscheme?expand=%7B%7D&maxResults=%7B%7D&startAt=%7B%7D",
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
            "description": "Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) list of [notification schemes](https://confluence.atlassian.com/x/8YdKLg) in order by display name.\n\n### About notification schemes\n\nA notification scheme is a list of events and recipients who will receive notifications for those events. The list is contained within the `notificationSchemeEvents` object and contains pairs of `events` and `notifications`:\n\n*   `event` Identifies the type of event. The events can be [Jira system events](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-eventsEvents) or [custom events](https://confluence.atlassian.com/x/AIlKLg).\n*   `notifications` Identifies the [recipients](https://confluence.atlassian.com/x/8YdKLg#Creatinganotificationscheme-recipientsRecipients) of notifications for each event. Recipients can be any of the following types:\n\n*   `CurrentAssignee`\n*   `Reporter`\n*   `CurrentUser`\n*   `ProjectLead`\n*   `ComponentLead`\n*   `User` (the `parameter` is the user key)\n*   `Group` (the `parameter` is the group name)\n*   `ProjectRole` (the `parameter` is the project role ID)\n*   `EmailAddress`\n*   `AllWatchers`\n*   `UserCustomField` (the `parameter` is the ID of the custom field)\n*   `GroupCustomField`(the `parameter` is the ID of the custom field)\n\n_Note that you should allow for events without recipients to appear in responses._\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with a notification scheme for it to be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5cb2426e-3ec1-41fa-8d88-0738a2bf9f91"
            }
          ]
        },
        {
          "id": "c9bae65d-6342-4d3e-9877-8335fe47304c",
          "name": "com.atlassian.jira.rest.v2.notification.NotificationSchemeResource.getNotificationScheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/notificationscheme/:id"
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
            "description": "Returns a [notification scheme](https://confluence.atlassian.com/x/8YdKLg), including the list of events and the recipients who will receive notifications for those events.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None, however the requesting user must have permission to administer at least one project associated with the requested notification scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fa859a0e-1da6-4a29-8de8-5a3ce2d15b0b"
            }
          ]
        }
      ]
    },
    {
      "name": "Permissions",
      "item": [
        {
          "id": "895bff2a-b7b1-4e2f-ae60-b2887632b9ef",
          "name": "com.atlassian.jira.rest.v2.permission.PermissionsResource.getAllPermissions_get",
          "request": {
            "url": "{{default}}/api/2/permissions",
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
            "description": "Returns all permissions that are present in the Jira instance - Global, Project and the global ones added by plugins"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "db3dd752-dac3-4ee9-a237-81593cd83769"
            }
          ]
        }
      ]
    },
    {
      "name": "Permitted",
      "item": [
        {
          "id": "14a7681b-9260-4a00-9e2e-519282fe99d9",
          "name": "com.atlassian.jira.rest.v2.permission.PermissionsResource.getPermittedProjects_post",
          "request": {
            "url": "{{default}}/api/2/permissions/project",
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
            "description": "Returns all projects where currently logged in user was granted ALL requested project permissions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "78ec5951-447a-4643-8b54-19a40275bf7b"
            }
          ]
        }
      ]
    },
    {
      "name": "Permission",
      "item": [
        {
          "id": "6e2db1eb-e735-4a7f-985a-17bb9235f80e",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getAllPermissionSchemes_g",
          "request": {
            "url": "{{default}}/api/2/permissionscheme?expand=%7B%7D",
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
            "description": "Returns all permission schemes.\n\n### About permission schemes and grants\n\nA permission scheme is a collection of permission grants. A permission grant consists of a `holder` and a `permission`.\n\n#### Holder\n\nThe `holder` object contains information about the user or group being granted the permission. For example, the _Administer projects_ permission is granted to a group named _Teams in space administrators_. In this case, the type is `\"type\": \"group\"`, and the parameter is the group name, `\"parameter\": \"Teams in space administrators\"`. The `holder` object is defined by the following properties:\n\n*   `type` Identifies the user or group (see the list of types below).\n*   `parameter` The value of this property depends on the `type`. For example, if the `type` is a group, then you need to specify the group name.\n\nThe following `types` are available. The expected values for the `parameter` are given in parenthesis (some `types` may not have a `parameter`):\n\n*   `anyone` Grant for anonymous users.\n*   `applicationRole` Grant for users with access to the specified application (application name). See [Manage application access](https://confluence.atlassian.com/cloud/manage-application-access-744721629.html) for more information.\n*   `assignee` Grant for the user currently assigned to an issue.\n*   `group` Grant for the specified group (group name).\n*   `groupCustomField` Grant for a user in the group selected in the specified custom field (custom field ID).\n*   `projectLead` Grant for a project lead.\n*   `projectRole` Grant for the specified project role (project role ID).\n*   `reporter` Grant for the user who reported the issue.\n*   `sd.customer.portal.only` Jira Service Desk only. Grants customers permission to access the customer portal but not Jira. See [Customizing Jira Service Desk permissions](https://confluence.atlassian.com/x/24dKLg) for more information.\n*   `user` Grant for the specified user (user ID).\n*   `userCustomField` Grant for a user selected in the specified custom field (custom field ID).\n\n#### Permissions\n\nThe [built-in Jira permissions](https://confluence.atlassian.com/x/yodKLg) are listed below. Apps can also define custom permissions. See the [project permission](https://developer.atlassian.com/cloud/jira/platform/modules/project-permission/) and [global permission](https://developer.atlassian.com/cloud/jira/platform/modules/global-permission/) module documentation for more information.\n\n**Project permissions**\n\n*   `ADMINISTER_PROJECTS`\n*   `BROWSE_PROJECTS`\n*   `MANAGE_SPRINTS_PERMISSION` (Jira Software only)\n*   `SERVICEDESK_AGENT` (Jira Service Desk only)\n*   `VIEW_DEV_TOOLS` (Jira Software only)\n*   `VIEW_READONLY_WORKFLOW`\n\n**Issue permissions**\n\n*   `ASSIGNABLE_USER`\n*   `ASSIGN_ISSUES`\n*   `CLOSE_ISSUES`\n*   `CREATE_ISSUES`\n*   `DELETE_ISSUES`\n*   `EDIT_ISSUES`\n*   `LINK_ISSUES`\n*   `MODIFY_REPORTER`\n*   `MOVE_ISSUES`\n*   `RESOLVE_ISSUES`\n*   `SCHEDULE_ISSUES`\n*   `SET_ISSUE_SECURITY`\n*   `TRANSITION_ISSUES`\n\n**Voters and watchers permissions**\n\n*   `MANAGE_WATCHERS`\n*   `VIEW_VOTERS_AND_WATCHERS`\n\n**Comments permissions**\n\n*   `ADD_COMMENTS`\n*   `DELETE_ALL_COMMENTS`\n*   `DELETE_OWN_COMMENTS`\n*   `EDIT_ALL_COMMENTS`\n*   `EDIT_OWN_COMMENTS`\n\n**Attachments permissions**\n\n*   `CREATE_ATTACHMENTS`\n*   `DELETE_ALL_ATTACHMENTS`\n*   `DELETE_OWN_ATTACHMENTS`\n\n**Time tracking permissions**\n\n*   `DELETE_ALL_WORKLOGS`\n*   `DELETE_OWN_WORKLOGS`\n*   `EDIT_ALL_WORKLOGS`\n*   `EDIT_OWN_WORKLOGS`\n*   `WORK_ON_ISSUES`\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b2e2239-5d18-4e2b-9ee5-c0f83a66dc61"
            }
          ]
        },
        {
          "id": "e3daa492-b761-4726-b7bd-edc4408d4195",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.createPermissionScheme_po",
          "request": {
            "url": "{{default}}/api/2/permissionscheme?expand=%7B%7D",
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
            "description": "Creates a new permission scheme. You can create a permission scheme with or without defining a set of permission grants. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fccfcf38-ca1f-4ef2-b63e-7a68cd33d944"
            }
          ]
        },
        {
          "id": "30322438-f855-484d-84e1-db6eeeff0324",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionScheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/permissionscheme/:schemeId"
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
                  "id": "schemeId",
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
            "description": "Returns a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f85a0cfb-a4df-43db-8ee4-69abb5ad8238"
            }
          ]
        },
        {
          "id": "bd050571-559b-4a8e-9447-f1c9e3844884",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.updatePermissionScheme_pu",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/permissionscheme/:schemeId"
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
                  "id": "schemeId",
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
            "description": "Updates a permission scheme. Below are some important things to note when using this resource:\n\n*   If a permissions list is present in the request, then it will be set in the permission scheme, overwriting _all existing_ grants.\n*   If you want to update only the name and description, then do not send a permissions list in the request.\n*   Sending an empty list will remove all permission grants from the permission scheme.\n\nIf you want to add or delete a single permission grant instead of updating the whole list, see [Create permission grant](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-post) or [Delete permission scheme entity](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-schemeId-permission-permissionId-delete). See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de0ea00e-dbca-4382-9364-14d0c2222d3e"
            }
          ]
        },
        {
          "id": "8fc878e1-28b9-4539-8493-da4017b4ab1c",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionScheme_de",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/permissionscheme/:schemeId"
              ],
              "variable": [
                {
                  "id": "schemeId",
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
            "description": "Deletes a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5d0c724c-688f-4019-8575-4c3616fe0222"
            }
          ]
        },
        {
          "id": "afbf71a3-f88a-40cd-813a-6a8fc1d1d612",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrants",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/permissionscheme/:schemeId/permission"
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
                  "id": "schemeId",
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
            "description": "Returns all permission grants for a permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "92f2cd7a-d0c3-4766-b921-3d4d03e6357b"
            }
          ]
        },
        {
          "id": "0dbef08a-14a6-4fc8-918d-a985601a13ee",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.createPermissionGrant_pos",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/permissionscheme/:schemeId/permission"
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
                  "id": "schemeId",
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
            "description": "Creates a new permission grant in the given permission scheme. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "797adc01-03d4-4da7-85f4-0e360a65b387"
            }
          ]
        },
        {
          "id": "206649d3-a6e1-4550-af54-d07da656ecf6",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.getPermissionSchemeGrant_",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/permissionscheme/:schemeId/permission/:permissionId"
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
                  "id": "permissionId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "schemeId",
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
            "description": "Returns a permission grant. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d0e18d83-3910-4a3f-a12f-7472fefbbc17"
            }
          ]
        },
        {
          "id": "345509c1-f7a0-4185-b62a-25f7c9a38317",
          "name": "com.atlassian.jira.rest.v2.admin.permissionscheme.PermissionSchemeResource.deletePermissionSchemeEnt",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/permissionscheme/:schemeId/permission/:permissionId"
              ],
              "variable": [
                {
                  "id": "permissionId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "schemeId",
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
            "description": "Deletes a permission grant from a permission scheme. See [About permission schemes and grants](https://developer.atlassian.com/cloud/jira/platform/rest/#about-permission-schemes) for more details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bbff634a-4e86-44cc-85f0-563245e4f6dc"
            }
          ]
        }
      ]
    },
    {
      "name": "Priorities",
      "item": [
        {
          "id": "ecdae2d9-f49a-4a0c-b796-f403cd2037f5",
          "name": "com.atlassian.jira.rest.v2.issue.PriorityResource.getPriorities_get",
          "request": {
            "url": "{{default}}/api/2/priority",
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
            "description": "Returns a list of all issue priorities."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "85068a74-5bb3-4d09-b897-19382494d352"
            }
          ]
        }
      ]
    },
    {
      "name": "Priority",
      "item": [
        {
          "id": "282290a1-2e92-4516-8cd8-84dde4bde577",
          "name": "com.atlassian.jira.rest.v2.issue.PriorityResource.getPriority_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/priority/:id"
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
            "description": "Returns an issue priority."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "48c59219-d475-42b5-b42e-f105d0f699d6"
            }
          ]
        }
      ]
    },
    {
      "name": "Projects",
      "item": [
        {
          "id": "9e368081-ed34-4ebd-8ccd-a6fd51610353",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getAllProjects_get",
          "request": {
            "url": "{{default}}/api/2/project?expand=%7B%7D&recent=%7B%7D",
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
            "description": "Returns all projects visible to the currently logged in user. For projects to be visible, the authenticated user must be granted either _Browse projects_ or _Administer projects_ permissions. If no user is logged in, it returns all projects that are visible for anonymous users.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e10561b3-21e7-46fe-a41a-d65cc1f0db93"
            }
          ]
        }
      ]
    },
    {
      "name": "Project",
      "item": [
        {
          "id": "451c503f-26dd-40ea-8494-2235856ba587",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.createProject_post",
          "request": {
            "url": "{{default}}/api/2/project",
            "method": "POST",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8dc27c7f-3f6c-47df-8755-dde34e0711fb"
            }
          ]
        },
        {
          "id": "0a2df518-77a2-4483-8e72-98167c3207e7",
          "name": "com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getAllProjectTypes_get",
          "request": {
            "url": "{{default}}/api/2/project/type",
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
            "description": "Returns all [project types](https://confluence.atlassian.com/x/Var1Nw), whether or not the instance has a valid license for each type.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fb384a58-2d4a-491b-abf7-130cca2a71c9"
            }
          ]
        },
        {
          "id": "965d1cbc-e371-4459-a9a3-23c39c295c24",
          "name": "com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getProjectTypeByKey_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/type/:projectTypeKey"
              ],
              "variable": [
                {
                  "id": "projectTypeKey",
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
            "description": "Returns a [project type](https://confluence.atlassian.com/x/Var1Nw).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7e27ef73-3e6b-448e-bb6f-5601adf1c3c4"
            }
          ]
        },
        {
          "id": "19aa1e89-ff3d-4109-9bcf-94b6805ba4e9",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getProject_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey"
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
                  "id": "projectIdOrKey",
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
            "description": "Returns the [project details](https://confluence.atlassian.com/x/ahLpNw) for the specified project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ecc197b9-4131-4be5-8c73-2f19c85df5ea"
            }
          ]
        },
        {
          "id": "8ddc58d4-13ac-44e5-8fff-02a832154bd3",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.updateProject_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey"
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
                  "id": "projectIdOrKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Updates the [project details](https://confluence.atlassian.com/x/ahLpNw) of an existing project.\n\nAll parameters are optional in the body of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e2289271-a834-4e28-9813-94d6d71cf29d"
            }
          ]
        },
        {
          "id": "697e84f5-8072-4b62-8ea3-e754c1d1f208",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.deleteProject_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Deletes an existing project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d3f78ae8-5dbc-456e-9f9b-4d2487371d2e"
            }
          ]
        },
        {
          "id": "488832cc-be3e-4738-92f3-da631069a4ff",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.updateProjectAvatar_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/avatar"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Update project avatar"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ab55d945-383c-48fe-8468-b5dbfefde0c3"
            }
          ]
        },
        {
          "id": "9e9c2f45-5d2c-4039-a4be-9571c2cee13c",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.deleteProjectAvatar_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/avatar/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "projectIdOrKey",
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
            "description": "Deletes an avatar of a single project. It is only possible to delete custom avatars."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e16b474d-b675-40d4-9e43-2c4099342d7c"
            }
          ]
        },
        {
          "id": "5747f0b0-fee2-42e8-9143-6b8a32915763",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.createProjectAvatar_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/avatar2"
              ],
              "query": [
                {
                  "key": "size",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "x",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "y",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Creates an avatar for a single project. Use it to upload an image to be be set as a project's avatar. The uploaded image will be cropped according to the crop parameters defined in the request. If no crop parameters are specified, the image will be cropped to a square. The square will originate at the top left of the image and the length of each side will be set to the smaller of the height or width of the image."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0549736-fa26-4b28-a527-720c22598f44"
            }
          ]
        },
        {
          "id": "9ab70c64-1227-444c-8edb-3fe798d63a3d",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getAllProjectAvatars_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/avatars"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns all project avatars visible for the currently logged in user. The avatars are grouped into system avatars and custom avatars."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "190be408-2708-41ae-9a44-eb8a1f87ad79"
            }
          ]
        },
        {
          "id": "f183798d-807c-4676-9438-a94cf0efcfec",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectComponentsPaginated_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/component"
              ],
              "query": [
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "orderBy",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "query",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all components existing in a single project. See the [Get project components](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-components-get) resource if you want to get a full list of versions without pagination.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c8fa1302-8986-4c0f-867d-9e7638a2b0c0"
            }
          ]
        },
        {
          "id": "11f5aa73-91d7-40db-8ffc-6d58ce6638d4",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectComponents_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/components"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns all components existing in a single project. See the [Get project components paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-component-get) resource if you want to get a full list of components with pagination.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4a08c252-79ac-4fa8-bcbc-9a0b763ce5bb"
            }
          ]
        },
        {
          "id": "1e7d51f3-9d54-4a88-8f3f-4b2d0f52fad4",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.getProjectPropertyKeys_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/properties"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns all [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) keys for the project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e2f253ad-86b3-4ed0-8c47-996cb6cb98fc"
            }
          ]
        },
        {
          "id": "3ee80ea6-2311-4097-be94-f0edf386cb59",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.getProjectProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Returns the value of the [project property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e17b2836-c86f-46ff-ba1d-f5263ed65c48"
            }
          ]
        },
        {
          "id": "199e3784-a9f9-4804-822a-56b5bd7ba5b1",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectPropertyResource.deleteProjectProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/properties/:propertyKey"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "propertyKey",
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
            "description": "Removes the [property](https://developer.atlassian.com/cloud/jira/platform/storing-data-without-a-database/#a-id-jira-entity-properties-a-jira-entity-properties) from the project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8b40b10-abb1-48c5-b824-56df16672810"
            }
          ]
        },
        {
          "id": "5ce658f2-3327-47d6-9382-7061c5e10229",
          "name": "com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.getProjectRoles_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/role"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns a list of [project roles](https://confluence.atlassian.com/x/3odKLg) for the project.\n\nNote that all project roles are shared with all projects in Jira Cloud. See the [Get all project roles](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-get) resource for more information.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f892c4d8-6c3b-45a3-bd78-db1ab66e436d"
            }
          ]
        },
        {
          "id": "91aa136a-e776-41f9-9a2f-ac37b91ac5cd",
          "name": "com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.getProjectRole_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/role/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns the project role's details and actors associated with the project. The list of actors is sorted by display name.\n\nIf you would like to check to see whether a user belongs to a role based on their group memberships, use the [Get user](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-get) resource with the `groups` expand parameter selected. Then check whether the user keys and groups match with the actors returned for the project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7d746604-e223-4842-84bc-e4c0a453e5f7"
            }
          ]
        },
        {
          "id": "2ef1c091-e641-476e-8269-a8548a8b840d",
          "name": "com.atlassian.jira.rest.v2.issue.project.ProjectRoleDetailsResource.getProjectRoleDetails_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/roledetails"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns all [project roles](https://confluence.atlassian.com/x/3odKLg) and the details for each role. Note that the list of project roles is common to all projects."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "df7aa852-fa64-41be-9a6c-19134abad118"
            }
          ]
        },
        {
          "id": "db10d8ad-2b37-45d6-9894-599c8177d7f8",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.updateProjectType_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/type/:newProjectTypeKey"
              ],
              "variable": [
                {
                  "id": "newProjectTypeKey",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "projectIdOrKey",
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
            "description": "Updates the [project type](https://confluence.atlassian.com/x/GwiiLQ).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a08a1f8c-2897-4265-9ac5-daf9f9234d0c"
            }
          ]
        },
        {
          "id": "db5a8b00-7bb1-40dc-97c7-2e35f52d0dac",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectVersionsPaginated_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/version"
              ],
              "query": [
                {
                  "key": "expand",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "maxResults",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "orderBy",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "query",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "startAt",
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
                  "id": "projectIdOrKey",
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
            "description": "Returns a [paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#pagination) representation of all versions existing in a single project. See the [Get project versions](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-versions-get) resource if you want to get a full list of versions without pagination.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "631215d1-a7a8-4b50-99ae-1cfa0477648f"
            }
          ]
        },
        {
          "id": "29216c3c-ef8d-47a5-ac2c-476909440230",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getProjectVersions_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/versions"
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
                  "id": "projectIdOrKey",
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
            "description": "Returns all versions existing in a single project. The response is not paginated. Use [Get project versions paginated](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-version-get) if you want to get the versions in a project with pagination.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1c450e8b-d614-40d3-8086-5dc8f0080a98"
            }
          ]
        },
        {
          "id": "f98d24e8-f705-43a6-ac48-35d7a62c2560",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectIssueSecurityLevelSchemeResource.getIssueSecurityScheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectKeyOrId/issuesecuritylevelscheme"
              ],
              "variable": [
                {
                  "id": "projectKeyOrId",
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
            "description": "Returns the [issue security scheme](https://confluence.atlassian.com/x/J4lKLg) associated with the project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or the _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0b77a87d-d2e8-49a9-bc23-7738e2beab2c"
            }
          ]
        },
        {
          "id": "b07d90e2-4724-419b-8e1b-01a768d5ea27",
          "name": "com.atlassian.jira.rest.v2.notification.ProjectNotificationSchemeResource.getNotificationScheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectKeyOrId/notificationscheme"
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
                  "id": "projectKeyOrId",
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
            "description": "Gets a [notification scheme](https://confluence.atlassian.com/x/8YdKLg) associated with the project. See the [Get notification scheme](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-id-get) resource for more information about notification schemes.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3124afa7-b598-41fe-b74c-21f91c902097"
            }
          ]
        },
        {
          "id": "1c81ff1d-e3cd-4b2b-98b8-56b14d5800b1",
          "name": "com.atlassian.jira.rest.v2.securitylevel.ProjectSecurityLevelResource.getSecurityLevelsForProject_ge",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectKeyOrId/securitylevel"
              ],
              "variable": [
                {
                  "id": "projectKeyOrId",
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
            "description": "Returns all [issue security](https://confluence.atlassian.com/x/J4lKLg) levels for the project that the currently authenticated user has access to. If the user does not have permission to see an issue security level, then that level is not returned. If the user lacks the _Set Issue Security_ permission, then an empty list is returned.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Set Issue Security_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "79e800ef-6826-41dc-a588-8443d55b4a4b"
            }
          ]
        },
        {
          "id": "f3632606-b45a-4486-8b06-2fc8834f7574",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.getAllProjectCategories_get",
          "request": {
            "url": "{{default}}/api/2/projectCategory",
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
            "description": "Returns all project categories"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5614aa62-6ebe-4587-89da-b08cc105a309"
            }
          ]
        },
        {
          "id": "999f16bc-399a-4a62-b5eb-0560fe5106cb",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.createProjectCategory_post",
          "request": {
            "url": "{{default}}/api/2/projectCategory",
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
            "description": "Create a project category via POST."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43001e14-92b0-40cf-9591-446aba4e4c8d"
            }
          ]
        },
        {
          "id": "0f2ae5f9-829c-4de5-8ac8-10dae7dd4ecc",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.getProjectCategoryById_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/projectCategory/:id"
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
            "description": "Contains a representation of a project category in JSON format."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3f1661e5-9439-4795-a8f3-fc5b33589e80"
            }
          ]
        },
        {
          "id": "90f8be3a-1e53-4845-a8c4-7ad0df0dbd09",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectCategoryResource.updateProjectCategory_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/projectCategory/:id"
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
            "description": "Modify a project category via PUT. Any fields present in the PUT will override existing values. As a convenience, if a field is not present, it is silently ignored."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0624540b-604f-43fd-a644-7a6d7325c2b6"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "5b47f204-a052-4461-9fa6-ec5482d004df",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.searchProjects_get",
          "request": {
            "url": "{{default}}/api/2/project/search?action=%7B%7D&categoryId=%7B%7D&expand=%7B%7D&maxResults=%7B%7D&orderBy=%7B%7D&query=%7B%7D&startAt=%7B%7D&typeKey=%7B%7D",
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
            "description": "Returns all projects visible to the currently logged in user, i.e. all projects the user has permission defined by the {@code action} parameter. If no user is logged in, all projects visible to anonymous users are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "88bf0e6e-60ff-46c4-adfd-ddf3cfa6a6a2"
            }
          ]
        }
      ]
    },
    {
      "name": "Accessible",
      "item": [
        {
          "id": "7094d4ab-6fd7-4ffa-87f8-db6279d54379",
          "name": "com.atlassian.jira.rest.v2.project.type.ProjectTypeResource.getAccessibleProjectTypeByKey_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/type/:projectTypeKey/accessible"
              ],
              "variable": [
                {
                  "id": "projectTypeKey",
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
            "description": "Returns a [project type](https://confluence.atlassian.com/x/Var1Nw) if it is accessible to the logged in user.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to log in to Jira (that is, member of the _users_ [group](https://confluence.atlassian.com/x/24xjL))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "115b7e4e-e9b9-4c95-a994-844562e46c18"
            }
          ]
        }
      ]
    },
    {
      "name": "Actors",
      "item": [
        {
          "id": "f286b42e-fe64-41a8-8189-3b6addfddc87",
          "name": "com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.addActorUsers_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/role/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "projectIdOrKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Adds additional actors to a project role for the project.\n\nIf you want to replace all actors for the project, then use [Set actors for project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-project-projectIdOrKey-role-id-put).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "427a91e9-0489-40dd-8c2a-7cbd7225b48e"
            }
          ]
        },
        {
          "id": "e94fac91-afe0-4df8-bd1f-5af61c112b4a",
          "name": "com.atlassian.jira.rest.v2.issue.project.ProjectRoleResource.deleteActor_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/role/:id"
              ],
              "query": [
                {
                  "key": "group",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "user",
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
                  "id": "projectIdOrKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "force-account-id",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Deletes actors from a project role for the project.\n\nIf you want to remove default actors from the project role, see the [Delete default actors from project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-delete) resource.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f214c982-3f05-4beb-ab42-e4e7ed8dba05"
            }
          ]
        }
      ]
    },
    {
      "name": "Statuses",
      "item": [
        {
          "id": "b6133844-0550-4809-ad85-4e0c10e81162",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectResource.getAllStatuses_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectIdOrKey/statuses"
              ],
              "variable": [
                {
                  "id": "projectIdOrKey",
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
            "description": "Returns the valid statuses for a project. The statuses are grouped by issue type, as each project has a set of valid issue types and each issue type has a set of valid statuses.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse Projects_ project permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b67e959d-314b-4148-870e-ab5b412a48a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "fecd4171-213f-4002-bf6d-b27a1cd58ad8",
          "name": "com.atlassian.jira.rest.v2.permission.ProjectPermissionSchemeResource.getAssignedPermissionScheme_ge",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/project/:projectKeyOrId/permissionscheme"
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
                  "id": "projectKeyOrId",
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
            "description": "Gets the [permission scheme](https://confluence.atlassian.com/x/yodKLg) associated with the project.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d314f01b-7967-4d4f-bf3c-bd878b8a64c8"
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