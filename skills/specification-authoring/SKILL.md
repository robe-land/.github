---
name: specification-authoring
description: Use when someone requests a specification or when an existing specification is part of the task; helps capture proportionate, verifiable capability needs.
license: MIT
---

# Specification Authoring

Use this skill when someone requests a specification or when an existing
specification is part of the task. A specification is one way to record
capability needs; it is not a prerequisite for each implementation change.

## Understand the work

- Identify the intended outcome, accountable capability owner, readers,
  boundaries, and exclusions.
- Read the owning repository's instructions and relevant documents. Follow
  its documentation location and format.
- Find accepted ADRs, contracts, schemas, and other authoritative sources.
  Link to those sources instead of restating settled decisions or duplicating
  their definitions.
- Distinguish established decisions from proposals and unresolved questions.
  Do not fill evidence gaps with assumptions.

## Describe what matters

- State expected behavior so that a reader can tell what must be true.
- Make requirements, fixed constraints, and non-binding recommendations
  visibly distinct.
- Describe interfaces and data boundaries when they affect ownership,
  semantics, compatibility, failure behavior, or relevant security and
  operational obligations. Point to the authoritative contract or schema
  where one exists.
- Provide observable acceptance checks. Use requirement identifiers only when
  they help connect requirements to reviews, interfaces, or tests.
- Include dependencies, examples, assumptions, and edge cases only when they
  clarify scope or change how the outcome is assessed.
- Avoid prescribing implementation choices unless they are established
  constraints or necessary to the agreed outcome.

## Keep the document useful

- Scale the document to the capability and the uncertainty being resolved.
  The companion [template](./templates/specification.md) is optional; retain
  only sections that help explain or verify this work.
- Inherit the owning repository's testing and documentation practices. Do not
  introduce test frameworks, coverage targets, or documentation requirements
  that the repository has not established.
- Before finishing, check that scope and exclusions are understandable,
  acceptance checks can be evaluated, references work, and the document does
  not conflict with authoritative decisions.
- Revisit the document when related changes make it inaccurate. Keep it in
  the repository that owns the described capability.

## Platform capabilities

For a capability owned by `robe-event-platform`, its specification belongs
to that repository and follows its documentation conventions. Consult
ADR-0005, Evolutionary Architecture and Incremental Delivery, to separate
current acceptance needs from future concerns. Recording a future concern
does not make it an implementation requirement or justify speculative
scaffolding.
