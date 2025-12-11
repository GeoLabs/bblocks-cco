
# Common Core Ontology - Extended Relation Ontology (Schema)

`ogc.bbr.cco.extended-relation` *v2.0*

CCO Extended Relation Ontology defines Additional relations beyond BFO

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Extended Relation Ontology

## Overview

The CCO Extended Relation Ontology provides additional object properties beyond those in BFO, enabling richer semantic relationships.

## Key Concepts

### Relations

- **partOf**: Relates a part to its whole
- **hasPart**: Relates a whole to its parts
- **memberOf**: Relates a member to its collection
- **hasMember**: Relates a collection to its members
- **agentIn**: Relates an agent to processes they participate in
- **participatesIn**: Relates an entity to processes it participates in
- **locatedIn**: Relates an entity to its containing location
- **contains**: Relates a location to entities it contains

## Usage

This ontology extends BFO with commonly used relations for:
- Part-whole relationships
- Membership relations
- Agency and participation
- Spatial containment

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

### Relation Example
#### json
```json
{
  "type": "Relation",
  "id": "https://example.org/relation/part-of",
  "name": "Part Of Relation"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/context.jsonld",
  "type": "Relation",
  "id": "https://example.org/relation/part-of",
  "name": "Part Of Relation"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/relation/part-of> a <file:///github/workspace/Relation> ;
    rdfs:label "Part Of Relation" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Extended Relation module with atomic building
  blocks
$defs:
  Relation:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/Relation/schema.yaml
  SpatialRelation:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/SpatialRelation/schema.yaml
anyOf:
- $ref: '#/$defs/Relation'
- $ref: '#/$defs/SpatialRelation'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/extended-relation`

