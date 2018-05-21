---
swagger: "2.0"
x-collection-name: Azure Logic Apps
x-complete: 1
info:
  title: LogicManagementClient
  description: rest-api-for-azure-logic-apps
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Logic/integrationAccounts/{integrationAccountName}/schemas
  : get:
      summary: Schemas List By Integration Accounts
      description: Gets a list of integration account schemas.
      operationId: Schemas_ListByIntegrationAccounts
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftlogicintegrationaccountsintegrationaccountnameschemas-get
      parameters:
      - in: query
        name: $filter
        description: The filter to apply on the operation
      - in: query
        name: $top
        description: The number of items to be included in the result
      - in: path
        name: integrationAccountName
        description: The integration account name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      responses:
        200:
          description: OK
      tags:
      - Schemas Integration Accounts
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Logic/integrationAccounts/{integrationAccountName}/schemas/{schemaName}
  : get:
      summary: Schemas Get
      description: Gets an integration account schema.
      operationId: Schemas_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftlogicintegrationaccountsintegrationaccountnameschemasschemaname-get
      parameters:
      - in: path
        name: integrationAccountName
        description: The integration account name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      - in: path
        name: schemaName
        description: The integration account schema name
      responses:
        200:
          description: OK
      tags:
      - Schemas
    put:
      summary: Schemas Create Or Update
      description: Creates or updates an integration account schema.
      operationId: Schemas_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftlogicintegrationaccountsintegrationaccountnameschemasschemaname-put
      parameters:
      - in: path
        name: integrationAccountName
        description: The integration account name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      - in: body
        name: schema
        description: The integration account schema
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: schemaName
        description: The integration account schema name
      responses:
        200:
          description: OK
      tags:
      - Schemas
    delete:
      summary: Schemas Delete
      description: Deletes an integration account schema.
      operationId: Schemas_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoftlogicintegrationaccountsintegrationaccountnameschemasschemaname-delete
      parameters:
      - in: path
        name: integrationAccountName
        description: The integration account name
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The resource group name
      - in: path
        name: schemaName
        description: The integration account schema name
      responses:
        200:
          description: OK
      tags:
      - Schemas
---