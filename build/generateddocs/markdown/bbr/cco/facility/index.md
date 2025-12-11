
# Common Core Ontology - Facility Ontology (Schema)

`ogc.bbr.cco.facility` *v2.0*

CCO Facility Ontology defines Buildings, infrastructure, and constructed facilities

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Facility Ontology

## Overview

The CCO Facility Ontology provides a framework for representing built environments, infrastructure, and constructed facilities.

## Key Concepts

### Classes

- **Facility**: A permanent or semi-permanent structure
- **Building**: A structure with walls and a roof
- **Infrastructure**: Basic physical systems of a region
- **Road**: A paved way for vehicles
- **Airport**: A facility for aircraft operations
- **Harbor**: A facility for maritime vessels
- **Stadium**: A facility for sporting events

### Relations

- **hasFacilityFunction**: Relates a facility to its intended function
- **locatedAt**: Relates a facility to its location
- **containsFacility**: Relates a facility to sub-facilities
- **partOfFacility**: Relates a facility to its parent facility

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

### Building Example
#### json
```json
{
  "type": "Building",
  "id": "https://example.org/building/office-tower",
  "name": "Office Tower"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/context.jsonld",
  "type": "Building",
  "id": "https://example.org/building/office-tower",
  "name": "Office Tower"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/building/office-tower> a <file:///github/workspace/Building> ;
    rdfs:label "Office Tower" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Facility module with atomic building blocks
$defs:
  Facility:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Facility/schema.yaml
  Building:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Building/schema.yaml
  Infrastructure:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/classes/Infrastructure/schema.yaml
anyOf:
- $ref: '#/$defs/Facility'
- $ref: '#/$defs/Building'
- $ref: '#/$defs/Infrastructure'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/facility/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/facility`

