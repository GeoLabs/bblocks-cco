
# CCO MeasurementUnit (Schema)

`ogc.bbr.cco.units-of-measure.classes.MeasurementUnit` *v2.0*

A standard unit used to express measurements

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# MeasurementUnit

A standard unit used to express measurements

## Examples

### MeasurementUnit Example
#### json
```json
{
  "type": "MeasurementUnit",
  "id": "https://example.org/units-of-measure/measurementunit-1",
  "name": "Example MeasurementUnit"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/MeasurementUnit/context.jsonld",
  "type": "MeasurementUnit",
  "id": "https://example.org/units-of-measure/measurementunit-1",
  "name": "Example MeasurementUnit"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/units-of-measure/measurementunit-1> a <file:///github/workspace/MeasurementUnit> ;
    rdfs:label "Example MeasurementUnit" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/MeasurementUnit
title: MeasurementUnit
description: A standard unit used to express measurements
type: object
properties:
  type:
    const: MeasurementUnit
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/MeasurementUnit/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/MeasurementUnit/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/MeasurementUnit/context.jsonld)

## Sources

* [Common Core Ontologies - Units-Of-Measure Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/units-of-measure/classes/MeasurementUnit`

