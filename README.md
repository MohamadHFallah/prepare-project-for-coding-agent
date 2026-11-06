# Prepare a Legacy Project for Coding Agents

This repository contains reusable prompts and safety guidance for documenting an existing codebase before asking a coding agent to work on it. The aim is to help a person and an agent understand a legacy project, record its verified conventions, and make future changes with less guesswork.

The prompts currently use a Next.js e-commerce application as their example. Adapt the project-specific details to your own repository before using them; do not treat the example stack or features as facts about another codebase.

## What’s here

- `AGENTS.md` — project safety rules for agents. In particular, analysis is read-only, dependencies must not be installed, and database schemas or data must not be changed.
- `discovery-project.md` — prompt for a read-only architecture and legacy-code assessment, including risks and open business-rule questions.
- `documents-structure-prompt.md` — prompt for creating technical documentation grounded in the actual implementation.
- `create-agents-prompt.md` — prompt for drafting concise, project-specific root agent instructions.
- `create-design.md` — prompt for analyzing the existing UI and documenting its design conventions in `design.md`.

## Suggested workflow

1. **Start with safety.** Read `AGENTS.md` and preserve its boundaries. Treat the target project as production code: inspect first, and do not change application code during analysis.
2. **Discover the project.** Run the instructions in `discovery-project.md` against the target repository. Verify findings in source files and note uncertainties rather than filling gaps with assumptions.
3. **Document what is verified.** Use `documents-structure-prompt.md` to create the proposed architecture, structure, database, authentication, feature, and testing documents. Mark unresolved business rules as open questions.
4. **Prepare agent guidance.** Use `create-agents-prompt.md` to write concise instructions that refer to the actual project architecture, scripts, conventions, and documentation.
5. **Document the UI when relevant.** For a project with a user interface, use `create-design.md` to document its existing patterns. The prompt asks for `design.md` and prohibits redesigning or modifying application source code.
6. **Review before implementation.** Check file references and claims against the repository, separate observations from recommendations, resolve open questions with a human, and have the project owner review the documentation before agents rely on it.

## Guidelines for adapting these prompts

- Replace example technologies and feature lists with details appropriate to the target project.
- Ask the agent to report evidence and file paths; do not ask it to infer undocumented behavior.
- Keep analysis and implementation as separate phases. Explicitly authorize code changes only when ready for implementation.
- Preserve existing architecture and conventions unless a human has approved a change.
- Do not install dependencies or alter database schemas/data as part of documentation work.
- Run only checks that are already available in the target project, and follow its own instructions.

These prompts are starting points, not a substitute for repository-specific review or human decisions about business rules.
