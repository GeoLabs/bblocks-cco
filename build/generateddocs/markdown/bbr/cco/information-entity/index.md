
# Common Core Ontology - Information Entity Ontology (Schema)

`ogc.bbr.cco.information-entity` *v2.0*

CCO Information Entity Ontology defines information artifacts, documents, data, and their representations

[*Status*](http://www.opengis.net/def/status): Under development

## Description

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
## Examples

### Document Example
#### json
```json
{
  "type": "Document",
  "id": "https://example.org/doc/report-2025",
  "name": "Annual Report 2025"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/context.jsonld",
  "type": "Document",
  "id": "https://example.org/doc/report-2025",
  "name": "Annual Report 2025"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/doc/report-2025> a <file:///github/workspace/Document> ;
    rdfs:label "Annual Report 2025" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Information Entity module with atomic building
  blocks
$defs:
  InformationContentEntity:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/InformationContentEntity/schema.yaml
  Document:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Document/schema.yaml
  Dataset:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Dataset/schema.yaml
  Image:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Image/schema.yaml
  Text:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Text/schema.yaml
  DataFile:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/DataFile/schema.yaml
  Identifier:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Identifier/schema.yaml
  Name:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Name/schema.yaml
  Description:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/classes/Description/schema.yaml
anyOf:
- $ref: '#/$defs/InformationContentEntity'
- $ref: '#/$defs/Document'
- $ref: '#/$defs/Dataset'
- $ref: '#/$defs/Image'
- $ref: '#/$defs/Text'
- $ref: '#/$defs/DataFile'
- $ref: '#/$defs/Identifier'
- $ref: '#/$defs/Name'
- $ref: '#/$defs/Description'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/information-entity/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/information-entity`

