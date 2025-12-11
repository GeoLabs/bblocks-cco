
# CCO GeospatialRegion (Schema)

`ogc.bbr.cco.geospatial.classes.GeospatialRegion` *v2.0*

A three-dimensional spatial region located on or near Earth's surface

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# GeospatialRegion

## Overview

A three-dimensional spatial region located on or near Earth's surface

This class is a subclass of `cco:SpatialRegion`.

## Usage

Used to represent instances of GeospatialRegion in CCO.

## Namespace

- **Namespace**: `https://www.commoncoreontologies.org/`
- **Suggested Prefix**: `cco:`
- **Class**: `cco:GeospatialRegion`

## Examples

### Example 1
#### json
```json
example.json
```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialRegion/context.jsonld",
  "@graph": "example.json"
}
```

#### ttl
```ttl


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: A three-dimensional spatial region located on or near Earth's surface
type: object
properties:
  type:
    type: string
    const: cco:GeospatialRegion
    x-jsonld-id: '@type'
  id:
    type: string
    x-jsonld-id: '@id'
required:
- type
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialRegion/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialRegion/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": "@type",
    "id": "@id",
    "cco": "https://www.commoncoreontologies.org/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeospatialRegion/context.jsonld)

## Sources

* [Common Core Ontologies - GeospatialRegion](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial/classes/GeospatialRegion`

