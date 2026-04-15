
# Data Model

## Core Entities

### Component
- id
- type
- reference
- pins

### Pin
- id
- name
- function

### Net
- id
- name
- connected pins

### Connection
- from pin
- to pin
- net reference

## Rules

- every pin must belong to a component
- every connection must map to a net
