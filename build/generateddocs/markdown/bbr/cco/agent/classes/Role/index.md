
# CCO Role (Schema)

`ogc.bbr.cco.agent.classes.Role` *v2.0*

A role - a realizable entity that exists because of the realization of some characteristic or set of characteristics

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Role

A role is a realizable entity that exists because of the realization of some characteristic or set of characteristics.

## Properties

- **type**: Type of role (Role, OccupationalRole, SocialRole)
- **id**: URI identifier for the role
- **name**: Name of the role
- **description**: Description of the role

## Semantic Model

This building block maps to the CCO Role class: `https://www.commoncoreontologies.org/Role`

### Role Types

- **Role**: General role
- **OccupationalRole**: A role that inheres in an agent by virtue of their occupation
- **SocialRole**: A role that inheres in an agent by virtue of social relationships

## Example

See examples for concrete usage patterns.

## Examples

### Occupational Role
#### json
```json
{
  "type": "OccupationalRole",
  "id": "https://example.org/role/software-developer",
  "name": "Software Developer",
  "description": "Develops and maintains software applications"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Role/context.jsonld",
  "type": "OccupationalRole",
  "id": "https://example.org/role/software-developer",
  "name": "Software Developer",
  "description": "Develops and maintains software applications"
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/role/software-developer> a <file:///github/workspace/OccupationalRole> ;
    rdfs:label "Software Developer" ;
    dcterms:description "Develops and maintains software applications" .


```


### Social Role
#### json
```json
{
  "type": "SocialRole",
  "id": "https://example.org/role/mentor",
  "name": "Mentor",
  "description": "Provides guidance and support to mentees"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Role/context.jsonld",
  "type": "SocialRole",
  "id": "https://example.org/role/mentor",
  "name": "Mentor",
  "description": "Provides guidance and support to mentees"
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/role/mentor> a <file:///github/workspace/SocialRole> ;
    rdfs:label "Mentor" ;
    dcterms:description "Provides guidance and support to mentees" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Role
title: Role
description: A role that can be held by an agent
type: object
properties:
  type:
    type: string
    enum:
    - Role
    - OccupationalRole
    - SocialRole
    x-jsonld-id: '@type'
    x-jsonld-type: '@id'
  id:
    type: string
    format: uri
    x-jsonld-id: '@id'
  name:
    type: string
    description: Name of the role
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
  description:
    type: string
    description: Description of the role
    x-jsonld-id: http://purl.org/dc/terms/description
required:
- type
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/
  rdfs: http://www.w3.org/2000/01/rdf-schema#
  dcterms: http://purl.org/dc/terms/

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Role/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Role/schema.yaml)


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
    "description": "dcterms:description",
    "cco": "https://www.commoncoreontologies.org/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "dcterms": "http://purl.org/dc/terms/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Role/context.jsonld)

## Sources

* [Common Core Ontologies - Agent Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/agent/classes/Role`

