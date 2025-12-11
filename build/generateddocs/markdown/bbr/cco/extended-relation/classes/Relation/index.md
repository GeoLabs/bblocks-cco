
# CCO Relation (Schema)

`ogc.bbr.cco.extended-relation.classes.Relation` *v2.0*

A relationship between entities

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Relation

A relationship between entities

## Examples

### Relation Example
#### json
```json
{
  "type": "Relation",
  "id": "https://example.org/extended-relation/relation-1",
  "name": "Example Relation"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/Relation/context.jsonld",
  "type": "Relation",
  "id": "https://example.org/extended-relation/relation-1",
  "name": "Example Relation"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/extended-relation/relation-1> a <file:///github/workspace/Relation> ;
    rdfs:label "Example Relation" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Relation
title: Relation
description: A relationship between entities
type: object
properties:
  type:
    const: Relation
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/Relation/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/Relation/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/classes/Relation/context.jsonld)

## Sources

* [Common Core Ontologies - Extended-Relation Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/extended-relation/classes/Relation`

