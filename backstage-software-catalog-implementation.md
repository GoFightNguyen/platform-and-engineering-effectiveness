# [Backstage Software Catalog](https://backstage.io/docs/features/software-catalog/software-catalog-overview)

For backstage, the catalog is built around metadata YAML files stored with the code, which are then harvested and visualized in backstage.

There are 3 ways to add components to the catalog:
- manual registration of existing components through the UI
- creating new components through the UI
- static configuration (such as adding entries to the `app-config.yaml`)

## [Catalog Configuration](https://backstage.io/docs/features/software-catalog/configuration)

### Processors
The catalog has a concept of _processors_ to perform ingestion tasks, such as reading raw entity data from a remote source, parsing it, transforming it, and validating it.
These processors are configured under the `catalog.processors` configuration key.

Some processors do not need configuration, such as the default `UrlReaderProcessor`, while others do.

#### Integration Processors
There are integration processors, such as the one for GitHub that will scan a GitHub org for entity descriptor files.

#### Custom Processors
These are considered external integrations and can be used to ingest entities from an existing system already tracking software.

### Catalog Rules
By default the catalog only allows ingestion of entities with the kind `Component`, `API`, and `Location.`
This can be overridden globally in `catalog.rules`.

### Readonly mode
Setting `catalog.readonly` to true disables the mutating backend catalog APIs and prevents users from registering new entities at run-time.

### Some options using GitHub
- use the [GitHub Discovery Processor](https://backstage.io/docs/integrations/github/discovery)
- using the [catalog-import plugin](https://github.com/backstage/backstage/tree/master/plugins/catalog-import), teams can have a PR auto-created that generates a Component entity for them

## [System Model](https://backstage.io/docs/features/software-catalog/system-model)

### Core Entities
In backstage, software is modeled in the catalogue using 3 core entities:
- component
- api
- resource

#### Component
Individual pieces of software.

- can implement APIs for others to consume
- can consume APIs provided by other components
- can depend on resources that are attached to it at runtime (like a database)

#### API
Implemented by components and form boundaries between components.

APIs are an abstraction allowing our software ecosystem(s) to scale, therefore backstage treats them as a first class citizen.

The primary way to discover existing functionality in the ecosystem.

APIs might be defined using an RPC IDL (eg. GraphQL), a data scheme (eg. Avro), or as code interfaces.
Regardless, APIs exposed by components need to be in a known machine-readable format for further tooling and analysis on top.

Backstage recommends documenting, indexing, and searching across all APIs whether they are:
- public
- restricted (only available to specific consumers)
- private (only available within the providing component's system)

#### Resource
Physical or virtual infrastructure needed to operate a component.

Examples:
- databases
- pub/sub topics
- CDNs

### Ecosystem Modeling
Your ecosystem might need more options for categorizing entities.
Two more are:
- system
- domain

#### System
A collection of entities cooperating to perform some function, an encapsulation for related entities.

A system is a collection of resources and components exposing one or several public APIs.
The main benefit of modeling a system is that it hides its resources and private APIs between the components for any consumers.

Typically, a system will consist of at most a handful of components

#### Domain
Relate entities and systems to part of the business.

Groups a collection of systems that share terminology, domain models, metrics, KPIs, business purpose, or documentation; i.e. they form a bounded context.

Example: a "payments" domain might include documentation on how to accept payments for a new product or use-case and share the same entity types in their APIs