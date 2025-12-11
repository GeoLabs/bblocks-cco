
# CCO InformationContentEntity (Schema)

`ogc.bbr.cco.information-entity.classes.InformationContentEntity` *v2.0*

An entity that consists of information

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# InformationContentEntity

## Overview

An entity that consists of information

## Usage

Used to represent instances of InformationContentEntity in CCO.

## Namespace

- **Namespace**: `https://www.commoncoreontologies.org/`
- **Suggested Prefix**: `cco:`
- **Class**: `cco:InformationContentEntity`

## Examples

### Example 1
#### json
```json
example.json
```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/InformationContentEntity/context.jsonld",
  "@graph": "example.json"
}
```

#### ttl
```ttl


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: An entity that consists of information
type: object
properties:
  type:
    type: string
    const: cco:InformationContentEntity
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/InformationContentEntity/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/InformationContentEntity/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/InformationContentEntity/context.jsonld)

## Sources

* [Common Core Ontologies - InformationContentEntity](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/information-entity/classes/InformationContentEntity`

