{
  "info": {
    "name": "Plentymarkets List order shipping packages",
    "_postman_id": "de77d045-1050-4655-9860-2485d0f8888b",
    "description": "Lists order shipping packages. The ID of the order must be specified.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "0f113d5f-2dbe-40db-a8a0-2e30c08a5674",
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
              "id": "1ff6de22-3640-4a01-a1b8-01c7c36f6619"
            }
          ]
        }
      ]
    }
  ]
}