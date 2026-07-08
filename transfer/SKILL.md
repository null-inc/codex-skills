---
name: transfer
description: Transfer the current project state to another agent.
argument-hint: "What should the next agent focus on?"
disable-model-invocation: true
user-invocable: true
---

Your objective is NOT to summarize the conversation.

Your objective is to transfer the current state of the project so another agent can continue working with minimal additional context.

Assume the next agent has access to the repository and existing project documentation, but NOT this conversation.

The handoff should act as the project's recent working memory rather than permanent documentation.

## Principles

- Prefer project state over conversation history.
- Prefer final decisions over discussions.
- Prefer references over duplication.
- Prefer concise explanations over exhaustive detail.
- Preserve the reasoning behind important technical decisions.

Before writing the handoff, silently identify:

- obsolete discussion
- abandoned approaches
- duplicated information
- temporary debugging
- conversational filler

Exclude them unless they explain an important decision.

Do not duplicate information already documented elsewhere (PRDs, ADRs, Issues, Plans, Commits, Changelogs, etc.).

Reference existing artifacts instead.

Redact sensitive information.

If the user supplied an argument, tailor the handoff toward that upcoming work.

## Output

Save the handoff document to:

~/.codex/handoffs/

Create the directory if it does not already exist.

Determine the project name from the repository name when possible.

Save the document as:

<project-name>.md

If the project name cannot be determined automatically, ask the user before saving.

Overwrite any existing handoff for the same project.

## Handoff Format

# Project

## Goal

Briefly describe the purpose of the project.

## Current Focus

What was the previous session primarily working on?

## Current State

Summarize the current state of the project.

## Recent Progress

Describe the most significant progress made since the previous handoff.

## Technical Decisions

Document important technical decisions together with the reasoning behind them.

## Outstanding Work

List remaining work ordered by priority.

## Open Questions

Document unresolved questions that should be answered in future sessions.

## Known Issues / Risks

Document bugs, blockers, technical debt or known risks.

## Suggested First Step

Describe the most useful first action for the next session.

## References

Reference relevant documentation, issues, plans, ADRs, commits or files instead of duplicating their contents.
