
# CCO Vehicle (Schema)

`ogc.bbr.cco.artifact.classes.Vehicle` *v2.0*

An artifact designed to transport persons or cargo

[*Status*](http://www.opengis.net/def/status): Under development

## Description

# Vehicle

An artifact designed to transport persons or cargo

## Examples

### Vehicle Example
#### json
```json
{
  "type": "Vehicle",
  "id": "https://example.org/artifact/vehicle-1",
  "name": "Example Vehicle"
}

```

#### jsonld
```jsonld
{
  "@context": "https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Vehicle/context.jsonld",
  "type": "Vehicle",
  "id": "https://example.org/artifact/vehicle-1",
  "name": "Example Vehicle"
}
```

#### ttl
```ttl
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .

<https://example.org/artifact/vehicle-1> a <file:///github/workspace/Vehicle> ;
    rdfs:label "Example Vehicle" .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://www.commoncoreontologies.org/Vehicle
title: Vehicle
description: An artifact designed to transport persons or cargo
type: object
properties:
  type:
    const: Vehicle
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

* YAML version: [schema.yaml](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Vehicle/schema.json)
* JSON version: [schema.json](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Vehicle/schema.yaml)


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
[context.jsonld](https://raw.githubusercontent.com/GeoLabs/bblocks-cco/undefined/build/annotated/bbr/cco/artifact/classes/Vehicle/context.jsonld)

## Sources

* [Common Core Ontologies - Artifact Ontology](https://github.com/CommonCoreOntology/CommonCoreOntologies)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/GeoLabs/bblocks-cco](https://github.com/GeoLabs/bblocks-cco)
* Path: `_sources/artifact/classes/Vehicle`

