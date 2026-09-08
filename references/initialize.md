# Initialize a Referee Response Harness

Use this procedure to construct the harness, including an empty
response-letter scaffold. Do not draft substantive replies or revise
existing scholarly deliverables during initialization.

## 1. Establish the target

Identify the paper root and inspect applicable repository instructions
before writing. Determine:

- authoritative manuscript entry point and all included source files;
- bibliography, class, style, figure, data, supplement, and
  response-letter dependencies;
- existing build, clean, and comparison commands, noting which are
  unavailable;
- reviewer-report sources and whether their text can be extracted
  reliably;
- journal requirements, page limits, deadlines, or author-supplied
  constraints;
- existing `AGENTS.md` files and revision artifacts that must be
  preserved;
- current working-tree changes that belong to the author.

Identify the tools used to build the manuscript and whether its content
spans multiple source files. These findings inform the build and
comparison configuration in Section 4 Configure build and comparison
instructions.

Ask a narrow question only when uncertainty about the paper root,
authoritative deliverable, reviewer source, or build/comparison method
would make the generated harness materially wrong. Record non-blocking
unknowns as unresolved configuration.

## 2. Design the project-specific harness

Create or reconcile this structure beneath the paper root:

```text
AGENTS.md
HUMAN_GUIDE.md
review/
  revision-notes.md
  revision-ledger.md
  revision-issues.md
  consistency-check.md
  HANDOFF.md
  comparisons/
  response/
    response-writing.md
    response-letter.tex
```

Preserve existing project paths, reviewer sources, and response letters;
adapt this layout rather than relocating files for uniformity. Add
supplement, experiment, or multiple-manuscript branches only when
needed.

If an `AGENTS.md` already exists, preserve its unrelated instructions.
Add the revision contract at the narrowest directory that governs the
paper, or integrate it without duplicating or weakening active rules.

When completing a partial harness, preserve existing reviewer IDs,
decisions, approvals, and workflow state. Apply initialization defaults
only to newly created records.

## 3. Adapt the templates

Use the templates under `assets/` to create the files identified in
Section 2, removing the `.template` suffix.

- Fill placeholders with verified project information. State unknown
  values explicitly and record unresolved configuration in `HANDOFF.md`.
- Set `{{HARNESS_VERSION}}` from `metadata.version` in `SKILL.md`.
- Preserve the templates' format instructions. Remove inapplicable
  sections and unused example entries.
- Adapt paths and commands to the project while preserving existing
  content as required by Section 2.

Adapt [response-writing.md](response-writing.md) into the project's
response directory, identifying the local evidence sources, response
letter, and build command.

If no response letter exists, create an empty scaffold from its
template, adapting it to any supplied journal requirements. Keep the
reusable LaTeX definitions and instructional comments.

## 4. Configure build and comparison instructions

Using the project information gathered in Section 1, fill the build
and comparison fields in the generated `AGENTS.md`.

Preserve existing build tooling. Reuse an existing comparison command
when suitable; otherwise, prepare one using available tools that
covers the manuscript's source files. Specify each command's working
directory, required arguments, and output location.

Include response-letter and supplement builds when applicable.

If the available tools or project information are insufficient to
configure a command, mark it as unresolved and explain the limitation
in `review/HANDOFF.md`.

Create the comparison directory, but leave baseline creation and
comparison generation to later revision work.

## 5. Validate and hand off

Check the generated workspace:

- Files required by the adapted layout exist, and local file links
  resolve.
- Template placeholders and unused example entries are removed. Unknown
  configuration is stated explicitly.
- Documented paths, commands, and required tools match the project.
  Distinguish commands inspected from commands successfully tested.
- A newly created response letter contains no substantive replies. Build
  it when the required tools are available and check for errors.
- Existing scholarly deliverables, reviewer sources, decisions,
  approvals, revision progress, and comparison baselines are preserved.

Fix defects introduced during initialization and repeat the affected
checks. Record any checks that could not run and why.

Update `review/HANDOFF.md` with the checks performed, unresolved
configuration, and the next author action. For a new harness, state that
reviewer import and revision planning have not started. For a partial
harness, describe the preserved workflow state.

Report the files created or changed and remaining limitations. Stop
after initialization.
