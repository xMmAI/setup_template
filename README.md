# Antigravity Skills Template

This repository contains a comprehensive set of "Skills" for the Antigravity agent environment, along with a system for generating new high-quality skills to development.

## 🚀 Key Features

- **Skill Creator System**: A set of instructions to generate consistent, high-quality skills.
- **CTO Architecture Skill**: Acting as a technical lead to bridge product and engineering.
- **Optimized Planning**: Clear, minimal, and concise task tracking with emoji status updates.
- **Collaborative Brainstorming**: A structured process for refining ideas into designs.
- **Advanced Code Review**: Comprehensive checklists for quality, security, and performance.
- **Troubleshooting**: Master error handling patterns across multiple languages (Python, TS, Rust, Go).
- **Automated Testing**: Support for Vite and Next.js testing workflows.
- **Brand Identity**: Centralized design tokens and technical constraints.

## 📂 Project Structure

```text
.
├── .agent/
│   ├── skills/              # Managed skills directory
│   │   ├── acting-as-cto/   # Architecture & strategy role
│   │   ├── ...              # Other specialized skills
│   └── workflows/           # Procedural slash commands
│       ├── draft-prd        # /draft-prd command
│       ├── generate-tasks   # /generate-tasks command
│       └── execute-tasks    # /execute-tasks command
└── antigravity-skill-creator.md # System instructions for skill generation
```

## 🌊 Workflows (Commands)

These are specific, procedural "recipes" you can trigger using slash commands:

- **`/draft-prd`**: Guided interview to turn a vague idea into a detailed Product Requirements Document (tasks/ folder).
- **`/generate-tasks`**: Analyzes a PRD and generates a hierarchical checklist (tasks/ folder).
- **`/execute-tasks`**: The coding engine. Implements tasks one-by-one, runs tests, and creates standardized commits.

## 🛠 Using the Skill Creator

To create a new skill, follow these steps:

1.  Open `antigravity-skill-creator.md`.
2.  Provide these instructions to the Antigravity agent.
3.  Trigger a creation: *"Based on my skill creator instructions, build me a skill for [Task]"*.

## ⚖️ Standards

Every skill in this repository adheres to:
- **Gerund Naming**: (e.g., `reviewing-code`, `managing-databases`).
- **Claude Way**: Concise, progressive disclosure, and smart defaults.
- **Workflow-Driven**: High-freedom heuristics mixed with low-freedom commands.
- **Status Tracking**: Uses 🟩, 🟨, 🟥 for progress visualization in plans.
