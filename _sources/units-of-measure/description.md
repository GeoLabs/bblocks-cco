# Common Core Ontology - Units of Measure Ontology

## Overview

The CCO Units of Measure Ontology provides a framework for representing measurement units, quantities, and unit conversions.

## Key Concepts

### Classes

- **MeasurementUnit**: A standardized unit for quantifying
- **LengthUnit**: Units for measuring distance (meter, foot, etc.)
- **MassUnit**: Units for measuring mass (kilogram, pound, etc.)
- **TimeUnit**: Units for measuring time (second, hour, etc.)
- **TemperatureUnit**: Units for measuring temperature (Celsius, Fahrenheit, etc.)
- **VelocityUnit**: Units for measuring speed

### Relations

- **hasUnit**: Relates a measurement to its unit
- **hasMeasurementValue**: Relates a measurement to its numeric value
- **convertToUnit**: Enables unit conversions

## Usage

This ontology enables:
- Representation of measurements with units
- Unit conversions
- Dimensional analysis
- Integration with standards like QUDT

## Namespace

- **Prefix**: `cco`
- **URI**: `https://www.commoncoreontologies.org/`

## License

**Building Block**: Apache License 2.0

**CCO Ontology**: BSD 3-Clause License

Copyright (c) 2024, CUBRC, INC.

This building block documentation and examples are licensed under Apache-2.0.
The underlying Common Core Ontologies are licensed under BSD-3-Clause.