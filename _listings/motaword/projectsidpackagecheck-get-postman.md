{
  "info": {
    "name": "Mota Word Track the status of translation packaging.",
    "_postman_id": "cff39910-ad39-471e-8255-42be9972909f",
    "description": "This request will tell you the current progress of the translation packaging. You will use the 'key' provided by the /package call.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Projects",
      "item": [
        {
          "id": "8a009203-538c-4b40-88d7-03aa18b89f47",
          "name": "getProjects",
          "request": {
            "url": "http://api.motaword.com/projects?page=%7B%7D&per_page=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of your projects."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6080d407-2989-4294-875e-a766102a2bcd"
            }
          ]
        },
        {
          "id": "8cf5dab4-1284-4f08-822d-1722e2865742",
          "name": "createProject",
          "request": {
            "url": "http://api.motaword.com/projects",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "callback_url",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "custom",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "documents",
                  "value": "[{}]",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "glossaries",
                  "value": "[{}]",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "source_language",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "styleguides",
                  "value": "[{}]",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "target_languages",
                  "value": "[{}]",
                  "disabled": false,
                  "description": ""
                }
              ]
            },
            "description": "Create a new project"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c6d3436-330f-4a9b-b8ad-981eea4e5ca8"
            }
          ]
        },
        {
          "id": "6f32a09e-772f-472c-a5db-c4dd584e4ad3",
          "name": "getProject",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id"
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
            "body": {
              "mode": "raw"
            },
            "description": "Get single project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "195f9fa4-6247-4b95-a959-068d3505ca3e"
            }
          ]
        },
        {
          "id": "a815f190-96c0-4294-ad45-533d30ed24ca",
          "name": "updateProject",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id"
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
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "callback_url",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "custom",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "source_language",
                  "value": "{}",
                  "disabled": false,
                  "description": ""
                },
                {
                  "key": "target_languages",
                  "value": "[{}]",
                  "disabled": false,
                  "description": ""
                }
              ]
            },
            "description": "Update project language pairs."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "59fee090-7093-47b4-b8f7-6131dfb01b88"
            }
          ]
        },
        {
          "id": "22eb62f5-b1db-4f4c-aa10-adbcc864d02a",
          "name": "deleteProject",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id"
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
            "body": {
              "mode": "raw"
            },
            "description": "Delete(cancel) a project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "39010649-2aac-4476-9283-c16da9538785"
            }
          ]
        },
        {
          "id": "0889e6e3-a477-4b68-84e0-c0026fabc8fb",
          "name": "triggerCallback",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id/callback/:actionType"
              ],
              "variable": [
                {
                  "id": "actionType",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Trigger a call to your callback url related to this project.."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f6a0c0e7-a91b-4116-9c5b-86fd515271d7"
            }
          ]
        },
        {
          "id": "39b8a7b1-4f95-4318-a000-b118dcc67419",
          "name": "cancelProject",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id/cancel"
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
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "reason",
                  "value": "{}",
                  "disabled": false,
                  "description": "Cancellation reason"
                }
              ]
            },
            "description": "Cancel your translation project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ef1cb805-55f3-4152-b547-0ab013820616"
            }
          ]
        },
        {
          "id": "3715c097-dd0f-4ae6-a708-1ba6b4bdfc72",
          "name": "download",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id/download"
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
            "body": {
              "mode": "raw"
            },
            "description": "Download the latest translation package. You must have given a /package call beforehand and wait until the packaging status is 'completed'."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0af0ba60-b2ff-45aa-bc35-3fce7aa606b8"
            }
          ]
        },
        {
          "id": "5eec6070-56d1-4747-a5a4-58632fb5bcf1",
          "name": "downloadLanguage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id/download/:language"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "language",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Download only the translation package of this language. You must have given a /package call beforehand and wait until the packaging status is 'completed'."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8760a9d8-c89c-4f29-9cf6-78b83dd7c57e"
            }
          ]
        },
        {
          "id": "d0cf88eb-4f91-4317-b65d-1e6cabd65e75",
          "name": "launchProject",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id/launch"
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
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "budget_code",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional with corporate accounts"
                },
                {
                  "key": "payment_code",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional"
                },
                {
                  "key": "payment_method",
                  "value": "{}",
                  "disabled": false,
                  "description": "Optional"
                }
              ]
            },
            "description": "Launch your translation project."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4be78577-bcf7-4907-9da7-4087c85d1289"
            }
          ]
        },
        {
          "id": "e2fe2a48-c742-43e8-aba7-fe6bd9186e9a",
          "name": "package",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id/package"
              ],
              "query": [
                {
                  "key": "async",
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
            "body": {
              "mode": "raw"
            },
            "description": "Package the translation project, make it ready to be downloaded."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c35134cb-611b-48a6-8282-6908d5381f56"
            }
          ]
        },
        {
          "id": "d0d1545e-19bc-41b5-9842-b4ac23fb9a11",
          "name": "trackPackage",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.motaword.com",
              "path": [
                "projects/:id/package/check"
              ],
              "query": [
                {
                  "key": "key",
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
            "body": {
              "mode": "raw"
            },
            "description": "This request will tell you the current progress of the translation packaging. You will use the 'key' provided by the /package call."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ebe6fe67-b560-477e-b22c-24afab86e293"
            }
          ]
        }
      ]
    }
  ]
}