---
swagger: "2.0"
x-collection-name: Watchful
x-complete: 1
info:
  title: Watchful
  description: watchful-resulted-from-the-need-for-a-single-unified-dashboard-to-easily-monitor-all-of-the-web-sites-in-our-portfolios--after-years-of-evolution-our-solution-has-matured-into-a-simple-complete-and-professional-service--
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
---