
# CCO Color (Schema)

`ogc.bbr.cco.quality.classes.Color` *v2.0*

A quality inhering in an entity by virtue of light

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Color

A quality inhering in an entity by virtue of light

## Examples

### Color Example
#### json
```json
{
  "type": "Color",
  "id": "https://example.org/quality/color-1",
  "name": "Example Color"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Color/context.jsonld",
  "type": "Color",
  "id": "https://example.org/quality/color-1",
  "name": "Example Color"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/quality/color-1> a <file:///github/workspace/Color> ;
    rdfs:label "Example Color" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Color
title: Color
description: A quality inhering in an entity by virtue of light
type: object
properties:
  type:
    const: Color
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Color/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Color/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Color/context.jsonld)

## Sources

* [Common Core Ontologies - Quality Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/quality/classes/Color`

