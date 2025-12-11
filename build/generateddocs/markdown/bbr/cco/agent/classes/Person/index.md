
# CCO Person (Schema)

`ogc.bbr.cco.agent.classes.Person` *v2.0*

A person - an agent that is a human being

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Person

A person is an agent that is a human being.

## Properties

- **type**: Must be "Person"
- **id**: URI identifier for the person
- **name**: Name of the person
- **birthDate**: Date of birth
- **hasRole**: Role(s) held by the person (references Role building block)
- **hasAffiliation**: Organization affiliation(s) (references Organization building block)

## Semantic Model

This building block maps to the CCO Person class: `https://www.commoncoreontologies.org/Person`

A Person is defined as:
- A subclass of Agent
- An agent that is a human being

## Related Building Blocks

- [Role](../Role/README.md)
- [Organization](../Organization/README.md)

## Example

See examples for concrete usage patterns.

## Examples

### Simple Person Example
#### json
```json
{
  "type": "Person",
  "id": "https://example.org/person/john-doe",
  "name": "John Doe",
  "birthDate": "1985-03-15"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Person/context.jsonld",
  "type": "Person",
  "id": "https://example.org/person/john-doe",
  "name": "John Doe",
  "birthDate": "1985-03-15"
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://example.org/person/john-doe> a <file:///github/workspace/Person> ;
    rdfs:label "John Doe" ;
    cco:hasBirthDate "1985-03-15"^^xsd:date .


```


### Person with Role
#### json
```json
{
  "type": "Person",
  "id": "https://example.org/person/jane-smith",
  "name": "Jane Smith",
  "birthDate": "1990-07-22",
  "hasRole": {
    "type": "OccupationalRole",
    "id": "https://example.org/role/senior-engineer",
    "name": "Senior Software Engineer"
  },
  "hasAffiliation": {
    "type": "Organization",
    "id": "https://example.org/org/tech-corp",
    "name": "Tech Corporation"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Person/context.jsonld",
  "type": "Person",
  "id": "https://example.org/person/jane-smith",
  "name": "Jane Smith",
  "birthDate": "1990-07-22",
  "hasRole": {
    "type": "OccupationalRole",
    "id": "https://example.org/role/senior-engineer",
    "name": "Senior Software Engineer"
  },
  "hasAffiliation": {
    "type": "Organization",
    "id": "https://example.org/org/tech-corp",
    "name": "Tech Corporation"
  }
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://example.org/person/jane-smith> a <file:///github/workspace/Person> ;
    rdfs:label "Jane Smith" ;
    cco:hasAffiliation <https://example.org/org/tech-corp> ;
    cco:hasBirthDate "1990-07-22"^^xsd:date ;
    cco:hasRole <https://example.org/role/senior-engineer> .

<https://example.org/org/tech-corp> a <file:///github/workspace/Organization> ;
    rdfs:label "Tech Corporation" .

<https://example.org/role/senior-engineer> a <file:///github/workspace/OccupationalRole> ;
    rdfs:label "Senior Software Engineer" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Person
title: Person
description: A person - an agent that is a human being
type: object
properties:
  type:
    type: string
    const: Person
    x-jsonld-id: '@type'
    x-jsonld-type: '@id'
  id:
    type: string
    format: uri
    x-jsonld-id: '@id'
  name:
    type: string
    description: Name of the person
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
  birthDate:
    type: string
    format: date
    description: Date of birth
    x-jsonld-id: https://www.commoncoreontologies.org/hasBirthDate
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#date
  hasRole:
    description: Role held by the person
    x-jsonld-id: https://www.commoncoreontologies.org/hasRole
    x-jsonld-type: '@id'
    oneOf:
    - type: object
    - type: string
      format: uri
    - type: array
      items:
        anyOf:
        - type: object
        - type: string
          format: uri
  hasAffiliation:
    description: Organization affiliation
    x-jsonld-id: https://www.commoncoreontologies.org/hasAffiliation
    x-jsonld-type: '@id'
    oneOf:
    - type: object
    - type: string
      format: uri
    - type: array
      items:
        anyOf:
        - type: object
        - type: string
          format: uri
required:
- type
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/
  rdfs: http://www.w3.org/2000/01/rdf-schema#
  xsd: http://www.w3.org/2001/XMLSchema#

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Person/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Person/schema.yaml)


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
    "cco": "https://www.commoncoreontologies.org/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Person/context.jsonld)

## Sources

* [Common Core Ontologies - Agent Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/agent/classes/Person`

