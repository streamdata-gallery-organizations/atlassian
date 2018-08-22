{
  "info": {
    "name": "Jira Cloud API Get issue link",
    "_postman_id": "3170b8bb-5651-453e-8166-7f54a51b84d6",
    "description": "Returns an issue link with the specified id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "a297cb0a-3f3d-4c83-8447-7246e86ae582",
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
              "id": "09a0d7a0-4847-4808-9d32-a1888eebbe3f"
            }
          ]
        },
        {
          "id": "b4749fe4-9acf-41e6-9dc0-da6d8f356b00",
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
              "id": "f663dba2-b7b3-4ebf-869c-6a7e02ac2e30"
            }
          ]
        },
        {
          "id": "172fbb93-76c2-46c3-9c90-d40ac3c67278",
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
              "id": "b404a74b-047f-47e9-9daf-9b17a8f49c42"
            }
          ]
        }
      ]
    },
    {
      "name": "Advanced",
      "item": [
        {
          "id": "cfef89d1-e851-4780-8593-aa84da9a3300",
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
              "id": "e75bab4b-9e2a-4fee-b34f-894c53604e8f"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "ea337eae-5ced-4564-9bb2-b33080fdc52c",
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
              "id": "d590ff4f-0bd5-4edf-aa8e-0a94d6ea7c9d"
            }
          ]
        },
        {
          "id": "dfd3a3a4-faf3-439b-8bdb-c54ce50ef7e8",
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
              "id": "5df91ff2-df22-49c0-8ef9-de386b04ca63"
            }
          ]
        },
        {
          "id": "2322781b-a631-411a-a0a7-bd5cbf6c267b",
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
              "id": "bd1eec57-ad6c-46b9-82bd-091a2169a36a"
            }
          ]
        },
        {
          "id": "70514a4f-6bdf-4886-9e13-5845dd837756",
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
              "id": "429fa334-ac05-4085-aa0e-f1645e45bf73"
            }
          ]
        },
        {
          "id": "0fb7badf-688c-46db-89b6-d18a542977fe",
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
              "id": "52b41671-b02d-4306-beaf-38702bf87ce3"
            }
          ]
        },
        {
          "id": "e962224f-ac3d-4fe4-b86a-b9dfa2f79505",
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
              "id": "27da3b55-a8be-4ada-9641-108c8b6742ad"
            }
          ]
        },
        {
          "id": "d53856c0-32cf-4652-abc5-cc133f93422e",
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
              "id": "13e771ad-6467-4332-8576-d5fc5a1674ae"
            }
          ]
        },
        {
          "id": "79179e0c-1bc8-45bf-9063-dd0a31340572",
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
              "id": "31f16751-88fa-47c0-8dc6-a6a260b93f4d"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "2106dff7-662e-4a29-87ba-ecc8b352eec4",
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
              "id": "bc04ca4e-ef54-432d-889f-94d37b5be3c8"
            }
          ]
        },
        {
          "id": "10ae2548-b413-4569-8e4a-b53bc883b801",
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
              "id": "0c48fae6-0a66-4556-9771-eeec02868f34"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "daf7dc0a-66bd-4495-9c39-27de268ef3ce",
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
              "id": "ec99ae89-3ff7-42c8-a950-8745eda3ed09"
            }
          ]
        },
        {
          "id": "38f6e96a-07f6-47b8-bc7e-b598ffddf320",
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
              "id": "f07aa5ff-ebc3-441c-9fc6-607ebb9ade85"
            }
          ]
        },
        {
          "id": "6d5a00e0-c26e-44ad-8ada-dabe8f61d708",
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
              "id": "1d6d8e8d-2c3c-45e2-bb74-f5e643a7cc90"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadataan",
      "item": [
        {
          "id": "3567e9e3-d7e5-48e5-ab1d-8fc87747b18c",
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
              "id": "acdad6c6-e0ed-433b-8caf-911a0ec7acc0"
            }
          ]
        }
      ]
    },
    {
      "name": "Contents",
      "item": [
        {
          "id": "55bd4fee-50ac-47e3-9a89-ad292e81b7c0",
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
              "id": "30b4ab21-c0ab-481f-a1e2-ba2e2028cc06"
            }
          ]
        }
      ]
    },
    {
      "name": "Audit",
      "item": [
        {
          "id": "b64c4ffe-434c-4d0b-bf38-9f6835ef097a",
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
              "id": "93214c32-5e5f-4c50-b059-e8ad91a9633c"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "5b87957b-1113-44e6-bdf1-d7fcf99c1e38",
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
              "id": "fc455770-b891-44a7-808f-8106230cdfbb"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "bd65d298-7dba-42e7-a48c-211040e8c02a",
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
              "id": "39abf648-df65-4d37-94d0-3965434a40d5"
            }
          ]
        },
        {
          "id": "b0cc14bf-df28-47ea-b65f-277b4d6af921",
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
              "id": "d231b0b9-7f66-4442-ae55-b854bd311d29"
            }
          ]
        }
      ]
    },
    {
      "name": "Comment",
      "item": [
        {
          "id": "5c1e7319-cf5b-4385-9632-16c1facff1c0",
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
              "id": "fba03409-924c-478c-8618-c98d8b1df230"
            }
          ]
        },
        {
          "id": "2a3462fc-47f3-4a84-ac58-c3fce5af6411",
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
              "id": "50f24437-3995-4936-b4b8-d0a1fa303a7e"
            }
          ]
        },
        {
          "id": "ded038ad-9ed3-428a-811e-e40ad570c30b",
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
              "id": "0f9068bd-26c4-4b5d-9414-1580fa3b3d55"
            }
          ]
        },
        {
          "id": "2a2dc6c1-4e45-4465-a31e-c57fe3dc87cf",
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
              "id": "f038705b-2d41-4326-abe7-a602efc1e107"
            }
          ]
        },
        {
          "id": "33de53e7-59e2-42d9-9bea-14cdafd26074",
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
              "id": "169ae700-4bbd-4d99-a929-df97f7d629f8"
            }
          ]
        },
        {
          "id": "c0f2e9a4-06b4-452b-932f-abaa186a2b9b",
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
              "id": "49ee27ed-505c-41e3-99eb-13a523608156"
            }
          ]
        },
        {
          "id": "6d18c120-dd3d-44f6-812d-23824b6ced9b",
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
              "id": "8212f17b-014c-4435-bebe-0bb64700125d"
            }
          ]
        }
      ]
    },
    {
      "name": "Component",
      "item": [
        {
          "id": "9b928314-96cd-4837-970c-a8648d120a33",
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
              "id": "65d034ab-9ce5-4786-aa93-373e794e0ca0"
            }
          ]
        },
        {
          "id": "80c99be3-33ce-4cfa-81e4-2f70f2dd0617",
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
              "id": "929d2eae-d6c0-4232-a53c-a4431c5f9b73"
            }
          ]
        },
        {
          "id": "3452416b-176b-4bf6-ab0b-748ab471aadd",
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
              "id": "ae2e2758-b670-46af-8410-6899b7e9cd64"
            }
          ]
        },
        {
          "id": "ef0260c2-bfa6-4cd1-9394-82faccd11503",
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
              "id": "dba31247-3f0f-43cc-ac87-12835c84d75a"
            }
          ]
        },
        {
          "id": "ba48d2f9-5218-4e66-804d-e86a38af683e",
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
              "id": "3e4779e1-aee8-4c8b-8338-97f77ffb1dfa"
            }
          ]
        }
      ]
    },
    {
      "name": "Selected",
      "item": [
        {
          "id": "655e2044-138b-43ac-927e-d2f547d92679",
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
              "id": "730e6ae0-fbbf-4a08-a7cf-928056ca7c41"
            }
          ]
        }
      ]
    },
    {
      "name": "Select",
      "item": [
        {
          "id": "9c57ea46-9a94-43d9-9433-1b1b64ffb027",
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
              "id": "8c81c12c-0d7f-4370-be1f-ae1534210e3f"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "cbea8e07-2e7f-4d79-91ac-51e6591a67e6",
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
              "id": "3707d40c-bba7-4be0-8e0f-33c9c6e5ed92"
            }
          ]
        }
      ]
    },
    {
      "name": "Time",
      "item": [
        {
          "id": "b4c16565-1608-4783-bc9e-6c32dbed8174",
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
              "id": "0a68d8ad-3aaf-45ca-a613-44f3239b5a85"
            }
          ]
        },
        {
          "id": "7e6a7ad0-91ab-4d2d-ac93-0205886d0004",
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
              "id": "1e2efbf7-2e0a-4de3-9889-274cae12ed32"
            }
          ]
        }
      ]
    },
    {
      "name": "Custom",
      "item": [
        {
          "id": "b525b3f4-1e76-4bf7-a716-e818c91fdea8",
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
              "id": "ffe8b167-f5e1-42ef-b362-5561cc729099"
            }
          ]
        },
        {
          "id": "af0c4780-6d0d-48e8-a88f-61d970e0f2b9",
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
              "id": "5caa1d2b-70ea-48cd-bb2c-1ea9047c4eeb"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboards",
      "item": [
        {
          "id": "deca264a-09bf-4df0-ab78-683a2eb373e2",
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
              "id": "966996b2-b422-4875-bbfb-3ffaba52223b"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboard",
      "item": [
        {
          "id": "940ed2d6-276f-4ca4-8c77-ec63ad94d922",
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
              "id": "5118fb2c-96c4-4e46-8c80-07bd1c68bee8"
            }
          ]
        },
        {
          "id": "74a6d889-ab8a-4bea-b0b4-5d5e73353942",
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
              "id": "19ec5ee9-c3e8-437d-ba5a-ffe038c76208"
            }
          ]
        },
        {
          "id": "4d8417e2-aaaf-433a-8cfa-7198da2dcafb",
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
              "id": "55186f03-f922-46ba-9e92-ff5409bc96cc"
            }
          ]
        },
        {
          "id": "b3b61c6b-cb2f-49a2-855f-40ff664a3ba2",
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
              "id": "c011eb18-f2a5-46c4-a16e-a80e254a039b"
            }
          ]
        }
      ]
    },
    {
      "name": "Evaluate",
      "item": [
        {
          "id": "1155c123-0265-43ac-98ed-7938a22f2fc6",
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
              "id": "e7f0ed82-1136-4629-916d-f87ba2d249b6"
            }
          ]
        }
      ]
    },
    {
      "name": "Fields",
      "item": [
        {
          "id": "3f0d78c0-ee3f-470f-ba31-755cbbf6ffac",
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
              "id": "3cd8297d-33f1-4b4c-b9b2-c1e631f0f9f7"
            }
          ]
        }
      ]
    },
    {
      "name": "Issue",
      "item": [
        {
          "id": "5f6912d1-b8a8-4ec1-ab54-c26b532d6fb8",
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
              "id": "97b682f3-81af-411d-a92e-089648d0fe0f"
            }
          ]
        },
        {
          "id": "dabf4e11-d32e-4002-8676-112a805f2d70",
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
              "id": "0fd2ae6e-287e-43a8-94e0-9f6882d07da1"
            }
          ]
        },
        {
          "id": "3c463c36-b350-42e3-aadc-2d2a32a0433d",
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
              "id": "4d6f0144-4280-4512-a4be-508a786a13b3"
            }
          ]
        },
        {
          "id": "b9dbc234-de7e-4dee-a072-7fc399d67536",
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
              "id": "c5e75697-661d-4d66-9935-038e9509c117"
            }
          ]
        },
        {
          "id": "231f41af-f422-4cc7-ad30-46424406e7be",
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
              "id": "3133cc98-9b7a-4e00-b132-fcd83bc0999f"
            }
          ]
        },
        {
          "id": "1efa0173-d4cd-40d0-b80d-b613feda7171",
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
              "id": "65e0be64-1a3a-41ed-b66d-ec7d6d12aaf8"
            }
          ]
        },
        {
          "id": "eecf3abc-7b26-4010-b9af-51d3542ad5d9",
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
              "id": "94f25208-09f8-4366-8056-294cc2af4534"
            }
          ]
        },
        {
          "id": "6f12a549-38a0-4810-878f-d8802dae77d3",
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
              "id": "b23f762d-a13c-4141-ae18-7b2923bc4676"
            }
          ]
        },
        {
          "id": "ba135270-265b-48da-8754-48fc8587bb4e",
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
              "id": "5fc90b74-ad0c-4ded-a02a-e8222ce6e2cc"
            }
          ]
        },
        {
          "id": "de118b7a-4501-48c5-bd2c-1ca26cee6087",
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
              "id": "cfc7d94f-ad4b-459d-a460-b6768076bfcf"
            }
          ]
        },
        {
          "id": "eeb6c10a-80bf-4e51-8025-a878066cc86c",
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
              "id": "91914a6a-dafb-488c-879d-9b02873e8cb1"
            }
          ]
        },
        {
          "id": "d2da2930-c93f-4671-9497-5f6512fd58da",
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
              "id": "251312a9-fbd1-47f7-9aea-68485431b29f"
            }
          ]
        },
        {
          "id": "2c8c3f71-019d-42eb-9a70-9ab4e832ad8d",
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
              "id": "92df67d6-dc24-4e33-93b0-fd46cb301351"
            }
          ]
        },
        {
          "id": "bfa328ba-1cc3-476e-91ea-08512f45cb0b",
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
              "id": "45f1fd29-1741-492e-a9ee-918c1ccc57f5"
            }
          ]
        },
        {
          "id": "3be39374-ad7c-41c6-9b6b-476d4937d2e0",
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
              "id": "131370a9-c432-4565-8944-0323f27ed98f"
            }
          ]
        }
      ]
    },
    {
      "name": "Selectable",
      "item": [
        {
          "id": "bfcfbb30-a490-47d5-8447-2b7bef867fb4",
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
              "id": "0d90e50a-872e-4f66-95ff-d669ee28664f"
            }
          ]
        }
      ]
    },
    {
      "name": "Visible",
      "item": [
        {
          "id": "417ed599-88b5-42f2-a60f-c5c7f051d7ed",
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
              "id": "d06e3697-7b69-44eb-955d-bf3d3d799db9"
            }
          ]
        }
      ]
    },
    {
      "name": "Replace",
      "item": [
        {
          "id": "fc526eaf-8bab-46d0-ab47-1447d4eb1acf",
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
              "id": "aa62e7f9-fadd-4f97-84f6-d92fdb7e840e"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "d07af973-bce7-4b86-a94f-ac1abc2ce30f",
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
              "id": "65253e4a-7b30-4ad9-bb55-15d04190b244"
            }
          ]
        }
      ]
    },
    {
      "name": "Filter",
      "item": [
        {
          "id": "67a96b0f-5e6a-4a7b-b837-dcecd2db1e0e",
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
              "id": "6e1126b9-0589-4a5b-ae41-2defe4af92b4"
            }
          ]
        },
        {
          "id": "679a6d0f-1241-4726-b979-dd6424b18017",
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
              "id": "f9343238-fd14-4573-af3e-6a7a4718e36c"
            }
          ]
        },
        {
          "id": "395e5c99-2793-436f-a8b4-801276941149",
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
              "id": "95a29857-ecf6-4b83-9b2d-2e648a7e7c09"
            }
          ]
        },
        {
          "id": "11ca02b4-6d8e-422a-802b-eb66a191e9ca",
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
              "id": "a834f00e-7ebd-4369-807e-663591e74dbd"
            }
          ]
        },
        {
          "id": "0457014f-c907-4591-a417-4d4763942775",
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
              "id": "95176e71-8d7a-45ea-9881-b423a77130ae"
            }
          ]
        }
      ]
    },
    {
      "name": "Default",
      "item": [
        {
          "id": "ca29f7cf-0407-4fc9-b485-33e85643b547",
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
              "id": "f5b2dfa1-9ca1-4976-b5f2-a25d83203cab"
            }
          ]
        }
      ]
    },
    {
      "name": "Favourite",
      "item": [
        {
          "id": "aac6f411-955c-4953-bbab-62ec414ca607",
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
              "id": "81702715-b2af-45a2-8fa2-dc708ec931fa"
            }
          ]
        }
      ]
    },
    {
      "name": "My",
      "item": [
        {
          "id": "3327a457-76a4-4ce1-8019-3f9076f1ce22",
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
              "id": "5d464041-2969-45aa-9d75-b07c249d7db0"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchfilters",
      "item": [
        {
          "id": "14041b5e-b965-40f7-ac50-b2d93041bfaa",
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
              "id": "42c7a7d8-56ee-4f69-90b2-6f3e88f304ad"
            }
          ]
        }
      ]
    },
    {
      "name": "Columns",
      "item": [
        {
          "id": "a3e98dfc-b12e-4a2e-9c0a-a9a8ee5c457d",
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
              "id": "49ab969b-1255-45ce-aa87-a34fca37d914"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "2a4c07d1-4105-4629-9f30-1de30775bf90",
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
              "id": "9799be2b-503c-4b32-b172-8a63d9dca699"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "fdd72f58-d5d4-4a0b-b400-44c06da26c09",
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
              "id": "c8a1a468-a95f-42a8-a4f4-d6efd950532d"
            }
          ]
        },
        {
          "id": "6f7a4fe0-8afe-479c-8c1d-c90535a75b46",
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
              "id": "0c0e78da-b474-4f19-87a0-832c905ddc93"
            }
          ]
        },
        {
          "id": "a0d99609-fa18-402b-9219-f8cace6074b7",
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
              "id": "dfbb1c8a-6a71-4959-b939-dcdf9dabb99a"
            }
          ]
        },
        {
          "id": "a4c2ad12-5124-45bd-8ae1-3df5c4b9ee48",
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
              "id": "f7e1e8be-435a-4e21-b710-f605e1c1fb10"
            }
          ]
        },
        {
          "id": "106d93ca-577c-4ed6-9e3e-c790b2490341",
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
              "id": "b7f642bb-6692-4da1-802d-4d21e273359f"
            }
          ]
        }
      ]
    },
    {
      "name": "Share",
      "item": [
        {
          "id": "f7740206-4055-46bc-852e-aeeb8d1f6429",
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
              "id": "33079731-a4aa-473e-95f0-d0c6a911af58"
            }
          ]
        },
        {
          "id": "22853617-2bd7-4124-914f-fd284fc8d647",
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
              "id": "01e679a4-855e-4a98-9e65-08de80fb9de9"
            }
          ]
        },
        {
          "id": "993b3d3c-b88d-427e-863d-c9c86812d7e4",
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
              "id": "aca8eb4b-a77e-45e0-b6be-25c4534a97bb"
            }
          ]
        },
        {
          "id": "118a69fe-187c-4dd8-8777-1d04f52039ca",
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
              "id": "627a9362-9a7b-4dd2-a7d3-87f759464f69"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "974dadb8-bbe9-4d4e-b4f6-397f2b4dcbdb",
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
              "id": "38e39b4d-6b9b-450a-957f-e416072cf6a0"
            }
          ]
        },
        {
          "id": "93a87b2b-46ec-475a-9b63-01567f1bcb6c",
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
              "id": "689fa055-2f2c-4017-8dc8-35ed8bece3e1"
            }
          ]
        }
      ]
    },
    {
      "name": "Users",
      "item": [
        {
          "id": "5b90cfeb-3835-4261-a5a4-5855f985b35e",
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
              "id": "1c3a7ef0-5ba7-40bc-8f98-1919c6fefcdd"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "ec8b1f39-e37d-4924-ae26-5bda39deba05",
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
              "id": "65bc1c3a-6649-4119-b766-c292d5cc0564"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "8c023f3b-a395-4a10-b58e-09a470368e99",
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
              "id": "205b4a95-3612-4244-bc6b-d262a4c687b5"
            }
          ]
        },
        {
          "id": "c2120fe7-7c6e-4179-b22e-f07917487048",
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
              "id": "71f3724a-b270-40c9-a55f-3c6ae0ade493"
            }
          ]
        }
      ]
    },
    {
      "name": "Issues",
      "item": [
        {
          "id": "4e4b7913-5bd6-49cf-bb26-f3008f6a4644",
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
              "id": "f6dc1c50-d703-4572-ad2c-cac26273b4a7"
            }
          ]
        }
      ]
    },
    {
      "name": "Create",
      "item": [
        {
          "id": "896f0159-76e4-4d07-b192-82202d39c3bb",
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
              "id": "306b9655-27b0-4888-9996-033a1aae1246"
            }
          ]
        }
      ]
    },
    {
      "name": "Bulk",
      "item": [
        {
          "id": "ffc6a8a9-fc0f-43bd-a435-b796833693d3",
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
              "id": "1f566848-47ca-4571-b5fa-39bcd7d02bcf"
            }
          ]
        },
        {
          "id": "fd5012b4-323c-4592-8bd7-553d312db14f",
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
              "id": "5c9b41d9-c272-4387-b4ab-60840b42250f"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "a14f8769-a422-40be-8887-810ec3a542c6",
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
              "id": "1a4eb1ec-36ac-4ec2-9653-30dcddd3e964"
            }
          ]
        },
        {
          "id": "8cdd43a5-9cd1-4440-bba6-40b1882d19b5",
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
              "id": "09e581e4-c2e6-4aff-908d-79b314baaa94"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "34ab8f25-fa79-45a0-b1df-97f979aefd98",
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
              "id": "5ade14cb-6ea7-4446-8569-dab03cb13461"
            }
          ]
        }
      ]
    },
    {
      "name": "Change",
      "item": [
        {
          "id": "1ad68dce-0606-43cd-ac4d-53612e6a1750",
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
              "id": "f58a0735-cbdf-4bd0-925f-5b1a1db2d23f"
            }
          ]
        }
      ]
    },
    {
      "name": "Notify",
      "item": [
        {
          "id": "6c05e029-443f-4a1c-8b31-0b646c990b35",
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
              "id": "b6fbef97-6179-49f5-aae2-1b0bbf119338"
            }
          ]
        }
      ]
    },
    {
      "name": "Remote",
      "item": [
        {
          "id": "432814b7-dcd2-45de-b8a4-f4a41614e624",
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
              "id": "14e6ad6b-ba41-4c44-a825-5d6e9ad10317"
            }
          ]
        },
        {
          "id": "ca1348f7-2458-48a9-98c4-7a4349cdffb7",
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
              "id": "7c68b23d-5be5-4395-99b7-5a69e622f689"
            }
          ]
        },
        {
          "id": "1145150a-8727-48c7-b3c5-73ecb3b7d644",
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
              "id": "221108a5-dffe-4896-8736-d797811bd9df"
            }
          ]
        },
        {
          "id": "26706dc8-370f-4828-9ab3-d2f6bdc47849",
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
              "id": "38cc6b13-f09f-46eb-a52f-b23e11b105ac"
            }
          ]
        },
        {
          "id": "7d0981f1-1869-4d78-bb8d-45d00f3deeaa",
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
              "id": "6aad4a70-bf73-4b79-982f-1a986e2914a6"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "c2d5d73d-9a42-4767-ad02-cb3113ecd015",
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
              "id": "dcac5ed5-780e-49e1-9f95-ad2871b05640"
            }
          ]
        }
      ]
    },
    {
      "name": "Transitions",
      "item": [
        {
          "id": "77988d6d-f0f8-4756-89b2-d46beef6acd5",
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
              "id": "5c84f03c-3b01-4438-92f6-958b4b79c351"
            }
          ]
        }
      ]
    },
    {
      "name": "Do",
      "item": [
        {
          "id": "295a42d9-d3bb-497c-a526-9592d0cb0cb6",
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
              "id": "f8173bbe-7e8a-4981-9a6f-c5a7df7f6581"
            }
          ]
        }
      ]
    },
    {
      "name": "Votes",
      "item": [
        {
          "id": "ca9e0bd2-05b2-4834-8b45-81131d4bf16c",
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
              "id": "aba6daa6-46ef-428c-aeff-c85086f45e9d"
            }
          ]
        }
      ]
    },
    {
      "name": "Vote",
      "item": [
        {
          "id": "36c05e6e-6aa3-4fa7-a8cd-3b1450a1c911",
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
              "id": "a233a476-496a-4eeb-88d4-c2565658948d"
            }
          ]
        }
      ]
    },
    {
      "name": "Watcher",
      "item": [
        {
          "id": "a5bc9af8-6f90-4148-a05c-47f1bfa373b8",
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
              "id": "a44221fe-9b5c-445a-abd1-f4cad7d9bd62"
            }
          ]
        }
      ]
    },
    {
      "name": "Worklog",
      "item": [
        {
          "id": "7558c8d0-eb29-4cc5-9ca6-b4ce3441df8b",
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
              "id": "68487eb6-f854-4716-b103-7674e8555b15"
            }
          ]
        },
        {
          "id": "64a24b60-5e27-4c33-9ed2-69864a401a63",
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
              "id": "7ee6b352-4fca-437b-9f6a-a90ac1fba585"
            }
          ]
        },
        {
          "id": "e157aea6-2603-4959-8871-d7753d409efa",
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
              "id": "b558f771-aeb5-4e34-8274-376f2df59080"
            }
          ]
        },
        {
          "id": "04a46186-62fb-480b-82df-35e421c74e0e",
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
              "id": "41bc6f48-5cda-4c4a-93e4-76c2fe34cab4"
            }
          ]
        },
        {
          "id": "24b342ec-3cbb-4966-8efb-8ed0dfddbd57",
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
              "id": "8858dc96-53b6-4709-bf8c-df5ba7f712ed"
            }
          ]
        },
        {
          "id": "1133792b-a1db-4e0e-941c-bcff8c55ec7c",
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
              "id": "0c75f3fd-aa85-479b-913c-fddd517eb195"
            }
          ]
        },
        {
          "id": "ca8b11f8-7400-4786-a8bb-50c24efbb5f6",
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
              "id": "b784ca9c-6723-4896-b1cc-c619d914a97f"
            }
          ]
        }
      ]
    },
    {
      "name": "Link",
      "item": [
        {
          "id": "75db747c-df5f-46fe-9413-da0759fa5dea",
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
              "id": "00d4b938-060e-4e6f-911f-159b0d7027ab"
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