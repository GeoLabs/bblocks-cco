
# CCO TemporalRegion (Schema)

`ogc.bbr.cco.time.classes.TemporalRegion` *v2.0*

A region of time

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# TemporalRegion

A region of time

## Examples

### TemporalRegion Example
#### json
```json
{
  "type": "TemporalRegion",
  "id": "https://example.org/time/temporalregion-1",
  "name": "Example TemporalRegion"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TemporalRegion/context.jsonld",
  "type": "TemporalRegion",
  "id": "https://example.org/time/temporalregion-1",
  "name": "Example TemporalRegion"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/time/temporalregion-1> a <file:///github/workspace/TemporalRegion> ;
    rdfs:label "Example TemporalRegion" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/TemporalRegion
title: TemporalRegion
description: A region of time
type: object
properties:
  type:
    const: TemporalRegion
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TemporalRegion/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TemporalRegion/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TemporalRegion/context.jsonld)

## Sources

* [Common Core Ontologies - Time Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/time/classes/TemporalRegion`

