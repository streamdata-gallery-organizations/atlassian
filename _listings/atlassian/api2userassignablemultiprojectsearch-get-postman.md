{
  "info": {
    "name": "Jira Cloud API Find users assignable to projects",
    "_postman_id": "c6bc2bd7-5006-45f4-859f-8d43b4deea96",
    "description": "Returns a list of users who fulfill both of these criteria:\n\n*   their user attributes match a string.\n*   they can be assigned issues in one or more projects.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "751f67c3-30d0-40d0-9a7d-8816a74ebbfa",
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
              "id": "da736f82-0d59-4655-ac15-a9fe07d8f4ba"
            }
          ]
        },
        {
          "id": "f45a9e47-78d2-4114-b1af-52cdc6f947d2",
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
              "id": "d0df00b4-745c-4561-87c0-eb5917264665"
            }
          ]
        },
        {
          "id": "d72fd3c9-1029-4b10-bb88-da8f7c37be03",
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
              "id": "57b4d887-a05a-4a28-aca6-b3817e125669"
            }
          ]
        }
      ]
    },
    {
      "name": "Advanced",
      "item": [
        {
          "id": "cd133de8-82c8-44e1-8d99-1e0c693bc425",
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
              "id": "adff6ae7-8478-400e-b30d-b0ec3921569b"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "cdfc1ca8-3435-429d-88c3-79744cab7c6f",
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
              "id": "4b437c63-2934-463f-92e2-759277bc8f97"
            }
          ]
        },
        {
          "id": "8a222ef0-e143-4a87-8a7a-171400240423",
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
              "id": "fa870b8e-e5de-4d7e-9b05-8f3d16b8c0c9"
            }
          ]
        },
        {
          "id": "2f84d676-6bcb-4538-bc03-1e649993d115",
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
              "id": "ac409151-4bb3-4044-8458-869d813ffbcb"
            }
          ]
        },
        {
          "id": "2a5d1428-0591-4f8e-918d-3fbb0f20040d",
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
              "id": "469786b6-0732-438e-93f5-dbcc9866a18b"
            }
          ]
        },
        {
          "id": "79806004-3d98-4691-b655-505378e17530",
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
              "id": "93514b9b-3a51-4798-b49a-6d4224dc85e5"
            }
          ]
        },
        {
          "id": "b9b7bc38-abed-4068-9768-40d2c39f27cb",
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
              "id": "323f5289-5905-4240-8e39-f106978cad11"
            }
          ]
        },
        {
          "id": "2eec3d4c-4d84-4516-a6b8-b035103fabe1",
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
              "id": "0ed469d0-3a3e-433c-be66-cccd1ce82a45"
            }
          ]
        },
        {
          "id": "25ebc8e1-bdad-405d-9a98-3e746e1c540e",
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
              "id": "da13aeb2-5ca3-4ddb-8ca7-69ffc370f8c8"
            }
          ]
        },
        {
          "id": "df1da31b-f1de-4c59-88b8-8f9cef1c0a33",
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
              "id": "17982e66-3e66-4ccc-a9d9-64fe705a1e52"
            }
          ]
        },
        {
          "id": "857c1628-fa19-4b7e-bd8d-4bf140a2af38",
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
              "id": "de261677-1589-436c-bc3c-ee0672b26835"
            }
          ]
        },
        {
          "id": "00751736-4661-45e2-88e8-0a9f12da7ca5",
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
              "id": "0f6ee4b9-ee88-46cb-aa66-d12c4cd74a28"
            }
          ]
        },
        {
          "id": "43e82280-1c63-420c-8e0f-67f6048c47b2",
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
              "id": "47cfd737-1c42-40fb-8328-599d887156c0"
            }
          ]
        },
        {
          "id": "c56faae8-bfb1-409a-b397-33d0f3a2b804",
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
              "id": "59f7cd80-2356-4787-908d-c12496e0de0f"
            }
          ]
        },
        {
          "id": "060912e7-c2bf-4e6c-85d9-927f97256054",
          "name": "com.atlassian.jira.rest.v2.admin.SettingsResource.setBaseURL_put",
          "request": {
            "url": "{{default}}/api/2/settings/baseUrl",
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
            "description": "Sets the base URL that is configured for this Jira instance."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4099e9f-7d62-4c61-9ad7-c16e1a2ff5a8"
            }
          ]
        },
        {
          "id": "862968f3-7556-4fcd-9e1c-d3ec4fcf857a",
          "name": "com.atlassian.jira.rest.v2.admin.SettingsResource.setIssueNavigatorDefaultColumns_put",
          "request": {
            "url": "{{default}}/api/2/settings/columns",
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
            "description": "Sets the default system columns for issue navigator. Admin permission will be required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fefc7844-349f-4168-8bba-92f825d3efae"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "4fd4c87a-54ed-4876-880d-9b9209fe5ebe",
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
              "id": "5b84c820-db04-4eb3-bcfa-c4b20131da67"
            }
          ]
        },
        {
          "id": "acb448c1-b665-4370-a44a-730ff52be9ca",
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
              "id": "f3a5d276-0bc3-44e3-afa2-423343d10f9e"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "7d6d8801-57a6-4a38-abf6-5aea88d21734",
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
              "id": "5738b5b5-2f95-4647-b637-6dc824e5222e"
            }
          ]
        },
        {
          "id": "92caa215-db1b-4ffa-b797-c6407145387d",
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
              "id": "6a5934a3-609b-44d9-81e7-c89898026b2e"
            }
          ]
        },
        {
          "id": "bb73f80d-4a62-4be9-97c8-7da7ad6ac59b",
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
              "id": "bc266c2a-1d5a-4083-83f3-85d6b737efd3"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadataan",
      "item": [
        {
          "id": "739ac926-e1c7-4bce-8259-6d8393801717",
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
              "id": "dd57d231-67e8-496b-a2c9-65e28359baf6"
            }
          ]
        }
      ]
    },
    {
      "name": "Contents",
      "item": [
        {
          "id": "58afebeb-604f-4fcf-9d1a-ddad6fc2da80",
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
              "id": "72c8cfc2-096a-4d87-a76b-31dbbd3b677d"
            }
          ]
        }
      ]
    },
    {
      "name": "Audit",
      "item": [
        {
          "id": "42fe3101-3a5d-4b0c-bcf9-296fbfde28d9",
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
              "id": "b03a5832-855b-4c95-87de-32db16930341"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "b41ee013-79c0-4f45-8fe9-2e804662e5f0",
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
              "id": "1be35d3e-b0ab-4f1b-9a06-03c4991d5185"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "05851a38-9f56-404c-9cbd-ff825163c1cb",
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
              "id": "3abfc192-cd7b-411b-85ec-28c5df6ab48a"
            }
          ]
        },
        {
          "id": "35cb719b-34b0-4525-b4c3-85a9dbf3012b",
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
              "id": "440bf2f7-d096-4998-acb5-74afb05c26d3"
            }
          ]
        }
      ]
    },
    {
      "name": "Comment",
      "item": [
        {
          "id": "c3b4e997-2820-4802-9f09-ea640dec763a",
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
              "id": "74ab06e9-cdff-4509-98c7-24a2a7b420a6"
            }
          ]
        },
        {
          "id": "29260482-c580-4d69-a236-821cda706db9",
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
              "id": "f6ba1b14-6af2-43c1-b3b4-978476140121"
            }
          ]
        },
        {
          "id": "4113e539-791f-4bc0-ab0b-bd567af7fa90",
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
              "id": "fe8c34a2-7ab7-4101-8588-f8675a84bfaa"
            }
          ]
        },
        {
          "id": "2c4e9c07-b36a-44bd-a454-bda2f51d2fdc",
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
              "id": "13ba33e1-affc-44ee-9ffd-0047b9ad43a1"
            }
          ]
        },
        {
          "id": "5f9e7d82-0c17-4324-8c91-255cf6402912",
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
              "id": "1811f9c1-04fc-44a2-b126-b05581138f3c"
            }
          ]
        },
        {
          "id": "93facaff-5015-40c8-9a4a-7da6084a6998",
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
              "id": "5ea526a0-3084-4d82-bf20-f5091e6941b3"
            }
          ]
        },
        {
          "id": "06b4a4b2-7775-4b54-892d-ac6180f64e2d",
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
              "id": "8b60a5ff-0f5c-41f9-ad57-df818b3f7c5c"
            }
          ]
        }
      ]
    },
    {
      "name": "Component",
      "item": [
        {
          "id": "f002ae6d-164d-49de-8f72-33eb8d4a5592",
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
              "id": "30d03bae-c01e-4a9d-8a84-e4267e542f15"
            }
          ]
        },
        {
          "id": "d044b218-a7d8-4dff-b59e-2899371cb616",
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
              "id": "5eab7265-2f92-4772-978b-6637afeb9d88"
            }
          ]
        },
        {
          "id": "7e4e9094-2d4e-459d-8d20-a5b6e41b4604",
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
              "id": "3d80d258-3a4d-4584-8aa0-8c74ba282cc3"
            }
          ]
        },
        {
          "id": "4b3ed4a6-a724-4ed8-95a9-04f0676dcc1a",
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
              "id": "00b45ead-2405-4d64-828a-bd8053987691"
            }
          ]
        },
        {
          "id": "b3d2590c-8c5b-4fcc-8f62-9943a27a9847",
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
              "id": "89149cf7-22c1-4594-90b2-720a98ff5115"
            }
          ]
        }
      ]
    },
    {
      "name": "Selected",
      "item": [
        {
          "id": "b4604362-f55f-42ef-b3eb-7eea7f78faf8",
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
              "id": "0774d70a-3618-41c5-92ae-c0279ce47ec2"
            }
          ]
        }
      ]
    },
    {
      "name": "Select",
      "item": [
        {
          "id": "2dce2312-b4ad-4692-8e85-1d51df485d50",
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
              "id": "5ee3b36a-2ed0-43e7-9a3c-fd12e280ec2a"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "428ef16d-21e5-432b-9399-ee18eb53be60",
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
              "id": "8a9892c5-81dd-4719-a346-4018a1bbbf25"
            }
          ]
        }
      ]
    },
    {
      "name": "Time",
      "item": [
        {
          "id": "f6be60fa-d265-4d62-8d4d-be645e1cce56",
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
              "id": "713cab82-cfa0-4d60-9a93-9e5c18eda351"
            }
          ]
        },
        {
          "id": "6895823b-bd4b-47b0-afae-d91f2ad127a4",
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
              "id": "8d0d36a9-a6ab-449c-ab6d-bea7044932bf"
            }
          ]
        }
      ]
    },
    {
      "name": "Custom",
      "item": [
        {
          "id": "d8c59869-4819-4086-8da6-62c38c98adba",
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
              "id": "2fdec26b-659c-4a92-8c89-5ec7c8483b1a"
            }
          ]
        },
        {
          "id": "79dae192-ab83-40fa-ab5d-68333e5c8ae6",
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
              "id": "b8e0b63c-baad-437e-bf55-d63eb56e6d18"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboards",
      "item": [
        {
          "id": "66324ed0-e0d1-4beb-a981-ade48193ddf2",
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
              "id": "002b4587-a7ca-4415-afb8-6221cee41c31"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboard",
      "item": [
        {
          "id": "6c637a6b-7899-4ec7-9839-441013c93c8d",
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
              "id": "e500e291-3c3e-4888-97b4-72f52baf3ceb"
            }
          ]
        },
        {
          "id": "546fedfa-dfd3-41ac-a817-cdc15c263f8d",
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
              "id": "b290efae-14d2-4afa-9de2-de10ae248e57"
            }
          ]
        },
        {
          "id": "9f68595c-7cef-456c-8807-3209d17d19fd",
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
              "id": "ec608b1d-cf5b-48e2-a565-82edd8b507c5"
            }
          ]
        },
        {
          "id": "231ab358-5be8-4015-8709-c75107931131",
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
              "id": "2971b3a1-8448-4a43-995b-36281c136065"
            }
          ]
        }
      ]
    },
    {
      "name": "Evaluate",
      "item": [
        {
          "id": "2d36bb85-5de1-40a6-a97f-97fd6d3938fc",
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
              "id": "04f28771-f47b-4d10-935d-e22610d89e5b"
            }
          ]
        }
      ]
    },
    {
      "name": "Fields",
      "item": [
        {
          "id": "69061c69-52fe-45f6-be80-2702d8756d15",
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
              "id": "f6f3b667-6fd3-436b-b7be-a05caa198f28"
            }
          ]
        }
      ]
    },
    {
      "name": "Issue",
      "item": [
        {
          "id": "eac56910-72f0-475b-9a70-75b5ddc2573e",
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
              "id": "0d46958c-e48d-428c-a5e8-90cd8c67ac20"
            }
          ]
        },
        {
          "id": "36cb3c9c-44ed-4baf-80ed-9eecfee0f351",
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
              "id": "ee55b37f-cc1f-4844-97ee-c7399f666795"
            }
          ]
        },
        {
          "id": "c677e12e-1649-42f0-ba5f-cc2bcf50ce4e",
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
              "id": "f93e49ea-9284-4d4e-a1dd-b6570ef91431"
            }
          ]
        },
        {
          "id": "33830f60-193e-4f48-8760-cd62fcd09a52",
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
              "id": "15123531-7535-4b17-8fd3-a7cbe06a2ca6"
            }
          ]
        },
        {
          "id": "03ae9301-fab1-4b58-bc6f-b60a36dffae6",
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
              "id": "57d25111-c53e-483e-92c9-0968fe00f8c7"
            }
          ]
        },
        {
          "id": "2ed2efd8-6242-4bca-90cb-4f592c2f5892",
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
              "id": "706ec8bf-4c46-4eb4-abf7-5787d02d51f4"
            }
          ]
        },
        {
          "id": "7fc1eb47-d915-4623-a4c3-d86a6d02048c",
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
              "id": "e0997ac3-d77d-438e-a7a5-5b7ab4f3a0aa"
            }
          ]
        },
        {
          "id": "5d1054d5-f513-45c6-b4d7-08de94981459",
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
              "id": "ed2c1950-da91-4d93-abf5-f9cbb85535d0"
            }
          ]
        },
        {
          "id": "ca406a28-957d-4dbb-8b71-a038d0c62236",
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
              "id": "1f27b771-b305-4078-8379-c95fb6be4b55"
            }
          ]
        },
        {
          "id": "60b4650e-559e-4272-a383-7499bfc51d5d",
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
              "id": "95e403c5-e724-4beb-9237-16d8efe43192"
            }
          ]
        },
        {
          "id": "5c93ef7d-6ca6-4ddb-b508-75b9fc9d3bca",
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
              "id": "8a622e1f-ca7a-4f6a-bd0d-71d75cca4c1c"
            }
          ]
        },
        {
          "id": "e3a12606-d25e-4447-afc5-94cb6eff2a10",
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
              "id": "711dbab1-56a7-4f88-9ee1-dedaf1946434"
            }
          ]
        },
        {
          "id": "ef88042a-75b7-48cf-a8fd-419ea6f81f31",
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
              "id": "c685d991-4286-44b5-9baa-7e2826bc1b77"
            }
          ]
        },
        {
          "id": "4c4c440d-f4c7-4317-b1f1-4beec0b197f4",
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
              "id": "cd202597-44ab-42f1-a732-a6d75bc3a8a1"
            }
          ]
        },
        {
          "id": "1837e994-31f7-4880-ba0f-a86c6caf9136",
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
              "id": "a19fb4b6-15ce-43ba-b08d-83d8d9590e84"
            }
          ]
        },
        {
          "id": "4a0f9678-0f4f-4bce-afed-c5723229bca8",
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
              "id": "c2ed7dbe-31e3-40b2-948e-c1881a599012"
            }
          ]
        },
        {
          "id": "118e343d-4876-4469-8a46-17e0d64f75c8",
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
              "id": "8f3851ad-3181-4caf-ac79-ba35f6f13729"
            }
          ]
        },
        {
          "id": "a02c71f3-5819-459c-a089-d30e5c39889b",
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
              "id": "dfaea230-0868-4c45-9974-74bc44fb89e6"
            }
          ]
        },
        {
          "id": "e9ff45d4-ca77-4c2c-bd9c-ca01c07bd9b1",
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
              "id": "a466ba51-842c-487a-9630-854702e0a29a"
            }
          ]
        },
        {
          "id": "5e68fbfc-725d-4ed6-871a-2cb73a21bced",
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
              "id": "137e863b-9ea6-4ecf-b82e-232d8329002d"
            }
          ]
        },
        {
          "id": "1004b9fc-60b2-461d-8b64-d80719d5bf81",
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
              "id": "5751e2cc-305b-441a-8edf-130a5afa77ce"
            }
          ]
        },
        {
          "id": "df54850f-c23e-4266-ad5b-adbaa5ec2f14",
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
              "id": "2a99bcf0-2326-4016-83a8-4ed6d1247458"
            }
          ]
        },
        {
          "id": "63ae4dd4-7eaa-43f2-b8eb-a19cb1579c57",
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
              "id": "f03e7e52-2ba1-4e14-9feb-7f76263c37fa"
            }
          ]
        },
        {
          "id": "fd5d1ef7-33a2-4486-8b4c-057df8ff5cc1",
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
              "id": "b7e26c9e-e2dd-48dc-b5d2-f46eca3f8cae"
            }
          ]
        },
        {
          "id": "6c6b8bba-fbc3-4b9a-a787-f06a64def2ed",
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
              "id": "05fa46f8-cbf7-4959-8707-3978185e514c"
            }
          ]
        },
        {
          "id": "63e2a0ba-c06c-412b-b7cb-8f037125b824",
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
              "id": "9ca7a885-37ab-4961-b6e2-179f1724026e"
            }
          ]
        },
        {
          "id": "b749c07f-25c8-4dcb-88bd-cfed9cff101c",
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
              "id": "a65af79b-9f84-4e38-8ff8-958d5c9adcb9"
            }
          ]
        },
        {
          "id": "a961d43f-2f4f-4fb4-a40d-b99e2f633769",
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
              "id": "ec6a83fb-e3de-41a4-8754-50b4ea6726f1"
            }
          ]
        },
        {
          "id": "69d73926-cbc9-4c6f-ba52-0d37233fc130",
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
              "id": "41d8351c-4ff2-4d82-bc7f-8aaa15c3c8dd"
            }
          ]
        },
        {
          "id": "90395433-4406-4088-a866-b657cedfb9e3",
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
              "id": "a22ce59f-3925-4925-9b4d-b4ffee48c956"
            }
          ]
        },
        {
          "id": "521d76c4-5e90-414c-a87b-dc4c435db7e1",
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
              "id": "58729e95-61e2-45b2-8e74-44df0f6de38d"
            }
          ]
        },
        {
          "id": "0661b3a7-c899-4ac5-bbf8-d52c5aaee982",
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
              "id": "33dd2f6d-9844-4acb-bc09-38292422d39f"
            }
          ]
        },
        {
          "id": "ce54bf77-ef3d-48d4-bfaa-70826e543c58",
          "name": "com.atlassian.jira.rest.v2.issue.IssueSecurityLevelResource.getIssueSecurityLevel_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/securitylevel/:id"
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
            "description": "Returns a full representation of the security level that has the given id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6954a4df-53fd-4508-9828-89ff2410fcc8"
            }
          ]
        },
        {
          "id": "95ba6a4e-bfba-4b66-a4bf-3670ecb884c7",
          "name": "com.atlassian.jira.rest.v2.admin.SettingsResource.getIssueNavigatorDefaultColumns_get",
          "request": {
            "url": "{{default}}/api/2/settings/columns",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the default system columns for issue navigator. Admin permission will be required."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "062d50fb-dfd6-4734-a129-570ee38e68b7"
            }
          ]
        }
      ]
    },
    {
      "name": "Selectable",
      "item": [
        {
          "id": "86d66b81-5f5b-4334-89e3-c06b6bdd8f47",
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
              "id": "912c68a6-fb93-46b1-8c70-799ed7cbafc1"
            }
          ]
        }
      ]
    },
    {
      "name": "Visible",
      "item": [
        {
          "id": "5e213331-4758-45e4-a9b4-468660687086",
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
              "id": "70d40456-7edf-48d2-9172-cbb6edaaf6ea"
            }
          ]
        }
      ]
    },
    {
      "name": "Replace",
      "item": [
        {
          "id": "96859098-4bda-4427-9b13-1ca2282956d0",
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
              "id": "0ae174d5-917c-4297-9f23-5093962ad5c1"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "0c558669-d97d-4812-84e3-cedd1a0ecfbb",
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
              "id": "3d9f4bfd-2df3-4ef3-90b9-eabd4fc6d2a2"
            }
          ]
        }
      ]
    },
    {
      "name": "Filter",
      "item": [
        {
          "id": "7b6712fe-dc73-4452-bbe4-e606313629fc",
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
              "id": "e99e5ffe-39d2-455a-af7c-e207355b80a9"
            }
          ]
        },
        {
          "id": "7de47c13-bdeb-424d-8e08-1e3dd79b8729",
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
              "id": "880698c1-7af8-48a7-98d8-059914aae4ba"
            }
          ]
        },
        {
          "id": "dee39a52-9245-4ca4-9c02-f501e82e94a5",
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
              "id": "92340f0b-5ab3-4ac0-833f-b398bb71ea96"
            }
          ]
        },
        {
          "id": "d676beb0-bc26-423f-b7cd-6376f71900d0",
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
              "id": "91d2dd41-57c8-4a4a-affd-bca0e7a656d6"
            }
          ]
        },
        {
          "id": "cb54ad3c-e81f-4b97-a6d5-9ca81b44682a",
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
              "id": "3132e1d9-9694-44e1-8535-8a0e01a71bf2"
            }
          ]
        }
      ]
    },
    {
      "name": "Default",
      "item": [
        {
          "id": "2fb3d387-d445-41a9-b280-ebff0358d860",
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
              "id": "261036ec-55fe-47f8-84f3-8ff08d86d2ca"
            }
          ]
        },
        {
          "id": "5a1052d8-c5d3-4db6-af62-e033314ea1b8",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.getProjectRoleActorsForRole_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/role/:id/actors"
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
            "description": "Returns the [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) for the project role.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cc4a25c8-460d-42f9-8377-023c8e8fad62"
            }
          ]
        },
        {
          "id": "a387a00f-2565-4d11-be02-01061d653af9",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.addProjectRoleActorsToRole_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/role/:id/actors"
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
            "description": "Adds [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) to the given role. You may add either groups or users, but you cannot add groups and users in the same request.\n\nChanging a project role's default actors does not affect project role members for projects already created.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b564b1ab-6177-48be-bb82-db0c6234d6c7"
            }
          ]
        },
        {
          "id": "c235cb6b-4d9d-4cfb-8764-d9894da7eaa6",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.deleteProjectRoleActorsFromRole_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/role/:id/actors"
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
            "description": "Removes [default actors](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-resolution-get) from the project role. You may remove either a group or user, but you cannot remove a group and a user in the same request.\n\nChanging a project role's default actors does not affect project role members for projects already created.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8107667f-36fa-4eb5-b68b-a4acca0b78ab"
            }
          ]
        }
      ]
    },
    {
      "name": "Favourite",
      "item": [
        {
          "id": "b8ab4a75-c571-42a9-990f-910883b2c0a1",
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
              "id": "2352792c-3fa6-4dbe-ae26-b5b6c8b77131"
            }
          ]
        }
      ]
    },
    {
      "name": "My",
      "item": [
        {
          "id": "a9ccaf56-3401-4da7-91e8-85399c566559",
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
              "id": "50097881-94da-4cff-8162-da9a7db2b6cd"
            }
          ]
        },
        {
          "id": "dcd02bc4-2e55-40a4-ba7d-7e0429efa2a2",
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
              "id": "adfd51da-46bc-418f-9555-e438f89cb0ac"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchfilters",
      "item": [
        {
          "id": "8764eb1a-6c6d-4d4d-9e84-6bd6dc528d91",
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
              "id": "6553c17c-ec93-4916-b3a2-ea5523fcaa47"
            }
          ]
        }
      ]
    },
    {
      "name": "Columns",
      "item": [
        {
          "id": "41878ddb-6560-4a5d-a121-494e8a90f719",
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
              "id": "7918a936-c95a-4751-8055-595ec665c081"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "9f4eaf8c-8a55-4400-aa71-8ef17fd81551",
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
              "id": "977fd4c6-4c0f-4432-8b7b-4f5d57df400f"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "f16e1ab4-8e6c-4c20-96e2-d691191eefcf",
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
              "id": "a7b29a3d-2cd9-47c0-8979-1a9560adbfd9"
            }
          ]
        },
        {
          "id": "b2c8db5b-ceed-4c9c-a7ba-4b095019a5d7",
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
              "id": "13b4cd43-56d3-4aeb-bfc6-d4a9ee22095f"
            }
          ]
        },
        {
          "id": "3f69814c-9103-4055-8c42-fd5349ebbe34",
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
              "id": "fa50bd8b-9e68-49d3-9508-966d2ff7c04c"
            }
          ]
        },
        {
          "id": "4c1cdd7a-a682-4d0a-814f-e9a92c944145",
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
              "id": "94386d43-a357-493e-a1ec-837c21cd5128"
            }
          ]
        },
        {
          "id": "410a47a8-7c12-403c-831c-f43eddafdf02",
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
              "id": "a5657da7-6e40-49fe-9364-55ec224c41ba"
            }
          ]
        },
        {
          "id": "e878c547-d67f-425a-aecb-c0d28a3372a1",
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
              "id": "aa13ccd7-d54f-465c-b9cd-58976cbd63b6"
            }
          ]
        },
        {
          "id": "e9e57364-8813-4181-b3a3-6aa9fedf88d3",
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
              "id": "b0149fb8-b3ac-4898-8fe0-58e4ffa97869"
            }
          ]
        },
        {
          "id": "305b0a59-85d1-413d-b88f-9ba28ed60154",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.removeScreenTabField_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs/:tabId/fields/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tabId",
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
            "description": "Removes field from given tab"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d846f1c1-999a-46c5-b25a-0831c96da472"
            }
          ]
        }
      ]
    },
    {
      "name": "Share",
      "item": [
        {
          "id": "463963f9-c1da-47bb-8761-51065064a170",
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
              "id": "414c83a0-22db-46c6-9c9b-40c2ec512ce5"
            }
          ]
        },
        {
          "id": "9515b577-2ff7-46d1-a128-d1e76300f99a",
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
              "id": "23f16c74-8bca-44bc-9f0d-68bfe201d935"
            }
          ]
        },
        {
          "id": "a86384ed-92df-46c9-b444-879950fb9ba8",
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
              "id": "50e508ff-1fb0-4cc7-80db-6c6a7d2ea70e"
            }
          ]
        },
        {
          "id": "947a5e43-d7a2-42fa-aafe-d12a667cb7c7",
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
              "id": "71517094-c7c6-4562-b815-1f17c1b03c94"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "0183a55e-e5fd-41f0-826b-ee66bd1804c0",
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
              "id": "a2bd5168-e6ce-4d33-b52b-8d6951ef18ae"
            }
          ]
        },
        {
          "id": "25dc0e87-1b75-4545-8dc7-ad5bbccb898a",
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
              "id": "1ce09327-7a06-49d7-a08b-5a80a4481983"
            }
          ]
        }
      ]
    },
    {
      "name": "Users",
      "item": [
        {
          "id": "ce096852-970f-4e11-b998-d5202d3393bd",
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
              "id": "4d0155a1-8883-46b4-87fb-409fb625ca58"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "0ab934cd-e3b8-443e-8d8a-91139ef141bd",
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
              "id": "caf01fa3-9910-4008-aebe-aef837606dc8"
            }
          ]
        },
        {
          "id": "014e4bd1-53f9-4f23-935b-eaf49f8db58c",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.getUser_get",
          "request": {
            "url": "{{default}}/api/2/user?accountId=%7B%7D&expand=%7B%7D&key=%7B%7D&username=%7B%7D",
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
            "description": "Returns a user. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** None."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7e9381f3-93b3-4914-944e-68b8689d539b"
            }
          ]
        },
        {
          "id": "a1edd929-6552-4301-9897-9e7672fe5434",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.createUser_post",
          "request": {
            "url": "{{default}}/api/2/user",
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
            "description": "Creates a user. This resource is retained for legacy compatibility. As soon as a more suitable alternative is available this resource will be deprecated. The option is provided to set or generate a password for the user. When using the option to generate a password, by omitting `password` from the request, include `\"notification\": \"true\"` to ensure the user is sent an email advising them that their account has been created. This email includes a link for the user to set their password. If the notification isn't sent for a generated password, the user will need to be sent a reset password request from Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=)"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fb37c245-0f82-445c-abc8-05d42ea69679"
            }
          ]
        },
        {
          "id": "5ffab18b-501c-4b47-93f2-1cbce404e27d",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.removeUser_delete",
          "request": {
            "url": "{{default}}/api/2/user?accountId=%7B%7D&key=%7B%7D&username=%7B%7D",
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
            "description": "Deletes a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Site administration (i.e., member of the site-admin [group](https://confluence.atlassian.com/display/Cloud/Manage+groups))."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2eb9b44c-7fd3-4ce3-b64d-fc23aa0daa06"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "1d8ec39b-c106-435a-aaa5-5ec0fa39aa52",
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
              "id": "4f43907d-78b2-45d7-8e6a-aa55456c941b"
            }
          ]
        },
        {
          "id": "882f62a2-a765-4606-a0af-7ea762b390e3",
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
              "id": "93d5cde4-b449-426f-b268-f9ea3796c689"
            }
          ]
        },
        {
          "id": "ed949d75-6151-48d9-ad0f-174dfed6137f",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.findBulkAssignableUsers_get",
          "request": {
            "url": "{{default}}/api/2/user/assignable/multiProjectSearch?maxResults=%7B%7D&projectKeys=%7B%7D&query=%7B%7D&startAt=%7B%7D&username=%7B%7D",
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
            "description": "Returns a list of users who fulfill both of these criteria:\n\n*   their user attributes match a string.\n*   they can be assigned issues in one or more projects.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** None."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "aa102379-18eb-4eff-b44f-df953c9528c0"
            }
          ]
        }
      ]
    },
    {
      "name": "Issues",
      "item": [
        {
          "id": "5f390477-8aea-4466-85ad-980a5ca93510",
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
              "id": "284374f9-a044-44a3-9d36-6c46c19a5c4d"
            }
          ]
        }
      ]
    },
    {
      "name": "Create",
      "item": [
        {
          "id": "55f8c84e-dd08-4818-96d7-c9353a8301ad",
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
              "id": "28e24e13-d5b7-46e9-b2ba-cdd1e1adf913"
            }
          ]
        }
      ]
    },
    {
      "name": "Bulk",
      "item": [
        {
          "id": "ff94cf2d-6db1-4dc2-b1e1-0dd53f943677",
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
              "id": "0bbbcf6e-0d94-4aa7-8164-1ba12d3ec4ea"
            }
          ]
        },
        {
          "id": "cc9612ab-fa7f-4b77-a88c-a26fdfeab1c5",
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
              "id": "9492b0a0-d51a-4ba2-bd33-bfd9043b773c"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "437cfb0f-8813-49fc-ad04-4235ba018384",
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
              "id": "a709d17e-dbf9-40ab-8520-13a2c03ce413"
            }
          ]
        },
        {
          "id": "b31eb978-327a-4830-b1d0-e2ec8bd89721",
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
              "id": "5ffe0377-5e83-47a9-a3fa-01a4479a2e34"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "4a6598cf-d708-49cc-9c74-9176b2be46ea",
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
              "id": "5368cfe6-0ec2-4d15-a5bc-ba08670494dc"
            }
          ]
        },
        {
          "id": "230f1c97-39f7-453c-a84a-8f68cbd4d16b",
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
              "id": "0f7f859f-8bb7-4191-8c88-edd5abca06ab"
            }
          ]
        }
      ]
    },
    {
      "name": "Change",
      "item": [
        {
          "id": "bb4ed89c-781a-41b8-8abe-250ca908cf64",
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
              "id": "5a2ebc26-16fb-457a-98f9-d0fc351dd191"
            }
          ]
        }
      ]
    },
    {
      "name": "Notify",
      "item": [
        {
          "id": "1dc8e738-85c2-4486-8f8b-54cd96d234b1",
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
              "id": "4bbb3ffd-63dd-45b0-ab3e-2dc5dee82a97"
            }
          ]
        }
      ]
    },
    {
      "name": "Remote",
      "item": [
        {
          "id": "8b58e8dc-bd6c-43cf-8b6c-e358a0b7a794",
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
              "id": "ba3d943c-442e-493b-a61b-b507322bd2b8"
            }
          ]
        },
        {
          "id": "21765388-8234-4998-946a-f6f0dd2f1be8",
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
              "id": "64f09cbf-4a9c-444f-bb23-750043e65570"
            }
          ]
        },
        {
          "id": "8842a019-cc70-4d98-b837-0a0f087006de",
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
              "id": "b4c3c23b-1a1e-4465-bac4-9d9d1b439c44"
            }
          ]
        },
        {
          "id": "14a38349-7cb0-489f-adec-763e51c81941",
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
              "id": "a1f37230-51ee-430d-8a03-c3a5a7b9fff8"
            }
          ]
        },
        {
          "id": "5f9d9f2c-65fa-4867-9214-2c5f6efd6047",
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
              "id": "f79e3640-e5fd-428a-b4f2-80147630ec57"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "f26b5a0e-e357-4814-818e-73fb66cbabb3",
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
              "id": "bbed0a24-b184-4fc8-a0d8-9367467a6fe9"
            }
          ]
        }
      ]
    },
    {
      "name": "Transitions",
      "item": [
        {
          "id": "c73be136-3745-4047-b81d-345ec710d6fc",
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
              "id": "78945bbc-abd5-4eca-acd8-3492901bd690"
            }
          ]
        }
      ]
    },
    {
      "name": "Do",
      "item": [
        {
          "id": "3f911873-f5d7-4ae9-b181-c6e69a1723fe",
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
              "id": "0cbf6863-d841-44d2-afaf-0bccee172549"
            }
          ]
        }
      ]
    },
    {
      "name": "Votes",
      "item": [
        {
          "id": "3cea98ee-b294-48ca-be01-662767f6ab1a",
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
              "id": "398c7ce3-41aa-4dfb-b8d5-438b74b1a277"
            }
          ]
        }
      ]
    },
    {
      "name": "Vote",
      "item": [
        {
          "id": "fc4f1715-8bd2-4150-9638-268495414967",
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
              "id": "c642ee77-753e-4051-a61d-998dc70cc88d"
            }
          ]
        }
      ]
    },
    {
      "name": "Watcher",
      "item": [
        {
          "id": "db38b1d7-9c88-4d83-9254-2d12dfd8b25f",
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
              "id": "79455d2a-4295-464a-bbdc-bbcd43d23f2f"
            }
          ]
        }
      ]
    },
    {
      "name": "Worklog",
      "item": [
        {
          "id": "feb169c9-19af-4935-854d-c28e4f4a2d6a",
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
              "id": "0eb04725-d724-4f95-8f8b-2cef6a12c97b"
            }
          ]
        },
        {
          "id": "176b3e1c-2840-40c2-b56c-127c9593bc75",
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
              "id": "99ca4a06-3ca5-4f2d-be79-cfd901e62ae6"
            }
          ]
        },
        {
          "id": "85133d3f-7f49-4772-b0bb-6814315abc17",
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
              "id": "3b6bbaff-0741-4240-a356-403f434059cf"
            }
          ]
        },
        {
          "id": "9e6666d0-f496-4d7d-b119-bbc80d0fcf93",
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
              "id": "fb650e9a-ae4f-4670-93ec-8388f399935f"
            }
          ]
        },
        {
          "id": "70d7917b-f9dc-45bc-a283-7785ba5564d7",
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
              "id": "ddae51ed-08c6-452a-a1cc-a05192349758"
            }
          ]
        },
        {
          "id": "7a08c9e7-ec4e-4ea8-9c9f-485711fd8fe6",
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
              "id": "5a17d02d-c5f7-445e-9d2f-2a6102e26f21"
            }
          ]
        },
        {
          "id": "e16f15d4-c5f2-4397-919c-3207ae5be616",
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
              "id": "d5f81338-e82e-48ea-937c-0a27de6d8918"
            }
          ]
        }
      ]
    },
    {
      "name": "Link",
      "item": [
        {
          "id": "e88c0bde-3e61-495a-9b3f-a3d65a7268b2",
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
              "id": "8b824cf5-6720-4cc3-bfc1-46bef6ba6cda"
            }
          ]
        }
      ]
    },
    {
      "name": "Alternative",
      "item": [
        {
          "id": "0e0c5714-4ddd-4243-9fce-ede79453fc83",
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
              "id": "73928611-da04-45fc-a2cd-c62f179cb2fd"
            }
          ]
        }
      ]
    },
    {
      "name": "Auto",
      "item": [
        {
          "id": "9c52e8ff-514b-4736-867f-1786a77c489b",
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
              "id": "ffc88a7c-50e9-4b6d-8fe8-9e7723479fb3"
            }
          ]
        }
      ]
    },
    {
      "name": "Field",
      "item": [
        {
          "id": "3bdbc0a6-debe-47f4-b7d1-941e167f0141",
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
              "id": "996b0300-4e09-47c6-9beb-244c1b888371"
            }
          ]
        },
        {
          "id": "db1e17ee-2210-4a32-9201-6e6d5206c143",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.addFieldToDefaultScreen_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/addToDefault/:fieldId"
              ],
              "variable": [
                {
                  "id": "fieldId",
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
            "description": "Adds field or custom field to the default tab"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "49fa0be5-752b-4f54-9a0b-877a6ebe3fcd"
            }
          ]
        }
      ]
    },
    {
      "name": "Validate",
      "item": [
        {
          "id": "0fc5be95-9a80-41e9-a289-9fed28d6d41b",
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
              "id": "2d6a0ef4-ca1b-4393-85e2-17eb14aade91"
            }
          ]
        },
        {
          "id": "cb9bd898-d265-4f6b-b552-34d54f60e0e1",
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
              "id": "e51d6b2f-dca9-4c11-b51a-ef250f26ac75"
            }
          ]
        }
      ]
    },
    {
      "name": "Preference",
      "item": [
        {
          "id": "8aee147f-e2f7-4b86-9866-1906ed5e6251",
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
              "id": "4a6f7861-ad90-4255-8c94-323f3fc4840e"
            }
          ]
        }
      ]
    },
    {
      "name": "Locale",
      "item": [
        {
          "id": "50888a6a-9bac-4806-9229-4862b9fcc088",
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
              "id": "818b5224-b15c-4d76-b26a-abf6cd562c29"
            }
          ]
        },
        {
          "id": "21d51d07-3d6d-4613-a93c-e052cc7a6d3b",
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
              "id": "8df854e9-40f5-43ca-a20a-d8dd56f385d8"
            }
          ]
        }
      ]
    },
    {
      "name": "Current",
      "item": [
        {
          "id": "48170a35-531b-41a2-b092-e510dec530e4",
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
              "id": "4594da13-6174-430a-ad38-1fb49b743a01"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "a6e3c485-0b54-4208-a622-4403f42507b8",
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
              "id": "fcdad9cb-1a5a-4244-b5bd-1332a0878fd7"
            }
          ]
        },
        {
          "id": "6df57de3-2079-4913-8100-f7361bcf08c6",
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
              "id": "f282d748-c086-4267-a496-01e8593004c7"
            }
          ]
        }
      ]
    },
    {
      "name": "Permissions",
      "item": [
        {
          "id": "33f1e9ec-dbb4-4f09-9903-ac5be64509f3",
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
              "id": "075aa49c-bfce-4287-8768-f3222b45e028"
            }
          ]
        }
      ]
    },
    {
      "name": "Permitted",
      "item": [
        {
          "id": "c8db754e-c4ba-4fbe-8a6e-9b0adcc26c44",
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
              "id": "4a54526d-5f27-494c-8727-c575579d1b21"
            }
          ]
        }
      ]
    },
    {
      "name": "Permission",
      "item": [
        {
          "id": "c414cede-ef7f-4ef6-b237-d334d931b1bf",
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
              "id": "e8d00985-6c9d-44d0-89d1-2f52f1c0c8dc"
            }
          ]
        },
        {
          "id": "481ef304-2896-4aae-be27-f36bb1dee1ad",
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
              "id": "1f5d0475-447b-487a-bc32-d176d4b7544e"
            }
          ]
        },
        {
          "id": "22a51a38-d31b-45ec-aed9-8ca68acdf331",
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
              "id": "f133451d-b5de-4a71-872b-f83cf0a5e0e3"
            }
          ]
        },
        {
          "id": "25f95b07-796d-4060-a03d-59c06a4d06db",
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
              "id": "0c856038-9ab0-49c9-9f8a-b597bbd1a947"
            }
          ]
        },
        {
          "id": "995a2b68-1138-440d-8d19-b3dcb597fd7d",
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
              "id": "45782967-aaca-4120-8dd4-e9d8736b5d2e"
            }
          ]
        },
        {
          "id": "01aaa3ac-00b3-45ef-9fcb-2f311b3557f7",
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
              "id": "9d64ca91-17ef-4a96-b553-147160abd679"
            }
          ]
        },
        {
          "id": "dd01096a-2417-41f9-906c-868a69cc42b1",
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
              "id": "fc58ac3f-5a65-48a1-a764-293322b82243"
            }
          ]
        },
        {
          "id": "a0216704-a0d1-4e3b-81d5-283121de4ee5",
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
              "id": "f573a0d1-a54e-410f-877f-398c71eca71c"
            }
          ]
        },
        {
          "id": "4b582006-c816-4a20-8597-cf6b13a71f47",
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
              "id": "537479b1-4298-4148-a1a6-a1b3c5d6c911"
            }
          ]
        }
      ]
    },
    {
      "name": "Priorities",
      "item": [
        {
          "id": "e972c8b2-d146-4703-8dc5-34adf538c14a",
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
              "id": "d6daad09-6567-47ab-98fc-8a4f7a27d56b"
            }
          ]
        }
      ]
    },
    {
      "name": "Priority",
      "item": [
        {
          "id": "9fcd0c02-e525-4925-909d-641a1a04b3cb",
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
              "id": "aa2e4a0e-c6ba-4718-9938-e4a9cf497012"
            }
          ]
        }
      ]
    },
    {
      "name": "Projects",
      "item": [
        {
          "id": "0d5e05b1-64ab-4223-a9da-540abce07178",
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
              "id": "bc1cd6a6-968d-4123-b99f-a666aaaa0979"
            }
          ]
        }
      ]
    },
    {
      "name": "Project",
      "item": [
        {
          "id": "bf2df338-9fc2-42dd-832f-6fd77bfd6b9e",
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
              "id": "056f317a-33f7-4f13-b589-43ec873fc48d"
            }
          ]
        },
        {
          "id": "1b374a01-4fdc-4882-b6ab-9664f7182779",
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
              "id": "7166238b-ff64-42d7-8603-3f4962dd7fb1"
            }
          ]
        },
        {
          "id": "8edac5bc-4b6b-4856-a6c5-bd211fd03fa2",
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
              "id": "9122f098-7e44-4727-9c31-363bfc8f032e"
            }
          ]
        },
        {
          "id": "8a4678fe-90d9-4e9c-95ec-e409f7c2d57d",
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
              "id": "d812fd6d-5497-497b-9ee3-205c88d71fe8"
            }
          ]
        },
        {
          "id": "da8f09a1-dbc5-4941-8604-1a4912c03593",
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
              "id": "122318b1-b69f-4bac-97a1-ff29057cc3e2"
            }
          ]
        },
        {
          "id": "35af3e03-750f-4a40-a8c0-1f17f3b798e7",
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
              "id": "a322cd33-9189-4c03-9e86-bd0427407319"
            }
          ]
        },
        {
          "id": "087f84a0-4a45-49b3-bab7-588288b51901",
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
              "id": "a356f2c8-309b-4eea-8314-c36c46907078"
            }
          ]
        },
        {
          "id": "ace4ee21-d342-47e3-a8c6-45d3e122d5b4",
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
              "id": "ed18fd47-f5cd-44b3-bfa6-560b8efbaacf"
            }
          ]
        },
        {
          "id": "b736191c-0969-4f2a-8e02-df0140e1eca2",
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
              "id": "361c85ac-19dc-4dbd-9c1c-8bbf670e1d92"
            }
          ]
        },
        {
          "id": "33aaad12-9a25-4865-8b47-479e22938846",
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
              "id": "32d182a4-6454-4cf0-b4ac-1b8035f08f9d"
            }
          ]
        },
        {
          "id": "e8a5e785-9937-46d3-ac83-35c4b452617a",
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
              "id": "60224f81-6a0c-4799-b8e3-c343ad502d29"
            }
          ]
        },
        {
          "id": "efde43cb-ef98-4e03-934c-14991897d0f6",
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
              "id": "ce294976-c8e9-4ec5-93d5-0b4a1cac519c"
            }
          ]
        },
        {
          "id": "468f38c2-8c81-4b57-9d37-9cff531def3a",
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
              "id": "d2033e9a-186a-4c3c-8c02-23a358cea6a2"
            }
          ]
        },
        {
          "id": "f26b8675-9717-407f-ba8b-91c787b73a7b",
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
              "id": "7be6de40-2af2-43c0-b062-9ae014ec2bdf"
            }
          ]
        },
        {
          "id": "50a9eb22-01ef-4870-a1b3-4506a4425a44",
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
              "id": "386dbf58-eafe-47d7-bc59-6ca967ea95ef"
            }
          ]
        },
        {
          "id": "9ed419da-218a-4ee6-aa9c-0e91ace64bf0",
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
              "id": "66f109c1-2c81-45a2-b981-a8cd70cadc8e"
            }
          ]
        },
        {
          "id": "af95a6fe-98c5-4a8a-b9e8-21363ce3a053",
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
              "id": "55b9b6c7-8f60-45d6-adae-a4a1f2841309"
            }
          ]
        },
        {
          "id": "f2e9b832-8384-4be0-be34-1ff5e259ee6e",
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
              "id": "37880f7d-7a48-4596-a2af-b09305f43a37"
            }
          ]
        },
        {
          "id": "372ddb4c-20d8-48bc-87cf-05dc043ddfbd",
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
              "id": "09a12c7d-4ce9-46f4-a0b2-949f85733d3b"
            }
          ]
        },
        {
          "id": "bc4748c0-d154-4edc-8924-505c021a0e89",
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
              "id": "35090d7a-42f2-4d12-bf91-6f25af9ff903"
            }
          ]
        },
        {
          "id": "46f7b208-4bb9-4e9b-9e37-1a8a09dff34c",
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
              "id": "7fe01f99-6d92-44b6-94b0-309fcb27804c"
            }
          ]
        },
        {
          "id": "ed86e8bf-78cf-45a4-af35-63a4cf527f5f",
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
              "id": "fb097b28-13a5-475f-9128-f269632ecdf1"
            }
          ]
        },
        {
          "id": "1e441684-b91c-4014-ae5c-baf171138451",
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
              "id": "6a074de7-ddc0-4ce6-84f7-49fbf113ec9c"
            }
          ]
        },
        {
          "id": "7b528f27-386d-4db6-af1c-ff7e69f99286",
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
              "id": "b3b88c03-4daf-4da1-8371-4cef8b784ccb"
            }
          ]
        },
        {
          "id": "2030d64d-72e6-4d4b-96bd-7e438a41661c",
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
              "id": "02d546b6-252a-4ba2-9aec-2c7d849c0c71"
            }
          ]
        },
        {
          "id": "743c85ba-0f31-4024-8499-40095ef330ef",
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
              "id": "39476899-571a-4c1e-a72c-5214bba6973e"
            }
          ]
        },
        {
          "id": "1e8fee76-5343-40c8-a29b-401151178c0a",
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
              "id": "ce99c1b5-b641-43ee-9ada-bb211bbf621c"
            }
          ]
        },
        {
          "id": "4019098e-fad3-4465-b05a-8c796c314325",
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
              "id": "8930136e-bd08-42c2-9108-2bff5f67b69d"
            }
          ]
        },
        {
          "id": "b661358a-026b-4ed8-a23c-56d7e753072d",
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
              "id": "ae7d49c2-1a8e-4691-8bf1-ca7b6149d703"
            }
          ]
        },
        {
          "id": "d054511f-6cc4-49d0-bd0b-f5c56ff94f50",
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
              "id": "f02282e1-32be-462e-bec0-37ff3de656a1"
            }
          ]
        },
        {
          "id": "2ced3e09-6b9e-4a43-9604-904667edf8ee",
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
              "id": "e4f311d4-b237-43d2-a953-dd6459f36965"
            }
          ]
        },
        {
          "id": "69f62724-93fe-4d42-a53e-36bcc2bfc223",
          "name": "com.atlassian.jira.rest.v2.issue.project.RoleResource.deleteProjectRole_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/role/:id"
              ],
              "query": [
                {
                  "key": "swap",
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
            "description": "Deletes a project role. You must specify a replacement project role if you wish to delete a project role that is in use.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "264e845f-a9ff-48ed-8d75-3ec981ff9009"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "1bd8c650-a85e-4d92-836e-ca3a65a2eef1",
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
              "id": "c8021740-6ee4-487d-9c34-e239f29f1815"
            }
          ]
        }
      ]
    },
    {
      "name": "Accessible",
      "item": [
        {
          "id": "f0b559c9-3586-4d33-98dd-e2db76c66adc",
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
              "id": "e33e3995-9430-4a75-baef-95b8b1019aea"
            }
          ]
        }
      ]
    },
    {
      "name": "Actors",
      "item": [
        {
          "id": "2843e8f1-538a-4e74-a738-0caf1b871b90",
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
              "id": "1c09bfce-578f-4a61-ade5-a05358eb421f"
            }
          ]
        },
        {
          "id": "9131e265-d6e6-423b-be21-98edf710a091",
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
              "id": "c79cf8e5-741f-4351-944c-7a908249a4e6"
            }
          ]
        }
      ]
    },
    {
      "name": "Statuses",
      "item": [
        {
          "id": "3ab23bf5-d8f0-494d-8f26-2d0635bc79c5",
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
              "id": "846b113f-f0de-4712-b976-463bc73f650d"
            }
          ]
        },
        {
          "id": "f12e4371-18c3-468d-be3d-0e33af364e95",
          "name": "com.atlassian.jira.rest.v2.issue.StatusResource.getStatuses_get",
          "request": {
            "url": "{{default}}/api/2/status",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all statuses"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "82a91b6a-f4fb-4360-9d71-53041f640436"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "5184ffd2-aee3-4ce1-a93e-7d3d8bad66da",
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
              "id": "e6bc15ee-41f6-4a42-9b56-39319101ccb3"
            }
          ]
        }
      ]
    },
    {
      "name": "Valid",
      "item": [
        {
          "id": "43da586a-c918-478e-aa42-327ddf9f9fde",
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
              "id": "7b612c7d-8d4f-4343-adf5-08721208de02"
            }
          ]
        },
        {
          "id": "8f7f94f9-65be-46cc-9a39-886ff319d28a",
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
              "id": "d533406e-5712-41b5-80c5-98da00ab2ed8"
            }
          ]
        }
      ]
    },
    {
      "name": "Resolutions",
      "item": [
        {
          "id": "bcf2aac4-a750-4622-a343-9056897ab90a",
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
              "id": "c7940f86-f6dd-4fa0-9b82-f5e3a57fdf59"
            }
          ]
        }
      ]
    },
    {
      "name": "Resolution",
      "item": [
        {
          "id": "a72a5b80-2cce-43cf-9f19-2a507b34ee5c",
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
              "id": "b897ae23-9480-4f26-9d7a-9b1b3288f510"
            }
          ]
        }
      ]
    },
    {
      "name": "Fully",
      "item": [
        {
          "id": "70a313a0-fd12-407e-92b7-f10f5dccf4de",
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
              "id": "88477f82-25fc-4c4e-8493-211f95ad1453"
            }
          ]
        }
      ]
    },
    {
      "name": "Partial",
      "item": [
        {
          "id": "a1aadef7-62a9-4f47-88ce-d3d9086de52a",
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
              "id": "483b08b2-61cc-4c13-90bb-b89590661815"
            }
          ]
        }
      ]
    },
    {
      "name": "Screens",
      "item": [
        {
          "id": "06169e9c-8b4a-4598-ae1a-f7e6d0f8e08c",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.getAllScreens_get",
          "request": {
            "url": "{{default}}/api/2/screens?maxResults=%7B%7D&startAt=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a [paginated](#pagination) list of all screens."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb934b99-21b7-4ba6-a207-3978eeec7a76"
            }
          ]
        }
      ]
    },
    {
      "name": "Available",
      "item": [
        {
          "id": "ec2d892e-4430-48cf-a5eb-df01fcb06e89",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.getAvailableScreenFields_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/availableFields"
              ],
              "variable": [
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets available fields for screen. i.e ones that haven't already been added."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4f514974-5bc5-4c3a-9078-8754f6af024b"
            }
          ]
        }
      ]
    },
    {
      "name": "Screen",
      "item": [
        {
          "id": "03e92c53-d392-4689-88e5-19d8279e5dc7",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.getAllScreenTabs_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs"
              ],
              "query": [
                {
                  "key": "projectKey",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all tabs for the given screen"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "27e7cd44-579d-4287-81c1-ff1d0e48b80d"
            }
          ]
        },
        {
          "id": "a34810ee-948b-40c7-9110-d4d5eb243735",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.addScreenTab_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs"
              ],
              "variable": [
                {
                  "id": "screenId",
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
            "description": "Creates tab for given screen"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c3816e47-eda8-4be6-9154-aaba9d3823a0"
            }
          ]
        },
        {
          "id": "7be6b2ca-ba90-412a-8978-feaf1528af06",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.deleteScreenTab_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs/:tabId"
              ],
              "variable": [
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tabId",
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
            "description": "Deletes tab to give screen"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83bea924-d463-49c6-9ce9-c1d0b7103f5a"
            }
          ]
        },
        {
          "id": "388222cc-403a-43b0-bd32-4d694e460c3c",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.getAllScreenTabFields_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs/:tabId/fields"
              ],
              "query": [
                {
                  "key": "projectKey",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tabId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets all fields for a given tab"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "101bff0d-dbc2-40b5-baef-c1885ae8cf65"
            }
          ]
        },
        {
          "id": "0a051820-80d2-47ee-b717-300ad9a6ff43",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.addScreenTabField_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs/:tabId/fields"
              ],
              "variable": [
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tabId",
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
            "description": "Adds field to the given tab."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "db40f323-2b44-45ce-816f-9ef5214f477a"
            }
          ]
        }
      ]
    },
    {
      "name": "Rename",
      "item": [
        {
          "id": "1176c58c-b0dc-4f86-a5a0-ac6fe7bb2153",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.renameScreenTab_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs/:tabId"
              ],
              "variable": [
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tabId",
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
            "description": "Renames tab on given screen"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a1d6e92f-f053-4851-b056-38f1e42c0ba5"
            }
          ]
        }
      ]
    },
    {
      "name": "Move",
      "item": [
        {
          "id": "6f59472d-3ad8-479a-847c-927730a3ffe5",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.moveScreenTabField_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs/:tabId/fields/:id/move"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tabId",
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
            "description": "Moves field on the given tab"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "24143047-2537-43b4-9013-52c0d1ff4d3f"
            }
          ]
        },
        {
          "id": "8aae9e13-64db-4e3d-8119-6992edb2f313",
          "name": "com.atlassian.jira.rest.v2.issue.ScreensResource.moveScreenTab_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/screens/:screenId/tabs/:tabId/move/:pos"
              ],
              "variable": [
                {
                  "id": "pos",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "screenId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tabId",
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
            "description": "Moves tab position"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4e4edb78-1bd2-4f99-b9ae-162d23858f65"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchissues",
      "item": [
        {
          "id": "3f4e4916-db17-4a58-9058-104dcad0f248",
          "name": "com.atlassian.jira.rest.v2.search.SearchResource.searchForIssuesUsingJql_get",
          "request": {
            "url": "{{default}}/api/2/search?expand=%7B%7D&fields=%7B%7D&fieldsByKeys=%7B%7D&jql=%7B%7D&maxResults=%7B%7D&properties=%7B%7D&startAt=%7B%7D&validateQuery=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.\n\nIf the JQL query expression is too large to be encoded as a query parameter, use the [POST](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-post) version of this resource."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8b5bb69c-9dfd-4213-98f5-b01e6dade217"
            }
          ]
        },
        {
          "id": "d278735f-4b49-4c2e-acf1-83fef60f29ee",
          "name": "com.atlassian.jira.rest.v2.search.SearchResource.searchForIssuesUsingJql_post",
          "request": {
            "url": "{{default}}/api/2/search",
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
            "description": "Searches for issues using [JQL](https://confluence.atlassian.com/x/egORLQ). **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira.\n\nThere is a [GET](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-search-get) version of this resource that can be used for smaller JQL query expressions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d435fcdf-5d07-44bb-b5fb-b2ba92615edf"
            }
          ]
        }
      ]
    },
    {
      "name": "Server",
      "item": [
        {
          "id": "9cece54c-dcdf-41ad-9a95-b6169371230d",
          "name": "com.atlassian.jira.rest.v2.ServerInfoResource.getServerInfo_get",
          "request": {
            "url": "{{default}}/api/2/serverInfo",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns general information about the current Jira server."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fdec2950-844e-4af3-a670-3c800f9acf14"
            }
          ]
        }
      ]
    },
    {
      "name": "Status",
      "item": [
        {
          "id": "7e1c719c-9e4d-4a26-8c31-cae073b10b56",
          "name": "com.atlassian.jira.rest.v2.issue.StatusResource.getStatus_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/status/:idOrName"
              ],
              "variable": [
                {
                  "id": "idOrName",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a full representation of the Status having the given id or name. If there are two statuses with the same name, only the first found status will be returned. Therefore searching by id is encouraged."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ce50a4b8-fc4b-479d-aadc-6a8fa72db688"
            }
          ]
        },
        {
          "id": "f93cb769-1dc8-485f-82df-19fea8b3d768",
          "name": "com.atlassian.jira.rest.v2.issue.StatusCategoryResource.getStatusCategories_get",
          "request": {
            "url": "{{default}}/api/2/statuscategory",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a list of all status categories"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "175ec33e-3e72-49f8-b3c8-b67d1191171d"
            }
          ]
        },
        {
          "id": "6c35f7e3-af06-42a0-b5db-adacee2d0b4f",
          "name": "com.atlassian.jira.rest.v2.issue.StatusCategoryResource.getStatusCategory_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/statuscategory/:idOrKey"
              ],
              "variable": [
                {
                  "id": "idOrKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns a full representation of the StatusCategory having the given id or key"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2691c098-0cea-43b6-b882-2df93923472d"
            }
          ]
        }
      ]
    },
    {
      "name": "Task",
      "item": [
        {
          "id": "b7555dcc-efed-4e6f-a456-bb504c52cd07",
          "name": "com.atlassian.jira.rest.v2.task.TaskResource.getTask_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/task/:taskId"
              ],
              "variable": [
                {
                  "id": "taskId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "This endpoint is used to check the status of a [long-running asynchronous task](#async).\n\nWhen the task is finished, it will contain a **result**. The result may be arbitrary JSON, its shape different for each task type. Consult the documentation of the method that created the task for more details.\n\nTo access a task, you need to be its creator or a Jira admin. Otherwise a 403 response will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f5f4f7cd-dc2b-422c-8c46-41d3e38d20b1"
            }
          ]
        }
      ]
    },
    {
      "name": "Cancel",
      "item": [
        {
          "id": "d14a691d-a97d-4188-8a07-9bc5b51da391",
          "name": "com.atlassian.jira.rest.v2.task.TaskResource.cancelTask_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/task/:taskId/cancel"
              ],
              "variable": [
                {
                  "id": "taskId",
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
            "description": "Requests that the task that corresponds to the given task id is cancelled.\n\nTo cancel a task, you need to be its creator or a Jira admin. Otherwise a 403 response will be returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0ba0cc8d-620e-47ce-8d51-69d4a9b68da9"
            }
          ]
        }
      ]
    },
    {
      "name": "Avatars",
      "item": [
        {
          "id": "5e20e3c6-e3a2-41b8-8f21-6a77b9f9f485",
          "name": "com.atlassian.jira.rest.v2.issue.UniversalAvatarResource.getAvatars_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/universal_avatar/type/:type/owner/:entityId"
              ],
              "variable": [
                {
                  "id": "entityId",
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
            "description": "Get avatars"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "569c5284-ed44-4523-b946-75768936836d"
            }
          ]
        }
      ]
    },
    {
      "name": "Store",
      "item": [
        {
          "id": "3965bffb-3ed5-4b58-b72b-86d6178e38f2",
          "name": "com.atlassian.jira.rest.v2.issue.UniversalAvatarResource.storeAvatar_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/universal_avatar/type/:type/owner/:entityId"
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
                  "id": "entityId",
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
            "description": "Creates an avatar for a given entity, for the given entity ID and type of entity. For example, you can create an avatar for an issue type, given the issue type Id. Uploading an avatar is supported for different types of entities across the Jira products. However, it is supported for the \"project\" and \"issuetype\" entity types for all Jira products. The uploaded image will be cropped according to the crop parameters listed below. If no crop parameters are specified, the image will be cropped to a square. The square will originate at the top left of the image and the length of each side will be set to the smaller of the height or width of the image."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fac3b601-4803-4476-ab07-14a5f66584df"
            }
          ]
        }
      ]
    },
    {
      "name": "Avatar",
      "item": [
        {
          "id": "8bf779b4-6d5a-412f-9e53-949dae3b9fc2",
          "name": "com.atlassian.jira.rest.v2.issue.UniversalAvatarResource.deleteAvatar_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/universal_avatar/type/:type/owner/:owningObjectId/avatar/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "owningObjectId",
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
            "description": "Deletes avatar"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a4cbea81-cfc7-4e08-91c0-14c89f105b25"
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