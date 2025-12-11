
# CCO SpatialRegion (Schema)

`ogc.bbr.cco.geospatial.classes.SpatialRegion` *v2.0*

A part or region of space

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# SpatialRegion

## Overview

A part or region of space

## Usage

Used to represent instances of SpatialRegion in CCO.

## Namespace

- **Namespace**: `https://www.commoncoreontologies.org/`
- **Suggested Prefix**: `cco:`
- **Class**: `cco:SpatialRegion`

## Examples

### Example 1
#### json
```json
example.json
```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/SpatialRegion/context.jsonld",
  "@graph": "example.json"
}
```

#### ttl
```ttl


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: A part or region of space
type: object
properties:
  type:
    type: string
    const: cco:SpatialRegion
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/SpatialRegion/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/SpatialRegion/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/SpatialRegion/context.jsonld)

## Sources

* [Common Core Ontologies - SpatialRegion](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial/classes/SpatialRegion`

