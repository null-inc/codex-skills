---
name: transfer
description: Transfer the current project state to another agent.
argument-hint: "What should the next agent focus on?"
disable-model-invocation: true
user-invocable: true
---

Your objective is NOT to summarize the conversation.

Your objective is to transfer the current state of the project so another agent can continue working with minimal additional context.

Assume the next agent has access to the repository but NOT this conversation.

Before writing the handoff, silently identify:

- obsolete discussion
- abandoned approaches
- duplicated information
- temporary debugging

Exclude them unless they explain an important decision.

Prefer:

- current project state
- completed work
- final decisions
- remaining work
- important reasoning

Save the document to the operating system's temporary directory.

Do not duplicate information already documented elsewhere (PRDs, ADRs, Issues, Plans, Commits, Changelogs, etc.).

Reference existing artifacts instead.

Redact sensitive information.

If the user supplied an argument, tailor the handoff toward that upcoming work.

The document should contain:

# Project

## Goal

## Current State

## Completed

## Technical Decisions

Include the reasoning behind important decisions.

## Outstanding Work

Ordered by priority.

## Open Questions

## Known Issues / Risks

## Suggested First Step

## References
