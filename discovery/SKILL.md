---
name: discovery
description: Interview the user to discover project requirements before producing a project plan.
argument-hint: "Briefly describe your project idea."
disable-model-invocation: true
user-invocable: true
---

Your objective is to help the user refine a project idea before any implementation begins.

Do not immediately produce a project plan.

Instead, interview the user to discover the project's goals, requirements, constraints, assumptions, and definition of success.

Prioritize understanding the problem over proposing solutions.

Throughout the interview, actively look for opportunities to reduce scope while still solving the user's core problem. Prefer identifying the smallest valuable MVP before discussing future enhancements.

## Guidelines

- Ask one question at a time.
- Allow each answer to influence the next question.
- Challenge assumptions when appropriate.
- Avoid making unnecessary assumptions.
- Avoid proposing an architecture until the requirements are sufficiently understood.
- If important information is missing, identify it and ask about it before proceeding.
- Periodically summarize what has been learned before continuing the interview.
- If multiple reasonable approaches exist, explain their trade-offs before recommending one.
- If a proposed feature significantly increases complexity, explain the trade-offs and ask whether it belongs in the MVP or a later milestone.
- Encourage keeping the initial scope as small as possible.

Continue interviewing until either:

- enough information has been gathered to produce a meaningful project plan, or
- the user explicitly asks to stop interviewing.

## Discovery Exit Criteria

Discovery is complete when the following are understood:

- The core problem.
- The target user.
- The project's success criteria.
- The agreed MVP scope.
- Major constraints and assumptions.
- Known risks.
- Remaining open questions.

## Phase 1 — Discovery

Interview the user to understand the problem.

Focus on questions such as:

- What problem are we solving?
- Who is the intended user?
- Why do existing solutions fall short?
- How will success be measured?
- What is the smallest useful version of this project?
- What constraints or limitations exist?

Remain in this phase until the Discovery Exit Criteria have been satisfied.

Do not propose implementation details or architecture yet.

## Phase 2 — Planning

Once sufficient information has been gathered, produce a project plan tailored to the user's goals.

## Project Plan Format

### Project Goal

A concise description of what the project aims to accomplish.

### Problem Statement

Describe the problem the project is solving.

### Target Users

Who will use the project?

### Success Criteria

Define what must be true for the MVP to be considered complete.

### Scope

Describe the agreed MVP.

### Core Features

Features required for the MVP.

### Future Enhancements

Ideas intentionally deferred until after the MVP.

### Non-goals

Things explicitly out of scope.

### Technical Constraints

Languages, platforms, integrations, performance requirements, or other constraints.

### Design Principles

High-level principles that should guide future decisions.

Examples:

- Simplicity over cleverness.
- Keyboard-first.
- Local-first.
- Fast startup.
- Minimal dependencies.

### Open Questions

Anything that still requires clarification.

### Risks

Potential technical or product risks.

### Technical Direction (if appropriate)

A high-level recommendation for the implementation approach.

Avoid detailed architecture unless necessary.

### Milestones

Break the project into logical implementation phases.

### Suggested Next Steps

Recommend the first concrete actions to begin the project.
