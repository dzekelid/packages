---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Update an order shipping package
  description: Updates an order shipping package. The ID of the order and the ID of
    the order shipping package must be specified.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/orders/{orderId}/shipping/packages:
    get:
      summary: List order shipping packages
      description: Lists order shipping packages. The ID of the order must be specified.
      operationId: getRestOrdersOrderShippingPackages
      x-api-path-slug: restordersorderidshippingpackages-get
      parameters:
      - in: query
        name: columns
        description: The properties to be loaded
      - in: path
        name: orderId
      - in: query
        name: with
        description: Possible value is labelBase64
      responses:
        200:
          description: OK
      tags:
      - List
      - Order
      - Shipping
      - Packages
    post:
      summary: Create an order shipping package
      description: Creates an order shipping package. The ID of the order must be
        specified.
      operationId: postRestOrdersOrderShippingPackages
      x-api-path-slug: restordersorderidshippingpackages-post
      parameters:
      - in: body
        name: /rest/orders/{orderId}/shipping/packages
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: orderId
      responses:
        200:
          description: OK
      tags:
      - Order
      - Shipping
      - Package
    delete:
      summary: Delete all order shipping packages for an order
      description: Deletes all order shipping packages for an order. The ID of the
        order must be specified.
      operationId: deleteRestOrdersOrderShippingPackages
      x-api-path-slug: restordersorderidshippingpackages-delete
      parameters:
      - in: path
        name: orderId
      responses:
        200:
          description: OK
      tags:
      - Order
      - Shipping
      - Packagesan
      - Order
  /rest/orders/shipping/package_types:
    get:
      summary: List shipping package types
      description: List shipping package types.
      operationId: getRestOrdersShippingPackageTypes
      x-api-path-slug: restordersshippingpackage-types-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Shipping
      - Package
      - Types
  /rest/orders/shipping/package_types/{shippingPackageTypeId}:
    get:
      summary: Get a shipping package type
      description: Gets a shipping package type. The ID of the shipping package type
        must be specified.
      operationId: getRestOrdersShippingPackageTypesShippingpackagetype
      x-api-path-slug: restordersshippingpackage-typesshippingpackagetypeid-get
      parameters:
      - in: path
        name: shippingPackageTypeId
      responses:
        200:
          description: OK
      tags:
      - Shipping
      - Package
      - Type
  /rest/orders/{orderId}/packagenumbers:
    get:
      summary: List package numbers of an order
      description: Lists the package numbers of an order. The ID of the order must
        be specified.
      operationId: getRestOrdersOrderPackagenumbers
      x-api-path-slug: restordersorderidpackagenumbers-get
      parameters:
      - in: path
        name: orderId
      responses:
        200:
          description: OK
      tags:
      - List
      - Package
      - Numbers
      - Of
      - Order
  /rest/orders/{orderId}/shipping/packages/{orderShippingPackageId}:
    delete:
      summary: Delete an order shipping package
      description: Deletes an order shipping package. The ID of the order and the
        ID of the order shipping package must be specified.
      operationId: deleteRestOrdersOrderShippingPackagesOrdershippingpackage
      x-api-path-slug: restordersorderidshippingpackagesordershippingpackageid-delete
      parameters:
      - in: path
        name: orderId
      - in: path
        name: orderShippingPackageId
      responses:
        200:
          description: OK
      tags:
      - Order
      - Shipping
      - Package
    get:
      summary: Get an order shipping package
      description: Gets an order shipping package. The ID of the order and the ID
        of the order shipping package must be specified.
      operationId: getRestOrdersOrderShippingPackagesOrdershippingpackage
      x-api-path-slug: restordersorderidshippingpackagesordershippingpackageid-get
      parameters:
      - in: query
        name: columns
        description: The properties to be loaded
      - in: path
        name: orderId
      - in: path
        name: orderShippingPackageId
      responses:
        200:
          description: OK
      tags:
      - Order
      - Shipping
      - Package
    put:
      summary: Update an order shipping package
      description: Updates an order shipping package. The ID of the order and the
        ID of the order shipping package must be specified.
      operationId: putRestOrdersOrderShippingPackagesOrdershippingpackage
      x-api-path-slug: restordersorderidshippingpackagesordershippingpackageid-put
      parameters:
      - in: body
        name: /rest/orders/{orderId}/shipping/packages/{orderShippingPackageId}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: orderId
      - in: path
        name: orderShippingPackageId
      responses:
        200:
          description: OK
      tags:
      - Order
      - Shipping
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