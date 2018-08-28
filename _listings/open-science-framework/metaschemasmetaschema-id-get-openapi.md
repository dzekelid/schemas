---
swagger: "2.0"
x-collection-name: Open Science Framework
x-complete: 0
info:
  title: Open Science Framework Retrieve a metaschema
  description: |-
    Retrieves the details of a given metaschema.

    Metaschemas describe the supplemental questions that accompany a registration.

    #### Returns
    Returns a JSON object with a `data` key containing the representation of the requested metaschema, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  contact:
    name: OSF
    url: https://osf.io/support
    email: support@osf.io
  version: "2.0"
host: test-api.osf.io
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /metaschemas/:
    get:
      summary: List all metaschemas
      description: |-
        A paginated list of all active metaschemas.
        Metaschemas describe the supplemental questions that accompany a registration.
        #### Returns
        Returns a JSON object containing `data` and `links` keys.

        The `data` key contains an array of 10 metaschemas. Each resource in the array is a separate metaschema object.

        The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

        This request should never return an error.
      operationId: metaschemas_list
      x-api-path-slug: metaschemas-get
      responses:
        200:
          description: OK
      tags:
      - Metaschemas
  /metaschemas/{metaschema_id}:
    get:
      summary: Retrieve a metaschema
      description: |-
        Retrieves the details of a given metaschema.

        Metaschemas describe the supplemental questions that accompany a registration.

        #### Returns
        Returns a JSON object with a `data` key containing the representation of the requested metaschema, if the request is successful.

        If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
      operationId: metaschemas_read
      x-api-path-slug: metaschemasmetaschema-id-get
      parameters:
      - in: path
        name: metaschema_id
        description: The unique identifier of the metaschema
      responses:
        200:
          description: OK
      tags:
      - Metaschemas
      - Metaschema
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