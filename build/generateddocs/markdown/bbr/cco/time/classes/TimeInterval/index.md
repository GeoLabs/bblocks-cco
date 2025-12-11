
# CCO TimeInterval (Schema)

`ogc.bbr.cco.time.classes.TimeInterval` *v2.0*

A one-dimensional temporal region

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# TimeInterval

A one-dimensional temporal region

## Examples

### TimeInterval Example
#### json
```json
{
  "type": "TimeInterval",
  "id": "https://example.org/time/timeinterval-1",
  "name": "Example TimeInterval"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TimeInterval/context.jsonld",
  "type": "TimeInterval",
  "id": "https://example.org/time/timeinterval-1",
  "name": "Example TimeInterval"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/time/timeinterval-1> a <file:///github/workspace/TimeInterval> ;
    rdfs:label "Example TimeInterval" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/TimeInterval
title: TimeInterval
description: A one-dimensional temporal region
type: object
properties:
  type:
    const: TimeInterval
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TimeInterval/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TimeInterval/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TimeInterval/context.jsonld)

## Sources

* [Common Core Ontologies - Time Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/time/classes/TimeInterval`

