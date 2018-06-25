---
name: IBM Watson
x-slug: ibm-watson
description: Meet IBM Watson, a cognitive system that enables a new partnership between
  people and computers that enhances and scales human expertise. Watson has been learning
  the language of professions and is trained by experts to work across many different
  industries.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
x-kinRank: "9"
x-alexaRank: "0"
tags: Schemas
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/apis.md
specificationVersion: "0.14"
apis:
- name: IBM Watson IoT Platform Query active schema definitions
  x-api-slug: ibm-watson-iot-platform
  description: "Schemas are used to define the structure of Events, Device State and\nThing
    State in the Watson IoT Platform.\n\n  - For Events, they define the structure
    of the payload of the events\n    that are published to the platform by devices.\n\n
    \ - For Device and Thing State, they define the structure of the state\n    that
    is stored by the platform.\n\nThe **schemas** endpoint returns the list of all
    of the active schema \ndefinitions for the organization in the Watson IoT Platform.
    \ Various\nquery parameters can be used to filter, sort and page through the list\nof
    schemas that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//schemas
  tags: Internet of Things,Schemas
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/schemas-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/schemas-get-openapi.md
- name: IBM Watson IoT Platform Get active schema definition metadata
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the metadata for the active schema definition with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//schemas/{schemaId}
  tags: Internet of Things,Schemas,SchemaId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/schemasschemaid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/schemasschemaid-get-openapi.md
- name: IBM Watson IoT Platform Get the contents of the active schema definition file
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the content of the active schema definition file with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//schemas/{schemaId}/content
  tags: Internet of Things,Schemas,SchemaId,Content
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/schemasschemaidcontent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/schemasschemaidcontent-get-openapi.md
- name: IBM Watson IoT Platform Query draft schema definitions
  x-api-slug: ibm-watson-iot-platform
  description: "Schemas are used to define the structure of Events, Device State and\nThing
    State in the Watson IoT Platform.\n\n  - For Events, they define the structure
    of the payload of the events\n    that are published to the platform by devices.\n\n
    \ - For Device and Thing State, they define the structure of the state\n    that
    is stored by the platform.\n\nThe **/draft/schemas** endpoint returns the list
    of all of the draft \nschema for the organization in the Watson IoT Platform.
    \ Various query\nparameters can be used to filter, sort and page through the list
    of\nschemas that are returned."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas
  tags: Internet of Things,Draft,Schemas
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemas-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemas-get-openapi.md
- name: IBM Watson IoT Platform Create a draft schema definition
  x-api-slug: ibm-watson-iot-platform
  description: "Creates a new draft schema definition for the organization in the
    Watson\nIoT Platform.\n\nThe schema definition file is passed to the Watson IoT
    Platform within a\nmultipart POST (multipart/form-data).  The body of the POST
    **must**\ncontain at least two parts:\n\n  - One with a name of **schemaFile**
    that contains the actual content\n    of the file as the body of the part.\n    \n
    \ - One with a name of **name** that contains a string that defines the\n    name
    of the schema resource in the body of the part.\n\nAdditional metadata can be
    passed in other parts within the multipart\nPOST.  For example, to specify a description
    for the new schema\ndefinition, you should include a part with the name **description**
    and\nthe description as the body of the part.  To specify the type of the\nschema,
    you should include a part with the name **schemaType** and one\nof the following
    in the body of the part (the schemaType defaults to\njson-schema if the no schemaType
    part is present):\n\n  - json-schema\n\nIf parts with names other than those specified
    above are included in the\nmultipart POST the request will fail and an HTTP status
    code of 400 will\nbe returned.\n\nThe content of the schema definition file that
    is passed to the platform\nis stored and a REST resource is created containing
    metadata that\ndescribes the schema definition."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas
  tags: Internet of Things,Draft,Schemas
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemas-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemas-post-openapi.md
- name: IBM Watson IoT Platform Get draft schema definition metadata
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the metadata for the draft schema definition with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}
  tags: Internet of Things,Draft,Schemas,SchemaId
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemasschemaid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemasschemaid-get-openapi.md
- name: IBM Watson IoT Platform Update draft schema definition metadata
  x-api-slug: ibm-watson-iot-platform
  description: "Updates the metadata for the draft schema definition with the specified\nid.
    The following properties can be updated:\n\n  - name\n  - description\n  \nNote
    that if the description field is omitted from the body of the\nupdate, then any
    existing description will be removed from the schema\ndefinition.\n  \nAny changes
    made to the values of the following properties will be\nignored:\n\n  - schemaType\n
    \ - schemaFilename\n  - contentType\n  - created\n  - createdBy\n  - updated\n
    \ - updatedBy\n  - refs\n  \nThe schemaFilename and contentType properties are
    updated when the\ncontent of the schema file is updated.\n\nThe values of the
    created, createdBy, updated, updatedBy and refs\nproperties are set on the server
    as a result of a successful update."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}
  tags: Internet of Things,Draft,Schemas,SchemaId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemasschemaid-put-openapi.md
- name: IBM Watson IoT Platform Delete a draft schema definition
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Deletes the draft schema definition with the specified id from the
    organization in the Watson IoT Platform.  Deleting the schema definition
    deletes both the metadata and the actual schema definition file from the
    Watson IoT Platform.

    Please note the the delete will fail if the draft schema definition is
    being referenced by an event type or logical interface.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}
  tags: Internet of Things,Draft,Schemas,SchemaId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemasschemaid-delete-openapi.md
- name: IBM Watson IoT Platform Get the contents of the draft schema definition file
  x-api-slug: ibm-watson-iot-platform
  description: |-
    Retrieves the content of the draft schema definition file with the
    specified id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}/content
  tags: Internet of Things,Draft,Schemas,SchemaId,Content
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemasschemaidcontent-get-openapi.md
- name: IBM Watson IoT Platform Update the content of a draft schema definition file
  x-api-slug: ibm-watson-iot-platform
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002//draft/schemas/{schemaId}/content
  tags: Internet of Things,Draft,Schemas,SchemaId,Content
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/draftschemasschemaidcontent-put-openapi.md
- name: IBM Watson IoT Platform
  x-api-slug: ibm-watson-iot-platform
  description: Meet IBM Watson, a cognitive system that enables a new partnership
    between people and computers that enhances and scales human expertise. Watson
    has been learning the language of professions and is trained by experts to work
    across many different industries.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/ibm-watson-logo.png
  humanURL: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
  baseURL: https:////api/v0002
  tags: Schemas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/ibm-watson/openapi.md
x-common:
- type: x-application-gallery
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/gallery.html
- type: x-blog
  url: https://developer.ibm.com/watson/blog/
- type: x-blog-rss
  url: https://developer.ibm.com/watson/feed/
- type: x-developer
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/doc/
- type: x-developer
  url: https://developer.ibm.com/watson/
- type: x-documentation
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/apis/
- type: x-forum
  url: https://developer.ibm.com/answers/smartspace/watson/
- type: x-getting-started
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/getstarted.html
- type: x-github
  url: https://github.com/IBM-Watson
- type: x-partners
  url: http://www.ibm.com/smarterplanet/us/en/ibmwatson/ecosystem.html
- type: x-privacy
  url: http://www.ibm.com/privacy/us/en/?lnk=flg-priv-usen
- type: x-terms-of-service
  url: http://www.ibm.com/legal/us/en/?lnk=flg-tous-usen
- type: x-twitter
  url: https://twitter.com/IBMWatson
- type: x-videos
  url: http://www.ibm.com/smarterplanet/us/en/ibmwatson/
- type: x-website
  url: https://www.ibm.com/smarterplanet/us/en/ibmwatson/developercloud/
- type: x-white-papers
  url: https://developer.ibm.com/watson/docs/whitepapers/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---