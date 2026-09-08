# Audit or Upgrade an Existing Harness

## Audit — read only

Inspect applicable repository instructions, the manuscript topology,
reviewer sources, and all harness files. Report concrete deviations in
these categories:

1. **Discovery:** the active `AGENTS.md` does not govern the intended
   paper root.
2. **Authority:** reviewer requests, author decisions, workflow state,
   diagnostics, or handoff text conflict or share an ambiguous canonical
   home.
3. **Coverage:** reviewer items, deliverables, dependencies, or clusters
   are missing or duplicated.
4. **State:** status vocabulary, transitions, plan confirmation, or
   author approvals are inconsistent.
5. **Preservation:** immutable reports or comparison baselines were
   modified, reconstructed, or cannot be identified.
6. **Verification:** build, log, page-count, source-diff, or comparison
   instructions are absent or invalid.
7. **Portability:** project instructions depend on this skill, a
   personal absolute path, or unavailable external configuration.
8. **Template drift:** format contracts, required fields, or generated
   file roles no longer agree.

Include the response letter and its local writing guide in the coverage
and portability checks. Read `response-writing.md` for the relevant
contract; verify that the guide identifies the actual evidence sources,
letter, and build command.

Do not edit the harness during an audit. Distinguish confirmed findings
from optional improvements and report the smallest bounded repair.

## Upgrade — explicit authorization required

An upgrade may improve structure and contracts, but it must preserve
scholarly and workflow state. Before editing, identify the current
canonical source for every mutable fact and map it to the target
structure.

If response resources are missing, an authorized upgrade may add the
local guide and empty letter scaffold using the initialization
procedure. Preserve an existing letter at its current path and adapt the
guide to it.

Never overwrite or silently regenerate:

- reviewer concern text;
- author dispositions, decisions, rationales, or approvals;
- ledger states and accepted page counts;
- author issue reports;
- unresolved diagnostic findings;
- immutable comparison baselines;
- manuscript, supplement, response-letter, bibliography, or source changes.

Integrate with an existing `AGENTS.md` rather than deleting unrelated
project rules. If two active sources disagree on mathematical
authorization, authoritative deliverables, or baseline identity, stop
and ask the author.

After a bounded upgrade, validate paths, tokens, states, and format
contracts; inspect the diff; and update the current handoff only when
its own contract requires it. Do not advance any workflow state merely
because the harness structure improved.
