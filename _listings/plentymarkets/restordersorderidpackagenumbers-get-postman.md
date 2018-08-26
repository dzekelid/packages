{
  "info": {
    "name": "Plentymarkets List package numbers of an order",
    "_postman_id": "16acd11c-b86a-4d10-9161-a4a3bf5a8170",
    "description": "Lists the package numbers of an order. The ID of the order must be specified.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "b408bed3-389c-4231-9b09-5da49379301b",
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
              "id": "77c1d3ef-719e-4269-ad74-6fd75cad1bd4"
            }
          ]
        },
        {
          "id": "2ee95095-321c-4a47-ad98-dffc586b1992",
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
              "id": "fccf147e-8e05-4263-80af-6031aa721273"
            }
          ]
        },
        {
          "id": "7948d02c-a082-48ef-915d-6fe84b669148",
          "name": "getRestOrdersOrderPackagenumbers",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/orders/:orderId/packagenumbers"
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
            "description": "Lists the package numbers of an order. The ID of the order must be specified."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d054c483-f6f7-407f-9fb1-f9850c4b7318"
            }
          ]
        }
      ]
    },
    {
      "name": "Shipping",
      "item": [
        {
          "id": "a7705190-22ed-489d-bba1-8a6626781afb",
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
              "id": "15213451-f9c4-4d82-8499-29a01bd4dfb3"
            }
          ]
        }
      ]
    }
  ]
}