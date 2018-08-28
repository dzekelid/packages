{
  "info": {
    "name": "Plentymarkets Get a shipping package type",
    "_postman_id": "d61c274b-1f6d-4430-aaf5-434fb866bfec",
    "description": "Gets a shipping package type. The ID of the shipping package type must be specified.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "20f5c320-852c-49aa-93c6-e7704768fc66",
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
              "id": "77e22324-aa36-4646-981a-e57e1c6fa0b3"
            }
          ]
        },
        {
          "id": "d8a09cfd-0e00-4e6f-a6c1-b22e0c5afeac",
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
              "id": "7b758ddd-5176-465f-83fd-47e5be8d0e34"
            }
          ]
        }
      ]
    },
    {
      "name": "Shipping",
      "item": [
        {
          "id": "75c84331-1dbe-4619-b4a3-075410118dd4",
          "name": "getRestOrdersShippingPackageTypesShippingpackagetype",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/orders/shipping/package_types/:shippingPackageTypeId"
              ],
              "variable": [
                {
                  "id": "shippingPackageTypeId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets a shipping package type. The ID of the shipping package type must be specified."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0a8e3a06-96f6-41be-a63b-dbbc3ec6893e"
            }
          ]
        }
      ]
    }
  ]
}