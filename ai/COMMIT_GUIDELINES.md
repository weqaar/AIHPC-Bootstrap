# Commit & AI Attribution Guidelines

This repository follows the Linux kernel project's guidance for
contributions made with the help of AI coding assistants:

- Upstream reference:
  <https://docs.kernel.org/process/coding-assistants.html>

These rules apply to **every commit** in this repo, including
documentation and curriculum content.

## Core principles

1. **Humans certify, not agents.** Only a human contributor may add a
   `Signed-off-by:` trailer. That trailer certifies the Developer
   Certificate of Origin (DCO) and means *you* take responsibility for
   the change. AI agents **must not** add `Signed-off-by:` lines on
   their own behalf.
2. **Review before you commit.** When an AI assistant produces code,
   docs, or config, the human author must read it, understand it, and
   verify it builds / runs / makes sense before staging it.
3. **Licensing compliance is the human's job.** Make sure AI-generated
   content is compatible with this repo's license (see `LICENSE`) and
   does not import incompatible third-party material.

## Attribution trailer

When an AI assistant materially contributed to a commit, add an
`Assisted-by:` trailer (one per agent) at the **bottom of the commit
message**, after any `Signed-off-by:` line:

```
Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]
```

- `AGENT_NAME` — the AI tool / framework (e.g. `Copilot`, `Claude`,
  `Cursor`, `Aider`).
- `MODEL_VERSION` — the specific model that produced the output
  (e.g. `gpt-5`, `claude-3.5-sonnet`, `claude-opus-4.7`).
- `[TOOL1] [TOOL2]` — *optional* specialized analysis tools the agent
  invoked while preparing the change (e.g. `coccinelle`, `sparse`,
  `smatch`, `clang-tidy`, `ruff`, `mypy`).

**Do not list everyday dev tools** (git, gcc, make, cmake, your
editor, shells, etc.) in the bracketed list.

> **Do not** use `Co-authored-by: Copilot <...>` or any other
> `Co-authored-by:` trailer for AI agents in this repository.
> AI assistants are not co-authors; they are tools, and `Assisted-by:`
> is the correct trailer.

### Examples

Single agent, no extra tooling:

```
docs(project-01): clarify cloud-init seed step

Walk through user-data / meta-data more explicitly so first-time
readers can reproduce the seed.iso build without guessing.

Signed-off-by: Jane Developer <jane@example.org>
Assisted-by: Copilot:claude-opus-4.7
```

Agent plus static-analysis tools:

```
projects/02: add MPI hello-world with bounds checks

Signed-off-by: Jane Developer <jane@example.org>
Assisted-by: Claude:claude-3.5-sonnet clang-tidy
```

Multiple agents collaborated on one change:

```
ai: refresh repo conventions for new curriculum modules

Signed-off-by: Jane Developer <jane@example.org>
Assisted-by: Copilot:gpt-5
Assisted-by: Claude:claude-3.5-sonnet
```

## When attribution is **not** required

- Trivial mechanical edits where no AI suggestion was used (typo
  fixes, whitespace, file moves).
- Cases where the AI assistant was used only as a search engine /
  rubber-duck and produced no text that landed in the commit.

If in doubt, add the trailer — over-attribution is harmless,
under-attribution is not.

## Suggested git commit template

Save this as `~/.gitmessage` and run
`git config --global commit.template ~/.gitmessage`:

```
<scope>: <short imperative summary>

<body: what & why, wrapped at 72 cols>

Signed-off-by: Your Name <you@example.org>
# Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]
```

Uncomment and fill in the `Assisted-by:` line whenever an AI agent
helped produce the change.
