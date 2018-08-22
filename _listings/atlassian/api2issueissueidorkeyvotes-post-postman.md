{
  "info": {
    "name": "Jira Cloud API Add vote",
    "_postman_id": "15323bb4-1459-49cf-97c8-aa6e27884220",
    "description": "Adds a vote on the issue for a current user.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "76ede287-efcf-466c-a4ec-d61cb0edbfdb",
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
              "id": "bae8f252-ebdc-47e5-9a7c-5a206fa017b1"
            }
          ]
        },
        {
          "id": "5c7d97e0-438e-4dde-bf14-7a374becca79",
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
              "id": "703e495d-de85-43ae-8ca7-72a7d1589d72"
            }
          ]
        },
        {
          "id": "9c6bb675-e485-4fe4-9feb-3adda186f1d9",
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
              "id": "16e5e91c-e844-4983-8125-a3207e80ada6"
            }
          ]
        }
      ]
    },
    {
      "name": "Advanced",
      "item": [
        {
          "id": "95da1a3f-0c8c-44f3-9365-54714c098bac",
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
              "id": "f2b90160-9479-4cd9-a8fe-4d888d42a4e5"
            }
          ]
        }
      ]
    },
    {
      "name": "Set",
      "item": [
        {
          "id": "5eca610a-dbc1-49f0-aa2f-79bdb0ba091f",
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
              "id": "54945e49-b51d-4f55-bbfc-2011ce24858c"
            }
          ]
        },
        {
          "id": "7db049c3-6c20-406f-afb3-ba986cbba370",
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
              "id": "c31a9e7a-99c4-403b-bd72-d4284db53c2c"
            }
          ]
        },
        {
          "id": "0122d451-e55c-43dd-bfe4-8e09098206d2",
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
              "id": "bdb1394a-0470-4c52-8d30-7cb37ec94bf4"
            }
          ]
        },
        {
          "id": "2a24df0f-a320-4000-bf61-2b703b2cc561",
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
              "id": "8b85459d-71c0-4772-9fbe-6f1a145a3092"
            }
          ]
        },
        {
          "id": "c3dfeb78-7830-4bb6-b408-8d08fadaa53e",
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
              "id": "f7f4f6f8-0b3b-4081-a7cb-42c156af4d2f"
            }
          ]
        },
        {
          "id": "f88f6ca2-b574-4165-a1f1-2568ec66d66c",
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
              "id": "3f34cf2b-affe-4d0e-89a6-6e4fcc90b7c4"
            }
          ]
        },
        {
          "id": "98ac8305-e1c8-4c33-a419-2ba40c08cbc6",
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
              "id": "d03a36ef-78c2-45cd-92b6-8dc2b73cc634"
            }
          ]
        }
      ]
    },
    {
      "name": "Global",
      "item": [
        {
          "id": "c11a9320-c2fa-421d-9091-d3cf6279e1d7",
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
              "id": "a3e04292-5416-4681-bccb-e529f9c4ef88"
            }
          ]
        },
        {
          "id": "4418431e-a32e-4e70-840d-b64b27cb7ad7",
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
              "id": "20037510-fd5c-4f59-817d-2ae8c5b53bcf"
            }
          ]
        }
      ]
    },
    {
      "name": "Attachment",
      "item": [
        {
          "id": "5e3ea811-4c6b-45d0-a421-802b6088b09e",
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
              "id": "1b6c1b20-1e82-4904-906d-e0a6e3eecb1a"
            }
          ]
        },
        {
          "id": "96b204ff-4482-4055-b18e-cdac377a8f14",
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
              "id": "adcaf518-a10d-44ea-99ac-497308ddc1ec"
            }
          ]
        },
        {
          "id": "14ae6d22-498d-409d-a4e7-a70f926bb6f9",
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
              "id": "677caf1d-4123-4416-924f-58324abaf23d"
            }
          ]
        }
      ]
    },
    {
      "name": "Metadataan",
      "item": [
        {
          "id": "5ae01a9b-ce2c-441f-9e73-f942a655885d",
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
              "id": "f2cd5056-6c69-44cb-9e97-8270d0453948"
            }
          ]
        }
      ]
    },
    {
      "name": "Contents",
      "item": [
        {
          "id": "15b345a0-6bfe-43eb-beb2-7591e140e6be",
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
              "id": "0bad2461-c11d-4441-9a5e-7d43056bec20"
            }
          ]
        }
      ]
    },
    {
      "name": "Audit",
      "item": [
        {
          "id": "5eeead98-e247-4a0c-b233-8b6334a31650",
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
              "id": "ffc0f8b2-2f3c-477f-8204-c36f839e5dc1"
            }
          ]
        }
      ]
    },
    {
      "name": "System",
      "item": [
        {
          "id": "54283d01-149c-4476-bd9f-08224002f3a8",
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
              "id": "40feebf3-517a-4f05-b220-6a6dc1679d92"
            }
          ]
        }
      ]
    },
    {
      "name": "Comments",
      "item": [
        {
          "id": "016db9a9-d114-48e5-a382-04e74842f826",
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
              "id": "242a58f9-9ab2-4296-90a2-3c477555b897"
            }
          ]
        },
        {
          "id": "91888fda-83b0-45b4-8a78-c9a903e98952",
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
              "id": "0bdcd171-1c15-4fba-b663-6f54f7710daf"
            }
          ]
        }
      ]
    },
    {
      "name": "Comment",
      "item": [
        {
          "id": "02c3a115-fc28-4ac6-ba93-9d1314d65f74",
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
              "id": "07e48f85-41fa-4fd9-abe4-0f496315aea5"
            }
          ]
        },
        {
          "id": "7a604e29-7508-4a54-b1f3-077cf5dff26f",
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
              "id": "e8cde3bc-94dd-419d-b76e-3c9d05192d0e"
            }
          ]
        },
        {
          "id": "be7c6a3f-a65f-44b8-8074-5906101765a5",
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
              "id": "38683dde-c9ef-4202-b44d-d807f0c20930"
            }
          ]
        },
        {
          "id": "a8e64836-4e4f-422a-914c-3951007fb37d",
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
              "id": "c4e63386-2f96-47b5-b437-063ca2c4ba71"
            }
          ]
        },
        {
          "id": "1312b74f-9ff8-412f-b3fb-95760bbdbd43",
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
              "id": "c80748e7-098d-40e0-84f6-09581919d038"
            }
          ]
        },
        {
          "id": "f562cffb-c621-4f3e-b0d3-9b263abb9318",
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
              "id": "35841a32-8b5a-4191-857d-bb28c51e0771"
            }
          ]
        },
        {
          "id": "68b35e3b-2e55-4333-b2fe-ca9636750f9e",
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
              "id": "cd5e5958-87dc-477d-9f1d-6110e714551d"
            }
          ]
        }
      ]
    },
    {
      "name": "Component",
      "item": [
        {
          "id": "52f442ae-325b-4167-89c6-e81a176c887b",
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
              "id": "6e3d836e-5c45-46d4-b932-b87874a71353"
            }
          ]
        },
        {
          "id": "b3240a6d-838c-4a19-b158-3ed82260cb09",
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
              "id": "df8bb9e5-90c0-4ad4-be9b-c2215113c613"
            }
          ]
        },
        {
          "id": "1d2e843f-37f8-4087-8422-e97510a04095",
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
              "id": "bf8a45be-9a39-47e7-93c4-c110815a2ae8"
            }
          ]
        },
        {
          "id": "6e8f8c3f-c035-45e7-a00a-81edaf44dbb4",
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
              "id": "6f37ec72-5e97-470a-8511-b33d14ccb090"
            }
          ]
        },
        {
          "id": "955e7025-b933-4cee-bfc8-169b840c455d",
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
              "id": "f6199e00-0104-4411-8112-2d73238d4e4e"
            }
          ]
        }
      ]
    },
    {
      "name": "Selected",
      "item": [
        {
          "id": "c338473e-66e6-42f9-8c2b-47c9839c81c0",
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
              "id": "79e52ba7-1658-4f65-800d-cb7b304c284c"
            }
          ]
        }
      ]
    },
    {
      "name": "Select",
      "item": [
        {
          "id": "19343204-725b-4d95-b15c-09b6ae14b50d",
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
              "id": "63ba7d8b-6603-4590-9fb7-536dae498225"
            }
          ]
        }
      ]
    },
    {
      "name": "Disable",
      "item": [
        {
          "id": "1c706947-cf44-4926-961b-f558bc7cb285",
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
              "id": "eabbcbd5-6623-4224-ba86-cb88a40e234b"
            }
          ]
        }
      ]
    },
    {
      "name": "Time",
      "item": [
        {
          "id": "03ede5b9-a995-4e08-a62b-18cf50646b2e",
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
              "id": "e9142fa5-9f8d-4ff7-90cd-4beaffef5c0c"
            }
          ]
        },
        {
          "id": "1e3f5c1c-b2bb-4549-b699-60e7648a6deb",
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
              "id": "0ee76d26-c18d-47c5-a865-6c2584658b98"
            }
          ]
        }
      ]
    },
    {
      "name": "Custom",
      "item": [
        {
          "id": "f5dde79c-7d64-4325-b0f6-69ec39abeab3",
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
              "id": "554a9d9c-f97b-43bf-8c44-7a8467ae4a50"
            }
          ]
        },
        {
          "id": "9145b6c8-4416-4766-899a-240503f0b312",
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
              "id": "a1e9b301-9151-4cfa-af27-b361abfe5645"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboards",
      "item": [
        {
          "id": "dfd6fdbb-4c55-47e5-bd8b-26fcde691fee",
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
              "id": "7366add6-604e-4e0f-bc60-b4ef1947ac56"
            }
          ]
        }
      ]
    },
    {
      "name": "Dashboard",
      "item": [
        {
          "id": "f0940f33-295c-4cc4-8a7e-d768c9aef42f",
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
              "id": "ee44a38b-e117-49c9-8e1d-6a2e9bee046a"
            }
          ]
        },
        {
          "id": "6dc3b8bd-3921-45a3-9353-f2e18ede8818",
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
              "id": "e938aef1-d7f4-49c2-b0c6-c14d659cd152"
            }
          ]
        },
        {
          "id": "27876b04-4e87-4b90-89a4-da685a8003f3",
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
              "id": "6b58caa8-c96f-4fff-adb7-39c5451be2ea"
            }
          ]
        },
        {
          "id": "322b01d8-fbd1-444c-b657-c27feb99fc9b",
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
              "id": "3bf43de4-fb9c-4d78-983d-bcdefe5a13dc"
            }
          ]
        }
      ]
    },
    {
      "name": "Evaluate",
      "item": [
        {
          "id": "ae948a13-a788-45e2-b46a-fa5e71ad911e",
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
              "id": "a257d97f-986e-45eb-9ea7-1ead48d1e7a8"
            }
          ]
        }
      ]
    },
    {
      "name": "Fields",
      "item": [
        {
          "id": "2298b20f-5236-48e4-b9cf-faa3061c2749",
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
              "id": "d814a7d0-1cf4-43e7-87c8-e208e7a4cfc6"
            }
          ]
        }
      ]
    },
    {
      "name": "Issue",
      "item": [
        {
          "id": "c67eb734-f441-473d-8d0c-d55e081d427e",
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
              "id": "9f467ac2-d940-4344-ad8e-80502ee8489b"
            }
          ]
        },
        {
          "id": "16951c7d-9fee-4a55-b913-890de2312261",
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
              "id": "5df532da-b6c3-4ae1-a45d-0ca41302db98"
            }
          ]
        },
        {
          "id": "2405cd80-15a6-4b50-8797-b684db4a4a36",
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
              "id": "8afd4815-84c1-47ac-bb9e-1518c31d86f3"
            }
          ]
        },
        {
          "id": "0b31d02c-41b6-43cf-8fe1-3be3e3d02bd5",
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
              "id": "3c639bae-3c85-4758-b718-80a2f3e200aa"
            }
          ]
        },
        {
          "id": "4a808c98-514b-4cfe-bcaa-d4457546dc24",
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
              "id": "02ab50e3-771a-403d-815f-24dd65102a02"
            }
          ]
        },
        {
          "id": "82d26c5c-8fa8-4c96-a365-f85ade6282cb",
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
              "id": "c9414408-a345-4ad1-a2d8-3cd3f3573970"
            }
          ]
        },
        {
          "id": "c3183164-8670-4506-8ad1-21537c0eb6a2",
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
              "id": "864025e4-0596-4df8-a1a5-ea76cca7f4f3"
            }
          ]
        },
        {
          "id": "24279a1e-2963-4308-a1d6-30f26b434a9d",
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
              "id": "1aa997ac-5050-4e65-8e0d-2cd55caa9152"
            }
          ]
        },
        {
          "id": "77244d1c-8c0d-4649-8da2-7737eff1ecfd",
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
              "id": "0c9e3e3a-9268-4faf-a776-2910cd1aca9d"
            }
          ]
        },
        {
          "id": "784bc369-7ff2-41fe-b9c0-b2291c788e1a",
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
              "id": "83b767d1-edfe-48b8-8bd2-6f30bbfdbb0e"
            }
          ]
        },
        {
          "id": "bc8bea91-d50d-48d1-930f-89c8fa7873ea",
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
              "id": "90380a1c-9854-4433-983d-28ef0984cefc"
            }
          ]
        },
        {
          "id": "1f03f0ef-dcf6-48be-a9aa-0b166cd9271e",
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
              "id": "c2937c65-ca27-4b79-a8ea-9f3551fa23c4"
            }
          ]
        }
      ]
    },
    {
      "name": "Selectable",
      "item": [
        {
          "id": "c96a247f-1f1c-4726-8b8d-fa5a01f1dcb6",
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
              "id": "8dd19af7-5a71-490c-a0a4-93a6028d30cf"
            }
          ]
        }
      ]
    },
    {
      "name": "Visible",
      "item": [
        {
          "id": "49958a2e-65fa-4230-9ce7-56a913d1cf37",
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
              "id": "acbf55b0-3302-4400-8196-4014fb593019"
            }
          ]
        }
      ]
    },
    {
      "name": "Replace",
      "item": [
        {
          "id": "938d31e4-b5ed-463a-b0d5-f6d6ce462483",
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
              "id": "e1efdd45-e6cf-471d-a47b-0ca478d083f3"
            }
          ]
        }
      ]
    },
    {
      "name": "Filters",
      "item": [
        {
          "id": "05d7cf29-25f2-4a3a-8bfa-7e479974b56b",
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
              "id": "539bc336-ee05-42ae-80ed-014b586583c3"
            }
          ]
        }
      ]
    },
    {
      "name": "Filter",
      "item": [
        {
          "id": "7e7eb0bc-bd09-464d-9ca3-9362fd9c19c1",
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
              "id": "3c648eb0-38eb-4d15-965d-8a8bc2eba60f"
            }
          ]
        },
        {
          "id": "b3c78794-6b01-4306-8074-c95bbc097699",
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
              "id": "22e626f4-5544-4b52-a894-6e6b4dce9941"
            }
          ]
        },
        {
          "id": "30a0b53d-6c23-496d-83fe-439e2050e8e7",
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
              "id": "d8021561-1410-441a-a239-3d77abcb02af"
            }
          ]
        },
        {
          "id": "efb4e014-2145-497e-807e-f65b8d39b75c",
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
              "id": "0c5d7af7-2580-4ea8-965f-f1347680547b"
            }
          ]
        },
        {
          "id": "348306a8-d561-4d60-9349-440b31a22f85",
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
              "id": "774e8bed-bc19-470a-b6a6-186890f4e47f"
            }
          ]
        }
      ]
    },
    {
      "name": "Default",
      "item": [
        {
          "id": "5aadc82b-511b-4843-9360-329f802760ef",
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
              "id": "1882c104-e010-4441-af37-698bc906ef43"
            }
          ]
        }
      ]
    },
    {
      "name": "Favourite",
      "item": [
        {
          "id": "40a70006-cf36-4e83-9d23-89204b868ff3",
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
              "id": "ca5e308e-4e96-467f-9aa9-e302d15a0ed8"
            }
          ]
        }
      ]
    },
    {
      "name": "My",
      "item": [
        {
          "id": "b66db8c9-c353-450b-a93e-41f964bbb05a",
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
              "id": "08c95952-6483-4bac-875c-3ca23ce66ef9"
            }
          ]
        }
      ]
    },
    {
      "name": "Searchfilters",
      "item": [
        {
          "id": "b103c333-c481-4e68-8bce-92d46dcefd5e",
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
              "id": "1caad8c4-270d-4242-b115-a44c85ec526a"
            }
          ]
        }
      ]
    },
    {
      "name": "Columns",
      "item": [
        {
          "id": "5b5a0f38-0e2c-41ef-8fce-65c560529b1d",
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
              "id": "a4bb82da-1b5f-466c-a456-c86efb768729"
            }
          ]
        }
      ]
    },
    {
      "name": "Reset",
      "item": [
        {
          "id": "9c77af05-14c4-4a2c-8589-94275dd69602",
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
              "id": "bb175d7c-db36-4a37-810a-70f07ffd03ce"
            }
          ]
        }
      ]
    },
    {
      "name": "Remove",
      "item": [
        {
          "id": "c574ad8d-ef57-4398-a382-45fb7c3c7aca",
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
              "id": "3aa9a969-8dc3-4786-9600-2dc87299b67d"
            }
          ]
        },
        {
          "id": "feaf798e-01b5-4359-8052-635c7acfe6c5",
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
              "id": "1251a1ab-2048-4662-a845-4bc5b2e9636e"
            }
          ]
        },
        {
          "id": "b82db225-ccca-46ae-af87-15be21881f2a",
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
              "id": "4f2f662e-038f-4dd4-b8f0-d4d435bbe30b"
            }
          ]
        }
      ]
    },
    {
      "name": "Share",
      "item": [
        {
          "id": "ded25e60-82f7-4fa0-8e14-960fc5275138",
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
              "id": "ede57900-da19-41fc-8132-27f8cb5da48a"
            }
          ]
        },
        {
          "id": "c0c5b9e5-299b-4e66-bb4a-b0ddee87e40c",
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
              "id": "8e5ba302-3fb0-4441-b339-424dd0d1a481"
            }
          ]
        },
        {
          "id": "bf559782-2c7e-4700-a1db-0c868f127d53",
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
              "id": "86732eba-7bc3-4266-ba82-40cf6b514ccd"
            }
          ]
        },
        {
          "id": "d40306c3-dbdf-4f1e-a98a-908cf8406c29",
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
              "id": "f3656e02-6e16-47cf-a1ee-ff45cc0df9db"
            }
          ]
        }
      ]
    },
    {
      "name": "Group",
      "item": [
        {
          "id": "08522ba0-1c56-4b86-aed9-c86bfb3e820f",
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
              "id": "adb7fff3-aaf1-4fb4-a3a0-8e0c42c72c6b"
            }
          ]
        },
        {
          "id": "a44820b1-0b5f-43e2-9349-b1cfcaf6cd9d",
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
              "id": "f7e02a01-eaae-46f8-9afb-d0e5fbd463fd"
            }
          ]
        }
      ]
    },
    {
      "name": "Users",
      "item": [
        {
          "id": "c15f0244-a9c6-411d-9627-411ad531b48f",
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
              "id": "7aa88312-a1f1-46c2-a7ca-98ef4603af35"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "5f868d1a-4e3e-4281-b7f8-e2d93480e44d",
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
              "id": "b4abb6ed-531f-42bb-bd00-ce7855b4e93d"
            }
          ]
        }
      ]
    },
    {
      "name": "Find",
      "item": [
        {
          "id": "e8d4450d-d7fc-4a47-985e-5208d4a5770f",
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
              "id": "f5e01a5c-6878-4826-b066-ad2370c8a674"
            }
          ]
        },
        {
          "id": "75663d3c-44f2-4381-a1cb-14f5a122cb12",
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
              "id": "ce4e48d7-7f64-4f21-8a74-67b1a871a649"
            }
          ]
        }
      ]
    },
    {
      "name": "Issues",
      "item": [
        {
          "id": "33257de0-1f8e-4529-91cc-33254c8f4c71",
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
              "id": "1fa8a936-6221-4c53-a645-d6841703346d"
            }
          ]
        }
      ]
    },
    {
      "name": "Create",
      "item": [
        {
          "id": "8fda7d33-6620-4e24-b9bf-354b6024f873",
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
              "id": "6cd1a3e8-ad1f-4cba-828d-55c3d5b0d3db"
            }
          ]
        }
      ]
    },
    {
      "name": "Bulk",
      "item": [
        {
          "id": "0f09986d-a09a-45ad-bf72-9857121bc88a",
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
              "id": "d6fb2242-38d4-469c-b4ee-ed1ff4152435"
            }
          ]
        },
        {
          "id": "3cfcccc6-b104-4ca6-9f6d-594cd293e786",
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
              "id": "54dbcde3-8b39-4ff9-bc48-dfdc630d58a4"
            }
          ]
        }
      ]
    },
    {
      "name": "Edit",
      "item": [
        {
          "id": "3fb4a403-7be0-4d1c-ab35-dd9b1cb6ae92",
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
              "id": "391d82aa-7b21-4b5c-94b9-30bda320b651"
            }
          ]
        },
        {
          "id": "064fd04b-aa1f-468b-96b1-ff73b90f900c",
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
              "id": "d790c497-1a7b-4f35-9cf1-a83a5d35bff8"
            }
          ]
        }
      ]
    },
    {
      "name": "Assign",
      "item": [
        {
          "id": "462f7cc0-c725-4464-b0f7-9687dd5e01f0",
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
              "id": "d4a1c339-4471-49f2-97f6-427600980381"
            }
          ]
        }
      ]
    },
    {
      "name": "Change",
      "item": [
        {
          "id": "33b6afd7-4fad-4a07-933e-c384c4a657ab",
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
              "id": "5ef12fbe-27f7-479a-8e50-65cfccf9d7bd"
            }
          ]
        }
      ]
    },
    {
      "name": "Notify",
      "item": [
        {
          "id": "5e8f02dc-6225-422b-9978-4f108bd03cd3",
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
              "id": "0e26dd40-1ea2-4213-8c80-778a1d6e870f"
            }
          ]
        }
      ]
    },
    {
      "name": "Remote",
      "item": [
        {
          "id": "69d9293c-2081-455e-846c-a031d589637c",
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
              "id": "cffa9e86-e50b-4695-90ed-0ad430bdd21a"
            }
          ]
        },
        {
          "id": "5187331b-2126-4109-b2c8-58ee1b7eefe7",
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
              "id": "148792c1-68c5-4ec0-a14a-3e30033bbcc2"
            }
          ]
        },
        {
          "id": "4992e000-db25-4a68-a797-57944bc71091",
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
              "id": "7a51dac8-4523-40b9-8490-eb3db2d7c454"
            }
          ]
        },
        {
          "id": "16d59ddc-d4b2-4736-a143-9a39e1f6919c",
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
              "id": "8230cad9-2a43-4080-beee-b15082f8c59b"
            }
          ]
        },
        {
          "id": "bd0c7f7b-633b-43c2-aa97-afb83409bdf8",
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
              "id": "e45314de-57ab-4ecf-8864-e12889bdbb5c"
            }
          ]
        }
      ]
    },
    {
      "name": "Update",
      "item": [
        {
          "id": "18b6a249-d28a-4087-8f55-bf005db953f1",
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
              "id": "1709eedc-151a-4a1b-9166-df72df68c946"
            }
          ]
        }
      ]
    },
    {
      "name": "Transitions",
      "item": [
        {
          "id": "6d07ba35-9a09-420e-9d27-92304ef322da",
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
              "id": "1dd1d3f4-0453-4d52-90a4-90458044b3bc"
            }
          ]
        }
      ]
    },
    {
      "name": "Do",
      "item": [
        {
          "id": "a191e4a0-19be-4f23-83fe-8a9d962d0d3b",
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
              "id": "6e3a0381-82a2-4a19-b9c1-463cd92b63ad"
            }
          ]
        }
      ]
    },
    {
      "name": "Votes",
      "item": [
        {
          "id": "2e2758c4-8ab0-4fbc-b846-9298f17dcb8a",
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
              "id": "6f3b3ae7-9ab0-48d3-a9d5-ae9de1813237"
            }
          ]
        }
      ]
    },
    {
      "name": "Vote",
      "item": [
        {
          "id": "c276ec52-bdf5-49b9-a4df-062641f81c15",
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
              "id": "49895b11-5c80-4585-9641-65c0b4ff907d"
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