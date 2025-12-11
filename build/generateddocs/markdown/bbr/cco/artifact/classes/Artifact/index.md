
# CCO Artifact (Schema)

`ogc.bbr.cco.artifact.classes.Artifact` *v2.0*

A material entity created or modified by human beings

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Artifact

A material entity created or modified by human beings

## Examples

### Artifact Example
#### json
```json
{
  "type": "Artifact",
  "id": "https://example.org/artifact/artifact-1",
  "name": "Example Artifact"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Artifact/context.jsonld",
  "type": "Artifact",
  "id": "https://example.org/artifact/artifact-1",
  "name": "Example Artifact"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/artifact/artifact-1> a <file:///github/workspace/Artifact> ;
    rdfs:label "Example Artifact" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Artifact
title: Artifact
description: A material entity created or modified by human beings
type: object
properties:
  type:
    const: Artifact
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Artifact/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Artifact/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Artifact/context.jsonld)

## Sources

* [Common Core Ontologies - Artifact Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/artifact/classes/Artifact`

