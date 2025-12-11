
# Agent Ontology (Schema)

`ogc.bbr.cco.agent` *v2.0*

The Agent Ontology represents agents (especially persons and organizations) and their roles within the Common Core Ontologies framework.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Agent Ontology

The Agent Ontology represents agents, especially persons and organizations, and their roles within various contexts.

## Overview

This ontology provides concepts for:
- **Persons**: Individual human beings with characteristics and capabilities
- **Organizations**: Structured groups of agents working toward common goals
- **Roles**: Functions and positions held by agents
- **Agent Capabilities**: Abilities and competencies of agents
- **Agent Relations**: Affiliations, hierarchies, and social relationships

## Key Concepts

### Agent Classes
- `cco:Agent` - An entity capable of performing intentional acts
- `cco:Person` - An individual human being
- `cco:Organization` - A structured group of agents
- `cco:Group` - A collection of agents
- `cco:Role` - A function or position held by an agent
- `cco:OccupationalRole` - A work-related role

### Key Relations
- `cco:hasRole` - Relates an agent to their role
- `cco:hasAffiliate` - Relates an organization to its members
- `cco:hasAffiliation` - Relates an agent to their organization

## Usage

This ontology is used for:
- Modeling organizational structures
- Representing persons and their roles in different contexts
- Capturing relationships between agents (employee-employer, member-organization, etc.)
- Describing capabilities and competencies of agents

## Namespace

- **Namespace**: `https://www.commoncoreontologies.org/`
- **Suggested Prefix**: `cco:`
- **Version**: 2.0 (2024-11-06)

## Dependencies

This ontology extends:
- Basic Formal Ontology (BFO) 2020
- Common Core Ontology Extended Relation Ontology

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.
## Examples

### Person with Role Example
#### json
```json
{
  "type": "Person",
  "id": "https://example.org/person/john-doe",
  "name": "John Doe",
  "hasRole": {
    "type": "Role",
    "id": "https://example.org/role/engineer",
    "name": "Software Engineer"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/context.jsonld",
  "type": "Person",
  "id": "https://example.org/person/john-doe",
  "name": "John Doe",
  "hasRole": {
    "type": "Role",
    "id": "https://example.org/role/engineer",
    "name": "Software Engineer"
  }
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/person/john-doe> a <file:///github/workspace/Person> ;
    rdfs:label "John Doe" ;
    cco:hasRole <https://example.org/role/engineer> .

<https://example.org/role/engineer> a <file:///github/workspace/Role> ;
    rdfs:label "Software Engineer" .


```


### Organization with Affiliates
#### json
```json
{
  "type": "Organization",
  "id": "https://example.org/org/tech-corp",
  "name": "Tech Corporation",
  "hasAffiliate": {
    "type": "Person",
    "id": "https://example.org/person/jane-doe",
    "name": "Jane Doe"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/context.jsonld",
  "type": "Organization",
  "id": "https://example.org/org/tech-corp",
  "name": "Tech Corporation",
  "hasAffiliate": {
    "type": "Person",
    "id": "https://example.org/person/jane-doe",
    "name": "Jane Doe"
  }
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/org/tech-corp> a <file:///github/workspace/Organization> ;
    rdfs:label "Tech Corporation" ;
    cco:hasAffiliate <https://example.org/person/jane-doe> .

<https://example.org/person/jane-doe> a <file:///github/workspace/Person> ;
    rdfs:label "Jane Doe" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Agent Ontology schema based on Common Core Ontologies
$defs:
  Agent:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Agent/schema.yaml
  Person:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Person/schema.yaml
  Organization:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Organization/schema.yaml
  Group:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Group/schema.yaml
  Role:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Role/schema.yaml
  OccupationalRole:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/OccupationalRole/schema.yaml
anyOf:
- $ref: '#/$defs/Agent'
- $ref: '#/$defs/Person'
- $ref: '#/$defs/Organization'
- $ref: '#/$defs/Group'
- $ref: '#/$defs/Role'
- $ref: '#/$defs/OccupationalRole'
- type: object
  properties:
    '@type':
      oneOf:
      - type: string
        enum:
        - Agent
        - Group
      - type: array
        items:
          type: string
    name:
      type: string
      description: Name of the agent
      x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
    hasRole:
      oneOf:
      - $ref: '#/$defs/Role'
      - type: array
        items:
          $ref: '#/$defs/Role'
      description: Role held by the agent
      x-jsonld-id: https://www.commoncoreontologies.org/hasRole
      x-jsonld-type: '@id'
    hasAffiliation:
      oneOf:
      - $ref: '#/$defs/Organization'
      - type: array
        items:
          $ref: '#/$defs/Organization'
      description: Organization affiliation
      x-jsonld-id: https://www.commoncoreontologies.org/hasAffiliation
      x-jsonld-type: '@id'
    hasAffiliate:
      oneOf:
      - $ref: '#/$defs/Person'
      - type: array
        items:
          $ref: '#/$defs/Person'
      description: Agent affiliated with organization
      x-jsonld-id: https://www.commoncoreontologies.org/hasAffiliate
      x-jsonld-type: '@id'
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/
  rdfs: http://www.w3.org/2000/01/rdf-schema#
  rdf: http://www.w3.org/1999/02/22-rdf-syntax-ns#

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": {
      "@id": "@type",
      "@type": "@id"
    },
    "id": "@id",
    "name": "rdfs:label",
    "birthDate": {
      "@id": "cco:hasBirthDate",
      "@type": "xsd:date"
    },
    "hasRole": {
      "@id": "cco:hasRole",
      "@type": "@id"
    },
    "hasAffiliation": {
      "@id": "cco:hasAffiliation",
      "@type": "@id"
    },
    "foundedDate": {
      "@id": "cco:foundedDate",
      "@type": "xsd:date"
    },
    "hasAffiliate": {
      "@id": "cco:hasAffiliate",
      "@type": "@id"
    },
    "hasSubOrganization": {
      "@id": "cco:hasSubOrganization",
      "@type": "@id"
    },
    "description": "dcterms:description",
    "@type": {
      "@context": {}
    },
    "cco": "https://www.commoncoreontologies.org/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "dcterms": "http://purl.org/dc/terms/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/context.jsonld)

## Sources

* [Common Core Ontologies - Agent Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies/blob/develop/src/cco-modules/AgentOntology.ttl)
* [Common Core Ontologies Website](https://commoncoreontology.github.io/cco-webpage/)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/agent`

