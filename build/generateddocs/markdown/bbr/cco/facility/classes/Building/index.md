
# CCO Building (Schema)

`ogc.bbr.cco.facility.classes.Building` *v2.0*

A structure with walls and a roof

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Building

A structure with walls and a roof

## Examples

### Building Example
#### json
```json
{
  "type": "Building",
  "id": "https://example.org/facility/building-1",
  "name": "Example Building"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Building/context.jsonld",
  "type": "Building",
  "id": "https://example.org/facility/building-1",
  "name": "Example Building"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/facility/building-1> a <file:///github/workspace/Building> ;
    rdfs:label "Example Building" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Building
title: Building
description: A structure with walls and a roof
type: object
properties:
  type:
    const: Building
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Building/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Building/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Building/context.jsonld)

## Sources

* [Common Core Ontologies - Facility Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/facility/classes/Building`

