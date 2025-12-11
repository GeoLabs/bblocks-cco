
# Common Core Ontology - Time Ontology (Schema)

`ogc.bbr.cco.time` *v2.0*

CCO Time Ontology defines Temporal entities, instants, and intervals

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Time Ontology

## Overview

The CCO Time Ontology provides a framework for representing temporal entities, instants, intervals, and temporal relationships.

## Key Concepts

### Classes

- **TemporalRegion**: A region of time
- **TemporalInstant**: A point in time with zero duration
- **TemporalInterval**: A region of time with duration
- **DateOfBirth**: The temporal instant when someone is born
- **DateOfDeath**: The temporal instant when someone dies

### Relations

- **hasStartTime**: Relates an interval to its start instant
- **hasEndTime**: Relates an interval to its end instant
- **hasDuration**: Relates an interval to its duration
- **before**: Temporal precedence relation
- **after**: Temporal succession relation
- **during**: Temporal containment relation

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

### Time Instant Example
#### json
```json
{
  "type": "TimeInstant",
  "id": "https://example.org/time/now",
  "name": "Current Moment"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/context.jsonld",
  "type": "TimeInstant",
  "id": "https://example.org/time/now",
  "name": "Current Moment"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/time/now> a <file:///github/workspace/TimeInstant> ;
    rdfs:label "Current Moment" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Time module with atomic building blocks
$defs:
  TemporalRegion:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TemporalRegion/schema.yaml
  TimeInstant:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TimeInstant/schema.yaml
  TimeInterval:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/classes/TimeInterval/schema.yaml
anyOf:
- $ref: '#/$defs/TemporalRegion'
- $ref: '#/$defs/TimeInstant'
- $ref: '#/$defs/TimeInterval'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/time`

