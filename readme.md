# Machine Readable Connectivity (MRC)

## A Structured Way to Represent Schematics, Nets, Components, and Board Connections

Proposed by: Richard Haberkern  
Contact: rmhaberkern@gmail.com

Free for evaluation. Commercial use requires permission. See license.md for more information.

Part of the EmbeddedX platform.

* * *

## Abstract

Engineers understand hardware through schematics. Schematics show how components are connected, how signals flow, and how circuits are designed.

Machine Readable Connectivity (MRC) takes that same information and turns it into a structured format that software can use.

MRC combines information from:

* schematics
* netlists
* bill of materials (BOM)
* board files

This allows tools and systems to understand not only what is connected, but how the circuit works.

* * *

## 1. Why MRC Exists

A schematic tells you how a board is designed.

A netlist tells you exactly which pins are connected.

A BOM tells you what parts are used.

A board file shows layout and routing.

These are all useful, but they are separate files and not easy for software to combine.

MRC exists to bring these together into one structured view.

* * *

## 2. Core Idea

Think of MRC like this:

* schematic: how humans understand the circuit
* netlist: exact electrical connections
* MRC: structured version of both

MRC should reflect what an engineer would see in a schematic, but in a format that can be validated and processed.

* * *

## 3. What MRC Describes

MRC can describe:

* components on the board
* pins and connections
* nets and signals
* signal paths through components
* power rails and domains
* common circuit structures such as pull-ups, dividers, and filters

* * *

## 4. Example Questions MRC Should Answer

* What is connected to this MCU pin?
* Which resistor pulls this signal up?
* Which sensor is on this bus?
* How is this analog signal filtered?
* Which power rail feeds this device?
* What does this part of the schematic do?

* * *

## 5. Relationship to EmbeddedX

MRC is one part of the EmbeddedX system:

* Machine Readable Datasheet (MRD) describes what hardware can do
* Machine Readable Connectivity (MRC) shows how the schematic and board are wired
* Model Definition Package (MDP) defines model inputs and outputs
* Embedded Intelligence Layer (EIL) adds runtime intelligence
* AI Integrated Coding System (AICS) controls code generation and validation
* Embedded Intelligence Package (EIP) packages the final output

* * *

## 6. Design Rule

If a connection or circuit matters in a schematic, MRC should be able to describe it.

* * *

## License

See license.md for terms.
