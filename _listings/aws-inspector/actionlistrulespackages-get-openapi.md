---
swagger: "2.0"
x-collection-name: AWS Inspector
x-complete: 0
info:
  title: AWS Inspector API List Rules Packages
  version: 1.0.0
  description: Lists all available Amazon Inspector rules packages.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeRulesPackages:
    get:
      summary: Describe Rules Packages
      description: |-
        Describes the rules packages that are specified by the ARNs of the rules
                 packages.
      operationId: describeRulesPackages
      x-api-path-slug: actiondescriberulespackages-get
      parameters:
      - in: query
        name: locale
        description: The locale that you want to translate a rules package description
          into
        type: string
      - in: query
        name: rulesPackageArns
        description: The ARN that specifies the rules package that you want to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - Rules Packages
  /?Action=ListRulesPackages:
    get:
      summary: List Rules Packages
      description: Lists all available Amazon Inspector rules packages.
      operationId: listRulesPackages
      x-api-path-slug: actionlistrulespackages-get
      parameters:
      - in: query
        name: maxResults
        description: You can use this parameter to indicate the maximum number of
          items you want in the         response
        type: string
      - in: query
        name: nextToken
        description: You can use this parameter when paginating results
        type: string
      responses:
        200:
          description: OK
      tags:
      - Rules Packages
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