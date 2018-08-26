{
  "info": {
    "name": "Automox Get Orgs Packages",
    "_postman_id": "df470fc8-e62b-42b5-b628-180790054a88",
    "description": "Returns all software packages discovered on all servers (endpoints) of an organization",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Events",
      "item": [
        {
          "id": "b805da87-05a7-4826-b6d2-ade67ba6e572",
          "name": "gets-all-event-objects-for-the-authenticated-user",
          "request": {
            "url": "http://console.automox.com/api/events",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets all `Event` objects for the authenticated user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2067a397-8d82-445a-963f-c2d9c383f404"
            }
          ]
        },
        {
          "id": "513e9a64-168e-4c81-a5dd-466501516663",
          "name": "gets-a-specific-event-object-for-the-authenticated-user",
          "request": {
            "url": {
              "protocol": "http",
              "host": "console.automox.com",
              "path": [
                "api",
                "events/:id"
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
            "description": "Gets a specific `Event` object for the authenticated user."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5b2cdbbb-caab-4189-a317-e97a91907a5c"
            }
          ]
        }
      ]
    },
    {
      "name": "Orgs",
      "item": [
        {
          "id": "e678e36b-c306-46bd-bee9-c36b8135cdd8",
          "name": "gets-all-organizations-for-the-api-key",
          "request": {
            "url": "http://console.automox.com/api/orgs",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets all organizations for the api key"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "484075bc-1427-45e6-bdd7-46aaa2791ffd"
            }
          ]
        },
        {
          "id": "9a9e06ec-e967-42e6-8b40-c98ac8742896",
          "name": "returns-all-software-packages-discovered-on-all-servers-endpoints-of-an-organization",
          "request": {
            "url": {
              "protocol": "http",
              "host": "console.automox.com",
              "path": [
                "api",
                "orgs/:id/packages"
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
            "description": "Returns all software packages discovered on all servers (endpoints) of an organization"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4415714-1685-49de-a3dd-d69964576b3d"
            }
          ]
        }
      ]
    }
  ]
}