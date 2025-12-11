
# Common Core Ontology - Quality Ontology (Schema)

`ogc.bbr.cco.quality` *v2.0*

CCO Quality Ontology defines Qualities, attributes, and characteristics

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Quality Ontology

## Overview

The CCO Quality Ontology provides a framework for representing qualities, attributes, characteristics, and their measurements.

## Key Concepts

### Classes

- **Quality**: An attribute or characteristic of an entity
- **PhysicalQuality**: A quality of physical entities
- **Color**: A visual quality
- **Shape**: A spatial quality
- **Mass**: A physical quality of matter
- **Length**: A spatial dimension quality
- **Temperature**: A thermal quality

### Relations

- **hasQuality**: Relates an entity to its qualities
- **qualityOf**: Inverse of hasQuality
- **hasValue**: Relates a quality to its measured value
- **hasUnit**: Relates a measurement to its unit

## Namespace

- **Prefix**: `cco`
- **URI**: `https://www.commoncoreontologies.org/`

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.
## Examples

### Quality Example
#### json
```json
{
  "type": "Quality",
  "id": "https://example.org/quality/color-red",
  "name": "Red Color"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/context.jsonld",
  "type": "Quality",
  "id": "https://example.org/quality/color-red",
  "name": "Red Color"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/quality/color-red> a <file:///github/workspace/Quality> ;
    rdfs:label "Red Color" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Quality module with atomic building blocks
$defs:
  Quality:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Quality/schema.yaml
  Measurement:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Measurement/schema.yaml
  Color:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Color/schema.yaml
anyOf:
- $ref: '#/$defs/Quality'
- $ref: '#/$defs/Measurement'
- $ref: '#/$defs/Color'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/quality`

