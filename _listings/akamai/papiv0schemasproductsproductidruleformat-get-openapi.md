---
swagger: "2.0"
x-collection-name: Akamai
x-complete: 0
info:
  title: Akamai API Get a Rule Format&#8217;s JSON Schema
  description: Get a Rule Format&#8217;s JSON Schema
  version: 1.0.0
host: developer.akamai.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /cloudlets/api/v2/schemas/{schemaName}:
    get:
      summary: Get a Schema
      description: Get a Schema
      operationId: cloudletsapiv2schemasschemaname
      x-api-path-slug: cloudletsapiv2schemasschemaname-get
      parameters:
      - in: query
        name: schemaName
        description: The name of the JSON schema file
        type: string
      responses:
        200:
          description: OK
      tags:
      - Cloudlets
      - Schemas
  /papi/v0/schemas/request/{filename}:
    get:
      summary: Get a Request&#8217;s JSON Schema
      description: Get a Request&#8217;s JSON Schema
      operationId: papiv0schemasrequestfilename
      x-api-path-slug: papiv0schemasrequestfilename-get
      parameters:
      - in: query
        name: filename
        description: Schema&#8217;s filename
        type: string
      responses:
        200:
          description: OK
      tags:
      - Papi
      - V0
      - Schemas
      - Request
      - Filename
  /papi/v0/schemas/products/{productId}/{ruleFormat}:
    get:
      summary: Get a Rule Format&#8217;s JSON Schema
      description: Get a Rule Format&#8217;s JSON Schema
      operationId: papiv0schemasproductsproductidruleformat
      x-api-path-slug: papiv0schemasproductsproductidruleformat-get
      parameters:
      - in: query
        name: productId
        description: Unique identifier for the product
        type: string
      - in: query
        name: ruleFormat
        description: Name of the rule format, either one frozen to a specific date,
          or representing the latest set of behaviors and criteria
        type: string
      responses:
        200:
          description: OK
      tags:
      - Papi
      - V0
      - Schemas
      - Products
      - Product
      - Ruleformat
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