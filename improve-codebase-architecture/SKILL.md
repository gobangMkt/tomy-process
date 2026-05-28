---
name: improve-codebase-architecture
description: Find deepening opportunities in a codebase, informed by the domain language in CONTEXT.md and the decisions in docs/adr/. Use when the user wants to improve architecture, find refactoring opportunities, consolidate tightly-coupled modules, or make a codebase more testable and AI-navigable.
---

# Improve Codebase Architecture

Surface architectural friction and propose **deepening opportunities** — refactors that turn shallow modules into deep ones. The aim is testability and AI-navigability.

## Key terms

- **Module** — anything with an interface and an implementation
- **Depth** — leverage at the interface: a lot of behaviour behind a small interface
- **Seam** — where an interface lives; a place behaviour can be altered without editing in place
- **Deletion test** — imagine deleting the module. If complexity vanishes, it was a pass-through.

## Process

### 1. Explore

Walk the codebase organically and note where you experience friction:
- Where does understanding one concept require bouncing between many small modules?
- Where are modules **shallow**?
- Where do tightly-coupled modules leak across their seams?
- Which parts are untested, or hard to test?

Apply the **deletion test** to anything you suspect is shallow.

### 2. Present candidates as an HTML report

Write a self-contained HTML file to the OS temp directory. For each candidate:

- **Files** — which files/modules are involved
- **Problem** — why the current architecture is causing friction
- **Solution** — plain English description of what would change
- **Benefits** — in terms of locality and leverage
- **Before / After diagram**
- **Recommendation strength** — `Strong`, `Worth exploring`, or `Speculative`

Ask the user: "Which of these would you like to explore?"

### 3. Grilling loop

Once the user picks a candidate, drop into a grilling conversation. Walk the design tree with them.
