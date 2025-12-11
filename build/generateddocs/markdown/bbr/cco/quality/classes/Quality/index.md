
# CCO Quality (Schema)

`ogc.bbr.cco.quality.classes.Quality` *v2.0*

An attribute inhering in an entity

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Quality

An attribute inhering in an entity

## Examples

### Quality Example
#### json
```json
{
  "type": "Quality",
  "id": "https://example.org/quality/quality-1",
  "name": "Example Quality"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Quality/context.jsonld",
  "type": "Quality",
  "id": "https://example.org/quality/quality-1",
  "name": "Example Quality"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/quality/quality-1> a <file:///github/workspace/Quality> ;
    rdfs:label "Example Quality" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Quality
title: Quality
description: An attribute inhering in an entity
type: object
properties:
  type:
    const: Quality
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Quality/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Quality/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/classes/Quality/context.jsonld)

## Sources

* [Common Core Ontologies - Quality Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/quality/classes/Quality`

