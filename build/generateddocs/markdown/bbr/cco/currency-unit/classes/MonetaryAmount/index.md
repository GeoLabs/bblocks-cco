
# CCO MonetaryAmount (Schema)

`ogc.bbr.cco.currency-unit.classes.MonetaryAmount` *v2.0*

An amount of money in a specific currency

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# MonetaryAmount

An amount of money in a specific currency

## Examples

### MonetaryAmount Example
#### json
```json
{
  "type": "MonetaryAmount",
  "id": "https://example.org/currency-unit/monetaryamount-1",
  "name": "Example MonetaryAmount"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/MonetaryAmount/context.jsonld",
  "type": "MonetaryAmount",
  "id": "https://example.org/currency-unit/monetaryamount-1",
  "name": "Example MonetaryAmount"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/currency-unit/monetaryamount-1> a <file:///github/workspace/MonetaryAmount> ;
    rdfs:label "Example MonetaryAmount" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/MonetaryAmount
title: MonetaryAmount
description: An amount of money in a specific currency
type: object
properties:
  type:
    const: MonetaryAmount
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/MonetaryAmount/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/MonetaryAmount/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/MonetaryAmount/context.jsonld)

## Sources

* [Common Core Ontologies - Currency-Unit Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/currency-unit/classes/MonetaryAmount`

