swagger: "2.0"
x-collection-name: IBM Watson
x-complete: 1
info:
  title: IBM Watson Machine Learning API
  description: -authorizationstep-by-step-instruction-how-to-use-watson-machine-learning-servicecan-be-found-herehttpsdatascience-ibm-comdocscontentanalyzedatamloverview-htmlcontextanalytics-ibm-watson-machine-learning-credentialsto-start-working-with-api-one-needs-to-generate-an-access-token-using-the-username-and-passwordavailable-on-the-service-credentials-tab-of-the-ibm-watson-machine-learning-service-instance-or-also-available-in-the-vcap-environment-variable-example-of-the-service-credentialsjson----url-httpsibmwatsonml-mybluemix-net----username-c1ef4b802ee2458eab92e9ca97ec657d----password-030528d45a3e4d4c92585d553513be6f----instance-id-a751c209954edc32b441ad56ce7a9f40example-of-obtaining-access-token-from-token-endpoint-using-http-basic-auth-for-details-please-refer-to-token-section-belowcurl-basic-user-usernamepassword-httpsibmwatsonml-mybluemix-netv3identitytokenthe-obtained-access-token-needs-to-be-prepended-with-bearer-word-and-it-needs-to-be-passed-in-the-authorization-header-for-api-calls-example-of-api-request-with-bearer-access-tokencurl-httpsibmwatsonml-mybluemix-netv3wml-instances00fd89e68cf24712a068ade10277b649published-models-h-authorization-bearer-eyjhbgcioijsuzuxmiisinr5cci6ikpxvcj9-eyj0zw5hbnrjzci6imu4ymqzzgm3lwi5y2utndy1oc1iz----apache-spark-service-credentialsthe-ibm-watson-machine-learning-cooperates-with-the-apache-spark-as-a-service-to-create-batch-stream-deploymentsand-for-learning-configuration-functionality-for-api-methods-requiring-apache-spark-service-instance-a-custom-header-xsparkserviceinstancewith-service-credentials-must-be-specified-the-header-value-is-a-base64-encoded-string-with-the-json-data-containing-service-credentials-and-spark-version-example-of-the-json-data---credentials------tenant-ids068ade10277b6495605b1d10fv12b------tenant-id-full00fd89e68cf24712a068ade10277b649-41f37bf21b954c65a15605b1d10fb12b------cluster-master-urlhttpsspark-bluemix-net------instance-id00fd89e68cf24712a068ade10277b649------tenant-secretc74c37cf482a4da4836ef32ca26ccbb9------planibm-sparkservice-paygopersonal------version2-0
  version: 1.0.0
basePath: v3/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /schemas:
    get:
      summary: Query active schema definitions
      description: "Schemas are used to define the structure of Events, Device State
        and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define
        the structure of the payload of the events\n    that are published to the
        platform by devices.\n\n  - For Device and Thing State, they define the structure
        of the state\n    that is stored by the platform.\n\nThe **schemas** endpoint
        returns the list of all of the active schema \ndefinitions for the organization
        in the Watson IoT Platform.  Various\nquery parameters can be used to filter,
        sort and page through the list\nof schemas that are returned."
      operationId: schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla
      x-api-path-slug: schemas-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
  /schemas/{schemaId}:
    get:
      summary: Get active schema definition metadata
      description: |-
        Retrieves the metadata for the active schema definition with the
        specified id.
      operationId: retrieves-the-metadata-for-the-active-schema-definition-with-thespecified-id
      x-api-path-slug: schemasschemaid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
      - SchemaId
  /schemas/{schemaId}/content:
    get:
      summary: Get the contents of the active schema definition file
      description: |-
        Retrieves the content of the active schema definition file with the
        specified id.
      operationId: retrieves-the-content-of-the-active-schema-definition-file-with-thespecified-id
      x-api-path-slug: schemasschemaidcontent-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Schemas
      - SchemaId
      - Content
  /draft/schemas:
    get:
      summary: Query draft schema definitions
      description: "Schemas are used to define the structure of Events, Device State
        and\nThing State in the Watson IoT Platform.\n\n  - For Events, they define
        the structure of the payload of the events\n    that are published to the
        platform by devices.\n\n  - For Device and Thing State, they define the structure
        of the state\n    that is stored by the platform.\n\nThe **/draft/schemas**
        endpoint returns the list of all of the draft \nschema for the organization
        in the Watson IoT Platform.  Various query\nparameters can be used to filter,
        sort and page through the list of\nschemas that are returned."
      operationId: schemas-are-used-to-define-the-structure-of-events-device-state-andthing-state-in-the-watson-iot-pla
      x-api-path-slug: draftschemas-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
    post:
      summary: Create a draft schema definition
      description: "Creates a new draft schema definition for the organization in
        the Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson
        IoT Platform within a\nmultipart POST (multipart/form-data).  The body of
        the POST **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile**
        that contains the actual content\n    of the file as the body of the part.\n
        \   \n  - One with a name of **name** that contains a string that defines
        the\n    name of the schema resource in the body of the part.\n\nAdditional
        metadata can be passed in other parts within the multipart\nPOST.  For example,
        to specify a description for the new schema\ndefinition, you should include
        a part with the name **description** and\nthe description as the body of the
        part.  To specify the type of the\nschema, you should include a part with
        the name **schemaType** and one\nof the following in the body of the part
        (the schemaType defaults to\njson-schema if the no schemaType part is present):\n\n
        \ - json-schema\n\nIf parts with names other than those specified above are
        included in the\nmultipart POST the request will fail and an HTTP status code
        of 400 will\nbe returned.\n\nThe content of the schema definition file that
        is passed to the platform\nis stored and a REST resource is created containing
        metadata that\ndescribes the schema definition."
      operationId: creates-a-new-draft-schema-definition-for-the-organization-in-the-watsoniot-platformthe-schema-defin
      x-api-path-slug: draftschemas-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
  /draft/schemas/{schemaId}:
    get:
      summary: Get draft schema definition metadata
      description: |-
        Retrieves the metadata for the draft schema definition with the
        specified id.
      operationId: retrieves-the-metadata-for-the-draft-schema-definition-with-thespecified-id
      x-api-path-slug: draftschemasschemaid-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
    put:
      summary: Update draft schema definition metadata
      description: "Updates the metadata for the draft schema definition with the
        specified\nid. The following properties can be updated:\n\n  - name\n  - description\n
        \ \nNote that if the description field is omitted from the body of the\nupdate,
        then any existing description will be removed from the schema\ndefinition.\n
        \ \nAny changes made to the values of the following properties will be\nignored:\n\n
        \ - schemaType\n  - schemaFilename\n  - contentType\n  - created\n  - createdBy\n
        \ - updated\n  - updatedBy\n  - refs\n  \nThe schemaFilename and contentType
        properties are updated when the\ncontent of the schema file is updated.\n\nThe
        values of the created, createdBy, updated, updatedBy and refs\nproperties
        are set on the server as a result of a successful update."
      operationId: updates-the-metadata-for-the-draft-schema-definition-with-the-specifiedid-the-following-properties-c
      x-api-path-slug: draftschemasschemaid-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: schemaDefinition
        description: The JSON representation of the schema definition
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
    delete:
      summary: Delete a draft schema definition
      description: |-
        Deletes the draft schema definition with the specified id from the
        organization in the Watson IoT Platform.  Deleting the schema definition
        deletes both the metadata and the actual schema definition file from the
        Watson IoT Platform.

        Please note the the delete will fail if the draft schema definition is
        being referenced by an event type or logical interface.
      operationId: deletes-the-draft-schema-definition-with-the-specified-id-from-theorganization-in-the-watson-iot-pla
      x-api-path-slug: draftschemasschemaid-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
  /draft/schemas/{schemaId}/content:
    get:
      summary: Get the contents of the draft schema definition file
      description: |-
        Retrieves the content of the draft schema definition file with the
        specified id.
      operationId: retrieves-the-content-of-the-draft-schema-definition-file-with-thespecified-id
      x-api-path-slug: draftschemasschemaidcontent-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
      - Content
    put:
      summary: Update the content of a draft schema definition file
      description: |-
        Updates the content of a draft schema definition file with the specified
        id.

        The schema definition file is passed to the Watson IoT Platform within a
        multipart POST (multipart/form-data).  The body of the POST **must**
        contain one part with a name of the **schemaFile** and the
        actual schema file as the body of the part.

        Please note that the schemaFilename and contentType properties of the
        schema definition will also be updated as a result of updating the
        content of the schema file.
      operationId: updates-the-content-of-a-draft-schema-definition-file-with-the-specifiedidthe-schema-definition-file
      x-api-path-slug: draftschemasschemaidcontent-put
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Internet of Things
      - Draft
      - Schemas
      - SchemaId
      - Content
host: ibm-watson-ml.mybluemix.net