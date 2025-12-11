# Common Core Ontology - Information Entity Ontology

## Overview

The CCO Information Entity Ontology provides a framework for representing information content entities, documents, datasets, and their semantic relationships. This ontology is essential for metadata management, data catalogs, and information resource description.

## Key Concepts

### Classes

- **InformationContentEntity**: An entity that consists of information
- **Document**: A bounded information content entity
- **Dataset**: A collection of related data
- **Image**: Visual information content entity
- **Text**: Textual information content entity
- **DataFile**: A digital file containing data
- **Identifier**: Information content entity that designates an entity
- **Name**: Identifier consisting of a word or phrase
- **Description**: Information content entity that describes something

### Relations

- **hasContent**: Relates an information bearer to its content
- **represents**: Relates information to what it represents
- **hasFormat**: Relates information to its format (MIME type, etc.)
- **createdBy**: Relates information to its creator
- **designatedBy**: Relates an entity to an identifier that designates it
- **describes**: Relates a description to what it describes

## Usage

This ontology enables representation of:
- Documents and their metadata
- Datasets and data files
- Images and multimedia content
- Identifiers and naming schemes
- Descriptions and documentation

## Namespace

- **Prefix**: `cco`
- **URI**: `https://www.commoncoreontologies.org/`

## Dependencies

- Basic Formal Ontology (BFO)
- OWL, RDF, RDFS

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.