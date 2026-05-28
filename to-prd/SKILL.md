---
name: to-prd
description: Turn the current conversation context into a PRD and publish it to the project issue tracker. Use when user wants to create a PRD from the current context.
---

This skill takes the current conversation context and codebase understanding and produces a PRD. Do NOT interview the user — just synthesize what you already know.

## Process

1. Explore the repo to understand the current state of the codebase, if you haven't already.

2. Sketch out the major modules you will need to build or modify. Check with the user that these modules match their expectations.

3. Write the PRD using the template below, then publish it to the project issue tracker.

## PRD Template

```
## Problem Statement

The problem that the user is facing, from the user's perspective.

## Solution

The solution to the problem, from the user's perspective.

## User Stories

A numbered list of user stories:
1. As an <actor>, I want a <feature>, so that <benefit>

## Implementation Decisions

- The modules that will be built/modified
- Architectural decisions
- Schema changes
- API contracts

## Testing Decisions

- Which modules will be tested
- What makes a good test in this context

## Out of Scope

Things explicitly not included in this PRD.
```
