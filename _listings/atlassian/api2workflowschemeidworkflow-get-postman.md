{
  "info": {
    "name": "Jira Cloud API Get workflow",
    "_postman_id": "4a390bdc-5b1c-422f-a163-4daa4f8edaa0",
    "description": "Returns the workflow mappings or requested mapping to the caller for the passed scheme.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "73646d1a-53ec-402b-aafa-f7e70c164bb9",
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
              "id": "997f8136-775e-4201-b176-4d04728a2b86"
            }
          ]
        },
        {
          "id": "e46562e9-7412-47ed-9034-ee191824900e",
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
              "id": "ae3f5571-5061-47ae-8bc8-44f7823a4f46"
            }
          ]
        },
        {
          "id": "fc149446-8688-40c8-ba83-bf0bf3b9b3c2",
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
              "id": "06e966c0-06c8-414b-9707-c2f8c211166f"
            }
          ]
        }
      ]
    },
    {
      "name": "Advanced",
      "item": [
        {
          "id": "fe6d4a2b-141a-4ea9-9fbc-17b11ba19f28",
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
              "id": "e9c5c237-50ed-4014-b1ec-bce76f4d48c9"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "b484be16-d0a9-4f0a-ad3e-1be707140fc5",
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
              "id": "9c14e0f3-6e11-4f16-8de5-5090b5a55274"
            }
          ]
        },
        {
          "id": "34c653e2-5f62-41dd-bd68-18226edbd5b1",
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
              "id": "77a6bc0c-1fff-430e-89cb-a225b3a8de63"
            }
          ]
        },
        {
          "id": "03a2e5f4-20b1-4c41-a8b1-02616efba939",
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
              "id": "31047014-1854-489d-81a0-ad521405bc33"
            }
          ]
        },
        {
          "id": "9ce662e6-ad0e-4f16-b950-4b7f00a290f5",
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
              "id": "5dc5ec76-85c7-46e5-a6a5-06c573b7176e"
            }
          ]
        },
        {
          "id": "bf95e28f-1f04-4a3c-b4ae-82f2b8c2353e",
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
              "id": "073a4199-3c5b-4379-87b9-59e7da9903c3"
            }
          ]
        },
        {
          "id": "6d09a649-ce9d-4f08-8e72-645212c4b1e3",
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
              "id": "c19c39e3-9eb0-44c4-b4f4-f96ac13e2959"
            }
          ]
        },
        {
          "id": "fbeae5ec-2f9a-4b7f-8a2d-dff7d3bf0d5a",
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
              "id": "9bf13511-7522-4cc5-b9bf-2d7c32068352"
            }
          ]
        },
        {
          "id": "77695bdd-afd5-49e6-9dbc-1c2a83bb06b0",
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
              "id": "d909d6b4-bcf6-4912-b2df-99c73f173cf8"
            }
          ]
        },
        {
          "id": "9a4e487b-f412-4baf-a517-429133abe5aa",
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
              "id": "df77102d-203e-48e4-b051-8fac2d0f3edc"
            }
          ]
        },
        {
          "id": "4916b027-9e6e-4fe4-bf69-024c728a4598",
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
              "id": "a41af501-605b-42c4-895b-9367d2248145"
            }
          ]
        },
        {
          "id": "82a5f941-c3ab-420c-84a4-7c4a6a0cf62d",
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
              "id": "0273cfdb-98e4-4aec-91b6-b14958ee2e35"
            }
          ]
        },
        {
          "id": "faf0b90b-25bf-4c96-bf27-7a8273ec8796",
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
              "id": "f6632f67-0ca9-4fa4-94df-20831384f56e"
            }
          ]
        },
        {
          "id": "7fd7a0a5-15d2-41e7-94e1-64d830e246cb",
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
              "id": "a29f8262-b5f2-4885-8dad-50f4d311e097"
            }
          ]
        },
        {
          "id": "fc144766-93e9-431c-88eb-a117637ae790",
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
              "id": "2f60bf42-b176-4a07-9dc9-383640f057d8"
            }
          ]
        },
        {
          "id": "8019eb97-1fb7-40f5-905a-17a59943e0f7",
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
              "id": "c8ce6f10-ceea-44e9-b078-404c17ff1225"
            }
          ]
        },
        {
          "id": "64b5a15f-7a18-4a71-a73e-bb0449c59b6b",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.setUserColumns_put",
          "request": {
            "url": "{{default}}/api/2/user/columns?accountId=%7B%7D",
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
            "description": "Sets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed, the calling user's default columns are set. If no column details are sent, then all default columns are removed. The parameters for this resource are expressed as HTML form data. For example, in curl: `curl -X PUT -d username= -d columns=summary -d columns=description ` **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).\n*   To set the calling user's columns: None"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f07adab5-d64f-4e34-b903-41f4b6ee5efa"
            }
          ]
        },
        {
          "id": "351df9bb-4a4d-4132-9c95-cf353d648b1d",
          "name": "com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.setUserProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/user/properties/:propertyKey"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "userKey",
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
                  "id": "propertyKey",
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
            "description": "Sets the value of a user's property. Use this resource to store custom data against a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   To set a property on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).\n*   To set a property on the calling user's record: None\n\nNote: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "836375a1-8b74-4669-967e-c0641a918620"
            }
          ]
        },
        {
          "id": "ca48ae51-09ed-4479-9e97-53f44566b3cb",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.setWorkflowSchemeDraftIssueTy",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/issuetype/:issueType"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "issueType",
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
            "description": "Set the issue type mapping for the passed draft scheme.\n\nThe passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme cannot be edited."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "37e494b5-6882-4b53-8482-7f7506497f72"
            }
          ]
        },
        {
          "id": "a953c5c8-71cd-414e-8b31-51a826f7ffb3",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.setWorkflowSchemeIssueType_pu",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/issuetype/:issueType"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "issueType",
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
            "description": "Set the issue type mapping for the passed scheme.\n\nThe passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme cannot be edited."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d1757304-bbd4-4211-b34f-0e084d6f06db"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "02d7e6a4-4b8a-4196-8d0b-00c6dcdc771e",
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
              "id": "5c63d41c-58aa-4446-8f50-3f0c61fcfe4f"
            }
          ]
        },
        {
          "id": "ba8c5e88-6077-4b12-9ea6-983165f9ba40",
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
              "id": "a353cd33-55e0-4217-b4ca-d071b47a390f"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "46329717-a33a-4f96-ba6b-413aebc781b6",
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
              "id": "2110d04f-9742-4ae1-94e4-1b77280d0c12"
            }
          ]
        },
        {
          "id": "1f78e632-b062-49ce-8677-d51e2052c629",
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
              "id": "ca66c98e-b41d-49e2-8649-1d2c898efeaa"
            }
          ]
        },
        {
          "id": "6c3c0819-ab48-4058-948d-6e56bba9dbf3",
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
              "id": "7382fc36-7322-417a-8f8c-981d056657f0"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadataan",
      "item": [
        {
          "id": "9166b80a-b654-4b0b-bf0a-7f740993b60d",
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
              "id": "e186ec17-76ce-4d8b-a482-dd7f45c8b415"
            }
          ]
        }
      ]
    },
    {
      "name": "Contents",
      "item": [
        {
          "id": "12be2c8a-3485-432f-953f-a00082ec8c46",
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
              "id": "2c369319-9286-407f-8178-9806e60fe53b"
            }
          ]
        }
      ]
    },
    {
      "name": "Audit",
      "item": [
        {
          "id": "44b5c7fc-a5aa-49df-9ab4-33705411eb01",
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
              "id": "e07e3b57-64c4-47ce-a8d2-f9b411f5e1b8"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "576fffb6-b1b7-438f-aa5c-898a353c68b4",
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
              "id": "fd3d3df4-8d9c-47ef-b20c-704199e48670"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "d40916fd-cfd6-4dd6-9b03-fa1330b92631",
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
              "id": "00ee87db-ea00-4a61-915f-6dc723dbe039"
            }
          ]
        },
        {
          "id": "97fc382c-3934-4949-9dd0-a058d0dc60d7",
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
              "id": "9f77e3fe-0e54-468e-ba71-d22fe396cf0d"
            }
          ]
        }
      ]
    },
    {
      "name": "Comment",
      "item": [
        {
          "id": "c06e8b56-eaa1-483d-b65e-ace9bf673a3d",
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
              "id": "da626101-1d9c-442a-ae80-2d8e8e8ab502"
            }
          ]
        },
        {
          "id": "f13a87e5-7c28-4352-9c28-7cfdedb28fbd",
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
              "id": "b6604344-de1c-412e-92ab-4da6c2e15257"
            }
          ]
        },
        {
          "id": "b35b9114-c648-4524-b5be-d66610d9f5f8",
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
              "id": "a22b5b21-be05-43d3-b02c-e87b5579a0be"
            }
          ]
        },
        {
          "id": "24242f2f-8e45-4bcb-a037-51c270296d7b",
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
              "id": "4632eb15-577c-4476-8a57-0273d5dde95a"
            }
          ]
        },
        {
          "id": "94b67d6a-d79f-47a4-ae7c-2c4ed8bf5624",
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
              "id": "7f9e6b74-74b0-40a1-9750-9be21e779e2d"
            }
          ]
        },
        {
          "id": "809beaff-4686-4f63-bc46-972643b7762a",
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
              "id": "d6c7220a-8b73-4914-a677-c4c82833ffa7"
            }
          ]
        },
        {
          "id": "f6103130-bf10-41f9-a3f9-fc82de06e457",
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
              "id": "a3259061-cc98-4af7-94e9-57f724efb63c"
            }
          ]
        }
      ]
    },
    {
      "name": "Component",
      "item": [
        {
          "id": "450d7d71-c70c-4a30-b583-f6934375423c",
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
              "id": "b1eaad43-6559-4289-944a-b81fb69bf9f2"
            }
          ]
        },
        {
          "id": "0abfc90a-f267-4f1b-a165-3c077a024d2e",
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
              "id": "5df3b68b-7d2d-4e06-a395-b56cccb71ad8"
            }
          ]
        },
        {
          "id": "5661ce46-0c32-4187-8d9d-c7426db76a37",
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
              "id": "56621569-757e-4757-858e-271c338526d0"
            }
          ]
        },
        {
          "id": "b69340a6-70dd-4f36-8d08-766585c78aeb",
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
              "id": "54a8874d-fef6-4417-982a-f8346475f1f9"
            }
          ]
        },
        {
          "id": "f9e3cf5d-3cbd-4e0d-a42c-2f805740e36e",
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
              "id": "91342b79-9eee-4804-bf05-94ba885315b7"
            }
          ]
        }
      ]
    },
    {
      "name": "Selected",
      "item": [
        {
          "id": "2019dd0c-8826-447e-bb63-0aca6f8306cd",
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
              "id": "8ea0ce54-5624-4be5-9978-df7b52cdab5b"
            }
          ]
        }
      ]
    },
    {
      "name": "Select",
      "item": [
        {
          "id": "2a90129f-afc8-4b44-9342-e0e4abd99e75",
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
              "id": "b6b7a052-cc79-4786-b0a7-967b0982a482"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "4fca3d9c-23f5-429e-b431-2a289720ec08",
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
              "id": "6f3bb054-a17a-4041-8773-ea11660f2322"
            }
          ]
        }
      ]
    },
    {
      "name": "Time",
      "item": [
        {
          "id": "b1552e47-77b9-438b-ace4-ba1d877c454e",
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
              "id": "1a108e11-fb03-4b15-9ff0-e3450e3aba2b"
            }
          ]
        },
        {
          "id": "9a6b2b58-9eb8-42da-82bf-8abceafa8b28",
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
              "id": "6cb41d1b-6449-492a-a379-62cf9c111164"
            }
          ]
        }
      ]
    },
    {
      "name": "Custom",
      "item": [
        {
          "id": "b85e10de-9bb9-4845-92df-1b18e31e79ae",
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
              "id": "c0565694-50f3-44a4-9414-e824e486a38c"
            }
          ]
        },
        {
          "id": "1f0b2db8-b13b-4e75-a352-fb36aec971a3",
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
              "id": "d8ecc5d3-1aaf-4570-b3a3-5679589fb1c3"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboards",
      "item": [
        {
          "id": "64e2579c-b3f3-4f67-b892-27015abfdcf0",
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
              "id": "661a95e3-2b27-4fdf-8f40-478d1b6bc012"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboard",
      "item": [
        {
          "id": "8ec4da8a-a5a1-42c7-80cc-789f26e25615",
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
              "id": "44c3321a-49be-4df1-a6b6-1de49314a396"
            }
          ]
        },
        {
          "id": "90b8707b-b318-4d48-86e4-5a0ee5917c3c",
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
              "id": "418f77e2-523b-427d-bee6-7cb0227a69e4"
            }
          ]
        },
        {
          "id": "1383d890-d17f-4ed5-8663-3bbc99ca3d8b",
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
              "id": "f5977c74-a950-4195-9e20-2bde139b0db7"
            }
          ]
        },
        {
          "id": "c83df62a-4de8-4426-ae07-8d4ce378586f",
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
              "id": "8c94fcb8-b051-4495-9133-ab07621625d7"
            }
          ]
        }
      ]
    },
    {
      "name": "Evaluate",
      "item": [
        {
          "id": "fc9f4bea-a031-42db-9bb1-5db0a26d0815",
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
              "id": "21d3c4cd-6a07-4539-83be-96a6bf8f79d6"
            }
          ]
        }
      ]
    },
    {
      "name": "Fields",
      "item": [
        {
          "id": "c609002b-9774-48ee-b2b3-1c70daafa665",
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
              "id": "73887419-7cfb-4f09-99f7-c4d1f58cf145"
            }
          ]
        }
      ]
    },
    {
      "name": "Issue",
      "item": [
        {
          "id": "b6ceed33-4777-4af4-b5d0-5538e2d65cc2",
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
              "id": "a9f7cb52-465f-4fdc-bf5c-8db69469d17f"
            }
          ]
        },
        {
          "id": "d63a9ffe-7986-4b39-91cd-f3ad217d9070",
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
              "id": "ba87ad9a-b541-4bda-bf49-5f13ac6862eb"
            }
          ]
        },
        {
          "id": "615334e9-14e6-4edb-8ee7-3cb18b74ee1e",
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
              "id": "ff61830c-c9a6-4c1e-b450-ecb908c7b751"
            }
          ]
        },
        {
          "id": "26428572-e25d-4fee-912d-8bac683a813d",
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
              "id": "5a2009c8-c6ec-4cdf-ae4e-59c6c97a823d"
            }
          ]
        },
        {
          "id": "cfa5ae2c-4919-4921-89e3-b9d9a9e794af",
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
              "id": "44f00a3c-2eb0-455e-89b7-4b055e504909"
            }
          ]
        },
        {
          "id": "94533199-5e81-4f60-b159-03bd19f8a74b",
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
              "id": "430dc5df-c78f-41d2-8220-d1ee1d43761a"
            }
          ]
        },
        {
          "id": "8a474d4e-8c78-436e-83cf-16a78b1e2af2",
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
              "id": "afeecc9f-194b-4344-b23e-fcb8715316ec"
            }
          ]
        },
        {
          "id": "fc2def33-44dc-47e8-ba4c-01821a8b64e4",
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
              "id": "49a78fb5-3d01-4ef0-a625-2421a97495d6"
            }
          ]
        },
        {
          "id": "b292ecd7-f3e5-4095-9a66-72a98099f5c2",
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
              "id": "8dfbc9b3-7c51-4322-bb64-0ef44193b450"
            }
          ]
        },
        {
          "id": "baa2d5b0-e6cc-4481-8854-de4e564b66ef",
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
              "id": "656baff3-93f7-4860-ba71-df2c98cf0e8e"
            }
          ]
        },
        {
          "id": "175d9efa-4d8f-4573-96bc-01d08b92ab2a",
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
              "id": "e21aa980-64b8-4d6f-a636-674a16f92f56"
            }
          ]
        },
        {
          "id": "04f205bf-2bff-465b-8554-83a2b81daae4",
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
              "id": "160abe58-84fd-4e6e-a9bf-8d21c9bd474e"
            }
          ]
        },
        {
          "id": "33eb10fe-aba3-4a6c-b513-0937ad90ba28",
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
              "id": "c0849b3a-28eb-4a65-a3d3-1bc5a0b3b80c"
            }
          ]
        },
        {
          "id": "8babd8e2-e705-44df-a484-2ee7ac8d5116",
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
              "id": "54ed797b-3c32-4fc2-8ed9-2fbc0658a2fb"
            }
          ]
        },
        {
          "id": "be7cf2c4-5468-4a0f-a564-7dbb40d9849a",
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
              "id": "e2095ca6-051b-47ce-b2d7-14500355b413"
            }
          ]
        },
        {
          "id": "11484a14-1ed6-4184-a4ee-7cc0f20abfe5",
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
              "id": "f2cea73a-8a8d-4130-91d0-f6ba4aa507a6"
            }
          ]
        },
        {
          "id": "30d3016d-3fa7-4827-9bbb-aa8a11ada131",
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
              "id": "8f51bc3f-9ac6-405a-8987-76d2f9e5385f"
            }
          ]
        },
        {
          "id": "d665e622-97f7-44d1-b8c0-aeff82879664",
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
              "id": "75115493-71cf-428b-a901-7c13636339eb"
            }
          ]
        },
        {
          "id": "3af8a9c8-a8f4-48f7-a687-a4ef8c4803c9",
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
              "id": "e7354604-5c2c-4020-a1e7-ccdd521efb88"
            }
          ]
        },
        {
          "id": "067c6e4e-16a9-4d7a-bb92-2c37975399fb",
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
              "id": "732fd61f-37a0-48bf-ae7d-f17e519aea9b"
            }
          ]
        },
        {
          "id": "7c9f6a4b-79ff-40cc-aeef-307ce0d2cc71",
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
              "id": "7461327d-8856-42b2-81a6-50c6dc721090"
            }
          ]
        },
        {
          "id": "720db3e2-a2e2-4529-bad2-4de58690d56a",
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
              "id": "fece7b24-9709-4500-adf0-8f8837764819"
            }
          ]
        },
        {
          "id": "4980262c-a02e-4ba6-8f92-66dfd8cf3aa9",
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
              "id": "8ed26139-1081-44fd-b76d-5e9bde859766"
            }
          ]
        },
        {
          "id": "3f613782-fd33-452a-8bb6-4ef2e66c7c5d",
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
              "id": "916146e3-d74d-40e1-9004-40431b2c4b9f"
            }
          ]
        },
        {
          "id": "5e905f95-41e9-4cdf-89f8-0e114f6df110",
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
              "id": "82a08272-93fe-44d8-bf92-78284ee4647f"
            }
          ]
        },
        {
          "id": "6026299a-4865-47ae-a0fc-b89768877a15",
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
              "id": "de4f2bcc-a627-46d1-b884-488d10f08afc"
            }
          ]
        },
        {
          "id": "ebe4e4ef-d19b-42e8-a31d-775200f305cb",
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
              "id": "4fb9e325-535e-43b9-b5ed-651861350d57"
            }
          ]
        },
        {
          "id": "1cd078da-c543-459c-b8f9-a8f6a856e5a3",
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
              "id": "1fb3452b-7a40-4e50-b26f-351950f6255d"
            }
          ]
        },
        {
          "id": "eeb8c507-5fe6-4b33-a2f7-341e8f8837f4",
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
              "id": "486cd7ff-5665-4401-a3ff-8c4f4d0166a2"
            }
          ]
        },
        {
          "id": "be479094-e185-4ded-93b0-22c64c2e6e50",
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
              "id": "85c88bff-f78a-4c91-bd9c-afaf8bb7aa4a"
            }
          ]
        },
        {
          "id": "89fdb298-f163-4ea7-ab29-06811154e6eb",
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
              "id": "77440265-08b3-432b-8fbc-31c72c134ac9"
            }
          ]
        },
        {
          "id": "9718878a-34da-4cfe-aacf-05aacf54ee65",
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
              "id": "a036bb8b-7b30-4141-9a9d-9c8e854c6658"
            }
          ]
        },
        {
          "id": "bc5c4cd8-8005-4b06-9248-4a13fa66bbce",
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
              "id": "83e90eed-2ae5-48fc-bf19-157b3b899cbb"
            }
          ]
        },
        {
          "id": "34193528-c16c-40d1-b64d-4f3943b228a4",
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
              "id": "bb61a7b5-489b-421a-81db-775eccabb7b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Selectable",
      "item": [
        {
          "id": "1cdb77a6-8206-4ae4-b63c-25c399a60332",
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
              "id": "d265f2c4-cb15-4a94-947e-873425d1e142"
            }
          ]
        }
      ]
    },
    {
      "name": "Visible",
      "item": [
        {
          "id": "d795d375-c092-4fb2-8d4e-815d9fb8284b",
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
              "id": "f9c16cc6-85c7-49b2-bb48-d52d5101d934"
            }
          ]
        }
      ]
    },
    {
      "name": "Replace",
      "item": [
        {
          "id": "17e6574e-8000-460f-8132-8bdf668115ee",
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
              "id": "7ed752dc-6b66-490f-9315-b8b4eaa0e29f"
            }
          ]
        },
        {
          "id": "10f72012-c874-4601-b4eb-398b3792b25b",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.deleteAndReplaceVersion_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id/removeAndSwap"
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
            "description": "Deletes a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg). Alternative versions can be provided to update issues that use the deleted version in `fixVersion`, `affectedVersion`, or any version picker custom fields. If alternatives are not provided, occurrences of `fixVersion`, `affectedVersion`, and any version picker custom field, that contain the deleted version, are cleared. Any replacement version must be in the same project as the version being deleted and cannot be the version being deleted."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "22112547-af8c-476d-9c72-1e3a8074ea3f"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "05cccdde-6421-414e-b4ed-8a0756f4daff",
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
              "id": "2ab73bfb-c0eb-4718-bc89-76d995d6273d"
            }
          ]
        }
      ]
    },
    {
      "name": "Filter",
      "item": [
        {
          "id": "670d7821-843e-4882-9dc0-dea2ed01bc72",
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
              "id": "22ea8aa5-489a-4459-bfa6-b3185231717c"
            }
          ]
        },
        {
          "id": "fa285611-8bb9-4335-a830-268031f62829",
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
              "id": "c826e8ec-4fa8-489d-80fc-998a62ecc46f"
            }
          ]
        },
        {
          "id": "05eabd95-6988-4ef2-9ac0-f9cccbcc6af6",
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
              "id": "50fb459c-3a0c-41c6-8d11-8e5ed599f924"
            }
          ]
        },
        {
          "id": "f6e53563-0e68-4e35-90e9-530751217087",
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
              "id": "d8a30497-4852-408a-aba6-67596c79a6a6"
            }
          ]
        },
        {
          "id": "8310e3e0-4a23-4b2d-808d-d1885a459e21",
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
              "id": "d17c857c-f677-4d36-a0c9-309ea8f6ea26"
            }
          ]
        }
      ]
    },
    {
      "name": "Default",
      "item": [
        {
          "id": "1085afaf-9e7d-46bd-ad9e-0eef40b3bd83",
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
              "id": "ab484c03-ebe9-4b94-a101-6b33bbf43099"
            }
          ]
        },
        {
          "id": "c7ff462a-6483-4e4c-9148-61726c36dad3",
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
              "id": "5cdaec59-d9a2-4d41-acd9-bf13ca6b7a2f"
            }
          ]
        },
        {
          "id": "7732a397-5c7a-4f15-8982-d99a531ee468",
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
              "id": "fbafe87c-26a2-444d-83f7-d620c3aea54d"
            }
          ]
        },
        {
          "id": "5877e368-85d0-4c4c-97f2-29143ce294c1",
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
              "id": "1e36cfb3-835c-4263-9018-eff15370be97"
            }
          ]
        },
        {
          "id": "d255623e-ddc8-4484-97b2-9b40efacd2c3",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getDefaultWorkflow_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/default"
              ],
              "query": [
                {
                  "key": "returnDraftIfExists",
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
            "description": "Return the default workflow from the passed workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "89983001-d9fd-4ba2-b8b8-5bf16077d946"
            }
          ]
        },
        {
          "id": "375d7506-2237-4d1c-87f8-b1eb0a0b86f0",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateDefaultWorkflow_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/default"
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
            "description": "Set the default workflow for the passed workflow scheme.\n\nThe passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created/updated when the actual scheme cannot be edited."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6ffde9db-f946-4ab7-a45c-99e55ee7e9a1"
            }
          ]
        },
        {
          "id": "be9911c7-ab60-4694-ab15-92072c92699f",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.deleteDefaultWorkflow_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/default"
              ],
              "query": [
                {
                  "key": "updateDraftIfNeeded",
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
            "description": "Remove the default workflow from the passed workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "986c2be5-c1f7-48d4-9f97-f93b06e6ca29"
            }
          ]
        }
      ]
    },
    {
      "name": "Favourite",
      "item": [
        {
          "id": "7421c23a-9c05-4ec5-af97-5ecdf8d4e5b7",
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
              "id": "87be28c8-cfad-4677-83cd-5eb30207ad8c"
            }
          ]
        }
      ]
    },
    {
      "name": "My",
      "item": [
        {
          "id": "2d70c1cd-918b-42be-a78e-49a23b4e78b1",
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
              "id": "0fb46930-dc49-4b61-8205-587887c177f0"
            }
          ]
        },
        {
          "id": "862a645f-be84-42f2-ad92-d56ef1fa161b",
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
              "id": "a1249570-ae2b-4f1d-9c99-2138e85de5a3"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchfilters",
      "item": [
        {
          "id": "4bb72a92-e826-4b2f-8e35-c84fd5be98cc",
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
              "id": "4a766f85-75d2-4cc4-8ad7-a6990d17ee38"
            }
          ]
        }
      ]
    },
    {
      "name": "Columns",
      "item": [
        {
          "id": "e7ca0f8e-3f4a-4527-9cd8-1235737a6ecf",
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
              "id": "6bba3bb3-e580-4185-8fa6-5082ce91a605"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "53e5c8cd-1f49-4171-b160-adb7afdb8089",
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
              "id": "a32e8aef-a406-48c8-af14-8edb9bcb0be5"
            }
          ]
        },
        {
          "id": "f3f7e858-f466-4bfa-911d-4f8b6624f065",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.resetUserColumns_delete",
          "request": {
            "url": "{{default}}/api/2/user/columns?accountId=%7B%7D&username=%7B%7D",
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
            "description": "Resets the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user to the system default. If a username is not passed, the calling user's default columns are reset. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   To set the columns on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).\n*   To set the calling user's columns: None"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8a51e528-33b0-470a-a8e1-39dd9a0d1a08"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "a9186ed3-9108-4b72-baab-6369f77b5211",
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
              "id": "549f28dd-7c39-4abe-ad98-66b288b89b29"
            }
          ]
        },
        {
          "id": "ba626594-4318-408f-83b4-ba027a5b210c",
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
              "id": "d7aefdfe-fdaa-4388-9f34-3ba610093fdf"
            }
          ]
        },
        {
          "id": "471019cd-ae5f-47c6-aa19-d990699aedf2",
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
              "id": "3a612693-03c6-4340-9400-5d627da99f78"
            }
          ]
        },
        {
          "id": "a7646870-effa-45fa-9ee4-b7dc879a76ce",
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
              "id": "8c99a3b5-8e3a-441d-a823-48758430ecb5"
            }
          ]
        },
        {
          "id": "f9c6ca05-fe2e-453a-9ce6-923f12b01367",
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
              "id": "ea052eec-b98a-492f-a7c1-53633b975643"
            }
          ]
        },
        {
          "id": "d0f74fd1-fe5f-49a0-bf9b-bf40cfefc2a0",
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
              "id": "7ed3b113-ce24-444c-a262-4e22560460f5"
            }
          ]
        },
        {
          "id": "c9c2bcc3-78ee-46be-b89c-e04438c89260",
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
              "id": "681de3b3-025a-4ecf-8096-c09e7e7e1dc4"
            }
          ]
        },
        {
          "id": "2c4d07fd-7833-4e17-b54a-fe28b6a5ef25",
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
              "id": "3b167002-4995-4c25-8e48-c19d787b30f5"
            }
          ]
        }
      ]
    },
    {
      "name": "Share",
      "item": [
        {
          "id": "c4ae61a3-e276-4ba0-bc2a-3e67253127f1",
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
              "id": "c28fa4eb-496a-4e40-8df9-4744eab602bf"
            }
          ]
        },
        {
          "id": "1bb674ea-4ea9-4a3c-98b4-f258aad17aec",
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
              "id": "97cbe7c6-4a92-43c7-bc30-06403e8ac469"
            }
          ]
        },
        {
          "id": "e2a0172b-b190-434d-8359-10940fa26bdd",
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
              "id": "3907492f-7c10-434e-97e8-b78badb5a6d0"
            }
          ]
        },
        {
          "id": "7c05c59d-96bf-447a-9959-4ef22091a008",
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
              "id": "13ec3089-1744-4913-b281-47bfee60f440"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "fd56ab68-fbc6-4606-9f52-cfdbc9eff0e4",
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
              "id": "6a3f8647-76d5-434d-9440-d5f87b4045da"
            }
          ]
        },
        {
          "id": "7a330b2f-cdb1-4f7c-b0c7-98869120a6b6",
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
              "id": "5d5f6910-d277-4c8b-acd4-deb988d3c4ab"
            }
          ]
        }
      ]
    },
    {
      "name": "Users",
      "item": [
        {
          "id": "c67df592-a315-4c8a-a43d-3893b1d3f667",
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
              "id": "0c34192a-f337-4874-8855-800360f7720d"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "bef0b515-3be0-4a15-8682-ac2c98472671",
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
              "id": "48c91ee9-e437-4c32-8701-56411489ef68"
            }
          ]
        },
        {
          "id": "2344d954-9f13-4953-b288-fdfc777fafd5",
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
              "id": "d5179d75-6b30-4a6b-873c-61590e9085a1"
            }
          ]
        },
        {
          "id": "d91c1cd2-c317-4547-a79a-9fa1dce22e30",
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
              "id": "35a01d56-8beb-4904-9787-99b2bfb9b40c"
            }
          ]
        },
        {
          "id": "3a187ce0-a2a3-4d20-a1f6-a7bd4e1d54b2",
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
              "id": "98448123-92e1-4b0b-992f-7e7ec99a0b96"
            }
          ]
        },
        {
          "id": "1bbc22ce-0698-4a1f-ad6a-aa8f8e81fcf5",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.getUserDefaultColumns_get",
          "request": {
            "url": "{{default}}/api/2/user/columns?accountId=%7B%7D&username=%7B%7D",
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
            "description": "Returns the default [issue table columns](https://confluence.atlassian.com/x/XYdKLg) for the user. If a username is not passed in the request, the calling user's details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   To get the column details for any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLgl).\n*   To get the calling user's column details: None"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f20ce4a8-aaa5-4f66-9e2b-35a04a333686"
            }
          ]
        },
        {
          "id": "7a8a451f-4078-4cd5-a47b-f457c2b0974b",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.getUserGroups_get",
          "request": {
            "url": "{{default}}/api/2/user/groups?accountId=%7B%7D&key=%7B%7D&username=%7B%7D",
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
            "description": "Returns the groups to which a user belongs. **[Permissions required](https://confluence.atlassian.com/x/FQiiLQ):** _Browse users and groups_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7253f7a7-2e40-49ce-990e-0c6b6a12e325"
            }
          ]
        },
        {
          "id": "4a6cf5d8-65d4-4a12-b57a-4cddb8f4ffef",
          "name": "com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.getUserPropertyKeys_get",
          "request": {
            "url": "{{default}}/api/2/user/properties?accountId=%7B%7D&userKey=%7B%7D&username=%7B%7D",
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
            "description": "Returns all property keys on a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   To access the property keys on any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).\n*   To access the calling user's property keys: None\n\nNote: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8034bc3e-31cd-464a-9998-b92560c4938b"
            }
          ]
        },
        {
          "id": "60f73445-3e9d-4a51-ae58-130b96e75eac",
          "name": "com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.getUserProperty_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/user/properties/:propertyKey"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "userKey",
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
                  "id": "propertyKey",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "Returns the value of a user's property. If no property key is provided [Get user property keys](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-user-properties-get) is called. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   To get a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).\n*   To get a property from the calling user's record: None\n\nNote: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d5ed492-68b7-4462-b813-8bb872f0eecd"
            }
          ]
        },
        {
          "id": "64f57590-d160-4272-b4a9-4143dc7a4c8e",
          "name": "com.atlassian.jira.rest.v2.userproperty.UserPropertyResource.deleteUserProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/user/properties/:propertyKey"
              ],
              "query": [
                {
                  "key": "accountId",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "userKey",
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
                  "id": "propertyKey",
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
            "description": "Deletes a property from a user. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   To delete a property from any user: _Administer Jira_ [global permission](https://confluence.atlassian.com/adminjiracloud/managing-global-permissions-776636359.html).\n*   To delete a property from the calling user's record: None\n\nNote: These user properties are unrelated to the [Jira properties](https://confluence.atlassian.com/cloud/add-data-to-users-for-advanced-functions-jira-applications-only-744721649.html) that can be set through the UI."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "da3d477c-150a-4d34-a452-0ecd0f0adfcc"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "da15df65-8c5f-45ba-a3d8-f848505d2c70",
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
              "id": "aa4388a7-5879-4f62-8bb2-f20868d296df"
            }
          ]
        },
        {
          "id": "41b52fe2-f652-49bc-8efc-e501936b444b",
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
              "id": "de5de3a6-907e-447a-90ae-bfec115cc7a2"
            }
          ]
        },
        {
          "id": "e5f1256b-26f5-4338-bdda-e8ae317a90b1",
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
              "id": "c80eb7c1-5341-4ea1-83b0-e5cee93fd5fd"
            }
          ]
        },
        {
          "id": "4f6c2539-ef15-4e64-9bf8-d70040045014",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.findAssignableUsers_get",
          "request": {
            "url": "{{default}}/api/2/user/assignable/search?actionDescriptorId=%7B%7D&issueKey=%7B%7D&maxResults=%7B%7D&project=%7B%7D&query=%7B%7D&startAt=%7B%7D&username=%7B%7D",
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
            "description": "Returns a list of users that can be assigned to an issue. Use this method to find the list of users who can be assigned to:\n\n*   a new issue, by providing the `projectKeyOrId`.\n*   an updated issue, by providing the `issueKey`.\n*   to an issue during a transition (workflow action), by providing the `issueKey` and the transition id in `actionDescriptorId`. You can obtain the IDs of an issue's valid transitions using the `transitions` option in the `expand` parameter of [Get issue](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-issue-issueIdOrKey-get).\n\nIn all these cases, you can pass a username to determine if a user can be assigned to an issue. The user is returned in the response if they can be assigned to the issue or issue transition. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** Permission to access Jira."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8f7ce91f-b0f4-4882-9900-83621d300333"
            }
          ]
        },
        {
          "id": "2b3eab1e-ce1f-45e4-ac7e-b82078472e88",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.findUsersWithAllPermissions_get",
          "request": {
            "url": "{{default}}/api/2/user/permission/search?issueKey=%7B%7D&maxResults=%7B%7D&permissions=%7B%7D&projectKey=%7B%7D&query=%7B%7D&startAt=%7B%7D&username=%7B%7D",
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
            "description": "Returns a list of users who fulfill both of these criteria:\n\n*   their user attributes match a search string.\n*   they have a set of permissions for a project or issue.\n\nIf no search string is provided, a list of all users with the permissions is returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:**\n\n*   Get users for any project, _Administer Jira_ [global permission](href=).\n*   Get users for a project, _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg) for the project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e06d5adb-458c-4525-8c35-65dca8c65fa4"
            }
          ]
        },
        {
          "id": "8a89e258-6992-41f5-bff1-364eecc8f8b6",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.findUsersForPicker_get",
          "request": {
            "url": "{{default}}/api/2/user/picker?exclude=%7B%7D&excludeAccountIds=%7B%7D&maxResults=%7B%7D&query=%7B%7D&showAvatar=%7B%7D",
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
            "description": "Returns a list of users whose attributes match the query term. The returned object includes the `html` field where the matched query term is highlighted with the HTML strong tag. A list of usernames can be provided to exclude users from the results. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but will only get search results for an exact name match."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6808076a-d1a0-4e01-9cf1-b3a4c779b89a"
            }
          ]
        },
        {
          "id": "8f692c7a-f8fc-4441-9d1f-60f8242bee5f",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.findUsers_get",
          "request": {
            "url": "{{default}}/api/2/user/search?includeActive=%7B%7D&includeInactive=%7B%7D&maxResults=%7B%7D&property=%7B%7D&query=%7B%7D&startAt=%7B%7D&username=%7B%7D",
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
            "description": "Returns a list of users that match the search string and property. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "16bfc411-0ca6-4ccd-9b4e-ddd36030ee67"
            }
          ]
        },
        {
          "id": "a8fd628e-da4b-4ea9-a440-19cbc9a44ab0",
          "name": "com.atlassian.jira.rest.v2.search.UserSearchResource.findUsersByQuery_get",
          "request": {
            "url": "{{default}}/api/2/user/search/query?includeInactive=%7B%7D&maxResults=%7B%7D&query=%7B%7D&startAt=%7B%7D",
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
            "description": "Finds users using a structured query and returns user details. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). The available queries statements are:\n\n`is assignee of PROJ` Returns the users that are assignees of at least one issue in project _PROJ_.*   `is assignee of (PROJ-1, PROJ-2)` Returns users that are assignees on the issues _PROJ-1_ or _PROJ-2_.\n*   `is reporter of (PROJ-1, PROJ-2)` Returns users that are reporters on the issues _PROJ-1_ or _PROJ-2_.\n*   `is watcher of (PROJ-1, PROJ-2)` Returns users that are watchers on the issues _PROJ-1_ or _PROJ-2_.\n*   `is voter of (PROJ-1, PROJ-2)` Returns users that are voters on the issues _PROJ-1_ or _PROJ-2_.\n*   `is commenter of (PROJ-1, PROJ-2)` Returns users that have posted a comment on the issues _PROJ-1_ or _PROJ-2_.\n*   `is transitioner of (PROJ-1, PROJ-2)` Returns users that have performed a transition on issues _PROJ-1_ or _PROJ-2_.\n*   `[propertyKey].entity.property.path is \"property value\"` Returns users with the entity property value.\n\nThe list of issues can be extended as needed, as in _(PROJ-1, PROJ-2, ... PROJ-n)_. Statements can be combined using the `AND` and `OR` operators to form more complex queries, for example:\n\n`is assignee of PROJ AND [propertyKey].entity.property.path is \"property value\"`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e7ec7769-8ec5-4a6d-9568-ef706d20aeec"
            }
          ]
        },
        {
          "id": "307824c9-2d89-47d4-bc38-b0f7899edaf9",
          "name": "com.atlassian.jira.rest.v2.search.UserSearchResource.findUserKeysByQuery_get",
          "request": {
            "url": "{{default}}/api/2/user/search/query/key?includeInactive=%7B%7D&maxResults=%7B%7D&query=%7B%7D&startAt=%7B%7D",
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
            "description": "Finds users using a structured query and returns a list of user keys. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). The available query statements are:\n\n*   `is assignee of PROJ` Returns the users that are assignees of at least one issue in project _PROJ_.\n*   `is assignee of (PROJ-1, PROJ-2)` Returns users that are assignees on the issues _PROJ-1_ or _PROJ-2_.\n*   `is reporter of (PROJ-1, PROJ-2)` Returns users that are reporters on the issues _PROJ-1_ or _PROJ-2_.\n*   `is watcher of (PROJ-1, PROJ-2)` Returns users that are watchers on the issues _PROJ-1_ or _PROJ-2_.\n*   `is voter of (PROJ-1, PROJ-2)` Returns users that are voters on the issues _PROJ-1_ or _PROJ-2_.\n*   `is commenter of (PROJ-1, PROJ-2)` Returns users that have posted a comment on the issues _PROJ-1_ or _PROJ-2_.\n*   `is transitioner of (PROJ-1, PROJ-2)` Returns users that have performed a transition on issues _PROJ-1_ or _PROJ-2_.\n*   `[propertyKey].entity.property.path is \"property value\"` Returns users with the entity property value.\n\nThe list of issues can be extended as needed, as in _(PROJ-1, PROJ-2, ... PROJ-n)_. Statements can be combined using the `AND` and `OR` operators to form more complex queries, for example:\n\n`is assignee of PROJ AND [propertyKey].entity.property.path is \"property value\"`"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56c38460-7f2b-4723-a0a9-a78d3922fd55"
            }
          ]
        },
        {
          "id": "21ed990c-6202-4929-8f1e-b6b6222d7fec",
          "name": "com.atlassian.jira.rest.v2.issue.UserResource.findUsersWithBrowsePermission_get",
          "request": {
            "url": "{{default}}/api/2/user/viewissue/search?issueKey=%7B%7D&maxResults=%7B%7D&projectKey=%7B%7D&query=%7B%7D&startAt=%7B%7D&username=%7B%7D",
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
            "description": "Returns a list of users who fulfill both of these criteria:\n\n*   their user attributes match a search string.\n*   they have permission to browse issues.\n\nUse this resource to find users who can browse:\n\n*   an issue, by providing the `issueKey`.\n*   any issue in a project, by providing the `projectKey`.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Browse users and groups_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "491708c2-3d6f-4280-87d1-96ffab464305"
            }
          ]
        }
      ]
    },
    {
      "name": "Issues",
      "item": [
        {
          "id": "0d5346fa-91ef-4fe5-a2a6-a51718023a88",
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
              "id": "98e61873-7d7a-4fa7-ac53-8090c2da59e8"
            }
          ]
        }
      ]
    },
    {
      "name": "Create",
      "item": [
        {
          "id": "3385772d-a874-4816-b555-f7df2be0e780",
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
              "id": "dd480738-b73b-4795-b341-34dd959a2e43"
            }
          ]
        }
      ]
    },
    {
      "name": "Bulk",
      "item": [
        {
          "id": "7fad5074-6885-4854-a08f-8952e4169ebd",
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
              "id": "d077848f-491c-4088-abfc-54a7fd32adfe"
            }
          ]
        },
        {
          "id": "6ca30625-4a3f-4969-b7ec-047ad2149303",
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
              "id": "e00bd2df-e7f5-41a8-bd55-516fbf87b13d"
            }
          ]
        },
        {
          "id": "fc3beb98-0822-4553-a3eb-e74f7b0c247d",
          "name": "com.atlassian.jira.rest.v2.user.UserBulkResource.bulkGetUsers_get",
          "request": {
            "url": "{{default}}/api/2/user/bulk?key=%7B%7D&maxResults=%7B%7D&startAt=%7B%7D&username=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns details of users specified in a list of usernames or keys. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](href=). Users with permission to access Jira can call this method, but empty search results are returned."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "db9f6eab-308c-4cfd-933a-a656c14a84b3"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "307c357d-9717-4d9b-9c3d-0904043ee537",
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
              "id": "2748e8f7-46d9-4bc6-b6c0-4f06a4cdf1c0"
            }
          ]
        },
        {
          "id": "fc945553-33d0-4a14-bbc8-a5ed22a9db7a",
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
              "id": "642d0eac-42b6-4cb8-ae4c-8db5bdb8f64a"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "96a6d8fe-90c2-403e-bcdb-790616365229",
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
              "id": "ab4cbbaa-f6ae-4092-ad12-81625ae56e5b"
            }
          ]
        },
        {
          "id": "da1d525e-279b-468a-83a2-0f50003cc382",
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
              "id": "c024a8bd-5db8-46a4-951a-a75d72f891b0"
            }
          ]
        }
      ]
    },
    {
      "name": "Change",
      "item": [
        {
          "id": "b0bc5d36-2154-4484-bf58-cdc9503ffd72",
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
              "id": "201f7466-f340-4015-b28a-00b96930ea36"
            }
          ]
        }
      ]
    },
    {
      "name": "Notify",
      "item": [
        {
          "id": "b2860825-b104-478a-ab6d-49134a5b740a",
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
              "id": "66da13d8-b947-43ce-947c-3a66c350980b"
            }
          ]
        }
      ]
    },
    {
      "name": "Remote",
      "item": [
        {
          "id": "ff8ad985-88f0-4d33-9dd6-8036f27cdeb1",
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
              "id": "0d91c76c-a526-4a9f-bcd0-eca567a94b57"
            }
          ]
        },
        {
          "id": "7cc74ad2-e39d-4d8b-9201-38e49e4045fc",
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
              "id": "7d411733-8055-4606-9615-3a3e8ce491bd"
            }
          ]
        },
        {
          "id": "c1414f7c-49b0-4da5-b536-6afd106d4e34",
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
              "id": "0a67724e-a050-47d7-9c10-4922d6e81e83"
            }
          ]
        },
        {
          "id": "a001f0cc-c1be-4f12-9965-562f34a711e2",
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
              "id": "6a37998a-3790-4569-8c61-a53871681c4e"
            }
          ]
        },
        {
          "id": "32895c3e-7863-47df-bb40-2dbb9e89849e",
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
              "id": "cb2e8aa1-ae03-4cb7-8a09-012707890c08"
            }
          ]
        },
        {
          "id": "a252c338-7d67-4514-81f1-2cb7a1722031",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.getRemoteVersionLinks_get",
          "request": {
            "url": "{{default}}/api/2/version/remotelink?globalId=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the remote version links for a given global ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3b3dba25-6c30-4496-9279-83c00a50f349"
            }
          ]
        },
        {
          "id": "23fc604f-7651-46f3-ae1c-b3ac5be3990f",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.getRemoteVersionLinksByVersionId_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:versionId/remotelink"
              ],
              "variable": [
                {
                  "id": "versionId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the remote version links associated with the given version ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60cbb58a-6a00-436a-a9f9-e5ac2f72cfc5"
            }
          ]
        },
        {
          "id": "3735c654-887d-40cb-9129-5d48abb10b12",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.deleteRemoteVersionLinksByVersionId_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:versionId/remotelink"
              ],
              "variable": [
                {
                  "id": "versionId",
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
            "description": "Delete all remote version links for a given version ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1fb2a77f-c086-4f26-96da-f9ba49a8b6d7"
            }
          ]
        },
        {
          "id": "4aa9af5a-2ce4-4cd0-aa29-3815d5adde39",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.getRemoteVersionLink_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:versionId/remotelink/:globalId"
              ],
              "variable": [
                {
                  "id": "globalId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "versionId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "A REST sub-resource representing a remote version link"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8f4879f-33aa-40c2-9e38-3d27308fab78"
            }
          ]
        },
        {
          "id": "3b1cf4fd-f876-4065-aa2a-73c1d69f6c8a",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.deleteRemoteVersionLink_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:versionId/remotelink/:globalId"
              ],
              "variable": [
                {
                  "id": "globalId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "versionId",
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
            "description": "Delete a specific remote version link with the given version ID and global ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1ec7f8ea-6c9f-4ebf-80ec-a688e8c65119"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "3c43922b-6c76-46b2-bda2-3e669b1f9e1e",
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
              "id": "2ab06505-5794-439e-80da-0684c8aef178"
            }
          ]
        },
        {
          "id": "45b0b0db-4eda-4f67-8b63-9e0231d47f8b",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.createOrUpdateRemoteVersionLink_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:versionId/remotelink"
              ],
              "variable": [
                {
                  "id": "versionId",
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
            "description": "Create a remote version link via POST. The link's global ID will be taken from the JSON payload if provided; otherwise, it will be generated."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06a30e29-1b6b-4f7a-ac93-d7f923535131"
            }
          ]
        },
        {
          "id": "6f72a4c9-0bb7-4dd9-b89a-3622f038a480",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.createOrUpdateRemoteVersionLinkWithGlobalId_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:versionId/remotelink/:globalId"
              ],
              "variable": [
                {
                  "id": "globalId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "versionId",
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
            "description": "Create a remote version link via POST using the provided global ID."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9b4625fd-2ab9-4c08-badf-b5ea8b51efec"
            }
          ]
        }
      ]
    },
    {
      "name": "Transitions",
      "item": [
        {
          "id": "bbf175bf-f1d3-4089-9f93-fa84a5c95398",
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
              "id": "2506572a-4263-4427-9416-7f851eeddf91"
            }
          ]
        }
      ]
    },
    {
      "name": "Do",
      "item": [
        {
          "id": "df603de4-17ee-4b92-9fc9-859389e84170",
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
              "id": "8a01bf60-e0ea-44b3-b303-364f2469dbbe"
            }
          ]
        }
      ]
    },
    {
      "name": "Votes",
      "item": [
        {
          "id": "396d7cbf-15dc-42f4-bfd0-dc0d9b84323b",
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
              "id": "192fa359-9c9e-47e1-9149-827f84f5d168"
            }
          ]
        }
      ]
    },
    {
      "name": "Vote",
      "item": [
        {
          "id": "f073c233-6e60-4417-9d25-86b7bb6f4d15",
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
              "id": "8e0ce5ae-8762-4474-81f9-ef856794c5c4"
            }
          ]
        }
      ]
    },
    {
      "name": "Watcher",
      "item": [
        {
          "id": "708ee241-6169-41fc-a9b6-5d8019ce36db",
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
              "id": "1e5de132-1935-454e-95d6-bc1079e9a87c"
            }
          ]
        }
      ]
    },
    {
      "name": "Worklog",
      "item": [
        {
          "id": "3a7271fd-5866-4365-9e87-f8d6ff6c2b39",
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
              "id": "30e66273-2595-4d96-a37b-f36d739550cd"
            }
          ]
        },
        {
          "id": "65c8178a-0814-4b3f-a8ca-f9a040d6c11e",
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
              "id": "83fee16b-74b3-4e31-82b0-31f44790051e"
            }
          ]
        },
        {
          "id": "93dc9f43-9771-49e6-b2df-b9d2662b07e5",
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
              "id": "ab1014d4-e713-4e41-b4c0-0db529011786"
            }
          ]
        },
        {
          "id": "0cf01423-5766-4870-a7f4-53c3c89ba6c9",
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
              "id": "d865f90f-095c-479a-b117-3f3d1dc31c4f"
            }
          ]
        },
        {
          "id": "7dc0175a-e7a8-4645-8f2e-eb8917c402dd",
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
              "id": "103aeac5-b965-4847-81de-a119c51cf971"
            }
          ]
        },
        {
          "id": "7976ef6a-188b-4b6f-b07f-0b1e7ad0f78b",
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
              "id": "4febed9c-0100-41ea-a0fa-0fecb88ef017"
            }
          ]
        },
        {
          "id": "509f8ccd-b732-4901-8542-c753af7adab9",
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
              "id": "31ec6060-e798-433f-b609-410a39960721"
            }
          ]
        }
      ]
    },
    {
      "name": "Link",
      "item": [
        {
          "id": "64852b28-4529-49e0-bac3-866736369723",
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
              "id": "3a4e6eac-9acf-4960-b591-24620c284da6"
            }
          ]
        }
      ]
    },
    {
      "name": "Alternative",
      "item": [
        {
          "id": "10c7f5a0-fdd1-411e-8d6f-ff7123dd9cb7",
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
              "id": "ff58045b-3f91-45e2-9f02-2cd8e0eb565b"
            }
          ]
        }
      ]
    },
    {
      "name": "Auto",
      "item": [
        {
          "id": "69b9377a-cb05-4f81-9a39-778e6f5c27d4",
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
              "id": "d717c920-b0be-411a-be3d-4f859a9c0b5e"
            }
          ]
        }
      ]
    },
    {
      "name": "Field",
      "item": [
        {
          "id": "20168e32-682a-40c0-8603-1a283c0d8f10",
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
              "id": "395d016e-8c6b-49a9-902f-cc3eaf72addf"
            }
          ]
        },
        {
          "id": "b14c8ae1-f1b6-4593-aa19-e996844aff39",
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
              "id": "8658d774-6237-4145-a125-98ee404961fc"
            }
          ]
        }
      ]
    },
    {
      "name": "Validate",
      "item": [
        {
          "id": "f75daa89-5730-4f4d-a2bc-10e00455ec9f",
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
              "id": "2bbf9d85-ab03-4112-a2e2-b533bff16386"
            }
          ]
        },
        {
          "id": "f68173de-dca5-4829-8569-1a4328431998",
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
              "id": "46f144ff-957e-4bf4-a44e-5e3abee05857"
            }
          ]
        }
      ]
    },
    {
      "name": "Preference",
      "item": [
        {
          "id": "865029ce-3c68-48db-9a65-ab56d901a76a",
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
              "id": "bf49cd99-6e15-4c5e-85f3-30bccfb17b9d"
            }
          ]
        }
      ]
    },
    {
      "name": "Locale",
      "item": [
        {
          "id": "0862c06a-0194-4e61-a750-c0a724ed041a",
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
              "id": "7c7dde38-fd01-4a50-8a07-4eacd0b7ceeb"
            }
          ]
        },
        {
          "id": "f25a6e97-7684-496c-b4a2-8bfab1cfba63",
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
              "id": "0912ada3-3be2-4cf2-bc42-6f90aeeb68ff"
            }
          ]
        }
      ]
    },
    {
      "name": "Current",
      "item": [
        {
          "id": "d677902f-33a6-4225-a73a-6398a8259b4f",
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
              "id": "65e40770-eddd-4242-a6b6-389cdb0bf94e"
            }
          ]
        }
      ]
    },
    {
      "name": "Notification",
      "item": [
        {
          "id": "078d5fa9-6cea-45c2-8fe6-5ef9184acf02",
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
              "id": "70cf5a3c-e2b0-4d67-8e42-846f6d200e2a"
            }
          ]
        },
        {
          "id": "8f5d0bdb-34d7-46a9-bbf0-9776ed7fbe10",
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
              "id": "486e0c22-efd5-42ad-b25b-0dc8bdfa7933"
            }
          ]
        }
      ]
    },
    {
      "name": "Permissions",
      "item": [
        {
          "id": "22e2d7e0-f6cd-4f9a-b85a-44b9f67ff07d",
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
              "id": "791bceae-0fac-48dd-8611-18ae7fc9978b"
            }
          ]
        }
      ]
    },
    {
      "name": "Permitted",
      "item": [
        {
          "id": "86306ce5-a12e-45be-a812-18bdd6f6ba6f",
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
              "id": "8a7dfda0-9d1a-463e-abab-a9d37d81f0e5"
            }
          ]
        }
      ]
    },
    {
      "name": "Permission",
      "item": [
        {
          "id": "c64f8cc9-a1fd-4303-8ea1-f4fa76f89b9c",
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
              "id": "c1c004e6-a470-4f8f-bbbd-a7131b236b20"
            }
          ]
        },
        {
          "id": "17b996ba-1611-4c6d-abe2-dba619dd3adc",
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
              "id": "988684b9-6a5f-478b-8c8f-e4728ed12452"
            }
          ]
        },
        {
          "id": "0f5b5ef1-183b-4e21-a541-ddb750e49abf",
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
              "id": "4cab6796-e5cc-48b0-89ae-1b5585040080"
            }
          ]
        },
        {
          "id": "85d2ca6b-0def-4551-b67e-920cd5acf468",
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
              "id": "6da64906-e676-4db5-b65b-07b24245296c"
            }
          ]
        },
        {
          "id": "fa4f7c8c-b0f8-4be8-bab4-92251badfa5d",
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
              "id": "1af9e811-b657-45ab-a498-527f442947ba"
            }
          ]
        },
        {
          "id": "1be055dd-71a3-4b80-9ac8-0dcd08f26959",
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
              "id": "afe13cbe-7a51-428d-8168-30262dfa74c7"
            }
          ]
        },
        {
          "id": "debee6d2-cd98-4bf5-8f85-e48cda06c186",
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
              "id": "f974496d-cfde-4a49-8783-200ea2d2ce42"
            }
          ]
        },
        {
          "id": "c37958a6-6c29-48df-801e-7736ef95d237",
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
              "id": "2729de67-22b2-4f9d-bb42-8bf0be9ea9d3"
            }
          ]
        },
        {
          "id": "452080fa-ef47-4d43-9b79-8206e70958f8",
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
              "id": "de9e762c-b46d-42b0-b390-6ed31a62b3f8"
            }
          ]
        }
      ]
    },
    {
      "name": "Priorities",
      "item": [
        {
          "id": "4215693a-e51f-4253-81d2-7676217c857a",
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
              "id": "b149589c-5161-40d7-a5dd-ac3b272ad2ca"
            }
          ]
        }
      ]
    },
    {
      "name": "Priority",
      "item": [
        {
          "id": "4d2dfd97-a236-4301-a2b1-43a477923eac",
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
              "id": "0d218acb-e42a-4f66-b84f-4628bd8c7675"
            }
          ]
        }
      ]
    },
    {
      "name": "Projects",
      "item": [
        {
          "id": "524e01d6-ff2c-4aeb-a740-754e858c3015",
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
              "id": "3d1d0b7d-d879-4c1c-bc9b-7c6ed26b8190"
            }
          ]
        }
      ]
    },
    {
      "name": "Project",
      "item": [
        {
          "id": "d0f30d0c-cd48-48cc-a729-2a06d2204f20",
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
              "id": "6ec1d018-1cf3-482c-8263-bab7ab96c766"
            }
          ]
        },
        {
          "id": "b91a3355-1e5f-4b80-9a0f-9ddf7a6e43c0",
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
              "id": "57e05d0f-3e08-4fb8-81e6-aa3953ee3433"
            }
          ]
        },
        {
          "id": "7bf1233c-529d-4bb0-b7b2-8a97e785c8c5",
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
              "id": "ffd9dbbe-be72-4839-a6f0-b765e0650081"
            }
          ]
        },
        {
          "id": "a8b92844-224e-4b3c-88ef-1624cbf58b9a",
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
              "id": "8ef8a22f-519d-40d0-be98-5765f12221f4"
            }
          ]
        },
        {
          "id": "8af49c05-bccf-4ebd-a1b9-95f177b8095f",
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
              "id": "62bf32b4-daca-4ebc-a8ca-ffe009ae3784"
            }
          ]
        },
        {
          "id": "726f595f-6c46-4d51-8368-494abfc25f06",
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
              "id": "d30d6438-19d6-4ba6-9cef-44c811a77bf3"
            }
          ]
        },
        {
          "id": "beb182b0-beb5-4b00-b31e-ce641e959800",
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
              "id": "6184a865-0250-464e-8f1a-ebd31abe0824"
            }
          ]
        },
        {
          "id": "ddd56396-2b41-4697-a4bb-0e37588d6877",
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
              "id": "8cec16a2-2c6a-4ed1-b97a-4af22e7b244f"
            }
          ]
        },
        {
          "id": "5d94ecb0-3f35-4ddc-852c-60c009063d2a",
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
              "id": "a294b842-6a9a-4c48-932a-ce8c7368bbc1"
            }
          ]
        },
        {
          "id": "a52a0bb0-496c-46ef-b9e5-9c0777265d4f",
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
              "id": "4915cfdb-e4d3-4949-9af0-5759538385b5"
            }
          ]
        },
        {
          "id": "92f9de7d-84bc-4499-aac3-971a755e2d29",
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
              "id": "33971d59-1c60-4615-8b04-6f715b30fa11"
            }
          ]
        },
        {
          "id": "2f86617f-4b5c-4dc9-b906-e0a78b8b9a67",
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
              "id": "077421ae-94cc-4854-84e2-624e6cdc6c33"
            }
          ]
        },
        {
          "id": "7b33c132-17cd-46f1-9820-12def750400d",
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
              "id": "b195db0e-d965-4b62-bc33-42b8a22490e2"
            }
          ]
        },
        {
          "id": "afdd697c-0afd-439d-8d41-0c3a72c0d0fe",
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
              "id": "c028a3b5-d7cb-4fcd-967e-c08acf0df877"
            }
          ]
        },
        {
          "id": "60324fb4-e3d6-45be-a12f-51a58b2bcf0e",
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
              "id": "55d39273-a8e8-4415-9fdb-e45d82ec95f8"
            }
          ]
        },
        {
          "id": "316549ed-f6c5-49ff-948a-158742db7757",
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
              "id": "55637672-dd20-41c1-b586-63363db3e922"
            }
          ]
        },
        {
          "id": "d56f14a4-24d4-4760-bf53-0da2ffede187",
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
              "id": "f41d2724-9b8c-417d-a1c6-c5843220f6c6"
            }
          ]
        },
        {
          "id": "59442d83-c42b-42c0-ae21-20e69574ba23",
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
              "id": "f9f11eef-c4fc-4188-beaf-fd99d137dc01"
            }
          ]
        },
        {
          "id": "ec3c49a0-0131-428f-a8b9-e10ab52045c5",
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
              "id": "ce6b5a48-9f36-448b-8971-a8ce6e16a0a5"
            }
          ]
        },
        {
          "id": "e527b755-a05f-447b-ae77-b381f6b626a8",
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
              "id": "edca4981-4da1-497e-92a2-f4d15a947457"
            }
          ]
        },
        {
          "id": "40d8732e-0875-453f-9fa1-518c6b0f241c",
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
              "id": "cd837cfb-d315-488b-9ff5-9b9d775506aa"
            }
          ]
        },
        {
          "id": "8aa5ab25-4b60-4d80-a132-1d550a6bfb4b",
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
              "id": "14a0ba3b-396d-4819-a7a3-3e50a84234f2"
            }
          ]
        },
        {
          "id": "c996768e-33f7-4eaf-b813-9aacd62281d6",
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
              "id": "fdd49344-e35c-4943-ab57-fe960e19e0da"
            }
          ]
        },
        {
          "id": "a7c26f93-b6f4-49b5-8859-0539e73f88ac",
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
              "id": "8c0e8fc5-271a-429f-81cf-3812259075c9"
            }
          ]
        },
        {
          "id": "34596a1b-9f93-4093-a86e-cdcd9bbca525",
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
              "id": "56f640ad-136f-4767-acd8-d108590caca1"
            }
          ]
        },
        {
          "id": "196d9712-89e4-4da6-ba60-c8aee4230dfa",
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
              "id": "1d9541a7-cb2f-4299-84a9-12c6b4c6776c"
            }
          ]
        },
        {
          "id": "c060f5dd-5ee4-4dfa-8f00-52d6f32a42e4",
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
              "id": "8fbd0ff0-72b2-4168-acc6-eb7522d50e32"
            }
          ]
        },
        {
          "id": "46f2a7c5-a280-40e6-a2a0-61dbd9304197",
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
              "id": "5656bce9-7296-4f2d-aa64-78ef85da3023"
            }
          ]
        },
        {
          "id": "4dbeef1a-6b15-4e11-9409-f24faea0b84c",
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
              "id": "b81f95f7-17c7-4b71-b8f5-d82a9dfd798f"
            }
          ]
        },
        {
          "id": "ec6f7d89-6626-41fa-8fd0-512d819b976a",
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
              "id": "f5c515d9-e58a-4b3e-b713-566bd30e67c8"
            }
          ]
        },
        {
          "id": "bfc99eba-38b7-4361-9f3a-c9555c99ec66",
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
              "id": "0388dbd2-1a9a-4714-ba30-172bd216b5b1"
            }
          ]
        },
        {
          "id": "98a7908c-80b8-4502-9b80-23032b144b03",
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
              "id": "a6a999f9-7a87-4c0f-80de-df9d9dd816c2"
            }
          ]
        }
      ]
    },
    {
      "name": "Search",
      "item": [
        {
          "id": "571c2309-20c6-4915-b36d-c868b06c6372",
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
              "id": "245f1733-24cf-4378-8941-cf1422eb6256"
            }
          ]
        }
      ]
    },
    {
      "name": "Accessible",
      "item": [
        {
          "id": "cd02cdea-0f05-498f-84ae-67a1f8ec8f02",
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
              "id": "13704fa0-8d94-4547-a003-eee4831b23ce"
            }
          ]
        }
      ]
    },
    {
      "name": "Actors",
      "item": [
        {
          "id": "2fa34772-95b3-41f9-9add-70590dc1f4db",
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
              "id": "7a28d385-1aaf-437f-ac43-4f81f15dbb50"
            }
          ]
        },
        {
          "id": "6e683e0e-d357-4ed2-8e2c-4062e5174946",
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
              "id": "66fe1583-1a1f-4bbd-bf60-e2c8bcda9035"
            }
          ]
        }
      ]
    },
    {
      "name": "Statuses",
      "item": [
        {
          "id": "ed133b27-0756-4645-b88d-0da80deaacc1",
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
              "id": "5baf53cb-de6f-4859-bb0d-fd3f53be69ac"
            }
          ]
        },
        {
          "id": "5a87aeb5-8f4a-4b34-844e-d9141fbabac9",
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
              "id": "ea903773-4ffc-48ba-9532-9492767e6a97"
            }
          ]
        }
      ]
    },
    {
      "name": "Assigned",
      "item": [
        {
          "id": "6f867e7a-e7d9-4d58-a401-73e99390c9db",
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
              "id": "bc8a6b55-97ae-4f58-9baa-6a62b8188d72"
            }
          ]
        }
      ]
    },
    {
      "name": "Valid",
      "item": [
        {
          "id": "cecbe997-6011-46d0-8c06-05d6ab6c13ec",
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
              "id": "99290698-48d7-45b9-8fe1-48e1e5cad02e"
            }
          ]
        },
        {
          "id": "78b1fd07-436e-4988-a915-2a9821670a03",
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
              "id": "832081c7-f8b3-460b-b6a3-a62c60b6816c"
            }
          ]
        }
      ]
    },
    {
      "name": "Resolutions",
      "item": [
        {
          "id": "a0a795cf-b6d0-4f5e-a64b-7ed51b362f3f",
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
              "id": "99173197-8316-4261-94cb-46668e80f4a4"
            }
          ]
        }
      ]
    },
    {
      "name": "Resolution",
      "item": [
        {
          "id": "0a51110c-1907-4fcf-9480-706cefa386e0",
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
              "id": "17203ea6-553b-4d2a-ba00-493bbe18e919"
            }
          ]
        }
      ]
    },
    {
      "name": "Fully",
      "item": [
        {
          "id": "4e80b91e-3aa3-457e-bd70-f5a4b343b3f9",
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
              "id": "f2165326-58e7-4a6b-a292-e6c1288ec736"
            }
          ]
        }
      ]
    },
    {
      "name": "Partial",
      "item": [
        {
          "id": "86737294-0efb-4257-b31c-de2993500c95",
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
              "id": "8acdbdda-711b-4a57-9e90-9f2c5f15509e"
            }
          ]
        }
      ]
    },
    {
      "name": "Screens",
      "item": [
        {
          "id": "162dc616-30b8-44bf-a5f2-79911da404b7",
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
              "id": "2f96015a-851e-47b6-a15f-bd1008054f1a"
            }
          ]
        }
      ]
    },
    {
      "name": "Available",
      "item": [
        {
          "id": "c08c99cd-6931-4fdb-af88-c0bb1373a7fc",
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
              "id": "8ee2078b-17dd-428c-abf1-138af43376e0"
            }
          ]
        }
      ]
    },
    {
      "name": "Screen",
      "item": [
        {
          "id": "57641e44-1a8c-46d4-9d78-2f3aeb7f7c1e",
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
              "id": "29bc1d02-2051-4f94-9568-c5054f0b8613"
            }
          ]
        },
        {
          "id": "87fb5e14-9614-43fc-955e-4216497a99dc",
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
              "id": "8a6c6bfe-3942-4f9c-8d29-27c57a7686cb"
            }
          ]
        },
        {
          "id": "cc81d658-cec7-4a27-bbf5-fd3e0d4518b0",
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
              "id": "8cb95e16-c37e-4d9d-9b70-47a9c3aa74ba"
            }
          ]
        },
        {
          "id": "38256c18-b028-4547-a445-261001d26331",
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
              "id": "b6921f5c-97da-483b-b4f9-b6c4013d1ecb"
            }
          ]
        },
        {
          "id": "16f9d733-19bd-4d56-9fe4-beb88039eaff",
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
              "id": "927ecb5c-65e2-4586-91dd-01b53d61f494"
            }
          ]
        }
      ]
    },
    {
      "name": "Rename",
      "item": [
        {
          "id": "e8812c83-4ef3-454a-b0a0-5685a3b79d95",
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
              "id": "4f1c2a37-42b2-4a46-a804-04ae127da9f2"
            }
          ]
        }
      ]
    },
    {
      "name": "Move",
      "item": [
        {
          "id": "d1eaf4ff-cf01-4189-a22f-881e4d30f2a2",
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
              "id": "c00b8b45-1072-4e90-b33c-abebf76b705b"
            }
          ]
        },
        {
          "id": "f4e022d0-3ae7-42df-8f5b-bcc389cda703",
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
              "id": "d32141fc-3da1-4ea9-affb-e1d0983d0e44"
            }
          ]
        },
        {
          "id": "4cddfe78-0898-404d-9d23-0dc7316f8d39",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.moveVersion_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id/move"
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
            "description": "Modifies the version's sequence within the project, which affects the display order of the versions in Jira. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b715976d-8f94-4ad4-8d31-78886f787eff"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchissues",
      "item": [
        {
          "id": "2798d9dd-cb66-4148-8d7c-8df93346fc36",
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
              "id": "b88e4575-4fb8-4f73-8d4f-40c13cbfac6e"
            }
          ]
        },
        {
          "id": "d77d71d3-b6f4-4a0e-8b79-a8d97b946a37",
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
              "id": "34daf6ed-cba0-45e4-9d39-3d7db3f988cf"
            }
          ]
        }
      ]
    },
    {
      "name": "Server",
      "item": [
        {
          "id": "86d2fef1-e481-474d-bf15-a37c5d2144fc",
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
              "id": "9ccea69e-ca6d-4fdb-9e83-3a55b04fc959"
            }
          ]
        }
      ]
    },
    {
      "name": "Status",
      "item": [
        {
          "id": "6f48ce0f-0258-4a2a-87a6-07400217679f",
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
              "id": "710a9977-848c-4528-bc25-fefdbdc852b2"
            }
          ]
        },
        {
          "id": "b282e3af-abe9-4210-9d5f-c3708b4742a7",
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
              "id": "14f58285-be23-4579-a608-fb87cf88c9dc"
            }
          ]
        },
        {
          "id": "f059aea5-c080-4c56-8382-c8d63edea594",
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
              "id": "e8d50996-7225-4fb4-b1a2-a361dc7c0ada"
            }
          ]
        }
      ]
    },
    {
      "name": "Task",
      "item": [
        {
          "id": "d1eb4aa5-aa06-4f03-b190-4a32a2a8acad",
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
              "id": "d2b58b03-5ec8-465b-9ea7-72bf3f526b9f"
            }
          ]
        }
      ]
    },
    {
      "name": "Cancel",
      "item": [
        {
          "id": "344646bf-280d-4ad6-b7dc-5c0168618e2e",
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
              "id": "bc08bbba-4a9a-46e6-b117-041cfa21f3b1"
            }
          ]
        }
      ]
    },
    {
      "name": "Avatars",
      "item": [
        {
          "id": "96bcd86a-f176-4b77-8778-68623b9e7974",
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
              "id": "df9490a9-9eb7-46e2-bdaf-492c97cc5336"
            }
          ]
        }
      ]
    },
    {
      "name": "Store",
      "item": [
        {
          "id": "76f495d0-51c8-4734-979e-05886ce5c4e2",
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
              "id": "74c32162-ba83-4865-9129-ea06a026c190"
            }
          ]
        }
      ]
    },
    {
      "name": "Avatar",
      "item": [
        {
          "id": "f0a0ba64-ad31-4c40-9982-d9b4d24c3b66",
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
              "id": "1a84ca6b-fa8e-422d-87ae-3659cabd41be"
            }
          ]
        }
      ]
    },
    {
      "name": "Version",
      "item": [
        {
          "id": "a13c3f7d-6448-427d-a902-883d33ab99b5",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.createVersion_post",
          "request": {
            "url": "{{default}}/api/2/version",
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
            "description": "Creates a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f67aeba5-92e1-431c-920f-8fac010ed432"
            }
          ]
        },
        {
          "id": "945a706e-edbc-46a1-8078-9946a84c1096",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.getVersion_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id"
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
            "description": "Returns a project version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ project permission"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56b6be70-dafb-47fb-82f5-00f1303d158f"
            }
          ]
        },
        {
          "id": "9bedb143-c8e4-4c8f-b6de-0ba63b1ed690",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.updateVersion_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id"
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
            "description": "Modifies a project version. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d2150474-fd91-41bc-ba2d-d8ce48deaf29"
            }
          ]
        },
        {
          "id": "5e7d51e0-dc35-4ca7-9acf-28c3c8528fd4",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.deleteVersion_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id"
              ],
              "query": [
                {
                  "key": "moveAffectedIssuesTo",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "moveFixIssuesTo",
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
            "description": "Deletes a project version. Deprecated, use [Delete and replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post) that supports swapping version values in custom fields, in addition to the swapping for `fixVersion` and `affectedVersion` provided in this resource. Alternative versions can be provided to update issues that use the deleted version in `fixVersion` or `affectedVersion`. If alternatives are not provided, occurrences of `fixVersion` and `affectedVersion` that contain the deleted version are cleared. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b6d92e90-3dfe-482d-9f27-c106382223f8"
            }
          ]
        }
      ]
    },
    {
      "name": "Merge",
      "item": [
        {
          "id": "2ddab58f-5b9e-4c03-b60b-85eafd0bd505",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.mergeVersions_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id/mergeto/:moveIssuesTo"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "moveIssuesTo",
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
            "description": "Merges two project versions. The merge is completed by deleting the version specified in `id` and replacing any occurrences of its ID in `fixVersion` with the version ID specified in `moveIssuesTo`. Consider using [Delete and replace version](https://developer.atlassian.com/cloud/jira/platform/rest/#api-api-2-version-id-removeAndSwap-post) instead. This resource supports swapping version values in `fixVersion`, `affectedVersion`, and custom fields. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg) or _Administer Projects_ [project permission](https://confluence.atlassian.com/x/yodKLg)."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "74cf6c5c-943c-49c6-b3df-b10815340be5"
            }
          ]
        }
      ]
    },
    {
      "name": "Versions",
      "item": [
        {
          "id": "6ff30b73-e42d-43ad-aed2-c8d989fdf223",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.getVersionRelatedIssues_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id/relatedIssueCounts"
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
            "description": "Returns the following counts for a version:\n\n*   Number of issues where the `fixVersion` is set to the version.\n*   Number of issues where the `affectedVersion` is set to the version.\n*   Number of issues where a version custom field is set to the version.\n\n[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ project permission"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5771bbe3-b286-429a-ab71-8e8f40ed606b"
            }
          ]
        },
        {
          "id": "1966d022-d618-448e-993e-892079870e59",
          "name": "com.atlassian.jira.rest.v2.issue.VersionResource.getVersionUnresolvedIssues_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/version/:id/unresolvedIssueCount"
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
            "description": "Returns counts of the issues and unresolved issues for the project version. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: _Browse projects_ project permission"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "585ea91a-486a-4d7d-9a72-e6294913fff6"
            }
          ]
        }
      ]
    },
    {
      "name": "Workflows",
      "item": [
        {
          "id": "2cabb805-e966-43c5-912c-b723c5215f81",
          "name": "com.atlassian.jira.rest.v2.admin.WorkflowsResource.getAllWorkflows_get",
          "request": {
            "url": "{{default}}/api/2/workflow?workflowName=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns all workflows in Jira or a single workflow.\n\nIf the `workflowName` parameter is specified, a workflow will be returned as an object (not in an array). Otherwise, an array of workflow objects will be returned.\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9dd0c22f-5f3d-4568-b903-bc8462460805"
            }
          ]
        }
      ]
    },
    {
      "name": "Workflow",
      "item": [
        {
          "id": "58735918-a0ed-4bbd-b1c6-a84475b60b8d",
          "name": "com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.getWorkflowTransitionProperties_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflow/transitions/:transitionId/properties"
              ],
              "query": [
                {
                  "key": "includeReservedKeys",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowMode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "transitionId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the properties on a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "307d8486-6519-4889-8e7e-bf6092a9c631"
            }
          ]
        },
        {
          "id": "d615188d-2fc7-47ad-a86d-8f02f4d2a0b4",
          "name": "com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.updateWorkflowTransitionProperty_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflow/transitions/:transitionId/properties"
              ],
              "query": [
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowMode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "transitionId",
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
            "description": "Updates a workflow transition by changing the property value. Trying to update a property that does not exist results in a new property being added to the transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3da1f6a4-a0c5-4f97-8ac5-bb974bdc0529"
            }
          ]
        },
        {
          "id": "07a19345-4864-44e1-8013-97382210d368",
          "name": "com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.createWorkflowTransitionProperty_post",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflow/transitions/:transitionId/properties"
              ],
              "query": [
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowMode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "transitionId",
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
            "description": "Adds a property to a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f79edb94-01b9-4d62-90d2-b0ecce97597a"
            }
          ]
        },
        {
          "id": "57fa756a-c99b-4964-b69a-0b919bcd1607",
          "name": "com.atlassian.jira.rest.v2.admin.WorkflowTransitionResource.deleteWorkflowTransitionProperty_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflow/transitions/:transitionId/properties"
              ],
              "query": [
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowMode",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowName",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "transitionId",
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
            "description": "Deletes a property from a workflow transition. Transition properties are used to change the behavior of a transition. For more information, see [Transition properties](https://confluence.atlassian.com/x/zIhKLg#Advancedworkflowconfiguration-transitionproperties) and [Workflow properties](https://confluence.atlassian.com/x/JYlKLg).\n\n**[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3f19016d-f856-4b46-80f2-035bf9d0f5f3"
            }
          ]
        },
        {
          "id": "22d39707-9511-41cc-9596-e6ff280f4f2a",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.createWorkflowScheme_post",
          "request": {
            "url": "{{default}}/api/2/workflowscheme",
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
            "description": "Create a new workflow scheme.\n\nThe body contains a representation of the new scheme. Values not passed are assumed to be set to their defaults."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f8298c9c-5290-4d70-9b9a-16ab2597a307"
            }
          ]
        },
        {
          "id": "3a763354-b951-419d-97da-edc2ca7e9e5e",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getWorkflowScheme_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id"
              ],
              "query": [
                {
                  "key": "returnDraftIfExists",
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
            "description": "Returns the requested workflow scheme to the caller."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5868039e-7f2b-474f-bb29-4462ade5119f"
            }
          ]
        },
        {
          "id": "29290be2-5ed8-4dc7-809b-b01c7cabd207",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateWorkflowScheme_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id"
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
            "description": "Update the passed workflow scheme.\n\nThe body of the request is a representation of the workflow scheme. Values not passed are assumed to indicate no change for that field.\n\nThe passed representation can have its updateDraftIfNeeded flag set to true to indicate that the draft should be created and/or updated when the actual scheme cannot be edited (e.g. when the scheme is being used by a project). Values not appearing the body will not be touched."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5bcfd6ec-ed28-4301-aaeb-670bd0e28f2f"
            }
          ]
        },
        {
          "id": "1b7c24fd-dc9a-4237-9236-0e6b8491622f",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.deleteWorkflowScheme_delete",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id"
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
            "description": "Delete the passed workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "877748ad-2ba1-4f7e-af16-83f52a5a91e5"
            }
          ]
        },
        {
          "id": "013444df-bfb3-47fd-b7ef-711449d789a4",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.createWorkflowSchemeDraftFrom",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/createdraft"
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
            "description": "Create a draft for the passed scheme. The draft will be a copy of the state of the parent."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "87ba6265-c402-4e4d-a80d-a2461a748f14"
            }
          ]
        },
        {
          "id": "ba4ef8b0-1a9f-4f46-a253-67c2eeaebe3d",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getWorkflowSchemeDraft_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft"
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
            "description": "Returns the requested draft workflow scheme to the caller."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "73bb14c8-4a7f-4b9a-9cc4-68ed7c174cdc"
            }
          ]
        },
        {
          "id": "f239e4e3-67d6-4d11-ad3c-598e46a780e1",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateWorkflowSchemeDraft_put",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft"
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
            "description": "Update a draft workflow scheme. The draft will created if necessary.\n\nThe body is a representation of the workflow scheme. Values not passed are assumed to indicate no change for that field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a0891a21-dd6c-43d5-b520-4d476e6a833f"
            }
          ]
        },
        {
          "id": "2ad49512-1382-4db6-96f5-a41d3745ab95",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.deleteWorkflowSchemeDraft_del",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft"
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
            "description": "Delete the passed draft workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30dded87-209f-468d-87e5-c12a59accc6a"
            }
          ]
        },
        {
          "id": "fac73bbe-ab20-47f9-a833-15fd498819d5",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getWorkflowSchemeDraftIssueTy",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/issuetype/:issueType"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "issueType",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the issue type mapping for the passed draft workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1bbcc17a-b861-4afb-9fc5-eda8e548b84c"
            }
          ]
        },
        {
          "id": "a691f396-bedd-419f-92f5-1ac57bd8d9e9",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.deleteWorkflowSchemeDraftIssu",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/issuetype/:issueType"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "issueType",
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
            "description": "Remove the specified issue type mapping from the draft scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d729ac5e-7547-48f1-b64a-594a85e9f604"
            }
          ]
        },
        {
          "id": "6475ea71-860d-4499-ad19-82d77563599d",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getWorkflowSchemeIssueType_ge",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/issuetype/:issueType"
              ],
              "query": [
                {
                  "key": "returnDraftIfExists",
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
                  "id": "issueType",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Returns the issue type mapping for the passed workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1bb3fc66-7341-42e8-a021-f76dc6acef46"
            }
          ]
        },
        {
          "id": "e4c476b0-ed65-4975-918f-e83c9b517bb5",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.deleteWorkflowSchemeIssueType",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/issuetype/:issueType"
              ],
              "query": [
                {
                  "key": "updateDraftIfNeeded",
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
                  "id": "issueType",
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
            "description": "Remove the specified issue type mapping from the scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "14f4fcb1-e907-433e-a31d-9b8d25a834d5"
            }
          ]
        },
        {
          "id": "65f80934-f181-4865-aef2-dd178f0eb61d",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getWorkflow_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/workflow"
              ],
              "query": [
                {
                  "key": "returnDraftIfExists",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "workflowName",
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
            "description": "Returns the workflow mappings or requested mapping to the caller for the passed scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "371573fe-92e5-4055-8833-8d758de41b2d"
            }
          ]
        }
      ]
    },
    {
      "name": "Draft",
      "item": [
        {
          "id": "c8fe83f6-7d9b-4cb4-b8f2-eabe2718d6b3",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getDraftDefaultWorkflow_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/default"
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
            "description": "Return the default workflow from the passed draft workflow scheme to the caller."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bfae08f5-74b3-451a-93c0-870ac9f838c7"
            }
          ]
        },
        {
          "id": "54aa2154-4553-4bc5-ad90-14f0c696e5f3",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateDraftDefaultWorkflow_pu",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/default"
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
            "description": "Set the default workflow for the passed draft workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec029864-737a-430e-a102-32dc44d6500c"
            }
          ]
        },
        {
          "id": "fa159999-0a9b-4e83-a2ff-286c44f6644b",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.deleteDraftDefaultWorkflow_de",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/default"
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
            "description": "Remove the default workflow from the passed draft workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "78cde181-adbb-4708-9236-ee14a3dbce9e"
            }
          ]
        },
        {
          "id": "1155203d-4820-48f6-8bba-70cd478ceccc",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.getDraftWorkflow_get",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/workflow"
              ],
              "query": [
                {
                  "key": "workflowName",
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
            "description": "Returns the draft workflow mappings or requested mapping to the caller."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c0d89153-4c23-4e11-826c-3b2fe6c93341"
            }
          ]
        },
        {
          "id": "fc82556b-65d1-4095-a720-af258b0fa1e6",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.updateDraftWorkflowMapping_pu",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/workflow"
              ],
              "query": [
                {
                  "key": "workflowName",
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
            "description": "Update the draft scheme to include the passed mapping.\n\nThe body is a representation of the workflow mapping. Values not passed are assumed to indicate no change for that field."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8190af49-358d-4852-be3e-76424872c826"
            }
          ]
        },
        {
          "id": "081d0351-f0a5-4e1d-9cb8-35f9c9e8086c",
          "name": "com.atlassian.jira.rest.v2.admin.workflowscheme.WorkflowSchemeResource.deleteDraftWorkflowMapping_de",
          "request": {
            "url": {
              "host": "{{default}}",
              "path": [
                "api/2/workflowscheme/:id/draft/workflow"
              ],
              "query": [
                {
                  "key": "workflowName",
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
            "description": "Delete the passed workflow from the draft workflow scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "91f23cb2-a548-4608-b65f-38a51e650914"
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