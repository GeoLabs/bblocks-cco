
# CCO Dataset (Schema)

`ogc.bbr.cco.information-entity.classes.Dataset` *v2.0*

A collection of related data

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Dataset

A collection of related data

## Examples

### Dataset Example
#### json
```json
{
  "type": "Dataset",
  "id": "https://example.org/information-entity/dataset-1",
  "name": "Example Dataset"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Dataset/context.jsonld",
  "type": "Dataset",
  "id": "https://example.org/information-entity/dataset-1",
  "name": "Example Dataset"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/information-entity/dataset-1> a <file:///github/workspace/Dataset> ;
    rdfs:label "Example Dataset" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Dataset
title: Dataset
description: A collection of related data
type: object
properties:
  type:
    const: Dataset
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Dataset/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Dataset/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Dataset/context.jsonld)

## Sources

* [Common Core Ontologies - Information-Entity Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/information-entity/classes/Dataset`

