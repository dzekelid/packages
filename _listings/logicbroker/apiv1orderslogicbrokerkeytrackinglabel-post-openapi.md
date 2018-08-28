---
swagger: "2.0"
x-collection-name: Logicbroker
x-complete: 0
info:
  title: Logic Broker CommerceAPI Generate a tracking label for a given package
  version: 1.0.0
  description: Request rate limited to 2 requests per second with bursts up to 25
    requests.
host: stage.commerceapi.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/Orders/{LogicbrokerKey}/TrackingLabel:
    post:
      summary: Generate a tracking label for a given package
      description: Request rate limited to 2 requests per second with bursts up to
        25 requests.
      operationId: Order_CreateTrackingLabel
      x-api-path-slug: apiv1orderslogicbrokerkeytrackinglabel-post
      parameters:
      - in: path
        name: LogicbrokerKey
        description: The Logicbroker key
      - in: body
        name: package
        description: Package details
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: useSenderAccount
        description: Set to true to use the senders shipping account
      responses:
        200:
          description: OK
      tags:
      - Generate
      - Tracking
      - Labela
      - Given
      - Package
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---