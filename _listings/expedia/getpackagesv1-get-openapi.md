---
swagger: "2.0"
x-collection-name: Expedia
x-complete: 0
info:
  title: Expedia Get Packages
  description: Gets packages and supports changed flights and hotels for flexible
    shopping.
  version: 0.0.1
host: apim.expedia.com
basePath: x/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /getpackages/v1:
    get:
      summary: Get Packages
      description: Gets packages and supports changed flights and hotels for flexible
        shopping.
      operationId: get-packages
      x-api-path-slug: getpackagesv1-get
      parameters:
      - in: query
        name: adultsPerRoom[1]
        description: How many adults will stay in the given room
      - in: query
        name: destination
        description: The userss search string
      - in: query
        name: destinationId
        description: Region ID of the origin or destination
      - in: query
        name: fromDate
        description: The date the customer wants to leave the origin
      - in: query
        name: ftla
        description: TLA (airport code or metrocode) for the origin (ftla) or destination
          (ttla)
      - in: query
        name: numberOfRooms
        description: How many hotel rooms you want
      - in: query
        name: origin
        description: The users search string
      - in: query
        name: originId
        description: Region ID of the origin or destination
      - in: query
        name: packagePIID
        description: Taken from a previous package response
      - in: query
        name: packageTripType
        description: i
      - in: query
        name: packageType
        description: Supports different views of F+H package
      - in: query
        name: pageType
        description: Only for change hotel
      - in: query
        name: searchProduct
        description: i
      - in: query
        name: toDate
        description: The date the customer wants to leave the destination
      - in: query
        name: ttla
        description: TLA (airport code or metrocode) for the origin (ftla) or destination
          (ttla)
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Packages
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