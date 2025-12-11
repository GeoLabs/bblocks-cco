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
