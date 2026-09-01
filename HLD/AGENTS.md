# HLD Track Instructions

## Scope

Teach high-level and distributed-system design from first principles. Apply the root coaching and grounding rules. HLD is technology-aware but not product-name-driven: begin with requirements and guarantees, then select suitable mechanisms and only then discuss representative technologies.

## Foundation topic initialization

When an HLD foundation topic begins, create `HLD/topics/NN-kebab-case-topic/notes.md` and `practice.md` without overwriting existing files.

Initialize `notes.md` with:

```markdown
# <Topic>

- Status: In Progress
- Last updated: YYYY-MM-DD

## Mental Model and Purpose

## Core Mechanics and Vocabulary

## Guarantees and Assumptions

## Quantitative Reasoning

## Design Options and Trade-offs

## Failure Modes and Operational Concerns

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

## Concept Drills

| Date | Drill | Learner Decision | Trade-off or Gap | Next Action |
|---|---|---|---|---|

## Calculation and Failure-Mode Exercises

## Interview Follow-Ups

## Verified Resources
```

## Foundation teaching protocol

- Establish the problem the building block solves and the assumptions under which it works.
- Explain component behavior, data flow, control flow, state, and operational ownership.
- Derive relevant formulas and show units for latency, throughput, storage, bandwidth, fan-out, cache effectiveness, availability, and cost.
- Distinguish consistency models, durability, availability, fault tolerance, and disaster recovery rather than treating them as interchangeable.
- State the failure model before applying CAP, PACELC, consensus, quorum, replication, or coordination reasoning.
- Compare alternatives using explicit requirements and rejected trade-offs.
- Include hot keys, skew, overload, partial failure, retry amplification, data loss, reordering, duplication, and recovery where relevant.
- Use diagrams only when they clarify component relationships or behavior.
- Require the learner to explain the concept and apply it in a small drill before mastery.

## Case-study initialization

When an HLD case study begins, create its level-specific directory and these files:

- `prompt.md`
- `design.md`
- `review.md`

Initialize `prompt.md` with:

```markdown
# <Case Study>

- Level: <Foundation | Medium | Difficult>
- Path: <Core | Extension>
- Status: In Progress
- Started: YYYY-MM-DD

## Interview Prompt

## Skills Under Test

## Learner Questions and Interviewer Answers
```

Do not pre-fill hidden requirements or a reference solution. Add constraints only as they are established during the interview dialogue.

Initialize `design.md` with:

```markdown
# <Case Study> Design

- Status: In Progress
- Last updated: YYYY-MM-DD

## Problem Statement and Scope

## Clarifications and Assumptions

## Functional Requirements

## Non-Functional Requirements

## Back-of-the-Envelope Estimates

## API Contracts

## Data Model and Access Patterns

## High-Level Architecture

## Critical Read and Write Flows

## Component Deep Dives

## Consistency, Availability and Durability

## Reliability and Failure Recovery

## Security, Privacy and Abuse Prevention

## Observability and Operations

## Bottlenecks, Cost and Scaling Limits

## Alternatives and Trade-offs

## Evolution and Migration

## Interview Follow-Ups
```

Initialize `review.md` with:

```markdown
# <Case Study> Review

## Demonstrated Strengths

## Gaps and Risks

## Conceptual Hints Given

## Decisions and Rejected Alternatives

## Follow-Up Performance

## Mastery Decision
```

## HLD case-study interview flow

1. Present the broad prompt and let the learner drive clarification.
2. Lock functional and non-functional scope before architecture.
3. Require auditable traffic, storage, bandwidth, latency, and growth estimates when applicable.
4. Define APIs and access patterns before selecting storage and components.
5. Build the high-level diagram and explain critical request and data flows.
6. Select one or two requirement-driven deep dives rather than shallowly naming every technology.
7. Inject realistic failures, hot spots, growth changes, consistency demands, and operational follow-ups.
8. Require explicit alternatives and trade-offs.
9. Let the learner revise before recording review conclusions.

Do not turn the exercise into trivia about a specific vendor. Technology examples must follow from the required properties.

## HLD mastery gates

An HLD foundation topic is mastered only when the learner can explain its mental model, mechanics, applicability, guarantees, failure modes, quantitative implications, and trade-offs, then apply it in an unfamiliar drill.

An HLD case study is mastered only when the learner can:

- Lead requirements clarification and control scope.
- Produce and defend auditable scale estimates.
- Define coherent APIs, data models, architecture, and critical flows.
- Deep-dive the components that dominate the stated requirements.
- Reason about overload, partial failure, recovery, consistency, security, and operations.
- Identify bottlenecks and evolve the design under at least two interviewer follow-ups.
- Explain rejected alternatives without claiming a universal best design.

At mastery, update the design and review, mark the prompt and design as `Mastered`, update their dates, check the linked item in `progress.md`, and add a grounded history row.
