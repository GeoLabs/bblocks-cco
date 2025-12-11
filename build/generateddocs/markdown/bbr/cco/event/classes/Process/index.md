
# CCO Process (Schema)

`ogc.bbr.cco.event.classes.Process` *v2.0*

A continuous series of actions or changes

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Process

A continuous series of actions or changes

## Examples

### Process Example
#### json
```json
{
  "type": "Process",
  "id": "https://example.org/event/process-1",
  "name": "Example Process"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Process/context.jsonld",
  "type": "Process",
  "id": "https://example.org/event/process-1",
  "name": "Example Process"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/event/process-1> a <file:///github/workspace/Process> ;
    rdfs:label "Example Process" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Process
title: Process
description: A continuous series of actions or changes
type: object
properties:
  type:
    const: Process
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Process/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Process/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Process/context.jsonld)

## Sources

* [Common Core Ontologies - Event Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/event/classes/Process`

