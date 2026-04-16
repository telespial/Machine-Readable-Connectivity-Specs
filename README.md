# Machine Readable Connectivity (MRC)

[← Back to EmbeddedX-Specs (canonical index)](https://github.com/telespial/EmbeddedX-Specs)

## Board Connectivity Data in a Form Tools Can Read

Proposed by: Richard Haberkern  
Contact: rmhaberkern@gmail.com

Free for evaluation. Commercial use requires permission. See `license.md` for more information.

Part of the **EmbeddedX specification family**.

**Canonical index:** start at `EmbeddedX-Specs`:
https://github.com/telespial/EmbeddedX-Specs

* * *

## Abstract

Machine Readable Connectivity (MRC) defines a structured format for embedded board connectivity. It captures how components, nets, signal paths, power domains, and electrical relationships are wired so tools and engineers can reason about the actual board without relying only on schematic PDFs.

MRC is designed to work with existing outputs such as netlists, BOMs, schematic exports, PCB design files, and manufacturing interchange data. It does not replace schematics. It gives board-level connectivity a representation that can be combined with MRD, MDP, EIL, AICS, and EIP in the broader EmbeddedX toolchain.

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

## 4. Relationship to Other Specifications

* **EmbeddedX (umbrella):** https://github.com/telespial/EmbeddedX-Specs
* **MRD:** https://github.com/telespial/Machine-Readable-Datasheets-Specs
* **MDP:** https://github.com/telespial/Model-Definition-Package-Specs
* **EIL:** https://github.com/telespial/Embedded-Intelligence-Layer-Specs
* **AICS:** https://github.com/telespial/AI-Coding-System-Specs
* **EIP:** https://github.com/telespial/Embedded-Intelligence-Package-Specs

* * *

## 5. Reading Order

Recommended reading order:

1. `README.md`
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
