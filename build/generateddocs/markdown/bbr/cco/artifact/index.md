
# Common Core Ontology - Artifact Ontology (Schema)

`ogc.bbr.cco.artifact` *v2.0*

CCO Artifact Ontology defines Artifacts, manufactured objects, and products

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Artifact Ontology

## Overview

The CCO Artifact Ontology provides a framework for representing manufactured objects, products, and their functions.

## Key Concepts

### Classes

- **Artifact**: An object intentionally created by an agent
- **Product**: A manufactured item for commercial use
- **Vehicle**: A transport artifact
- **Weapon**: An artifact designed for combat
- **Tool**: An artifact used to perform work
- **Equipment**: Artifacts used collectively for a purpose
- **Software**: A digital artifact consisting of programs and data

### Relations

- **hasArtifactFunction**: Relates an artifact to its intended function
- **hasManufacturer**: Relates an artifact to its creator
- **hasMaterial**: Relates an artifact to its constituent materials
- **designedFor**: Relates an artifact to its intended use

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

### Artifact Example
#### json
```json
{
  "type": "Artifact",
  "id": "https://example.org/artifact/tool-1",
  "name": "Hammer"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/context.jsonld",
  "type": "Artifact",
  "id": "https://example.org/artifact/tool-1",
  "name": "Hammer"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/artifact/tool-1> a <file:///github/workspace/Artifact> ;
    rdfs:label "Hammer" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Artifact module with atomic building blocks
$defs:
  Artifact:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Artifact/schema.yaml
  Vehicle:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Vehicle/schema.yaml
  Weapon:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Weapon/schema.yaml
anyOf:
- $ref: '#/$defs/Artifact'
- $ref: '#/$defs/Vehicle'
- $ref: '#/$defs/Weapon'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/artifact`

