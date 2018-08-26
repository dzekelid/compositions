---
swagger: "2.0"
x-collection-name: Codefresh
x-complete: 1
info:
  title: Codefresh API
  description: codefresh-api-swagger2-0-specification
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
    delete:
      summary: Delete Compositions
      description: Delete compositions.
      operationId: deleteCompositions
      x-api-path-slug: compositionsid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Compositions
  /compositions/{identifier}/run:
    post:
      summary: Post Compositions Entifier Run
      description: Post compositions entifier run.
      operationId: postCompositionsEntifierRun
      x-api-path-slug: compositionsidentifierrun-post
      parameters:
      - in: path
        name: identifier
        description: id or name of a composition
      - in: body
        name: payload
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Compositions
      - Entifier
      - Run
---