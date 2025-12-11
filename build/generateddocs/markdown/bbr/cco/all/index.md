
# Common Core Ontologies (Schema)

`ogc.bbr.cco.all` *v2.0*

The Common Core Ontologies (CCO) comprise eleven ontology modules that extend the Basic Formal Ontology (BFO). CCO provides a mid-level ontology framework for representing entities across multiple domains including agents, artifacts, events, facilities, geospatial features, information entities, qualities, time, units of measure, and relations.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontologies

## Overview

The Common Core Ontologies (CCO) comprise a suite of eleven ontology modules that extend the Basic Formal Ontology (BFO). CCO provides a comprehensive mid-level ontology framework for representing entities across multiple domains.

## Ontology Modules

### Core Domain Ontologies

1. **[Agent Ontology](../agent/)** - Agents, persons, organizations, and roles
2. **[Artifact Ontology](../artifact/)** - Manufactured objects and products
3. **[Event Ontology](../event/)** - Events, processes, and acts
4. **[Facility Ontology](../facility/)** - Buildings and infrastructure
5. **[Geospatial Ontology](../geospatial/)** - Locations, coordinates, and spatial features
6. **[Information Entity Ontology](../information-entity/)** - Documents, datasets, and information content
7. **[Quality Ontology](../quality/)** - Qualities, attributes, and measurements
8. **[Time Ontology](../time/)** - Temporal regions, instants, and intervals

### Supporting Ontologies

9. **[Extended Relation Ontology](../extended-relation/)** - Additional relations beyond BFO
10. **[Units of Measure Ontology](../units-of-measure/)** - Measurement units
11. **[Currency Unit Ontology](../currency-unit/)** - Monetary units

## Architecture

CCO is designed as a modular ontology suite where:
- Each module can be used independently
- Modules can be combined as needed
- All modules extend Basic Formal Ontology (BFO) 2020
- Cross-module dependencies are explicitly declared

## Key Features

- **Modular Design**: Use only the modules you need
- **BFO-Aligned**: All classes are properly grounded in BFO
- **Domain Coverage**: Comprehensive coverage of common domains
- **Well-Documented**: Each module and class has clear definitions
- **Community-Driven**: Developed and maintained by CUBRC and the CCO community

## Usage

This building block imports all eleven CCO modules. For applications that only need specific modules, import them individually instead of using this complete suite.

### Example: Complete CCO Instance

```json
{
  "@context": {
    "cco": "https://www.commoncoreontologies.org/"
  },
  "@graph": [
    {
      "@type": "cco:Person",
      "@id": "http://example.org/person/john",
      "cco:hasRole": {
        "@type": "cco:OccupationalRole",
        "@id": "http://example.org/role/engineer"
      }
    },
    {
      "@type": "cco:Organization",
      "@id": "http://example.org/org/acme",
      "cco:hasAffiliate": "http://example.org/person/john"
    },
    {
      "@type": "cco:GeospatialLocation",
      "@id": "http://example.org/location/office",
      "cco:latitude": 40.7128,
      "cco:longitude": -74.0060
    }
  ]
}
```

## Namespace

- **Namespace**: `https://www.commoncoreontologies.org/`
- **Suggested Prefix**: `cco:`
- **Version**: 2.0 (2024-11-06)

## Dependencies

- Basic Formal Ontology (BFO) 2020
- All eleven CCO modules (listed above)

## References

- [CCO GitHub Repository](https://github.com/CommonCoreOntology/CommonCoreOntologies)
- [CCO Website](https://commoncoreontology.github.io/cco-webpage/)
- [CCO Documentation](https://github.com/CommonCoreOntology/CommonCoreOntologies/tree/develop/documentation)
- [Basic Formal Ontology](https://basic-formal-ontology.org/)

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.

## Examples

### Example 1
#### json
```json
complete-example.json
```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/all/context.jsonld",
  "@graph": "complete-example.json"
}
```

#### ttl
```ttl


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontologies - Complete ontology suite
$defs:
  Agent:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/agent/schema.yaml
  Artifact:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/schema.yaml
  CurrencyUnit:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/currency-unit/schema.yaml
  Event:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/schema.yaml
  ExtendedRelation:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/extended-relation/schema.yaml
  Facility:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/schema.yaml
  Geospatial:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/geospatial/schema.yaml
  InformationEntity:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/schema.yaml
  Quality:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/quality/schema.yaml
  Time:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/time/schema.yaml
  UnitsOfMeasure:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/units-of-measure/schema.yaml
anyOf:
- $ref: '#/$defs/Agent'
- $ref: '#/$defs/Artifact'
- $ref: '#/$defs/CurrencyUnit'
- $ref: '#/$defs/Event'
- $ref: '#/$defs/ExtendedRelation'
- $ref: '#/$defs/Facility'
- $ref: '#/$defs/Geospatial'
- $ref: '#/$defs/InformationEntity'
- $ref: '#/$defs/Quality'
- $ref: '#/$defs/Time'
- $ref: '#/$defs/UnitsOfMeasure'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/all/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/all/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": {
      "@id": "@type",
      "@type": "@id"
    },
    "id": "@id",
    "name": "rdfs:label",
    "birthDate": {
      "@id": "cco:hasBirthDate",
      "@type": "xsd:date"
    },
    "hasRole": {
      "@id": "cco:hasRole",
      "@type": "@id"
    },
    "hasAffiliation": {
      "@id": "cco:hasAffiliation",
      "@type": "@id"
    },
    "foundedDate": {
      "@id": "cco:foundedDate",
      "@type": "xsd:date"
    },
    "hasAffiliate": {
      "@id": "cco:hasAffiliate",
      "@type": "@id"
    },
    "hasSubOrganization": {
      "@id": "cco:hasSubOrganization",
      "@type": "@id"
    },
    "description": "dcterms:description",
    "@type": {
      "@context": {}
    },
    "latitude": {
      "@id": "cco:hasLatitude",
      "@type": "xsd:decimal"
    },
    "longitude": {
      "@id": "cco:hasLongitude",
      "@type": "xsd:decimal"
    },
    "elevation": {
      "@id": "cco:hasElevation",
      "@type": "xsd:decimal"
    },
    "coordinateSystem": {
      "@id": "cco:usesCoordinateSystem",
      "@type": "@id"
    },
    "cco": "https://www.commoncoreontologies.org/",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "dcterms": "http://purl.org/dc/terms/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/all/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)
* [Common Core Ontologies Website](https://commoncoreontology.github.io/cco-webpage/)
* [Basic Formal Ontology](https://basic-formal-ontology.org/)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/all`

