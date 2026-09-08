# Referee Response Harness

A Codex skill that helps you organize a LaTeX paper revision—from reviewer comments to an author-approved response.

It sets up instructions and tracking files inside your paper project. Codex uses them to keep track of reviewer requests, your decisions, and revision progress. You decide what changes to make and approve the results.

## 1. Install

Download or clone this repository. Copy the whole folder to:

```text
~/.agents/skills/referee-response-harness/
```

Make sure `SKILL.md` is directly inside that folder, alongside `agents/`, `assets/`, and `references/`.

For installation in just one project, use `<paper-repository>/.agents/skills/referee-response-harness/` instead. If the skill does not appear in Codex, restart it. See the [Codex skill documentation](https://developers.openai.com/codex/skills) for details.

## 2. Set up your paper

Open Codex in your **paper project** and send this prompt, adjusting the paths:

```text
$referee-response-harness Initialize a revision harness for this paper.
The manuscript is main.tex, and the reviewer reports are in reviewer-reports/.
```

Mention any journal requirements or build commands you already use. If reviewer reports are not available yet, say so. Building and comparing revised documents later requires suitable LaTeX and comparison tools; Codex records missing configuration during setup.

Codex creates the revision workspace and tells you what needs attention. Setup preserves existing manuscript content and stops before importing reviewer comments or drafting substantive replies.

## 3. Start the revision

After reviewing the setup, send:

```text
Extract the reviewer comments and group related concerns into a proposed
revision plan. Leave undecided items pending and do not edit the manuscript.
```

From there, the workflow is:

1. Review the proposed plan.
2. Discuss each group of concerns and decide how to respond.
3. Authorize changes, then inspect the revised documents and comparisons.
4. Request corrections or approve the work.
5. Prepare the response letter and review the final submission materials.

You can continue in ordinary language. The generated project instructions guide later work without needing to invoke this skill again.

**Want to try it first?** Follow the [fictional paper example](examples/minimal/README.md), which includes a small LaTeX manuscript and two reviewer comments.

## Where to look

The skill adds these files to your paper project, adapting to its existing layout:

| File | What it helps with |
|---|---|
| `HUMAN_GUIDE.md` | Understanding the workflow when you need more detail. |
| `review/HANDOFF.md` | Seeing current progress and your next action. |
| `review/revision-notes.md` | Reviewing the referee concerns and your decisions. |
| `review/revision-ledger.md` | Tracking the revision plan and approvals. |

It also adds instructions for Codex in `AGENTS.md`, issue and consistency records, a comparison directory, and response-writing guidance. If no response letter exists, it creates an empty LaTeX scaffold.

## Already have a harness?

Check it without changing files:

```text
$referee-response-harness Audit this paper's revision harness without editing files.
```

Compare your harness with the current requirements and update outdated
instructions while preserving your work:

```text
$referee-response-harness Upgrade this paper's revision harness.
Preserve existing content, decisions, approvals, and revision progress.
```

Upgrade preserves project customizations and existing letter formatting.
It reports what changed, what was intentionally retained, and why no edits
were needed if the harness already meets the requirements.

For implementation details, see [SKILL.md](SKILL.md) and the [initialization](references/initialize.md) and [audit/upgrade](references/audit-upgrade.md) instructions. These documents are primarily for the agent and skill maintainers.

