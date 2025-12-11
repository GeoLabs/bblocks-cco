
# Common Core Ontology - Event Ontology (Schema)

`ogc.bbr.cco.event` *v2.0*

CCO Event Ontology defines Events, processes, and temporal occurrences

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Common Core Ontology - Event Ontology

## Overview

The CCO Event Ontology provides a framework for representing events, processes, and temporal occurrences. It enables modeling of actions, activities, and their participants.

## Key Concepts

### Classes

- **Event**: A process or occurrence that happens at a particular time
- **Act**: An event initiated by an agent
- **Process**: A series of actions or changes
- **PlannedEvent**: An event that has been intentionally planned
- **SocialAct**: An act involving social interaction
- **Meeting**: A planned gathering of people
- **Communication**: An act of conveying information

### Relations

- **hasParticipant**: Relates an event to its participants
- **occursAt**: Relates an event to its location
- **hasAgent**: Relates an act to the agent performing it
- **hasInput**: Relates a process to its inputs
- **hasOutput**: Relates a process to its outputs

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

### Event Example
#### json
```json
{
  "type": "Event",
  "id": "https://example.org/event/meeting-2025",
  "name": "Annual Meeting 2025"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/context.jsonld",
  "type": "Event",
  "id": "https://example.org/event/meeting-2025",
  "name": "Annual Meeting 2025"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/event/meeting-2025> a <file:///github/workspace/Event> ;
    rdfs:label "Annual Meeting 2025" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Common Core Ontology - Event module with atomic building blocks
$defs:
  Event:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Event/schema.yaml
  Act:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Act/schema.yaml
  Process:
    $ref: https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Process/schema.yaml
anyOf:
- $ref: '#/$defs/Event'
- $ref: '#/$defs/Act'
- $ref: '#/$defs/Process'

```

Links to the schema:

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/context.jsonld)

## Sources

* [Common Core Ontologies](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/event`

