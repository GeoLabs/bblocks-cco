
# CCO Geospatial Position (Schema)

`ogc.bbr.cco.geospatial.classes.GeospatialPosition` *v2.0*

A geospatial location specified by coordinates

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Geospatial Position

A geospatial position is a geospatial location specified by coordinates.

## Properties

- **type**: Must be "GeospatialPosition"
- **id**: URI identifier for the position
- **latitude**: Latitude coordinate in decimal degrees (-90 to 90)
- **longitude**: Longitude coordinate in decimal degrees (-180 to 180)
- **elevation**: Optional elevation above reference datum in meters
- **coordinateSystem**: Optional reference to the coordinate system used

## Semantic Model

This building block maps to the CCO GeospatialPosition class: `https://www.commoncoreontologies.org/GeospatialPosition`

## Examples

### Geospatial Position with coordinates
#### json
```json
{
  "type": "GeospatialPosition",
  "id": "https://example.org/position/eiffel-tower",
  "latitude": 48.8584,
  "longitude": 2.2945,
  "elevation": 330
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialPosition/context.jsonld",
  "type": "GeospatialPosition",
  "id": "https://example.org/position/eiffel-tower",
  "latitude": 48.8584,
  "longitude": 2.2945,
  "elevation": 330
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://example.org/position/eiffel-tower> a <file:///github/workspace/GeospatialPosition> ;
    cco:hasElevation 330.0 ;
    cco:hasLatitude 48.8584 ;
    cco:hasLongitude 2.2945 .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/GeospatialPosition
title: Geospatial Position
description: A geospatial location specified by coordinates
type: object
properties:
  type:
    type: string
    const: GeospatialPosition
    x-jsonld-id: '@type'
    x-jsonld-type: '@id'
  id:
    type: string
    format: uri
    x-jsonld-id: '@id'
  latitude:
    type: number
    description: Latitude coordinate in decimal degrees
    x-jsonld-id: https://www.commoncoreontologies.org/hasLatitude
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#decimal
    minimum: -90
    maximum: 90
  longitude:
    type: number
    description: Longitude coordinate in decimal degrees
    x-jsonld-id: https://www.commoncoreontologies.org/hasLongitude
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#decimal
    minimum: -180
    maximum: 180
  elevation:
    type: number
    description: Elevation above reference datum in meters
    x-jsonld-id: https://www.commoncoreontologies.org/hasElevation
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#decimal
  coordinateSystem:
    description: Reference coordinate system
    x-jsonld-id: https://www.commoncoreontologies.org/usesCoordinateSystem
    x-jsonld-type: '@id'
    oneOf:
    - type: object
    - type: string
      format: uri
required:
- type
- latitude
- longitude
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/
  xsd: http://www.w3.org/2001/XMLSchema#

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialPosition/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialPosition/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": {
      "@id": "@type",
      "@type": "@id"
    },
    "id": "@id",
    "latitude": {
      "@id": "cco:hasLatitude",
      "@type": "xsd:decimal"
    },
    "longitude": {
      "@id": "cco:hasLongitude",
      "@type": "xsd:decimal"
    },
    "elevation": {
      "@id": "cco:hasElevation",
      "@type": "xsd:decimal"
    },
    "coordinateSystem": {
      "@id": "cco:usesCoordinateSystem",
      "@type": "@id"
    },
    "cco": "https://www.commoncoreontologies.org/",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialPosition/context.jsonld)

## Sources

* [Common Core Ontologies - Geospatial Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial/classes/GeospatialPosition`

