
# CCO SpatialRelation (Schema)

`ogc.bbr.cco.extended-relation.classes.SpatialRelation` *v2.0*

A relationship involving spatial positioning

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# SpatialRelation

A relationship involving spatial positioning

## Examples

### SpatialRelation Example
#### json
```json
{
  "type": "SpatialRelation",
  "id": "https://example.org/extended-relation/spatialrelation-1",
  "name": "Example SpatialRelation"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/SpatialRelation/context.jsonld",
  "type": "SpatialRelation",
  "id": "https://example.org/extended-relation/spatialrelation-1",
  "name": "Example SpatialRelation"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/extended-relation/spatialrelation-1> a <file:///github/workspace/SpatialRelation> ;
    rdfs:label "Example SpatialRelation" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/SpatialRelation
title: SpatialRelation
description: A relationship involving spatial positioning
type: object
properties:
  type:
    const: SpatialRelation
    x-jsonld-id: '@type'
    x-jsonld-type: '@id'
  id:
    type: string
    format: uri
    x-jsonld-id: '@id'
  name:
    type: string
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#label
required:
- type
x-jsonld-prefixes:
  cco: https://www.commoncoreontologies.org/

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/SpatialRelation/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/SpatialRelation/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/SpatialRelation/context.jsonld)

## Sources

* [Common Core Ontologies - Extended-Relation Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/extended-relation/classes/SpatialRelation`

