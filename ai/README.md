# AI Agent Context & Instructions

This directory holds context, conventions, and instructions for AI coding
agents (GitHub Copilot, Claude, etc.) collaborating on this repository.

## Purpose

As the curriculum and projects evolve, this folder will accumulate:

- **Context files** — high-level descriptions of the repo, target audience,
  and current project focus.
- **Agent instructions** — coding conventions, doc style guides, preferred
  toolchains, and review checklists.
- **Prompts & playbooks** — reusable prompts for common tasks (generating
  lab guides, reviewing student PRs, scaffolding new projects).

## Repository overview

`AIHPC-Bootstrap` is a Training & Development repository focused on
**AI / HPC** topics. Audience: college students through experienced
professionals.

## Top-level layout

```
ai/         AI agent context and instructions (this folder)
docs/       Markdown documentation
docs/latex  LaTeX sources
docs/pdf    PDFs generated from docs/latex
projects/   Hands-on projects
```

## Conventions for agents

- Project documentation is authored in **Markdown** under
  `projects/<project-name>/` unless a project explicitly calls for LaTeX.
- LaTeX sources live in `docs/latex/`; generated PDFs in `docs/pdf/`
  (PDFs may be committed for convenience but are build artifacts).
- Each project gets its own numbered directory:
  `projects/NN-short-slug/` with a `README.md` as the entry point.
- Prefer reproducible, copy-pasteable shell snippets in lab/setup docs.
- Target Ubuntu LTS releases unless a project requires otherwise.

## Commit & AI attribution

All commits to this repo must follow
[`COMMIT_GUIDELINES.md`](COMMIT_GUIDELINES.md), which adopts the Linux
kernel project's
[coding-assistants guidance](https://docs.kernel.org/process/coding-assistants.html).

Key rules:

- Humans add `Signed-off-by:` and own DCO certification; AI agents
  must not.
- When an AI agent materially helps with a change, add an
  `Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]` trailer.
- **Do not** use `Co-authored-by: Copilot` (or any `Co-authored-by:`
  for an AI agent) in this repo.
