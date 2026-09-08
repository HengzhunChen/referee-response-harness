# Try the harness on a fictional paper

This example contains a short LaTeX manuscript and two invented reviewer
comments. No real research, author information, or reviewer material is used.
It is a starting project for trying the skill, not a completed revision.

The manuscript uses `main.tex` and an included file, `sections/method.tex`,
so the workflow must account for changes across multiple source files.
The comments ask for a fuller proof and a worked example of an elementary
least-squares result. No external data or bibliography is needed.

## 1. Make a working copy

Install the skill as described in the [main README](../../README.md).
Copy the `paper/` directory to a separate workspace so the original example
remains reusable. On macOS or Linux, run this from the skill repository root:

```sh
referee_demo_dir="$(mktemp -d)"
cp -R examples/minimal/paper "$referee_demo_dir/paper"
printf 'Open this paper workspace in Codex: %s\n' "$referee_demo_dir/paper"
```

This creates a temporary workspace. Use a permanent copy elsewhere if you
want to keep your revision work.

## 2. Initialize

Open the copied paper directory in Codex and send:

```text
$referee-response-harness Initialize a revision harness for this fictional
paper. The manuscript entry point is main.tex, which includes
sections/method.tex. The reviewer report is reviewer-reports/reviewer-1.md.
Build from the paper root with:
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
There are no journal requirements, supplements, or existing response letter.
Configure source comparisons using available tools and report any missing
configuration. Preserve the manuscript and original reviewer report.
```

The build requires a LaTeX installation with `latexmk` and the packages
loaded in `main.tex`. If those tools are unavailable, Codex should report
the limitation.

After initialization, check that:

- `AGENTS.md`, `HUMAN_GUIDE.md`, and the `review/` records exist.
- Manuscript sources and the reviewer report are unchanged.
- The generated instructions account for the included source file.
- The response letter has no substantive replies yet.
- `review/HANDOFF.md` identifies checks performed, unresolved configuration,
  and the next author action. Reviewer import and planning have not started.

## 3. Try the author workflow

Ask Codex:

```text
Import both reviewer comments, preserving their wording, and propose a
revision plan. Leave my decisions pending and do not edit the manuscript.
```

Review and confirm the proposed grouping. Discuss each group with Codex,
decide which changes to accept, and explicitly authorize implementation.
For this example, a possible treatment is to expand the proof, establish
uniqueness, add the requested numerical example, and explain the one-value
case. These are suggestions for you to consider, not pre-recorded decisions.

Inspect the source changes and cumulative comparisons before approving
the work. You can then authorize response drafting and the final audit.

To inspect the resulting harness without changing it, use:

```text
$referee-response-harness Audit this paper's revision harness without
editing files. Report concrete findings and any checks you could not run.
```
