
# CCO Organization (Schema)

`ogc.bbr.cco.agent.classes.Organization` *v2.0*

An organization - a collective of persons organized for a common purpose

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Organization

An organization is a collective of persons organized for a common purpose.

## Properties

- **type**: Must be "Organization"
- **id**: URI identifier for the organization
- **name**: Name of the organization
- **foundedDate**: Date the organization was founded
- **hasAffiliate**: Person(s) affiliated with the organization (references Person building block)
- **hasSubOrganization**: Sub-organization(s) (self-referential)

## Semantic Model

This building block maps to the CCO Organization class: `https://www.commoncoreontologies.org/Organization`

An Organization is defined as:
- A subclass of Agent
- A collective of persons organized for a common purpose

## Related Building Blocks

- [Person](../Person/README.md)

## Example

See examples for concrete usage patterns.

## Examples

### Simple Organization
#### json
```json
{
  "type": "Organization",
  "id": "https://example.org/org/acme-corp",
  "name": "ACME Corporation",
  "foundedDate": "2000-01-01"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Organization/context.jsonld",
  "type": "Organization",
  "id": "https://example.org/org/acme-corp",
  "name": "ACME Corporation",
  "foundedDate": "2000-01-01"
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://example.org/org/acme-corp> a <file:///github/workspace/Organization> ;
    rdfs:label "ACME Corporation" ;
    cco:foundedDate "2000-01-01"^^xsd:date .


```


### Organization with Affiliates
#### json
```json
{
  "type": "Organization",
  "id": "https://example.org/org/tech-innovations",
  "name": "Tech Innovations Inc.",
  "foundedDate": "2015-06-01",
  "hasAffiliate": [
    {
      "type": "Person",
      "id": "https://example.org/person/alice",
      "name": "Alice Johnson"
    },
    {
      "type": "Person",
      "id": "https://example.org/person/bob",
      "name": "Bob Williams"
    }
  ],
  "hasSubOrganization": {
    "type": "Organization",
    "id": "https://example.org/org/tech-innovations-labs",
    "name": "Tech Innovations Labs"
  }
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Organization/context.jsonld",
  "type": "Organization",
  "id": "https://example.org/org/tech-innovations",
  "name": "Tech Innovations Inc.",
  "foundedDate": "2015-06-01",
  "hasAffiliate": [
    {
      "type": "Person",
      "id": "https://example.org/person/alice",
      "name": "Alice Johnson"
    },
    {
      "type": "Person",
      "id": "https://example.org/person/bob",
      "name": "Bob Williams"
    }
  ],
  "hasSubOrganization": {
    "type": "Organization",
    "id": "https://example.org/org/tech-innovations-labs",
    "name": "Tech Innovations Labs"
  }
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://example.org/org/tech-innovations> a <file:///github/workspace/Organization> ;
    rdfs:label "Tech Innovations Inc." ;
    cco:foundedDate "2015-06-01"^^xsd:date ;
    cco:hasAffiliate <https://example.org/person/alice>,
        <https://example.org/person/bob> ;
    cco:hasSubOrganization <https://example.org/org/tech-innovations-labs> .

<https://example.org/org/tech-innovations-labs> a <file:///github/workspace/Organization> ;
    rdfs:label "Tech Innovations Labs" .

<https://example.org/person/alice> a <file:///github/workspace/Person> ;
    rdfs:label "Alice Johnson" .

<https://example.org/person/bob> a <file:///github/workspace/Person> ;
    rdfs:label "Bob Williams" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Organization
title: Organization
description: An organization - a collective of persons organized for a common purpose
type: object
properties:
  type:
    type: string
    const: Organization
    x-jsonld-id: '@type'
    x-jsonld-type: '@id'
  id:
    type: string
    format: uri
    x-jsonld-id: '@id'
  name:
    type: string
    description: Name of the organization
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
  foundedDate:
    type: string
    format: date
    description: Date the organization was founded
    x-jsonld-id: https://www.commoncoreontologies.org/foundedDate
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#date
  hasAffiliate:
    description: Person(s) affiliated with the organization
    x-jsonld-id: https://www.commoncoreontologies.org/hasAffiliate
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
  hasSubOrganization:
    description: Sub-organization(s)
    x-jsonld-id: https://www.commoncoreontologies.org/hasSubOrganization
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Organization/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Organization/schema.yaml)


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
    "cco": "https://www.commoncoreontologies.org/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/classes/Organization/context.jsonld)

## Sources

* [Common Core Ontologies - Agent Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/agent/classes/Organization`

