---
swagger: "2.0"
x-collection-name: MotaWord
x-complete: 0
info:
  title: Mota Word Package the translation of a specific target language to be downloaded.
  description: Package the translation of a specific target language to be downloaded..
  version: alpha-0.1.0
host: api.motaword.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /projects/{id}/package:
    post:
      summary: Package the translation of all languages to be downloaded.
      description: Package the translation project, make it ready to be downloaded.
      operationId: package
      x-api-path-slug: projectsidpackage-post
      parameters:
      - in: query
        name: async
        description: If you want to package and download the translation synchronously,
          mark this parameter as 0
      - in: path
        name: id
        description: Project ID
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Package
  /projects/{id}/package/check:
    get:
      summary: Track the status of translation packaging.
      description: This request will tell you the current progress of the translation
        packaging. You will use the 'key' provided by the /package call.
      operationId: trackPackage
      x-api-path-slug: projectsidpackagecheck-get
      parameters:
      - in: path
        name: id
        description: Project ID
      - in: query
        name: key
        description: This is the package tracking key provided in the response of
          a /package call
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Package
      - Check
  /projects/{id}/package/{language}:
    post:
      summary: Package the translation of a specific target language to be downloaded.
      description: Package the translation of a specific target language to be downloaded..
      operationId: packageLanguage
      x-api-path-slug: projectsidpackagelanguage-post
      parameters:
      - in: query
        name: async
        description: If you want to package and download the translation synchronously,
          mark this parameter as 0
      - in: path
        name: id
        description: Project ID
      - in: path
        name: language
        description: Language code
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Package
      - Language
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