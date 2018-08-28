---
swagger: "2.0"
x-collection-name: Watchful
x-complete: 0
info:
  title: 'Watchful '
  description: ""
  version: 1.0.0
host: watchful.li
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /packages:
    post:
      summary: ""
      description: ""
      operationId: packages.post
      x-api-path-slug: packages-post
      parameters:
      - in: formData
        name: file
        description: ZIP package
      responses:
        200:
          description: OK
      tags:
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