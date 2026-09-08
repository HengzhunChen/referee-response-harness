# Writing a Response to Reviewers

Draft from the original reviewer reports, current author decisions, and
verified manuscript and supplement. Continue the project's response
letter using its existing format. Follow the main harness for
authorization, workflow state, and author review.

## Structure

Begin with a brief acknowledgment and a short summary of the main
verified changes. Then address the editor and each referee in the
original report order. Write the summary after the detailed replies.

For each comment:

1. **Quote the original wording**, including its mathematical
   qualifications; decision notes may only be summaries. Check uncertain
   extraction against the source.
2. **Answer directly:** explain what changed or was retained and why it
   addresses the concern.

Map each reply to its reviewer IDs in a LaTeX source comment. Answer
every subquestion, even when related replies share an explanation.

## Content and tone

- For partial acceptance or disagreement, explain both the implemented
  treatment and the reason for the remaining boundary. Do not imply full
  compliance.
- Verify claimed additions, removals, or corrections against the source
  comparisons. An existing reply is not evidence that a change occurred.
- Match the manuscript's assumptions, quantifiers, and strength of
  claims. Distinguish this paper's results from verified results in
  companion work.
- Flag pending decisions or missing implementation as draft gaps. Do not
  invent completed work, promise unapproved experiments, or silently
  change the manuscript to fit the reply.
- Use concise, respectful, factual prose. Avoid repeated thanks,
  defensive language, and unsupported claims that every concern is
  resolved.

## Final check

Check the letter against all original comments, author decisions, and
current deliverables. Ensure the opening summary agrees with the
detailed replies.

Build the letter, check LaTeX errors and reference warnings, and confirm
readability. Verify all location and citation numbers against the final
manuscript build. Ordinary `\ref` cannot resolve manuscript labels from
a standalone letter unless cross-document referencing is configured.

Remove placeholders and examples before submission. Report unresolved
gaps and verification results through the normal handoff, and present
the letter for author review.
