
# CCO LengthUnit (Schema)

`ogc.bbr.cco.units-of-measure.classes.LengthUnit` *v2.0*

A unit of measure for length or distance

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# LengthUnit

A unit of measure for length or distance

## Examples

### LengthUnit Example
#### json
```json
{
  "type": "LengthUnit",
  "id": "https://example.org/units-of-measure/lengthunit-1",
  "name": "Example LengthUnit"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/LengthUnit/context.jsonld",
  "type": "LengthUnit",
  "id": "https://example.org/units-of-measure/lengthunit-1",
  "name": "Example LengthUnit"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/units-of-measure/lengthunit-1> a <file:///github/workspace/LengthUnit> ;
    rdfs:label "Example LengthUnit" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/LengthUnit
title: LengthUnit
description: A unit of measure for length or distance
type: object
properties:
  type:
    const: LengthUnit
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/LengthUnit/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/LengthUnit/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/LengthUnit/context.jsonld)

## Sources

* [Common Core Ontologies - Units-Of-Measure Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/units-of-measure/classes/LengthUnit`

