---
name: AWS Database Migration Service
x-slug: aws-database-migration-service
description: AWS Database Migration Service helps you migrate databases to AWS easily
  and securely. The source database remains fully operational during the migration,
  minimizing downtime to applications that rely on the database. The AWS Database
  Migration Service can migrate your data to and from most widely used commercial
  and open-source databases. The service supports homogenous migrations such as Oracle
  to Oracle, as well as heterogeneous migrations between different database platforms,
  such as Oracle to Amazon Aurora or Microsoft SQL Server to MySQL. It also allows
  you to stream data to Amazon Redshift from any of the supported sources including
  Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle, SAP ASE and SQL Server, enabling
  consolidation and easy analysis of data in the petabyte-scale data warehouse. AWS
  Database Migration Service can also be used for continuous data replication with
  high-availability.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AWSDatabaseMigrationService.png
x-kinRank: "10"
x-alexaRank: ""
tags: Schemas
created: "2018-05-20"
modified: "2018-05-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/aws-database-migration-service/apis.md
specificationVersion: "0.14"
apis:
- name: AWS Database Migration Service API Describe Refresh Schemas Status
  x-api-slug: aws-database-migration-service-api
  description: Returns the status of the RefreshSchemas operation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AWSDatabaseMigrationService.png
  humanURL: https://aws.amazon.com/dms/
  baseURL: ://///?Action=DescribeRefreshSchemasStatus
  tags: Schemas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/aws-database-migration-service/actiondescriberefreshschemasstatus-get-openapi.md
- name: AWS Database Migration Service API Describe Schemas
  x-api-slug: aws-database-migration-service-api
  description: Returns information about the schema for the specified endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AWSDatabaseMigrationService.png
  humanURL: https://aws.amazon.com/dms/
  baseURL: ://///?Action=DescribeSchemas
  tags: Schemas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/aws-database-migration-service/actiondescribeschemas-get-openapi.md
- name: AWS Database Migration Service API Refresh Schemas
  x-api-slug: aws-database-migration-service-api
  description: Populates the schema for the specified endpoint.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AWSDatabaseMigrationService.png
  humanURL: https://aws.amazon.com/dms/
  baseURL: ://///?Action=RefreshSchemas
  tags: Schemas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/aws-database-migration-service/actionrefreshschemas-get-openapi.md
- name: AWS Database Migration Service API
  x-api-slug: aws-database-migration-service-api
  description: AWS Database Migration Service helps you migrate databases to AWS easily
    and securely. The source database remains fully operational during the migration,
    minimizing downtime to applications that rely on the database. The AWS Database
    Migration Service can migrate your data to and from most widely used commercial
    and open-source databases. The service supports homogenous migrations such as
    Oracle to Oracle, as well as heterogeneous migrations between different database
    platforms, such as Oracle to Amazon Aurora or Microsoft SQL Server to MySQL. It
    also allows you to stream data to Amazon Redshift from any of the supported sources
    including Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle, SAP ASE and SQL Server,
    enabling consolidation and easy analysis of data in the petabyte-scale data warehouse.
    AWS Database Migration Service can also be used for continuous data replication
    with high-availability.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Database_AWSDatabaseMigrationService.png
  humanURL: https://aws.amazon.com/dms/
  baseURL: :///
  tags: Schemas
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/schemas/master/_listings/aws-database-migration-service/openapi.md
x-common:
- type: x-documentation
  url: http://docs.aws.amazon.com/dms/latest/APIReference/Welcome.html
- type: x-faq
  url: https://aws.amazon.com/dms/faqs/
- type: x-getting-started
  url: https://aws.amazon.com/dms/getting-started/
- type: x-partners
  url: https://aws.amazon.com/dms/partners/
- type: x-pricing
  url: https://aws.amazon.com/dms/pricing/
- type: x-schema-conversion
  url: https://aws.amazon.com/dms/#sct
- type: x-testimonials
  url: https://aws.amazon.com/dms/testimonials/
- type: x-website
  url: https://aws.amazon.com/dms/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---