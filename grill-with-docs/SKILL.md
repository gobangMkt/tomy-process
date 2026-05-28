---
name: grill-with-docs
description: Grilling session that challenges your plan against the existing domain model, sharpens terminology, and updates documentation (CONTEXT.md, ADRs) inline as decisions crystallise. Use when user wants to stress-test a plan against their project's language and documented decisions.
---

Interview me relentlessly about every aspect of this plan until we reach a shared understanding. Walk down each branch of the design tree, resolving dependencies between decisions one-by-one. For each question, provide your recommended answer.

Ask the questions one at a time, waiting for feedback on each question before continuing.

If a question can be answered by exploring the codebase, explore the codebase instead.

## During the session

### Challenge against the glossary

When the user uses a term that conflicts with existing language in `CONTEXT.md`, call it out immediately.

### Sharpen fuzzy language

When the user uses vague or overloaded terms, propose a precise canonical term.

### Cross-reference with code

When the user states how something works, check whether the code agrees. Surface contradictions.

### Update CONTEXT.md inline

When a term is resolved, update `CONTEXT.md` right there. Don't batch these up.

### Offer ADRs sparingly

Only offer to create an ADR when all three are true:
1. **Hard to reverse**
2. **Surprising without context**
3. **The result of a real trade-off**
