# Agent Ontology

The Agent Ontology represents agents, especially persons and organizations, and their roles within various contexts.

## Overview

This ontology provides concepts for:
- **Persons**: Individual human beings with characteristics and capabilities
- **Organizations**: Structured groups of agents working toward common goals
- **Roles**: Functions and positions held by agents
- **Agent Capabilities**: Abilities and competencies of agents
- **Agent Relations**: Affiliations, hierarchies, and social relationships

## Key Concepts

### Agent Classes
- `cco:Agent` - An entity capable of performing intentional acts
- `cco:Person` - An individual human being
- `cco:Organization` - A structured group of agents
- `cco:Group` - A collection of agents
- `cco:Role` - A function or position held by an agent
- `cco:OccupationalRole` - A work-related role

### Key Relations
- `cco:hasRole` - Relates an agent to their role
- `cco:hasAffiliate` - Relates an organization to its members
- `cco:hasAffiliation` - Relates an agent to their organization

## Usage

This ontology is used for:
- Modeling organizational structures
- Representing persons and their roles in different contexts
- Capturing relationships between agents (employee-employer, member-organization, etc.)
- Describing capabilities and competencies of agents

## Namespace

- **Namespace**: `https://www.commoncoreontologies.org/`
- **Suggested Prefix**: `cco:`
- **Version**: 2.0 (2024-11-06)

## Dependencies

This ontology extends:
- Basic Formal Ontology (BFO) 2020
- Common Core Ontology Extended Relation Ontology

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.