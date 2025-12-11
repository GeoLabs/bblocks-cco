
# Common Core Ontology - Units of Measure Ontology (Schema)

`ogc.bbr.cco.units-of-measure` *v2.0*

CCO Units of Measure Ontology defines Measurement units and quantities

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Units of Measure Ontology

## Overview

The CCO Units of Measure Ontology provides a framework for representing measurement units, quantities, and unit conversions.

## Key Concepts

### Classes

- **MeasurementUnit**: A standardized unit for quantifying
- **LengthUnit**: Units for measuring distance (meter, foot, etc.)
- **MassUnit**: Units for measuring mass (kilogram, pound, etc.)
- **TimeUnit**: Units for measuring time (second, hour, etc.)
- **TemperatureUnit**: Units for measuring temperature (Celsius, Fahrenheit, etc.)
- **VelocityUnit**: Units for measuring speed

### Relations

- **hasUnit**: Relates a measurement to its unit
- **hasMeasurementValue**: Relates a measurement to its numeric value
- **convertToUnit**: Enables unit conversions

## Usage

This ontology enables:
- Representation of measurements with units
- Unit conversions
- Dimensional analysis
- Integration with standards like QUDT

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

### Measurement Unit Example
#### json
```json
{
  "type": "MeasurementUnit",
  "id": "https://example.org/unit/meter",
  "name": "Meter"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/context.jsonld",
  "type": "MeasurementUnit",
  "id": "https://example.org/unit/meter",
  "name": "Meter"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/unit/meter> a <file:///github/workspace/MeasurementUnit> ;
    rdfs:label "Meter" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Units Of Measure module with atomic building blocks
$defs:
  MeasurementUnit:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/MeasurementUnit/schema.yaml
  LengthUnit:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/classes/LengthUnit/schema.yaml
anyOf:
- $ref: '#/$defs/MeasurementUnit'
- $ref: '#/$defs/LengthUnit'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/units-of-measure`

