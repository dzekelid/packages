{
  "info": {
    "name": "Expedia Get Packages",
    "_postman_id": "2751b649-985c-46e1-be43-ee0ccb873086",
    "description": "Gets packages and supports changed flights and hotels for flexible shopping.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "travel",
      "item": [
        {
          "id": "e026dd9c-fc34-414e-8c4f-f42ece12dd89",
          "name": "get-packages",
          "request": {
            "url": "http://apim.expedia.com/x/getpackages/v1?adultsPerRoom[1]=%7B%7D&destination=%7B%7D&destinationId=%7B%7D&fromDate=%7B%7D&ftla=%7B%7D&numberOfRooms=%7B%7D&origin=%7B%7D&originId=%7B%7D&packagePIID=%7B%7D&packageTripType=%7B%7D&packageType=%7B%7D&pageType=%7B%7D&searchProduct=%7B%7D&toDate=%7B%7D&ttla=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets packages and supports changed flights and hotels for flexible shopping"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "732901d0-35de-40de-9247-e2a44662f836"
            }
          ]
        }
      ]
    }
  ]
}