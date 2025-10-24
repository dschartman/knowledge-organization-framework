---
id: S-0005
date: 2025-10-24
author: @don.schartman
provenance: "Framework development conversation; parallels to software engineering principles"
tags: [separation-of-concerns, software-engineering, architecture]
---

## Observations

- Software engineering principle: separation of concerns improves maintainability
- Mixing data, logic, and presentation in code creates tight coupling and fragility
- Model-View-Controller (MVC) pattern separates data from presentation
- Git separates version control (infrastructure) from code content
- Similar pattern applicable to knowledge work: facts, meaning, and communication are distinct concerns
- Mixing these concerns in a single document makes updates difficult
- When facts, interpretation, and presentation are intertwined, changing one requires careful coordination
- Separated concerns allow independent evolution: facts can be updated without rewriting prose
- Clear boundaries between layers enable testing/validation at each level
- Software principle: "Don't Repeat Yourself" (DRY)—same facts shouldn't be duplicated across documents
- With separated concerns, single source of truth (facts) can feed multiple presentations

## Context

Framework architecture draws from software engineering patterns, particularly separation of concerns. However, the framework applies this to knowledge organization and communication, not just code. The three-layer architecture (Substrate-Essence-Expression) is an instance of separation of concerns applied to knowledge work.
