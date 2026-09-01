# LLD Track Instructions

## Scope and Python pedagogy

Teach low-level and object-oriented design in idiomatic Python after the required HLD path is complete. Assume the learner is a Python beginner.

- Introduce Python syntax and object-model behavior exactly when the design needs it.
- Explain names and references, mutability, identity versus equality, hashing, class and instance attributes, method binding, inheritance, composition, abstract base classes, protocols, dataclasses, enums, exceptions, context managers, iterators, and concurrency as relevant.
- Prefer explicit, readable interfaces and composition over unnecessary inheritance or pattern ceremony.
- Teach design patterns as responses to concrete forces and change scenarios, not as names to insert into every solution.
- Separate runtime and space complexity from coupling, cohesion, testability, and McCabe cyclomatic complexity.

## Foundation topic initialization

When an LLD foundation topic begins, create `LLD/topics/NN-kebab-case-topic/notes.md` and `practice.md` without overwriting existing files.

Initialize `notes.md` with:

```markdown
# <Topic>

- Status: In Progress
- Last updated: YYYY-MM-DD

## Mental Model and Purpose

## Python Object-Model Mechanics

## Contracts, Responsibilities and Invariants

## Design Principles or Patterns

## Complexity, Coupling and Testability

## Failure Modes and Edge Cases

## Google L4 Interview Lens

## Open Questions or Weak Spots

## Consolidation Package

### On-the-Go Revision Notes

### Interview Drills

### Further Practice and Visual Learning
```

Initialize `practice.md` with:

```markdown
# <Topic> Practice

## Design Drills

| Date | Drill | Learner Design | Gap or Trade-off | Next Action |
|---|---|---|---|---|

## Python Mechanics Practice

## Change-Request and Refactoring Drills

## Interview Follow-Ups

## Verified Resources
```

## Foundation teaching protocol

- Begin from requirements, use cases, invariants, and likely changes.
- Make the learner assign responsibilities and define contracts before writing implementation code.
- Explain the relevant Python mechanics and their consequences for correctness and design.
- Evaluate cohesion, coupling, dependency direction, extensibility, error behavior, and testability.
- Introduce a SOLID principle or design pattern only when a concrete design pressure makes it useful.
- Use class, sequence, or state diagrams when relationships or transitions are hard to explain linearly.
- Exercise the design with an extension request so abstractions are justified by change rather than speculation.
- Use McCabe complexity to discuss branching and maintainability only when it adds insight; never confuse it with Big-O complexity.

## Case-study initialization

When an LLD case study begins, create its level-specific directory with:

- `requirements.md`
- `design.md`
- `review.md`
- `src/`
- `tests/`

Do not generate a completed implementation. Source and tests are built incrementally from the learner's decisions.

Initialize `requirements.md` with:

```markdown
# <Case Study> Requirements

- Level: <Foundation | Medium | Difficult>
- Path: <Core | Extension>
- Status: In Progress
- Started: YYYY-MM-DD

## Interview Prompt

## Functional Requirements

## Non-Functional Requirements

## Use Cases

## Constraints and Assumptions

## Learner Questions and Interviewer Answers
```

Initialize `design.md` with:

```markdown
# <Case Study> Design

- Status: In Progress
- Last updated: YYYY-MM-DD

## Domain Model

## Responsibilities and Collaborators

## Public Interfaces and Contracts

## Invariants

## Class Diagram

## Critical Sequences

## States and Transitions

## Validation and Error Model

## Persistence and External Boundaries

## Concurrency and Thread Safety

## Complexity and Performance

## Test Strategy

## Extensibility and Change Scenarios

## Alternatives and Trade-offs

## Interview Follow-Ups
```

Initialize `review.md` with:

```markdown
# <Case Study> Review

## Demonstrated Strengths

## Design and Python Gaps

## Conceptual Hints Given

## Test and Failure Findings

## Change-Request Performance

## Decisions and Rejected Alternatives

## Mastery Decision
```

## LLD case-study interview flow

1. Clarify scope, actors, use cases, invariants, errors, and expected change.
2. Identify domain concepts and assign responsibilities.
3. Define contracts and relationships before implementation.
4. Draw only the diagrams needed to clarify structure, behavior, or state.
5. Implement one vertical core flow in Python.
6. Add tests for established requirements, invariants, errors, and state transitions.
7. Introduce a realistic change request or concurrency condition.
8. Refactor only when evidence reveals an abstraction or maintainability problem.
9. Record trade-offs and rejected alternatives.

## LLD pair-programming protocol

When code or tests fail:

1. Point to the responsible line, method, class, interface, state transition, or responsibility boundary.
2. Explain why the supplied requirement, test, or concurrency scenario exposes the flaw.
3. Give a conceptual hint or a focused question.

Do not provide corrected code or replace the learner's design. Small Python syntax demonstrations unrelated to the case-study solution are allowed when needed to teach the language.

## LLD mastery gates

An LLD foundation topic is mastered only when the learner can explain its mechanics and design pressure, use the relevant Python construct correctly, defend the trade-off, and apply it in an unfamiliar drill.

An LLD case study is mastered only when the learner can:

- Clarify requirements, use cases, invariants, errors, and change scenarios.
- Produce a cohesive domain model with defensible responsibilities and contracts.
- Implement the core workflow in idiomatic Python without receiving the solution.
- Demonstrate correctness with focused tests.
- Explain runtime, space, structural complexity, coupling, and testability where relevant.
- Handle a follow-up change or concurrency concern without an unrelated broad rewrite.
- Defend patterns used and explain why rejected patterns were unnecessary or harmful.

At mastery, update requirements, design, implementation, tests, and review; mark the artifacts as `Mastered`; check the linked item in `progress.md`; and add a grounded history row.
