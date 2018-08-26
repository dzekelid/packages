---
swagger: "2.0"
x-collection-name: AWS Inspector
x-complete: 1
info:
  title: AWS Inspector API
  version: 1.0.0
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
---