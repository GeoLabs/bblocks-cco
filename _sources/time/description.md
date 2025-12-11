# Common Core Ontology - Time Ontology

## Overview

The CCO Time Ontology provides a framework for representing temporal entities, instants, intervals, and temporal relationships.

## Key Concepts

### Classes

- **TemporalRegion**: A region of time
- **TemporalInstant**: A point in time with zero duration
- **TemporalInterval**: A region of time with duration
- **DateOfBirth**: The temporal instant when someone is born
- **DateOfDeath**: The temporal instant when someone dies

### Relations

- **hasStartTime**: Relates an interval to its start instant
- **hasEndTime**: Relates an interval to its end instant
- **hasDuration**: Relates an interval to its duration
- **before**: Temporal precedence relation
- **after**: Temporal succession relation
- **during**: Temporal containment relation

## Namespace

- **Prefix**: `cco`
- **URI**: `https://www.commoncoreontologies.org/`

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.