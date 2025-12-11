
# CCO Currency (Schema)

`ogc.bbr.cco.currency-unit.classes.Currency` *v2.0*

A system of money in use in a country

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Currency

A system of money in use in a country

## Examples

### Currency Example
#### json
```json
{
  "type": "Currency",
  "id": "https://example.org/currency-unit/currency-1",
  "name": "Example Currency"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/Currency/context.jsonld",
  "type": "Currency",
  "id": "https://example.org/currency-unit/currency-1",
  "name": "Example Currency"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/currency-unit/currency-1> a <file:///github/workspace/Currency> ;
    rdfs:label "Example Currency" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Currency
title: Currency
description: A system of money in use in a country
type: object
properties:
  type:
    const: Currency
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/Currency/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/Currency/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/Currency/context.jsonld)

## Sources

* [Common Core Ontologies - Currency-Unit Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/currency-unit/classes/Currency`

