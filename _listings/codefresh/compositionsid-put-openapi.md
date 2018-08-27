---
swagger: "2.0"
x-collection-name: Codefresh
x-complete: 0
info:
  title: Codefresh Put Compositions
  description: Put compositions.
  termsOfService: http://www.codefresh.io
  contact:
    name: Codefresh api team
    url: http://www.codefresh.io
  version: 1.0.0
host: g.codefresh.io
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /compositions:
    get:
      summary: Get Compositions
      description: Get compositions.
      operationId: getCompositions
      x-api-path-slug: compositions-get
      responses:
        200:
          description: OK
      tags:
      - Compositions
    post:
      summary: Post Compositions
      description: Post compositions.
      operationId: postCompositions
      x-api-path-slug: compositions-post
      parameters:
      - in: body
        name: payload
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Compositions
  /compositions/{identifier}:
    get:
      summary: Get Compositions Entifier
      description: Get compositions entifier.
      operationId: getCompositionsEntifier
      x-api-path-slug: compositionsidentifier-get
      parameters:
      - in: path
        name: identifier
        description: id or name of a composition
      responses:
        200:
          description: OK
      tags:
      - Compositions
      - Entifier
  /compositions/{id}/duplicate:
    post:
      summary: Post Compositions Duplicate
      description: Post compositions duplicate.
      operationId: postCompositionsDuplicate
      x-api-path-slug: compositionsidduplicate-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Compositions
      - Duplicate
  /compositions/{id}:
    put:
      summary: Put Compositions
      description: Put compositions.
      operationId: putCompositions
      x-api-path-slug: compositionsid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: payload
        description: Update the name/variables/body of the composition with the id
          inserted
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Compositions
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