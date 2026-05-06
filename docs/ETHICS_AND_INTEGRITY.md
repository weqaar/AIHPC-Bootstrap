# Ethics & Integrity

This document is **mandatory reading** for every participant in the
AIHPC-Bootstrap curriculum — students, mentors, and contributors alike.

---

## 1. IEEE Code of Ethics

All participants must read, understand, and abide by the
**IEEE Code of Ethics**:

> <https://www.ieee.org/about/corporate/governance/p7-8.html>

The Code commits members to the highest standards of integrity,
responsible behaviour, and ethical conduct in professional practice.
Key tenets relevant to this curriculum include:

- **Honesty in claims and estimates.** Represent your own work
  truthfully. Do not claim authorship of work you did not produce.
- **Avoidance of conflicts of interest and deceptive acts.**
- **Fair treatment of all persons** regardless of race, religion,
  gender, disability, age, national origin, sexual orientation, or
  gender identity.
- **Commitment to improving understanding of technology** and its
  appropriate application.

Violation of these principles is grounds for removal from the programme.

---

## 2. AI Ethics and Attribution

### 2.1 Philosophy: learn by doing

The purpose of this curriculum is to **build genuine competence**.
AI coding assistants (GitHub Copilot, ChatGPT, Claude, etc.) are
powerful tools, but they are exactly that — *tools*. They do not replace
the understanding that comes from working through problems yourself.

**The expectation is that you do most of the work yourself.** Use AI
assistance sparingly and only where it genuinely helps you learn faster:

| ✅ Acceptable AI use | ❌ Unacceptable AI use |
| --- | --- |
| Generate a **code stub or skeleton** that you then complete, debug, and understand line-by-line | Paste an entire assignment prompt into an AI and submit the raw output |
| Ask the AI to **explain a concept** you're struggling with (e.g. "explain virtual memory paging") | Let the AI write a complete solution you cannot explain or reproduce |
| Use **inline coding assistance** (autocomplete, linting suggestions) while you type | Bulk-generate documentation or reports without reading and verifying every claim |
| Ask for **guidance on an approach** ("what data structure fits this access pattern?") | Misrepresent AI-generated work as entirely your own |

### 2.2 Attribution is non-negotiable

When AI assistance materially contributes to a commit, lab report, or
any deliverable, you **must** attribute it. This repository uses the
`Assisted-by:` commit trailer defined in
[`ai/COMMIT_GUIDELINES.md`](../ai/COMMIT_GUIDELINES.md), which adopts
the Linux kernel project's
[coding-assistants policy](https://docs.kernel.org/process/coding-assistants.html).

```
Assisted-by: AGENT_NAME:MODEL_VERSION [TOOL1] [TOOL2]
```

Omitting attribution when AI was used is an integrity violation — treat
it the same as plagiarism.

### 2.3 You own the output

Using an AI tool does **not** absolve you of responsibility:

- You must **review** every line of AI-generated code or text.
- You must be able to **explain** what it does and **why** you chose it.
- Bugs, licensing issues, or incorrect claims in AI output are **your**
  responsibility once you commit them.

### 2.4 When in doubt

If you are unsure whether your use of AI crosses the line:

1. **Ask your mentor.** Transparency is always the right call.
2. **Add the attribution trailer.** Over-attribution is harmless;
   under-attribution is not.
3. **Re-derive the work yourself.** If you can't write the solution
   without the AI, you haven't learned the material yet — and that's
   the whole point.

---

## 3. Academic and professional integrity

Beyond AI-specific rules:

- **Do not plagiarise.** Always cite sources — papers, Stack Overflow
  answers, blog posts, textbooks — in your code comments or
  documentation.
- **Do not fabricate results.** Benchmarks, test outputs, and
  measurements must be real and reproducible.
- **Respect licences.** Understand the licence of any code you use
  (this repo is covered by the `LICENSE` file in the root). Do not
  import incompatibly-licensed code.
- **Collaborate honestly.** Helping peers is encouraged; doing their
  work for them is not.

---

## Summary

| Principle | In practice |
| --- | --- |
| Learn by doing | Do the bulk of the work yourself |
| Use AI as a tool, not a crutch | Stubs, explanations, guidance — not wholesale generation |
| Always attribute | `Assisted-by:` trailer on every AI-assisted commit |
| Follow IEEE Code of Ethics | Honesty, fairness, responsibility |
| Own your output | Review, understand, and stand behind everything you submit |
