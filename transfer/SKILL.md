---
name: transfer
description: Preserve the project's working memory for the next agent.
argument-hint: "What should the next agent focus on?"
disable-model-invocation: true
user-invocable: true
---

<!-- Transfer Skill v1.0.0 -->

Your objective is NOT to summarize the conversation.

Instead, preserve the project's working memory by transferring the current project state so another agent can continue working with minimal additional context.

Assume the next agent has access to the repository and existing project documentation, but NOT this conversation.

The handoff should serve as the project's recent working memory rather than permanent documentation.

The handoff should capture only the information that would otherwise be lost when the current conversation ends.

## Principles

- Prefer project state over conversation history.
- Prefer final decisions over discussions.
- Prefer references over duplication.
- Prefer concise explanations over exhaustive detail.
- Preserve the reasoning behind important technical decisions.
- Prefer current project state over historical context.

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

Include the following metadata at the beginning of the handoff:

- Generated timestamp (ISO 8601)
- Project name
- Git branch (if available)
- Current commit hash (if available)

The metadata should appear before the project sections.

## Handoff Format

# Project

Generated: <ISO 8601 timestamp>

Project: <project name>

Branch: <git branch>

Commit: <commit hash>

## Goal

Briefly describe the purpose of the project.

## Previous Session

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

Reference existing documentation instead of duplicating it whenever practical.
