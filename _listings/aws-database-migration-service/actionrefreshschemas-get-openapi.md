---
swagger: "2.0"
x-collection-name: AWS Database Migration Service
x-complete: 0
info:
  title: AWS Database Migration Service API Refresh Schemas
  version: 1.0.0
  description: Populates the schema for the specified endpoint.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeRefreshSchemasStatus:
    get:
      summary: Describe Refresh Schemas Status
      description: Returns the status of the RefreshSchemas operation.
      operationId: describeRefreshSchemasStatus
      x-api-path-slug: actiondescriberefreshschemasstatus-get
      parameters:
      - in: query
        name: EndpointArn
        description: The Amazon Resource Name (ARN) string that uniquely identifies
          the endpoint
        type: string
      responses:
        200:
          description: OK
      tags:
      - Schemas
  /?Action=DescribeSchemas:
    get:
      summary: Describe Schemas
      description: Returns information about the schema for the specified endpoint.
      operationId: describeSchemas
      x-api-path-slug: actiondescribeschemas-get
      parameters:
      - in: query
        name: EndpointArn
        description: The Amazon Resource Name (ARN) string that uniquely identifies
          the endpoint
        type: string
      - in: query
        name: Marker
        description: An optional pagination token provided by a previous     request
        type: string
      - in: query
        name: MaxRecords
        description: The maximum number of records to include in the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Schemas
  /?Action=RefreshSchemas:
    get:
      summary: Refresh Schemas
      description: Populates the schema for the specified endpoint.
      operationId: refreshSchemas
      x-api-path-slug: actionrefreshschemas-get
      parameters:
      - in: query
        name: EndpointArn
        description: The Amazon Resource Name (ARN) string that uniquely identifies
          the endpoint
        type: string
      - in: query
        name: ReplicationInstanceArn
        description: The Amazon Resource Name (ARN) of the replication instance
        type: string
      responses:
        200:
          description: OK
      tags:
      - Schemas
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