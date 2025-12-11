
# CCO Infrastructure (Schema)

`ogc.bbr.cco.facility.classes.Infrastructure` *v2.0*

Basic physical systems of a region

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Infrastructure

Basic physical systems of a region

## Examples

### Infrastructure Example
#### json
```json
{
  "type": "Infrastructure",
  "id": "https://example.org/facility/infrastructure-1",
  "name": "Example Infrastructure"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Infrastructure/context.jsonld",
  "type": "Infrastructure",
  "id": "https://example.org/facility/infrastructure-1",
  "name": "Example Infrastructure"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/facility/infrastructure-1> a <file:///github/workspace/Infrastructure> ;
    rdfs:label "Example Infrastructure" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Infrastructure
title: Infrastructure
description: Basic physical systems of a region
type: object
properties:
  type:
    const: Infrastructure
    x-jsonld-id: '@type'
    x-jsonld-type: '@id'
  id:
    type: string
    format: uri
    x-jsonld-id: '@id'
  name:
    type: string
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
required:
- type
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Infrastructure/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Infrastructure/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": {
      "@id": "@type",
      "@type": "@id"
    },
    "id": "@id",
    "name": "http://www.w3.org/2000/01/rdf-schema#label",
    "cco": "https://www.commoncoreontologies.org/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Infrastructure/context.jsonld)

## Sources

* [Common Core Ontologies - Facility Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/facility/classes/Infrastructure`

