
# Common Core Ontology - Currency Unit Ontology (Schema)

`ogc.bbr.cco.currency-unit` *v2.0*

CCO Currency Unit Ontology defines Currency types and monetary units

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Currency Unit Ontology

## Overview

The CCO Currency Unit Ontology provides a framework for representing currencies, monetary values, and exchange rates.

## Key Concepts

### Classes

- **CurrencyUnit**: A standardized unit of monetary value
- **USD**: United States Dollar
- **EUR**: Euro
- **GBP**: British Pound Sterling
- **JPY**: Japanese Yen
- **CNY**: Chinese Yuan

### Relations

- **hasCurrency**: Relates a monetary amount to its currency
- **hasMonetaryValue**: Relates an entity to its monetary value
- **exchangeRateTo**: Relates currencies via exchange rates

## Usage

This ontology enables:
- Representation of monetary amounts
- Currency designation
- Exchange rate modeling
- Financial transactions

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

### Currency Example
#### json
```json
{
  "type": "Currency",
  "id": "https://example.org/currency/usd",
  "name": "US Dollar"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/context.jsonld",
  "type": "Currency",
  "id": "https://example.org/currency/usd",
  "name": "US Dollar"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/currency/usd> a <file:///github/workspace/Currency> ;
    rdfs:label "US Dollar" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Currency Unit module with atomic building blocks
$defs:
  Currency:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/Currency/schema.yaml
  MonetaryAmount:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/classes/MonetaryAmount/schema.yaml
anyOf:
- $ref: '#/$defs/Currency'
- $ref: '#/$defs/MonetaryAmount'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/currency-unit`

