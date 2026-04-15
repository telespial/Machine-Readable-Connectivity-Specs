# Machine Readable Connectivity (MRC)

## A Structured Connectivity Contract for Nets, Components, Signal Paths, and Electrical Relationships in Embedded Hardware Designs

Proposed by: Richard Haberkern  
Contact: rmhaberkern@gmail.com

Free for evaluation. Commercial use requires permission. See license.md for more information.

Part of the [EmbeddedX platform](https://github.com/telespial/EmbeddedX-Specs).

* * *

## Abstract

Machine Readable Connectivity (MRC) establishes a structured connectivity contract for embedded hardware designs. It is intended to capture how components, nets, signal paths, power domains, and discrete electrical relationships are connected so that software systems, validation tools, and engineers can reason about the real wiring of a design without relying only on schematic PDFs.

MRC is designed to work with existing industry outputs such as netlists, BOMs, schematic exports, PCB design files, and manufacturing-oriented interchange data. It does not try to replace schematics. It establishes a machine-readable representation of board-level connectivity that can be combined with Machine Readable Datasheet (MRD), Model Definition Package (MDP), Embedded Intelligence Layer (EIL), AI Integrated Coding System (AICS), and Embedded Intelligence Package (EIP) within the EmbeddedX platform.

* * *

## 1. Why MRC Exists

Hardware datasheets explain what a device can do. Netlists explain what is connected. BOMs explain what the parts are. But those files are usually scattered, tool-specific, and difficult for software systems to reason about together.

MRC exists to turn that connectivity into a reusable contract that can answer questions such as:

* what is connected to this MCU pin
* what passives shape this signal
* which sensor sits on this interface
* which power domain feeds this peripheral
* whether pull-ups, dividers, filters, or level shifts are present
* which electrical assumptions firmware should respect

* * *

## 2. Scope

MRC may capture:

* board identity and revision
* connectivity sources and traceability
* component instances and classes
* net names and members
* interface groupings
* signal paths
* power domains
* derived electrical relationships
* inferred features with confidence markers
* compatibility notes and constraints

* * *

## 3. Core Principle

If board wiring changes firmware meaning, validation behavior, deployment assumptions, or model interpretation, MRC should be able to express it.

* * *

## 4. Relationship to Other Repositories

* [EmbeddedX-Specs](https://github.com/telespial/EmbeddedX-Specs) establishes the umbrella platform
* [Machine-Readable-Datasheets-Specs](https://github.com/telespial/Machine-Readable-Datasheets-Specs) establishes hardware-visible truth
* [Model-Definition-Package-Specs](https://github.com/telespial/Model-Definition-Package-Specs) establishes model truth
* [Embedded-Intelligence-Layer-Specs](https://github.com/telespial/Embedded-Intelligence-Layer-Specs) may use MRC to understand input provenance and degraded conditions
* [AI-Integrated-Coding-System-Spec](https://github.com/telespial/AI-Integrated-Coding-System-Spec) may use MRC to generate board-aware code and checks
* [Embedded-Intelligence-Package-Specs](https://github.com/telespial/Embedded-Intelligence-Package-Specs) may package MRC-linked deployment metadata

* * *

## 5. Reading Order

Recommended reading order:

1. `readme.md`
2. `docs/overview.md`
3. `docs/schema.md`
4. `docs/sources.md`
5. `docs/nets.md`
6. `docs/signal-paths.md`
7. `docs/derived-features.md`
8. `docs/power-domains.md`
9. `docs/interop.md`
10. `examples/example.mrc.json`

* * *

## License

See `license.md`.
