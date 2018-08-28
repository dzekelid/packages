---
swagger: "2.0"
x-collection-name: Paccurate
x-complete: 0
info:
  title: Paccurate Post
  version: 0.1.1
  description: a pure-JSON endpoint for packing requests.
host: api.paccurate.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /:
    post:
      summary: Post
      description: a pure-JSON endpoint for packing requests.
      operationId: .post
      x-api-path-slug: post
      parameters:
      - in: body
        name: pack
        description: complete set of items, boxes, and parameters to pack
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Shipping
      - Packaging
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