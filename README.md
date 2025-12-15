# OGC Building Blocks for Common Core Ontologies (CCO)

This repository contains [OGC Building Blocks](https://ogcincubator.github.io/bblocks-docs/) for the [Common Core Ontologies (CCO)](https://github.com/CommonCoreOntology/CommonCoreOntologies) version 2.0.

## Overview

The Common Core Ontologies (CCO) comprise a set of eleven ontology modules that extend the Basic Formal Ontology (BFO). This repository packages each CCO module as an OGC Building Block, enabling standardized usage, validation, and integration with other OGC standards.

## Building Blocks

This repository includes the following CCO ontology modules:

### Core Ontologies

1. **[Agent Ontology](https://www.commoncoreontologies.org/AgentOntology)** (`ogc.bbr.cco.agent`)
   - Defines agents, persons, organizations, and their roles

2. **[Geospatial Ontology](https://www.commoncoreontologies.org/GeospatialOntology)** (`ogc.bbr.cco.geospatial`)
   - Defines locations, coordinates, spatial regions, and geographic features
   - Particularly relevant for OGC applications

3. **[Information Entity Ontology](https://www.commoncoreontologies.org/InformationEntityOntology)** (`ogc.bbr.cco.information-entity`)
   - Defines documents, datasets, and information content entities

4. **[Event Ontology](https://www.commoncoreontologies.org/EventOntology)** (`ogc.bbr.cco.event`)
   - Defines events, processes, and temporal occurrences

5. **[Artifact Ontology](https://www.commoncoreontologies.org/ArtifactOntology)** (`ogc.bbr.cco.artifact`)
   - Defines manufactured objects, products, and tools

6. **[Facility Ontology](https://www.commoncoreontologies.org/FacilityOntology)** (`ogc.bbr.cco.facility`)
   - Defines buildings, infrastructure, and constructed facilities

7. **[Time Ontology](https://www.commoncoreontologies.org/TimeOntology)** (`ogc.bbr.cco.time`)
   - Defines temporal entities, instants, and intervals

8. **[Quality Ontology](https://www.commoncoreontologies.org/QualityOntology)** (`ogc.bbr.cco.quality`)
   - Defines qualities, attributes, and characteristics

### Supporting Ontologies

9. **[Extended Relation Ontology](https://www.commoncoreontologies.org/ExtendedRelationOntology)** (`ogc.bbr.cco.extended-relation`)
   - Provides additional relations beyond BFO

10. **[Units of Measure Ontology](https://www.commoncoreontologies.org/UnitsOfMeasureOntology)** (`ogc.bbr.cco.units-of-measure`)
    - Defines measurement units and quantities

11. **[Currency Unit Ontology](https://www.commoncoreontologies.org/CurrencyUnitOntology)** (`ogc.bbr.cco.currency-unit`)
    - Defines currency types and monetary units

## Structure

Each building block follows the OGC Building Blocks standard structure:

```
_sources/
  <module-name>/
    bblock.json         # Metadata
    schema.yaml         # JSON Schema with JSON-LD mappings
    description.md      # Documentation
    examples.yaml       # Example references
    examples/           # Example files
      *.json
    ontology.ttl        # RDF/OWL ontology
    context.jsonld      # JSON-LD context
```

## Usage

### JSON-LD Examples

Each building block provides JSON-LD examples demonstrating usage:

```json
{
  "@context": {
    "cco": "https://www.commoncoreontologies.org/"
  },
  "@type": "cco:Person",
  "name": "John Doe",
  "hasRole": {
    "@type": "cco:OccupationalRole",
    "name": "Software Engineer"
  }
}
```

### Integration with OGC Standards

These building blocks can be combined with other OGC building blocks for geospatial applications:

- Combine **Geospatial Ontology** with OGC GeoSPARQL
- Use **Information Entity Ontology** with OGC API - Records
- Integrate **Time Ontology** with OGC API - EDR temporal queries
- Apply **Agent Ontology** for provenance and attribution

## Validation

All building blocks include:
- JSON Schema for syntax validation
- JSON-LD contexts for semantic validation
- Example files demonstrating correct usage
- OWL ontologies for reasoning

## Version

- **CCO Version**: 2.0 (2024-11-06)
- **Building Blocks Version**: 1.0.0
- **Date**: 2025-01-24

## License

This repository uses a dual licensing approach:

### Building Blocks Infrastructure

The OGC Building Blocks infrastructure (schemas, examples, documentation, build scripts) is licensed under:

**Apache License 2.0**

Copyright (c) 2024, CUBRC, INC.

### Common Core Ontologies

The original CCO ontology content (RDF/OWL files) maintains its original license:

**BSD 3-Clause License**

Copyright (c) 2024, CUBRC, INC.

All rights reserved.

See individual ontology files (`ontology.ttl`) for the full BSD-3-Clause license text.

## References

- [Common Core Ontologies GitHub](https://github.com/CommonCoreOntology/CommonCoreOntologies)
- [CCO Documentation](https://github.com/CommonCoreOntology/CommonCoreOntologies/blob/develop/documentation/cco-pdf-documentation/)
- [OGC Building Blocks Documentation](https://ogcincubator.github.io/bblocks-docs/)
- [Basic Formal Ontology](https://basic-formal-ontology.org/)

## Contributing

Contributions are welcome! Please submit issues or pull requests via GitHub.

## Contact

For questions about CCO, see the [CCO GitHub repository](https://github.com/CommonCoreOntology/CommonCoreOntologies).

For questions about these OGC Building Blocks, please open an issue in this repository.
