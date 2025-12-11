
# CCO Geographic Feature (Schema)

`ogc.bbr.cco.geospatial.classes.GeographicFeature` *v2.0*

A feature of the Earth's surface

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Geographic Feature

A geographic feature is a feature of the Earth's surface.

## Examples

### Geographic Feature
#### json
```json
{
  "type": "GeographicFeature",
  "id": "https://example.org/feature/seine-river",
  "name": "Seine River"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeographicFeature/context.jsonld",
  "type": "GeographicFeature",
  "id": "https://example.org/feature/seine-river",
  "name": "Seine River"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/feature/seine-river> a <file:///github/workspace/GeographicFeature> ;
    rdfs:label "Seine River" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/GeographicFeature
title: Geographic Feature
description: A feature of the Earth's surface
type: object
properties:
  type:
    const: GeographicFeature
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeographicFeature/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeographicFeature/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/classes/GeographicFeature/context.jsonld)

## Sources

* [Common Core Ontologies - Geospatial Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/geospatial/classes/GeographicFeature`

