
# CCO Image (Schema)

`ogc.bbr.cco.information-entity.classes.Image` *v2.0*

Visual information content entity

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Image

Visual information content entity

## Examples

### Image Example
#### json
```json
{
  "type": "Image",
  "id": "https://example.org/information-entity/image-1",
  "name": "Example Image"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Image/context.jsonld",
  "type": "Image",
  "id": "https://example.org/information-entity/image-1",
  "name": "Example Image"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/information-entity/image-1> a <file:///github/workspace/Image> ;
    rdfs:label "Example Image" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Image
title: Image
description: Visual information content entity
type: object
properties:
  type:
    const: Image
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Image/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Image/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Image/context.jsonld)

## Sources

* [Common Core Ontologies - Information-Entity Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/information-entity/classes/Image`

