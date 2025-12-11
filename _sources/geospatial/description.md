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