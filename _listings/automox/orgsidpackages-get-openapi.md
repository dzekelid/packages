---
swagger: "2.0"
x-collection-name: Automox
x-complete: 0
info:
  title: Automox Get Orgs Packages
  description: Returns all software packages discovered on all servers (endpoints)
    of an organization
  termsOfService: https://www.automox.com/
  contact:
    name: support@automox.com
  version: 1.0.0
host: console.automox.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /orgs/{id}/packages:
    get:
      summary: Get Orgs Packages
      description: Returns all software packages discovered on all servers (endpoints)
        of an organization
      operationId: returns-all-software-packages-discovered-on-all-servers-endpoints-of-an-organization
      x-api-path-slug: orgsidpackages-get
      parameters:
      - in: path
        name: id
        description: Organization ID
      responses:
        200:
          description: OK
      tags:
      - Orgs
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