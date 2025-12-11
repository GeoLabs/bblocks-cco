
# CCO Coordinate System (Schema)

`ogc.bbr.cco.geospatial.classes.CoordinateSystem` *v2.0*

A system for uniquely determining position in space

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Coordinate System

A coordinate system is a system for uniquely determining position in space.

## Examples

### Coordinate System
#### json
```json
{
  "type": "CoordinateSystem",
  "id": "https://example.org/crs/wgs84",
  "name": "WGS84"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/CoordinateSystem/context.jsonld",
  "type": "CoordinateSystem",
  "id": "https://example.org/crs/wgs84",
  "name": "WGS84"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/crs/wgs84> a <file:///github/workspace/CoordinateSystem> ;
    rdfs:label "WGS84" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/CoordinateSystem
title: Coordinate System
description: A system for uniquely determining position in space
type: object
properties:
  type:
    const: CoordinateSystem
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/CoordinateSystem/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/CoordinateSystem/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/CoordinateSystem/context.jsonld)

## Sources

* [Common Core Ontologies - Geospatial Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial/classes/CoordinateSystem`

