---
name: Open Science Framework
x-slug: open-science-framework
description: OSF provides free and open source project management support for researchers
  across the entire research lifecycle. As a collaboration tool, OSF helps researchers
  work on projects privately with a limited number of collaborators and make parts
  of their projects public, or make all the project publicly accessible for broader
  dissemination. As a workflow system, OSF enables connections to the many services
  researchers already use to streamline their process and increase efficiency. As
  a flexible repository, it can store and archive research data, protocols, and materials.
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Schemas
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/open-science-framework/apis.md
specificationVersion: "0.14"
apis:
- name: Open Science Framework List all metaschemas
  x-api-slug: open-science-framework
  description: |-
    A paginated list of all active metaschemas.
    Metaschemas describe the supplemental questions that accompany a registration.
    #### Returns
    Returns a JSON object containing `data` and `links` keys.

    The `data` key contains an array of 10 metaschemas. Each resource in the array is a separate metaschema object.

    The `links` key contains a dictionary of links that can be used for [pagination](#Introduction_pagination).

    This request should never return an error.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//metaschemas/
  tags: Metaschemas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/open-science-framework/metaschemas-get-openapi.md
- name: Open Science Framework Retrieve a metaschema
  x-api-slug: open-science-framework
  description: |-
    Retrieves the details of a given metaschema.

    Metaschemas describe the supplemental questions that accompany a registration.

    #### Returns
    Returns a JSON object with a `data` key containing the representation of the requested metaschema, if the request is successful.

    If the request is unsuccessful, an `errors` key containing information about the failure will be returned. Refer to the [list of error codes](#Introduction_error_codes) to understand why this request may have failed.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2//metaschemas/{metaschema_id}
  tags: Metaschemas,Metaschema
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/open-science-framework/metaschemasmetaschema-id-get-openapi.md
- name: Open Science Framework
  x-api-slug: open-science-framework
  description: OSF provides free and open source project management support for researchers
    across the entire research lifecycle. As a collaboration tool, OSF helps researchers
    work on projects privately with a limited number of collaborators and make parts
    of their projects public, or make all the project publicly accessible for broader
    dissemination. As a workflow system, OSF enables connections to the many services
    researchers already use to streamline their process and increase efficiency. As
    a flexible repository, it can store and archive research data, protocols, and
    materials.
  image: ""
  humanURL: https://cos.io
  baseURL: https://test-api.osf.io//v2
  tags: Schemas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/open-science-framework/openapi.md
x-common:
- type: x-website
  url: https://cos.io
- type: x-github
  url: https://github.com/OSFramework
- type: x-twitter
  url: https://twitter.com/OSFramework
- type: x-website
  url: http://osf.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---