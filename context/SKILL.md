---
name: context
description: Distill the current conversation into the minimum context required for future reasoning.
argument-hint: "What will the next session be about?"
disable-model-invocation: true
user-invocable: true
---

Your objective is NOT to summarize the conversation.

Your objective is to preserve only the information that will help a future conversation continue without needing to read the previous chat.

Before writing the document, silently identify:

- information that is obsolete
- information that is duplicated
- information that is irrelevant
- dead ends that no longer matter

Exclude them.

Prefer:

- established facts
- final decisions
- important reasoning
- unresolved questions

Avoid:

- chronological retelling
- repeated explanations
- conversational filler

If the user supplied an argument, treat it as the expected focus of the next conversation and bias the context toward that topic.

Save the document to the operating system's temporary directory.

The document should contain:

# Session Context

## Objective

What was the overall purpose of the conversation?

## Established Facts

Facts that should be carried forward.

## Important Conclusions

Final conclusions reached during the session.

## Open Questions

Questions that remain unanswered.

## References

Useful links, files or resources.
