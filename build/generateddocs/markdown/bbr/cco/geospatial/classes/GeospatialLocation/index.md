
# CCO Geospatial Location (Schema)

`ogc.bbr.cco.geospatial.classes.GeospatialLocation` *v2.0*

A location on or relative to Earth

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Geospatial Location

A geospatial location is a location on or relative to Earth.

## Properties

- **type**: Must be "GeospatialLocation"
- **id**: URI identifier for the location
- **name**: Name of the location

## Semantic Model

This building block maps to the CCO GeospatialLocation class: `https://www.commoncoreontologies.org/GeospatialLocation`

A Geospatial Location is defined as:
- A subclass of Spatial Region
- A location on or relative to Earth's surface

## Examples

### Simple Geospatial Location
#### json
```json
{
  "type": "GeospatialLocation",
  "id": "https://example.org/location/paris",
  "name": "Paris"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialLocation/context.jsonld",
  "type": "GeospatialLocation",
  "id": "https://example.org/location/paris",
  "name": "Paris"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/location/paris> a <file:///github/workspace/GeospatialLocation> ;
    rdfs:label "Paris" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/GeospatialLocation
title: Geospatial Location
description: A location on or relative to Earth
type: object
properties:
  type:
    type: string
    const: GeospatialLocation
    x-jsonld-id: '@type'
    x-jsonld-type: '@id'
  id:
    type: string
    format: uri
    x-jsonld-id: '@id'
  name:
    type: string
    description: Name of the location
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
required:
- type
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/
  rdfs: http://www.w3.org/2000/01/rdf-schema#

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialLocation/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialLocation/schema.yaml)


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
    "cco": "https://www.commoncoreontologies.org/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialLocation/context.jsonld)

## Sources

* [Common Core Ontologies - Geospatial Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial/classes/GeospatialLocation`

