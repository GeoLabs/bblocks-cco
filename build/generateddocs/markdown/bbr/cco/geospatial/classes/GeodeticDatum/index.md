
# CCO GeodeticDatum (Schema)

`ogc.bbr.cco.geospatial.classes.GeodeticDatum` *v2.0*

A reference frame for measuring locations on Earth

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# GeodeticDatum

## Overview

A reference frame for measuring locations on Earth

## Usage

Used to represent instances of GeodeticDatum in CCO.

## Namespace

- **Namespace**: `https://www.commoncoreontologies.org/`
- **Suggested Prefix**: `cco:`
- **Class**: `cco:GeodeticDatum`

## Examples

### Example 1
#### json
```json
example.json
```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeodeticDatum/context.jsonld",
  "@graph": "example.json"
}
```

#### ttl
```ttl


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: A reference frame for measuring locations on Earth
type: object
properties:
  type:
    type: string
    const: cco:GeodeticDatum
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeodeticDatum/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeodeticDatum/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeodeticDatum/context.jsonld)

## Sources

* [Common Core Ontologies - GeodeticDatum](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial/classes/GeodeticDatum`

