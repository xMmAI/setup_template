---
name: writing-plans
description: Use when you have a spec or requirements for a multi-step task, before touching code. Generates bite-sized, actionable tasks.
---

# Planning Implementation

## When to use this skill
- When you have a design or requirements for a feature.
- Before starting any multi-step implementation.
- To break down complex tasks into manageable checkpoints.

## Plan Creation Stage

Based on the full exchange/design, produce a markdown plan document using the template below.

### Requirements for the plan:
- **Conciseness**: Include clear, minimal, and concise steps.
- **Status Tracking**: Track the status of each step using these emojis:
  - 🟩 Done
  - 🟨 In Progress
  - 🟥 To Do
- **Progress Tracking**: Include dynamic tracking of overall progress percentage (at top).
- **Scope Control**: Do NOT add extra scope or unnecessary complexity beyond explicitly clarified details.
- **Seamless Integration**: Steps should be modular, elegant, minimal, and integrate seamlessly within the existing codebase.

## Markdown Template

Use this exact structure for implementation plans:

```markdown
# [Feature Name] Implementation Plan

**Overall Progress:** `0%`

## TLDR
Short summary of what we're building and why.

## Critical Decisions
Key architectural/implementation choices made during exploration:
- Decision 1: [choice] - [brief rationale]
- Decision 2: [choice] - [brief rationale]

## Tasks:

- [ ] 🟥 **Step 1: [Name]**
  - [ ] 🟥 Subtask 1: [e.g. Write failing test for X]
  - [ ] 🟥 Subtask 2: [e.g. Implement minimal logic for X]
  - [ ] 🟥 Subtask 3: [e.g. Verify with command Y]

- [ ] 🟥 **Step 2: [Name]**
  - [ ] 🟥 Subtask 1
  - [ ] 🟥 Subtask 2
```

## Key Principles
- **Exact file paths always**: Never use placeholders.
- **Complete code in plan**: Do not say "add logic", show the exact code or specific implementation steps.
- **TDD approach**: Prefer writing the failing test before the implementation.
- **Frequent commits**: Each major step should end with a suggested commit.

## Resources
- [See examples/](examples/) for sample plans following this optimized format.
