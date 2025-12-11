
# CCO Act (Schema)

`ogc.bbr.cco.event.classes.Act` *v2.0*

An event performed by an agent

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Act

An event performed by an agent

## Examples

### Act Example
#### json
```json
{
  "type": "Act",
  "id": "https://example.org/event/act-1",
  "name": "Example Act"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Act/context.jsonld",
  "type": "Act",
  "id": "https://example.org/event/act-1",
  "name": "Example Act"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/event/act-1> a <file:///github/workspace/Act> ;
    rdfs:label "Example Act" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Act
title: Act
description: An event performed by an agent
type: object
properties:
  type:
    const: Act
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Act/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Act/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/event/classes/Act/context.jsonld)

## Sources

* [Common Core Ontologies - Event Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/event/classes/Act`

