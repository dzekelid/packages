swagger: "2.0"
x-collection-name: Logicbroker
x-complete: 1
info:
  title: CommerceAPI
  version: 1.0.0
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