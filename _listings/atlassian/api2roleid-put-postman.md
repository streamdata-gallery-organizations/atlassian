{
  "info": {
    "name": "Jira Cloud API Fully update project role",
    "_postman_id": "4fe10cc0-828c-4d47-9939-52b01025385c",
    "description": "Update the project role's name and description. You must include both a name and a description in the request.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "898856a4-b957-4a04-bc4c-0a112f64a701",
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
              "id": "91d836f0-7cd4-4216-966f-2ebbce31d349"
            }
          ]
        },
        {
          "id": "6c0020f6-227c-4bef-bc5c-27826572ecc8",
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
              "id": "3e48c58c-0323-4bb6-8ac9-5f6c8223100b"
            }
          ]
        },
        {
          "id": "53cab660-b617-4fb1-a60b-a83c6301e289",
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
              "id": "8dfeeb50-493b-4ef2-ad80-dfa6d465b623"
            }
          ]
        }
      ]
    },
    {
      "name": "Advanced",
      "item": [
        {
          "id": "3a71cd08-ebdb-4dc2-a494-bbc81e44a9eb",
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
              "id": "5e7c6a9d-6156-48d4-857f-4f397c4d4c49"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "b192d2ec-3b13-4e07-95a5-1a6b30911839",
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
              "id": "ecda6a8d-9dcb-41e9-b2e0-561cb5bd5a7f"
            }
          ]
        },
        {
          "id": "6d880700-fdfc-4f22-b77e-590ca288660e",
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
              "id": "14f79bcc-6830-46b2-8e6c-154d65381aaa"
            }
          ]
        },
        {
          "id": "e4511ecd-f59b-4888-9cec-1e0ca7d79a32",
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
              "id": "e2900156-4263-4ba9-9b7b-900eeaf46c70"
            }
          ]
        },
        {
          "id": "73b0540a-fbda-465d-adf8-97f1b2e2332b",
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
              "id": "be401898-a812-445d-8d4f-f0999a1365f6"
            }
          ]
        },
        {
          "id": "0d59a837-b1fe-484c-bfff-6a03cde3ec2a",
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
              "id": "127aea7f-b9f3-4b07-99f1-2d3f1b27e838"
            }
          ]
        },
        {
          "id": "632c8fd3-2285-44cc-81ce-52bb7787cedd",
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
              "id": "4bdd3a29-0d0b-48d7-b58c-8c13645462ef"
            }
          ]
        },
        {
          "id": "8d1b791a-f312-43af-845d-41418b2e27a8",
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
              "id": "dfce6c21-d259-437b-b8d5-48e8503c999b"
            }
          ]
        },
        {
          "id": "eb083f06-6193-4a87-81e8-99e4c55b874e",
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
              "id": "656bd60a-a5e0-47aa-977a-e8370cbf3587"
            }
          ]
        },
        {
          "id": "3c39ad46-dab3-4a18-902e-5f73a0498b41",
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
              "id": "605b213f-e235-42c1-a0f2-98ce844acd23"
            }
          ]
        },
        {
          "id": "0d192285-af1d-4dd2-913d-c8ba9dca4408",
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
              "id": "a26c1e17-03a4-48c0-b865-01251178d143"
            }
          ]
        },
        {
          "id": "7b970694-3acf-4f2e-938c-f21795389c12",
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
              "id": "9b96fcf5-1926-41eb-9815-6f95a18c4886"
            }
          ]
        },
        {
          "id": "c2743420-042e-415b-89c9-f86cbbbd152a",
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
              "id": "4476debc-fde9-48e5-a4a6-e6b29bbdbbab"
            }
          ]
        },
        {
          "id": "a70bf44a-5a3f-4747-8ee3-e179ecd3e4ad",
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
              "id": "bc3f4ac1-463d-4d91-8ee9-7322414042a1"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "1c076e08-1b7a-4077-ac1a-e32a7ccc0423",
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
              "id": "05495e23-d5dc-4bea-8a13-ecb2ce0c3552"
            }
          ]
        },
        {
          "id": "1c2bdba2-b855-4622-976d-2d6917d95825",
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
              "id": "6f03cbf2-3528-431c-bb33-daf2ac035de7"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "d3c01464-9cf9-4434-90b2-3dc9ec61b0bf",
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
              "id": "9adc5a53-3ab6-453c-8ff4-8a4c5d691a63"
            }
          ]
        },
        {
          "id": "b7c82490-a380-4302-a6f4-8b3df666a9a1",
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
              "id": "be443746-d413-41ee-9b5b-dde9f5bbe14e"
            }
          ]
        },
        {
          "id": "2bc7efeb-f4c6-4648-bf25-994c68452a34",
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
              "id": "f899656c-6c06-41dc-a07a-3b01a2ed19e1"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadataan",
      "item": [
        {
          "id": "04ba3fca-42de-43fa-b85a-d151abce7196",
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
              "id": "098a36d8-4f18-486b-ac19-f528b2c4869e"
            }
          ]
        }
      ]
    },
    {
      "name": "Contents",
      "item": [
        {
          "id": "71e29096-cd98-4018-a2d0-cf35fa8c7ead",
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
              "id": "ecd22483-6534-4df2-8f0f-205b5f1c44e7"
            }
          ]
        }
      ]
    },
    {
      "name": "Audit",
      "item": [
        {
          "id": "9a9d55e0-7270-4ce2-8027-a564e3d0aa3b",
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
              "id": "41ddde9e-b20a-4a23-8151-d3f22825326f"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "7b36e197-f901-4d2f-ba4a-fe369a947260",
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
              "id": "ba74a2e2-40e8-4ea4-b8b4-b0c8b5a953d2"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "f164555d-c8db-4abe-872a-bff93edf21eb",
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
              "id": "954c9522-89f5-4211-abf6-fe7e2035e9e9"
            }
          ]
        },
        {
          "id": "4e53eb4c-b48d-4cf4-b66f-bc8f5ab8f099",
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
              "id": "1a797482-2eab-4660-83ae-4fae414c394d"
            }
          ]
        }
      ]
    },
    {
      "name": "Comment",
      "item": [
        {
          "id": "c97c9179-1e54-464d-8bd3-2a9623df6454",
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
              "id": "fd6f91b6-62e7-4bda-81fb-3cc9f422a50e"
            }
          ]
        },
        {
          "id": "7a33534f-a2aa-4ab8-a181-e2c68d0f9286",
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
              "id": "778a38ba-a451-4d9b-8f7b-4e41cbd18dd1"
            }
          ]
        },
        {
          "id": "7696a7bd-9a24-4e78-8719-02ec72ba4996",
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
              "id": "e1a375fd-6fec-46b7-9c58-f5875a388900"
            }
          ]
        },
        {
          "id": "27af1dbf-3253-48d8-97d5-be6c889e09f4",
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
              "id": "f0e7542e-8ff2-4e45-ae5a-7ae4e33d320c"
            }
          ]
        },
        {
          "id": "d573af76-dfff-44fc-a499-ff9445061811",
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
              "id": "c0e88bb7-c3c3-4850-a081-ae19ae16f1d9"
            }
          ]
        },
        {
          "id": "771b4259-91b9-4819-8693-fe0eba855c6c",
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
              "id": "320d894e-be28-4356-bb46-1d9fbf658e53"
            }
          ]
        },
        {
          "id": "03b74fe0-b636-4187-97d9-967e23e96e39",
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
              "id": "5cdbf412-dade-4740-812a-185e243a1513"
            }
          ]
        }
      ]
    },
    {
      "name": "Component",
      "item": [
        {
          "id": "5a6e9184-159a-476f-bb4f-8cd4672497f5",
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
              "id": "375928b8-df63-4539-b4b7-e02559e31f08"
            }
          ]
        },
        {
          "id": "1a2b40be-2685-408c-9c7b-27958b699459",
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
              "id": "6c79affb-a1e0-4ba9-b720-a0b6e011a567"
            }
          ]
        },
        {
          "id": "9ce18c61-d9df-4a8f-8bf2-d5a1c694c080",
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
              "id": "c699ba61-4f5a-4990-ab56-2cd4c8ffeeda"
            }
          ]
        },
        {
          "id": "e3e3f75e-c441-41d6-b7a2-80feff20e4b3",
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
              "id": "ad278844-7863-4cee-9fd9-af11b12243c5"
            }
          ]
        },
        {
          "id": "6358837d-1bc0-4d7e-8f11-025de4244459",
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
              "id": "d8086ca6-4323-48b2-bed9-782784306989"
            }
          ]
        }
      ]
    },
    {
      "name": "Selected",
      "item": [
        {
          "id": "897ee76c-bbca-43c7-8f22-d64a6b43d518",
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
              "id": "ff00af51-1086-4d83-8311-dbad491b1443"
            }
          ]
        }
      ]
    },
    {
      "name": "Select",
      "item": [
        {
          "id": "389000f0-26c3-4429-ada7-03313fb469d9",
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
              "id": "9efcb1e2-983a-4fd8-9007-4aa73b1b0a82"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "5c331dd0-100d-4360-b19f-d6d673fb4d15",
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
              "id": "ccc6e434-ff81-4de1-a106-7f4cb35add29"
            }
          ]
        }
      ]
    },
    {
      "name": "Time",
      "item": [
        {
          "id": "af640942-f55a-4375-86d3-d3fd300aa5b4",
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
              "id": "2fa2c68f-1e5a-4bfc-996d-cfc01457aa14"
            }
          ]
        },
        {
          "id": "6622179a-e107-4ade-a36b-33c7a59393db",
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
              "id": "e8b74215-212b-4d1a-904b-dd90b70ea0ac"
            }
          ]
        }
      ]
    },
    {
      "name": "Custom",
      "item": [
        {
          "id": "5cff80c6-4e24-4a30-95f6-c059bb2f4289",
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
              "id": "57594b59-66fc-446e-8f79-f0e5d14a7502"
            }
          ]
        },
        {
          "id": "f488862b-3e88-41a7-b0f6-03b67a48de0a",
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
              "id": "397c5636-8c0c-4eb8-a995-6ae677cc000f"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboards",
      "item": [
        {
          "id": "510b83cd-b5e1-4113-af14-bafe75277542",
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
              "id": "9b9fae98-fa75-4625-9840-17a3c07771b1"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboard",
      "item": [
        {
          "id": "176beb9c-ea89-4c62-a2a4-aae7389d13f4",
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
              "id": "7ac74ba1-04fe-4cf4-b3db-a34b2c4c3d26"
            }
          ]
        },
        {
          "id": "8b2e64cb-76b0-4ef9-a367-69959102514e",
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
              "id": "bba29b8d-c4bb-4fba-a8ab-b0b5eeab7c8b"
            }
          ]
        },
        {
          "id": "46e5d96e-36c6-4c92-b691-6306278321e4",
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
              "id": "488ebaa5-27fe-4013-adb9-69f73729995b"
            }
          ]
        },
        {
          "id": "eb0c112b-6e29-42eb-8a37-9890f3917778",
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
              "id": "c9450ad4-e8bc-42c0-89ed-253098d82b54"
            }
          ]
        }
      ]
    },
    {
      "name": "Evaluate",
      "item": [
        {
          "id": "3068a980-efd9-4a61-ae6f-ad6cf7e93952",
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
              "id": "3da9ac55-9007-46ca-a844-17cf492df943"
            }
          ]
        }
      ]
    },
    {
      "name": "Fields",
      "item": [
        {
          "id": "65decd17-4c90-451a-b109-3c6a58710ec6",
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
              "id": "a4f5725e-53a3-40ca-a698-dd261e0772a5"
            }
          ]
        }
      ]
    },
    {
      "name": "Issue",
      "item": [
        {
          "id": "8ea2af30-e3cf-48c3-a0c3-4d0e3ad88dc9",
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
              "id": "0045a6fd-dc5a-4a72-912f-43e5824c47fb"
            }
          ]
        },
        {
          "id": "1236f668-cbc7-4dea-a1f4-33191caa7313",
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
              "id": "005a7caf-1a1f-4e6f-b8bb-aae89b438f6c"
            }
          ]
        },
        {
          "id": "844217b5-c898-40c4-bfa7-7cdd53306f0b",
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
              "id": "db4e4f36-0638-45ab-a871-25d4cb9f72fc"
            }
          ]
        },
        {
          "id": "65d0d4e5-6378-4723-8b2e-be395561b5ea",
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
              "id": "3c20e136-be04-4c04-b791-c2f251782b95"
            }
          ]
        },
        {
          "id": "6d28a49b-f871-4875-9fd1-bde52f584006",
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
              "id": "37a802dc-d265-4804-9ff7-8b9be48672b9"
            }
          ]
        },
        {
          "id": "625c01f4-1800-426f-a4da-8bbebec6b47a",
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
              "id": "e8606cd4-cc47-4d89-8dde-9b52ad98a621"
            }
          ]
        },
        {
          "id": "5a986936-4d7b-47ce-8f03-9e2ee267214c",
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
              "id": "94f6dc58-0a13-45a7-bcc5-39116cd0b391"
            }
          ]
        },
        {
          "id": "118113b6-3557-4487-bf44-70385ff5e52d",
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
              "id": "7160f7d6-faac-4c78-b236-b35b1b090b93"
            }
          ]
        },
        {
          "id": "6b7d7499-7b32-4bdc-9508-60a828333b06",
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
              "id": "61b1b116-d27d-4a4d-a8ce-f7b6bc9392e6"
            }
          ]
        },
        {
          "id": "8765c173-e898-436b-93de-390d26463a33",
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
              "id": "85b025b2-4a84-4854-9b6c-75f4104a9370"
            }
          ]
        },
        {
          "id": "8b938919-5160-454e-a255-f033662110b7",
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
              "id": "e6e5dd34-d04c-4d02-b51d-24724694bf77"
            }
          ]
        },
        {
          "id": "c9a2c5fd-180c-41f3-aaab-a56499da1b3f",
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
              "id": "0d0b5c98-4f13-424c-b68e-bc0c74e5b6f8"
            }
          ]
        },
        {
          "id": "1672de8b-2be8-4f41-b80a-d6862c7d8f85",
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
              "id": "b25b5e28-7c93-4816-aa34-ed4360b69e2d"
            }
          ]
        },
        {
          "id": "e4cfc1ae-a0ac-403b-b147-f21beedd9fa1",
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
              "id": "c5bc7224-342d-4820-b1dc-9a15a89ccbef"
            }
          ]
        },
        {
          "id": "9b773f18-ed59-485d-afd4-4602727ebde8",
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
              "id": "dc8af774-6da4-4ed6-8bda-318bcb31fd70"
            }
          ]
        },
        {
          "id": "cc626017-2643-4667-a8ab-9e05ec6490ae",
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
              "id": "96d239bf-9a4b-4dc0-9529-42a2e7dfe411"
            }
          ]
        },
        {
          "id": "d68137a8-feb0-43f6-a207-cadfb46fec3f",
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
              "id": "d3f31ec7-14ee-44cf-a6f0-a36bcf651f44"
            }
          ]
        },
        {
          "id": "f6848e77-d9f2-472d-962d-1fbb15e1240a",
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
              "id": "f23c77e4-5a52-4e6d-95b1-58ad46614f33"
            }
          ]
        },
        {
          "id": "f6129ffe-9393-40ac-916a-ec2aefa2aabb",
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
              "id": "a488b9d3-4f77-4ace-a71c-2495f1485d6e"
            }
          ]
        },
        {
          "id": "204df264-ddf9-45b4-8c14-3cedde3c86f3",
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
              "id": "724f8410-034c-4d2b-b271-214ead91aabb"
            }
          ]
        },
        {
          "id": "c8f0fa3f-8480-4f39-b7ed-0007aac096d8",
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
              "id": "87826217-1e64-4d44-a275-b66f08e71d73"
            }
          ]
        },
        {
          "id": "40cf5be0-22a7-429a-9819-7c2f12d046fb",
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
              "id": "a00ea8c4-3d56-4bcb-a82b-807f2f52e82b"
            }
          ]
        },
        {
          "id": "045b44eb-fbec-4e5c-ab47-1f73bc4c27d4",
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
              "id": "bd4bc98d-a258-47f2-b33f-1a9d10529bd4"
            }
          ]
        },
        {
          "id": "9b023c37-647a-4fee-af1b-0bb65d597954",
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
              "id": "e96d56c6-5c03-43bc-b754-2eccd132bde6"
            }
          ]
        },
        {
          "id": "fc0fcd1a-43ee-4cf0-bb2b-3fa3ffcf0d6a",
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
              "id": "ae088629-1fe5-4ea9-ab69-e8b68c50462b"
            }
          ]
        },
        {
          "id": "64d32a77-9704-4b45-9f1b-04f02d12ef7c",
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
              "id": "3ca0568c-dddc-4d48-acb5-b000c1f9bbfd"
            }
          ]
        },
        {
          "id": "bb01f8eb-baa0-4b66-bc24-5b1799412a2d",
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
              "id": "893e7067-fa32-47b5-89ec-79c5fbb7691d"
            }
          ]
        },
        {
          "id": "d6f9e74b-ae41-4642-a57c-ff3084608880",
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
              "id": "ae5d70cb-c7d0-484f-8880-7713aefa6ea0"
            }
          ]
        },
        {
          "id": "4b4153bf-47dd-48d9-9d1d-e330cc109419",
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
              "id": "a7e072ac-0d8f-44aa-abfa-840c2a590ea0"
            }
          ]
        },
        {
          "id": "7e089926-8bfa-4964-aca4-04d0bd019665",
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
              "id": "3d89334a-1fc5-42b6-84eb-720a72847de8"
            }
          ]
        },
        {
          "id": "b26f63e7-4139-4cf4-b15c-5aeb1f4c9602",
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
              "id": "6eb50a33-4053-4c64-8d75-a8be216398e7"
            }
          ]
        },
        {
          "id": "095171c5-0f7f-477d-8e1d-d0a471234596",
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
              "id": "38e2fb51-df29-4133-a603-d85656c41418"
            }
          ]
        }
      ]
    },
    {
      "name": "Selectable",
      "item": [
        {
          "id": "871f711d-4331-45ef-b982-dfdcdbb90340",
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
              "id": "7f659b0f-e106-415d-8788-5d21b6d47884"
            }
          ]
        }
      ]
    },
    {
      "name": "Visible",
      "item": [
        {
          "id": "a27548f9-fd5a-4e38-8bfe-eb2cf1e5a525",
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
              "id": "75668733-bfe8-4f3f-b901-b576660f5f61"
            }
          ]
        }
      ]
    },
    {
      "name": "Replace",
      "item": [
        {
          "id": "c9e5d938-2600-473b-8abe-6c9033126dd2",
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
              "id": "3f47ef9e-90e2-44a8-b1ad-6bcd195780fc"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "9322091a-9c7c-438b-bd47-66f7d403665f",
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
              "id": "7a88763b-781c-4a89-bd3e-4f75f0eebe27"
            }
          ]
        }
      ]
    },
    {
      "name": "Filter",
      "item": [
        {
          "id": "c4970281-f910-4a30-bd86-7c391b5139e8",
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
              "id": "bfb2bf97-7c6e-441e-bf78-aeca30837de8"
            }
          ]
        },
        {
          "id": "63f5e04a-620f-435b-8438-535492be66e9",
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
              "id": "2234a2b7-88f2-45c7-9061-0ec3abacf3f2"
            }
          ]
        },
        {
          "id": "6b827f71-a54b-4a40-9d6a-a78f7801ad3b",
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
              "id": "af1e552a-e268-469a-94cf-68fd9402fa4b"
            }
          ]
        },
        {
          "id": "6b950090-92c5-4ad3-b6b6-bea9f0f50431",
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
              "id": "c6d12b1e-aedc-4e66-9d59-dd0a96122dcb"
            }
          ]
        },
        {
          "id": "360543e1-2725-4d85-ad1e-5c5d3d59b304",
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
              "id": "d646f05f-f6b3-4e1d-9af7-ae27d42b5a28"
            }
          ]
        }
      ]
    },
    {
      "name": "Default",
      "item": [
        {
          "id": "57de740c-04d2-49ad-8761-5d1756829dbb",
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
              "id": "ecf7ca74-ad21-4080-9f3c-25a947595eec"
            }
          ]
        }
      ]
    },
    {
      "name": "Favourite",
      "item": [
        {
          "id": "6b53f2ac-68eb-41fb-aa5a-85445047d1ca",
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
              "id": "36d08c4c-2359-43b5-a556-aa682a32a6b4"
            }
          ]
        }
      ]
    },
    {
      "name": "My",
      "item": [
        {
          "id": "ea4ff53a-e03d-45cd-a71d-eec60ce48f86",
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
              "id": "f08a771f-3159-4434-bd8c-0d646ae0e068"
            }
          ]
        },
        {
          "id": "13d2180f-1a0d-47b0-b0ed-bd83976ef8fe",
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
              "id": "80e046af-f1d8-45d6-8f13-9812b87c3d11"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchfilters",
      "item": [
        {
          "id": "fa711758-ff32-4d7f-bb2c-07d8a12f5f46",
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
              "id": "5e63f127-4893-4fe0-9604-df19c0807deb"
            }
          ]
        }
      ]
    },
    {
      "name": "Columns",
      "item": [
        {
          "id": "aaee58a8-dcf4-4baa-a549-b54a3e5cc3ea",
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
              "id": "1ce60923-9dca-4aa4-b59f-47bdd624bdd1"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "19fbd9de-f833-45eb-aa21-8ac27c3b5632",
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
              "id": "5d0ef83b-6718-4639-847c-1a7ae5aaa71e"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "3c90e8a1-a097-4cae-aa83-d3e69b0c9e8e",
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
              "id": "282ea6cf-30bd-40ce-9c66-081b14deace3"
            }
          ]
        },
        {
          "id": "0ca1e5ac-ccc4-4a45-aed3-96b1f371b832",
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
              "id": "64c90ad2-993b-458c-9b0e-ac675fe96735"
            }
          ]
        },
        {
          "id": "da8df65b-07fe-4a7c-ac5a-f203df3c344f",
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
              "id": "fb619a92-5ef3-4994-bfa4-89812b13fc32"
            }
          ]
        },
        {
          "id": "e492c259-0bef-4600-a07b-ee41d5dc0ca9",
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
              "id": "c6c5bf02-0513-48f7-a2a2-5718688a5a8d"
            }
          ]
        },
        {
          "id": "1ebabd19-6063-4a72-b578-b9503aa047a3",
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
              "id": "9d14de37-c4e5-4391-9471-cee18870015b"
            }
          ]
        },
        {
          "id": "e5f5a9c2-c3f1-4bda-98f5-2a167916a113",
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
              "id": "86a28db5-d2af-4c67-9273-4e2ef9f5273e"
            }
          ]
        },
        {
          "id": "47b3097a-d9a5-4caf-a62a-2f3ef50e066f",
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
              "id": "cfe0604d-5ab6-4ad6-8a06-fcffb657541c"
            }
          ]
        }
      ]
    },
    {
      "name": "Share",
      "item": [
        {
          "id": "9cde0af2-ce84-4ac2-8c89-cb0c739a5ff3",
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
              "id": "a83747e5-8d73-460b-95a5-b98b08fd9627"
            }
          ]
        },
        {
          "id": "3fb80ba6-ed14-4b69-a054-400b02188fd8",
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
              "id": "bd24b33a-6d1f-4c2e-910a-f334c549d9d1"
            }
          ]
        },
        {
          "id": "8bb1a807-8cd2-4139-968c-f21023473b17",
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
              "id": "98b0cfc9-cb50-4ca1-9946-772cb1a5bc63"
            }
          ]
        },
        {
          "id": "196d76ca-3ddd-4abe-8ed5-0b734b42cd8d",
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
              "id": "9cb2e575-13b4-41f8-8c18-d104ca706753"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "34e4a54b-7f91-442e-9b68-758f1b826814",
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
              "id": "4d0f64ff-b58e-442a-a46b-4cbcd3daf633"
            }
          ]
        },
        {
          "id": "6fefe331-4efa-402d-b38d-b6d2ff5cc7fb",
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
              "id": "ddc9b7ea-6082-476d-ab9b-6da817216296"
            }
          ]
        }
      ]
    },
    {
      "name": "Users",
      "item": [
        {
          "id": "a5f139c1-1078-4fdc-8f26-61fd67f185fc",
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
              "id": "7b7d5c68-1415-4593-81f2-5295ce9029af"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "8ae1bd47-89a7-4ddc-ae92-a18c5be04455",
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
              "id": "a629cef1-d3f4-40e6-ae23-fab350ed88a6"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "deb64150-0ed4-45ff-abac-11a86bb538de",
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
              "id": "2d0accc5-2cd7-4d92-b1cb-23e8452054c0"
            }
          ]
        },
        {
          "id": "ee9bfd30-49e1-4cd4-99b3-59602fe555f7",
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
              "id": "93e9d60a-0605-44b8-8c5a-49f1c165094c"
            }
          ]
        }
      ]
    },
    {
      "name": "Issues",
      "item": [
        {
          "id": "cb2741e0-edcd-4669-b272-09e1c29ba4ef",
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
              "id": "281bd501-25a8-4edd-954a-c2a549c60902"
            }
          ]
        }
      ]
    },
    {
      "name": "Create",
      "item": [
        {
          "id": "75fd92b0-c953-426e-92b3-99e1cdfb11f0",
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
              "id": "4f41b2a4-28d3-470c-8396-9883955a4cc3"
            }
          ]
        }
      ]
    },
    {
      "name": "Bulk",
      "item": [
        {
          "id": "7915c443-0428-4914-b55e-1f8f07a98677",
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
              "id": "27050d88-8e8d-40a6-82fd-bea3cbc26b5a"
            }
          ]
        },
        {
          "id": "509d8d82-ea98-4f27-98fd-a91251562db9",
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
              "id": "340aac66-0bcf-4fa6-aaee-e5cde33d1289"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "b25ff0a6-bb00-41ce-861e-4c3b3f693d8f",
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
              "id": "69bce971-c9f8-4269-96c7-5b896a5a98fa"
            }
          ]
        },
        {
          "id": "9d6418ad-8a11-46b7-9148-31ef2baa5dcb",
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
              "id": "5f63f76d-dfd9-47bc-9c6e-e36107cfcf10"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "9ae96586-68be-415a-b29c-39ce45621670",
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
              "id": "c00fcf59-50cc-4113-9d61-90bebc4d30f9"
            }
          ]
        },
        {
          "id": "eb6b9c8a-33e2-4593-9df1-9d94c6d8b8b4",
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
              "id": "793d7282-c0c9-4ebf-9dd5-0bb28ff971de"
            }
          ]
        }
      ]
    },
    {
      "name": "Change",
      "item": [
        {
          "id": "455f84aa-9f02-4b24-b08b-786f101c3bf9",
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
              "id": "19cf28bf-61a3-49f6-b522-c99552d32d9b"
            }
          ]
        }
      ]
    },
    {
      "name": "Notify",
      "item": [
        {
          "id": "92141b1b-cba9-4d95-bdc2-7ae437e41e8a",
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
              "id": "035e4db1-df30-42b2-aa52-310ef43b8d8b"
            }
          ]
        }
      ]
    },
    {
      "name": "Remote",
      "item": [
        {
          "id": "227eb67c-ef9f-49c7-b62b-4cddccaa9b64",
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
              "id": "5a41ae7a-fb50-4552-bbcf-bee92dcf7ed0"
            }
          ]
        },
        {
          "id": "4db2eb97-17ca-4f00-888a-e1b45136652a",
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
              "id": "540112db-2ef0-4bc1-b93a-a64c32620f9c"
            }
          ]
        },
        {
          "id": "fc4dcbb9-f61a-449f-a8c7-dd1d7975698b",
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
              "id": "e8955f7d-4f2c-4266-9ffe-33b472044ac5"
            }
          ]
        },
        {
          "id": "dc6cfa4e-d3e0-44ff-a84e-38545bf57739",
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
              "id": "cfcefb36-b3d9-4cdb-b323-3adf708825c6"
            }
          ]
        },
        {
          "id": "336f8299-a7dd-48d9-b9a2-097743a831f2",
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
              "id": "9ee0a0f8-5569-485d-9090-1fbf26662c40"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "c80e7507-d086-4ad4-be3e-25d35a4574c1",
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
              "id": "14734f0d-b893-4fa6-b956-58bb72403f5d"
            }
          ]
        }
      ]
    },
    {
      "name": "Transitions",
      "item": [
        {
          "id": "5dc968a2-271b-4f91-bebe-5d759d6a8907",
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
              "id": "1b2a018b-fb1f-47d4-a2b1-92320ba29695"
            }
          ]
        }
      ]
    },
    {
      "name": "Do",
      "item": [
        {
          "id": "74f6f909-ba33-4c5e-8a5a-1e4971916a6c",
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
              "id": "278b9ee9-29f5-40d9-a685-c281273ee072"
            }
          ]
        }
      ]
    },
    {
      "name": "Votes",
      "item": [
        {
          "id": "7e22bae3-5dff-4238-af26-96cf1f16557c",
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
              "id": "a16f43ea-b1dd-48a7-8ae2-7236c615f514"
            }
          ]
        }
      ]
    },
    {
      "name": "Vote",
      "item": [
        {
          "id": "ad6c8dc6-0d2a-44b5-8a25-87527b1c6721",
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
              "id": "2d5d7af3-bf1c-4f49-923d-2111f2dbb91a"
            }
          ]
        }
      ]
    },
    {
      "name": "Watcher",
      "item": [
        {
          "id": "cb90f2ef-5031-449c-9e9c-b3effeb8e1f4",
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
              "id": "07c8a3ed-2837-4454-adf6-bf4cb6974241"
            }
          ]
        }
      ]
    },
    {
      "name": "Worklog",
      "item": [
        {
          "id": "682bd269-3082-415a-bffd-53f532dd9a71",
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
              "id": "81d517d3-c16b-4643-9634-6f8e46878ec9"
            }
          ]
        },
        {
          "id": "75599382-7161-4186-bcbf-0a19ded26a1c",
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
              "id": "a2c7c790-da7b-42cf-9145-023202a8052c"
            }
          ]
        },
        {
          "id": "cd7b0861-ca62-4a28-9f18-d55b19b59765",
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
              "id": "c25f363e-ba1e-45df-b88d-20fbd4c5aa2f"
            }
          ]
        },
        {
          "id": "41f0611b-c707-4b43-a25b-dc7d9fa501a3",
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
              "id": "e69c786e-1ead-493b-99d2-ab79e24d261b"
            }
          ]
        },
        {
          "id": "09ad7f90-4b4a-4648-bb52-c85cfc61bf1d",
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
              "id": "e47910a6-be82-4d85-aae2-74f93f73b593"
            }
          ]
        },
        {
          "id": "55b2d945-3a4f-4aa1-b027-9c4f4eb98b49",
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
              "id": "89340549-0af5-4ceb-be0e-b01e96b03120"
            }
          ]
        },
        {
          "id": "822a2b57-3c9f-426c-afe0-a024b6428b93",
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
              "id": "22ee2257-7f3f-479a-afba-900dd91f9932"
            }
          ]
        }
      ]
    },
    {
      "name": "Link",
      "item": [
        {
          "id": "1a4c0670-69d1-4837-8e13-1e8c4d0127f5",
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
              "id": "e0be5f66-7647-4f57-af9c-4ecb0fdfb576"
            }
          ]
        }
      ]
    },
    {
      "name": "Alternative",
      "item": [
        {
          "id": "2c3d7cb8-6520-4b05-a875-fdee2061aab7",
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
              "id": "56d2bc26-0795-49f2-bd9c-45575575fbc3"
            }
          ]
        }
      ]
    },
    {
      "name": "Auto",
      "item": [
        {
          "id": "8f059b85-3779-4b6a-bba7-a08e5fc8b727",
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
              "id": "3365ed26-6838-4874-81ae-5ce54f0aa45d"
            }
          ]
        }
      ]
    },
    {
      "name": "Field",
      "item": [
        {
          "id": "b9dda0ba-dc5c-4e9b-8466-13ce9912dbf7",
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
              "id": "fabd1554-3e2a-4d4a-aa0c-51e1e6290c34"
            }
          ]
        }
      ]
    },
    {
      "name": "Validate",
      "item": [
        {
          "id": "fbd72e62-8b0e-402f-9630-40f6ef1ca58d",
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
              "id": "c243494f-e655-4b49-a0bf-21e9ccf510d6"
            }
          ]
        },
        {
          "id": "7d9da9f6-00a7-43e9-b578-91c9b4cbc29f",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectValidateResource.validateProjectKey_get",
          "request": {
            "url": "{{default}}/api/2/projectvalidate/key?key=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Validates a project key."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de073a93-e7db-4dc1-a628-c815ae72fbe6"
            }
          ]
        }
      ]
    },
    {
      "name": "Preference",
      "item": [
        {
          "id": "d4a838c1-0d67-4611-a6fa-6a05bacbf6be",
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
              "id": "92a83af6-e4b4-478c-87ee-b88fe70ef1b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Locale",
      "item": [
        {
          "id": "dbaccead-f805-4284-90e5-f133df7ec547",
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
              "id": "fa736495-7f7e-47a8-aeea-dbae9d84c3ce"
            }
          ]
        },
        {
          "id": "7883e7ad-8c28-4428-a3db-8e6d92171acc",
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
              "id": "06b190fc-69d9-42e0-9bfe-6d298402153e"
            }
          ]
        }
      ]
    },
    {
      "name": "Current",
      "item": [
        {
          "id": "8f6e7f2f-d678-4580-a836-1f55cd7a8140",
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
              "id": "17df38b3-96f2-418d-87ee-b22795901855"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "c7b374b4-f192-4a7a-8081-f60fd1b8572c",
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
              "id": "588d2fb3-a178-44ca-8852-1beb8d7caf20"
            }
          ]
        },
        {
          "id": "a08ab56b-2aad-4ee5-84ec-1f7916ea6ed6",
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
              "id": "267dc9ad-72c3-4144-8147-1742e40a5b80"
            }
          ]
        }
      ]
    },
    {
      "name": "Permissions",
      "item": [
        {
          "id": "1c4b316c-61c5-4139-8a2e-62d6d3ca3a09",
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
              "id": "c07f7cd3-fde7-4737-8268-7f560466ad3b"
            }
          ]
        }
      ]
    },
    {
      "name": "Permitted",
      "item": [
        {
          "id": "7cb923dd-b1e9-4550-9339-9fc669a20db2",
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
              "id": "682c18d2-87d6-441f-8e6d-2f32b7302803"
            }
          ]
        }
      ]
    },
    {
      "name": "Permission",
      "item": [
        {
          "id": "e8a95d1b-a705-4af3-9419-6cb426d5cdba",
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
              "id": "86ab84e8-0b95-45cd-a4e2-93c90cf00793"
            }
          ]
        },
        {
          "id": "2818bffb-552b-4f1b-8479-95b121491125",
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
              "id": "13f2ed7e-138e-4d65-b1ee-c8a60a1887a6"
            }
          ]
        },
        {
          "id": "10941746-8d7d-410f-aa0b-997dc115c067",
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
              "id": "c3cf8317-1ad7-4d85-848b-ca334df1899e"
            }
          ]
        },
        {
          "id": "1f029173-b44b-4ede-bc4e-0aeb72964b6b",
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
              "id": "16088663-1bd1-4515-93ab-f0bd2a453204"
            }
          ]
        },
        {
          "id": "90117c10-f1ca-4c12-a14e-bc760548eb96",
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
              "id": "5203814a-e81b-4939-8373-18f70df4ac9a"
            }
          ]
        },
        {
          "id": "b62c2db1-cdd2-4ccd-b6c1-8214eb486242",
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
              "id": "2081a0b2-9812-4278-a5d2-d0ca54a8fda0"
            }
          ]
        },
        {
          "id": "848933ba-d7e5-458f-964e-4f6c86e5b4c4",
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
              "id": "c19dcb9b-8141-4cf4-9a7b-f6150b51cc18"
            }
          ]
        },
        {
          "id": "651e9d25-1a17-4b91-ac98-e7dc439ddec6",
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
              "id": "c1e2fd57-5318-4462-b871-8c47d551897c"
            }
          ]
        },
        {
          "id": "3330f0f0-73bd-4fc3-94a5-0e6c78b2e524",
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
              "id": "2156f19c-0ad4-4c9f-85cd-626a253b641d"
            }
          ]
        }
      ]
    },
    {
      "name": "Priorities",
      "item": [
        {
          "id": "bad2b375-338a-43fd-9b52-7dbdba73c3c7",
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
              "id": "5e5b656c-523c-4017-ba37-01699f79500a"
            }
          ]
        }
      ]
    },
    {
      "name": "Priority",
      "item": [
        {
          "id": "982c58e4-8ac4-4bed-b7df-04e4612dee00",
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
              "id": "06f43932-2cb1-42c7-9a10-cd637d82e07a"
            }
          ]
        }
      ]
    },
    {
      "name": "Projects",
      "item": [
        {
          "id": "2089fb6b-8bfc-42fb-9889-d1c106f4630c",
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
              "id": "b6a016bb-fd25-438d-aced-03478ffd22de"
            }
          ]
        }
      ]
    },
    {
      "name": "Project",
      "item": [
        {
          "id": "9fe20749-463c-4e09-8eb8-d7bc52c1101d",
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
              "id": "5735ad55-aa58-4447-aa90-3ecc505df9a8"
            }
          ]
        },
        {
          "id": "ded5c8e9-a70d-48b3-ba8f-6cf1607e1f9c",
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
              "id": "32a988cf-b7d3-4230-9864-a47d9d65a0cb"
            }
          ]
        },
        {
          "id": "668febd1-ce08-403e-98eb-d2228196e0fa",
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
              "id": "64de972c-fb0d-4dd1-a4b6-00041e2102e4"
            }
          ]
        },
        {
          "id": "708f3002-680d-4f13-93e8-2972fb82a71b",
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
              "id": "c8121e8f-5fe2-43ea-8c4b-0dcb2cc66be7"
            }
          ]
        },
        {
          "id": "e758b396-86c2-4fbd-ac57-de21121c3dce",
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
              "id": "722184e2-f44d-4781-9503-f0a060f08608"
            }
          ]
        },
        {
          "id": "b01fc296-cad8-48ef-bd08-3a05864609d7",
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
              "id": "6df1970b-2021-42cb-a365-cc9f2c01fd62"
            }
          ]
        },
        {
          "id": "19240e2f-8ee6-4b42-afce-c68938f57d9d",
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
              "id": "16cfcfce-c96a-42b2-b184-9ebf7208843a"
            }
          ]
        },
        {
          "id": "33712f40-349e-4c47-b13f-5a818175b7b4",
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
              "id": "a3376948-0066-4438-a21f-c2a18a97dc3b"
            }
          ]
        },
        {
          "id": "4d773068-9e29-4b79-bf1a-4401a45e3cca",
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
              "id": "bde83535-6704-4a41-a124-5164a41a35a3"
            }
          ]
        },
        {
          "id": "9d625b33-6ab7-419e-a8cb-70f73b34219e",
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
              "id": "75b7cc34-a8cf-432a-bd22-08fa690e1964"
            }
          ]
        },
        {
          "id": "93505600-7e85-489f-a2c9-2f6c4183c94f",
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
              "id": "3b46de4e-4969-4a82-8565-86370cef4ef1"
            }
          ]
        },
        {
          "id": "dfc62603-b127-465b-95b1-2be223e16203",
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
              "id": "54191329-3e38-419e-af29-26679bbb65fa"
            }
          ]
        },
        {
          "id": "37fe00da-3812-4694-8fef-f2ae95df3c7a",
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
              "id": "c5963f5c-820d-42fb-94e4-3e4101b4bfc9"
            }
          ]
        },
        {
          "id": "c3234beb-9cd4-45d0-ba17-9b1853850eb7",
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
              "id": "f5f76ad5-26e6-48d3-bcf7-77d4660aa25a"
            }
          ]
        },
        {
          "id": "66b61544-5f19-45e2-995f-9c421b10c2e0",
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
              "id": "f2ceae04-0438-4ef4-9ca5-863c353807be"
            }
          ]
        },
        {
          "id": "9d280a86-a30d-47b7-ae53-4d9c34c96fce",
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
              "id": "1bdc616b-5a96-4c11-b10c-e42375c55c63"
            }
          ]
        },
        {
          "id": "2a15972c-a4ad-45ff-8ad4-a3060dd5a5f3",
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
              "id": "5afc01d9-df95-4fb2-a30b-b01b19102e28"
            }
          ]
        },
        {
          "id": "f0ea45de-6882-4f7e-8ba6-762985b5d8d3",
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
              "id": "f64495e5-f14f-4e88-b67a-8b67c8f39dc4"
            }
          ]
        },
        {
          "id": "a59b1d9d-c8fd-4fc0-88cc-28be9f1a9c82",
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
              "id": "c2997033-b4b0-4ac1-83c3-426ae93f6a3d"
            }
          ]
        },
        {
          "id": "3efc39e4-e524-4928-ba00-24d9d5c8c811",
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
              "id": "e9659646-5ea5-4488-b9e2-7c68273dbd99"
            }
          ]
        },
        {
          "id": "1bf8a294-b502-4e25-96da-70b000997ff2",
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
              "id": "111f769a-693f-48c6-9bc4-6540dc0950b4"
            }
          ]
        },
        {
          "id": "8a138597-8272-4ac9-bec1-6c5221416fac",
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
              "id": "e91e7939-e11f-4436-b410-1b4fe642c978"
            }
          ]
        },
        {
          "id": "f01cd0fc-f00c-4454-a95c-b7ef1a821fd7",
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
              "id": "d9ee531e-0b47-498c-8d13-1879afea3faa"
            }
          ]
        },
        {
          "id": "9a84813f-5cdb-4b42-8939-f29733181798",
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
              "id": "e1457e72-1d07-4174-93cc-9d4d1b3883a8"
            }
          ]
        },
        {
          "id": "3c3beb82-b13e-4d81-b624-20402443c7a3",
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
              "id": "d02f86a7-05a2-4fa8-af7a-bd4e11ea4210"
            }
          ]
        },
        {
          "id": "8b14a410-6c3f-476f-a675-1746f12e618d",
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
              "id": "36ef102e-6cca-407e-b25b-6d34d931200c"
            }
          ]
        },
        {
          "id": "8e730127-e313-41cd-b308-69ebee1bb688",
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
              "id": "3643fda3-25eb-42f5-baec-b71a8a37147f"
            }
          ]
        },
        {
          "id": "b11312fb-7d3f-4556-a53f-d3c0c0feb8e0",
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
              "id": "aefb68f7-a36a-45e0-ac96-ec5eba845bdf"
            }
          ]
        },
        {
          "id": "726752db-98b3-438a-b088-16bf5b041327",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.getAllProjectRoles_get",
          "request": {
            "url": "{{default}}/api/2/role",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets a list of all project roles, complete with project role details and default actors.\n\n### About project roles\n\n[Project roles](https://confluence.atlassian.com/x/3odKLg) are a flexible way to to associate users and groups with projects. In Jira Cloud, the list of project roles is shared globally with all projects, but each project can have a different set of actors associated with it (unlike groups, which have the same membership throughout all Jira applications).\n\nProject roles can be used in [permission schemes](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-permissionscheme-get), [email notification schemes](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-notificationscheme-get), [issue security levels](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issuesecurityschemes-get), [comment visibility](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-comment-list-post), and workflow conditions.\n\n#### Members and actors\n\nIn the Jira REST API, a member of a project role is called an _actor_. An _actor_ is a group or user associated with a project role.\n\nActors may be set as [default members](https://confluence.atlassian.com/x/3odKLg#Managingprojectroles-Specifying'defaultmembers'foraprojectrole) of the project role or set at the project level:\n\n*   Default actors: Users and groups that are assigned to the project role for all newly created projects. The default actors can be removed at the project level later if desired.\n*   Actors: Users and groups that are associated with a project role for a particular project, which may differ from the default actors. This allows you to assign a particular user to different roles in different projects.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd6d326f-2ad8-47d0-aab7-d36d41c0ad37"
            }
          ]
        },
        {
          "id": "be581628-d60a-46b7-9d08-dcb306779d4a",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.createProjectRole_post",
          "request": {
            "url": "{{default}}/api/2/role",
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
            "description": "Creates a new project role with no [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get). You can use the [Add default actors to project role](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-role-id-actors-post) the project method to add default actors to the project role after creating it.\n\n_Note that although a new project role is available to all projects upon creation, any default actors that are associated with the project role are not added to projects that existed prior to the role being created._<\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6f9facee-c734-403c-8cc6-49d0bb99fc04"
            }
          ]
        },
        {
          "id": "5fcb4a2f-d41b-45c5-b538-9ee24fc20fcb",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.getProjectRoleById_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/role/:id"
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
            "description": "Gets the project role details and the default actors associated with the role. The list of default actors is sorted by display name.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a92b370-db3b-44d0-a021-fa563b94d5e5"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "63cc6cd4-4155-4655-ba8a-872ec4630c1c",
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
              "id": "f23799f9-b55f-4a4e-84d7-54b36fd2d393"
            }
          ]
        }
      ]
    },
    {
      "name": "Accessible",
      "item": [
        {
          "id": "994173db-1934-4822-a1ba-e6e07ca1c299",
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
              "id": "f264301e-e39a-4369-8202-e08404c79db4"
            }
          ]
        }
      ]
    },
    {
      "name": "Actors",
      "item": [
        {
          "id": "31554393-795c-4ec2-801e-517d1db87254",
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
              "id": "09b76c42-0ea0-4c62-8a6a-96e8546e000d"
            }
          ]
        },
        {
          "id": "95f10479-4aed-4beb-98b3-13cd708d69c8",
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
              "id": "c39f5cc0-b9bb-486c-879c-645e388be1e7"
            }
          ]
        }
      ]
    },
    {
      "name": "Statuses",
      "item": [
        {
          "id": "55a3cfab-cdd0-4a74-91f5-2a7c634c0666",
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
              "id": "6c384363-6ccf-4d09-9ae3-07de2b6bbfd7"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "aa19cbe7-5831-4f0c-aaa2-dabbb600ebe6",
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
              "id": "f4751292-d444-4b4d-8a4d-bedefebc6717"
            }
          ]
        }
      ]
    },
    {
      "name": "Valid",
      "item": [
        {
          "id": "30c31452-156a-4865-91a0-b6f132f62160",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectValidateResource.getValidProjectKey_get",
          "request": {
            "url": "{{default}}/api/2/projectvalidate/validProjectKey?key=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Validates the project key and generated a valid project key if the supplied key is invalid."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "687c9236-d480-4921-9c9d-878848662bfd"
            }
          ]
        },
        {
          "id": "19ba847b-278f-4aa1-adee-599fd48a907c",
          "name": "com.atlassian.jira.rest.v2.issue.ProjectValidateResource.getValidProjectName_get",
          "request": {
            "url": "{{default}}/api/2/projectvalidate/validProjectName?name=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Validates a project name. If the name is invalid, an attempt is made to produce a valid name based on the supplied one. If no such valid name can be found, an empty string is returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "63ad66a5-d2eb-4ba0-acf8-841d6c1259b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Resolutions",
      "item": [
        {
          "id": "e677e5f1-596f-4798-8fde-bd2c3f073265",
          "name": "com.atlassian.jira.rest.v2.issue.ResolutionResource.getResolutions_get",
          "request": {
            "url": "{{default}}/api/2/resolution",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all resolutions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f4bca535-10df-48fc-a18c-7c1ac1fe1919"
            }
          ]
        }
      ]
    },
    {
      "name": "Resolution",
      "item": [
        {
          "id": "27fce8b3-359e-4397-b5ac-c3668e31386a",
          "name": "com.atlassian.jira.rest.v2.issue.ResolutionResource.getResolution_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/resolution/:id"
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
            "description": "Returns a resolution."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1337032a-54a2-4236-ae04-f29ccb0359f2"
            }
          ]
        }
      ]
    },
    {
      "name": "Fully",
      "item": [
        {
          "id": "ba009b56-5161-43d8-80fd-9e1205189c2a",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.fullyUpdateProjectRole_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/role/:id"
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
            "description": "Update the project role's name and description. You must include both a name and a description in the request.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "808e6741-9569-4036-afee-7b0ba7d2a588"
            }
          ]
        }
      ]
    },
    {
      "name": "Partial",
      "item": [
        {
          "id": "26296eff-71de-49ee-94c4-133d1bcaea36",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.partialUpdateProjectRole_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/role/:id"
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
            "description": "Update either the project role's name or its description.\n\nYou cannot update both the name and description at the same time using this method. If you send a request with both a name and a description, then only the name will be updated, regardless of the order of appearance in the body of the request.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3bc60e4c-9a25-4833-bd4b-6e8a3ac7367f"
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