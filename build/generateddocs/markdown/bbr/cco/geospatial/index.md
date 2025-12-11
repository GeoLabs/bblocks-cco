
# Common Core Ontology - Geospatial Ontology (Schema)

`ogc.bbr.cco.geospatial` *v2.0*

CCO Geospatial Ontology defines geospatial features, locations, coordinate systems, and spatial relations

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Geospatial Ontology

## Overview

The CCO Geospatial Ontology provides a comprehensive framework for representing geospatial information including locations, coordinates, spatial regions, and geographic features. This ontology is particularly relevant for OGC applications dealing with geographic data, spatial analysis, and location-based services.

## Key Concepts

### Classes

- **GeospatialLocation**: A location on or relative to Earth
- **GeospatialRegion**: A three-dimensional spatial region located on or near Earth's surface
- **GeospatialPosition**: A geospatial location specified by coordinates
- **GeographicFeature**: A feature of the Earth's surface (e.g., mountain, river, city)
- **Coordinates**: A set of values that specify position within a coordinate system
- **GeodeticDatum**: A reference frame for measuring locations on Earth
- **CoordinateSystem**: A system for uniquely determining position in space
- **SpatialRegion**: A part or region of space

### Relations

- **hasLatitude**: Relates a position to its latitude value
- **hasLongitude**: Relates a position to its longitude value
- **hasElevation**: Relates a position to its elevation above a reference datum
- **locatedAt**: Relates an entity to its geospatial location
- **hasSpatialPart**: Relates a spatial region to its parts
- **spatialPartOf**: Inverse of hasSpatialPart
- **usesCoordinateSystem**: Relates a position to its coordinate system
- **hasDatum**: Relates a coordinate system to its geodetic datum

## Usage

This ontology enables representation of:
- Geographic coordinates (latitude, longitude, elevation)
- Spatial relationships between features
- Coordinate reference systems
- Geographic features and locations
- Spatial regions and their boundaries

## Namespace

- **Prefix**: `cco`
- **URI**: `https://www.commoncoreontologies.org/`

## Dependencies

- Basic Formal Ontology (BFO)
- OWL, RDF, RDFS

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.
## Examples

### Geographic Location with Coordinates
#### json
```json
{
  "type": "GeospatialPosition",
  "id": "https://example.org/location/eiffel-tower",
  "latitude": 48.8584,
  "longitude": 2.2945,
  "elevation": 330.0
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/context.jsonld",
  "type": "GeospatialPosition",
  "id": "https://example.org/location/eiffel-tower",
  "latitude": 48.8584,
  "longitude": 2.2945,
  "elevation": 330.0
}
```

#### ttl
```ttl
@prefix cco: <https://www.commoncoreontologies.org/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<https://example.org/location/eiffel-tower> a <file:///github/workspace/GeospatialPosition> ;
    cco:hasElevation 330.0 ;
    cco:hasLatitude 48.8584 ;
    cco:hasLongitude 2.2945 .


```


### Spatial Region with Parts
#### json
```json
{
  "type": "GeographicFeature",
  "id": "https://example.org/feature/seine-river",
  "name": "Seine River"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/context.jsonld",
  "type": "GeographicFeature",
  "id": "https://example.org/feature/seine-river",
  "name": "Seine River"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/feature/seine-river> a <file:///github/workspace/GeographicFeature> ;
    rdfs:label "Seine River" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Geospatial module with atomic building blocks
$defs:
  GeospatialLocation:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialLocation/schema.yaml
  GeospatialPosition:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialPosition/schema.yaml
  GeospatialRegion:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialRegion/schema.yaml
  GeographicFeature:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeographicFeature/schema.yaml
  CoordinateSystem:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/CoordinateSystem/schema.yaml
  Coordinates:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/Coordinates/schema.yaml
  GeodeticDatum:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeodeticDatum/schema.yaml
  SpatialRegion:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/SpatialRegion/schema.yaml
anyOf:
- $ref: '#/$defs/GeospatialLocation'
- $ref: '#/$defs/GeospatialPosition'
- $ref: '#/$defs/GeospatialRegion'
- $ref: '#/$defs/GeographicFeature'
- $ref: '#/$defs/CoordinateSystem'
- $ref: '#/$defs/Coordinates'
- $ref: '#/$defs/GeodeticDatum'
- $ref: '#/$defs/SpatialRegion'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/schema.yaml)


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
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial`

