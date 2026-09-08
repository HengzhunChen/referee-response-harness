---
name: referee-response-harness
description: Initialize, audit, or upgrade a structured revision harness for LaTeX scholarly papers. Use when asked to create or reuse project instructions, reviewer-decision tracking, author checkpoints, and cumulative comparison artifacts for a paper revision. Do not use for ordinary manuscript edits after an existing harness already governs the work.
metadata:
  version: "0.1.0"
---

# Referee Response Harness

Create and maintain a self-contained revision harness adapted to each paper's sources, reviewer reports, deliverables, and workflow. This skill initializes, audits, or upgrades auxiliary files such as `AGENTS.md`, `HUMAN_GUIDE.md`, decision records, and tracking templates.

The generated project instructions govern subsequent author-requested revision work. They must contain the paper-specific context and operational rules needed to continue without this skill installed. Manuscript revision is outside this skill's scope. 

## Select the operation

- **Initialize:** No complete harness exists, or the user asks to create one. Read [references/initialize.md](references/initialize.md), then adapt the files under `assets/` to the target paper.
- **Audit:** The user asks whether an existing harness is complete, coherent, or reusable. Read [references/audit-upgrade.md](references/audit-upgrade.md) and perform its read-only audit.
- **Upgrade:** The user explicitly asks to bring an existing harness to the current design. Read [references/audit-upgrade.md](references/audit-upgrade.md), preserve project state, and propose or apply bounded structural changes as authorized.

If the requested operation is clear, proceed without asking. If several candidate paper roots or authoritative manuscripts exist and choosing incorrectly would change files outside the intended paper, ask the user to identify the target.

## Rules for creating and maintaining the harness

- Preserve existing scholarly deliverables and author work.
  Initialization may create an empty response-letter scaffold.

- Preserve reviewer wording, recorded author decisions, approvals,
  and existing revision progress. Setting up or upgrading the
  harness must not reset them or imply new approval.

- Make the generated files distinguish reviewer requests,
  author decisions, and work progress, so later agents can tell
  what was requested, what was authorized, and what was completed.

## Finish the operation

Validate the generated or updated artifact set, inspect the diff, and report:

- the target paper root and authoritative deliverables;
- files created or changed;
- assumptions and unresolved configuration;
- validation performed;
- the single next author action.

For initialization, stop after the harness is ready for author review. Do not begin resolving reviewer items in the same operation.
