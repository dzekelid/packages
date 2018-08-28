{
  "info": {
    "name": "Plentymarkets List shipping package types",
    "_postman_id": "eed010d4-c097-4fef-84ce-64d01318d1be",
    "description": "List shipping package types.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "104bcb3a-5295-4e7e-831a-9751e6f1b4bc",
          "name": "getRestOrdersOrderShippingPackages",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/orders/:orderId/shipping/packages"
              ],
              "query": [
                {
                  "key": "columns",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "with",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "orderId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Lists order shipping packages. The ID of the order must be specified."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d64ee978-0c9a-4d1d-9322-f726aab38140"
            }
          ]
        },
        {
          "id": "7bd463d8-dc6d-47c0-8f7b-ff5b9ee82914",
          "name": "getRestOrdersShippingPackageTypes",
          "request": {
            "url": "http://example.com/rest/orders/shipping/package_types",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "List shipping package types."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5c84ac57-e5b7-4655-aa75-18dfd05d1f3b"
            }
          ]
        }
      ]
    }
  ]
}