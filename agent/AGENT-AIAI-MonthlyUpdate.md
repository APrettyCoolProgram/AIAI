<-- Last updated 261112 -->

# AIAI Monthly Update

You are maintaining these files in the AIAI folder:

- `README.md`: a reference of the AI models available in GitHub Copilot Pro, with use cases.
- `model/`: a datasheet for each model, plus the cross-provider table in `model/README.md`.
- `workflow/workflow.md`: the AI-assisted .NET development workflow, which names specific models in its phases, diagrams, matrix, escalation ladder, and cost tiers.

Read `README.md`, `workflow/workflow.md`, and all files in `model/` before changing anything. If I paste a model list below this prompt, treat it as the primary source for what is currently available.

---

## Step 1: Verify current model information

Check the current GitHub Copilot Pro model list, including availability, deprecation and shutdown dates, context window, and pricing.

Use official sources first:

- GitHub's supported-models documentation at docs.github.com (Copilot section), and the Copilot changelog at github.blog/changelog.
- Each provider's pricing page, as linked from its datasheet in `model/`.

Rules:

- Prices are provider API prices per 1M tokens, not Copilot premium-request multipliers. Do not convert between them.
- A model is in scope only if GitHub Copilot Pro offers it.
- Do not guess. If a value cannot be confirmed or sources conflict, keep the existing value, mark it "(unverified)" in the value cell the same way "(intro)" and "(sources differ)" are marked, and continue.
- Record the date you checked in the same "Month D, YYYY" format as `README.md`.
- Only bump a "Last updated" line if this run verified or changed at least one value.
- If no source could be reached, change nothing and say so in the report.

---

## Step 2: Update datasheets in `model/`

- Before editing anything, record the list of models added, removed, deprecated, or renamed. Steps 3 and 4 work from that list, because removed models no longer appear in `README.md`.
- For each model in the Step 1 results that has a datasheet, update its API ID, context window, input and output prices, status, shutdown date, and Copilot Pro availability where they changed. Keep the file's existing structure.
- Add an entry for each new model to the existing datasheet file for its provider. If no file exists for the provider, report it instead of creating one.
- For a model that has shut down, remove its entry only if the file has no legacy section for it. Otherwise report it.
- Apply the same "(unverified)" and "—" rules as Step 1 and Step 4.
- Set the "Last verified" line in each changed file to today's date, only if this run changed that file.
- Update the cross-provider table in `model/README.md` so it matches the datasheets, and set its "Last verified" line the same way. The datasheets are the source of truth for values. If `README.md` or the README table disagrees with a datasheet, change them to match.

---

## Step 3: Propagate changes to `workflow/workflow.md`

Search `workflow/workflow.md` for every model that was added, removed, deprecated, or renamed. Search by family and version, not only by full name, because `workflow/workflow.md` uses short forms such as "Opus 5.5", "Sonnet 5.5", "Fable 5.2", "Haiku 5.5", and "GPT-6.1 Sol", including in the Mermaid diagrams.

Check the Mermaid diagrams, phase tables, the assignment matrix (section 4), the deprecation notes, the escalation ladder (section 5), the cost tiers (section 8), and the quick-start checklist.

- If a model was removed or has shut down, replace it with another model from the same row of the matrix in section 4, preferring the Primary or Secondary option, and update the matching diagram node and cost tier. If that replacement is also removed or has shut down, stop for that use case and flag it in the report. Do not chain to a further replacement.
- A deprecated model that has not shut down stays in its phases and matrix. Flag it in the report, and replace it only after it shuts down.
- If a new model might suit a use case better, do not swap it in. List it as a suggestion in your report. These are judgment calls for me.
- Do not change the principles or the overall structure.
- If a row of the matrix in section 4 is added, removed, or changed, note it in the report so the Model assignment matrix in `README.md` can be updated to match.
- Keep the existing table formats. After editing, re-read each Mermaid diagram you changed and check the syntax: matching brackets, quoted labels, and valid arrows.
- Set the "Last updated" line to today's date, only if this run changed the file.

---

## Step 4: Update `README.md`

- Add new models to the table under the correct provider, using the same column format and a one-line summary in the same style. Add a model only if GitHub Copilot Pro offers it.
- For deprecated models, add the shutdown date to the summary. Remove models that have already shut down, and remove models that Copilot Pro no longer offers even if the provider still serves them.
- Update context, prices, and summaries that have changed. Keep prices as $ per 1M tokens. Use "—" only for values that do not exist or were never found. Mark unconfirmed values "(unverified)" as described in Step 1.
- Recalculate the Cost ratings when any price changes. Rate each model by input plus output price, from "Lowest" for the cheapest model to "Highest" for the most expensive, scaled on a log scale in between. Leave a model unrated ("—") if it has no usable price.
- Copy the matrix from section 4 of `workflow/workflow.md` into the Model assignment matrix section of `README.md`, exactly, with the same column names and alignment. Replace the table only when the matrix changed. Otherwise leave it alone.
- Set the "Last updated" line to today's date, only if this run changed the file.
- Do not create files that links point to. Report any link in `README.md` whose target file does not exist.

---

## Step 5: Check consistency

- Every model named in `workflow/workflow.md` is either in `README.md` or listed under the "Models not used in this workflow" list in `workflow/workflow.md` (section 4).
- Every model named in the Model assignment matrix in `README.md` exists in the Models table.
- The Model assignment matrix in `README.md` matches the matrix in section 4 of `workflow/workflow.md`, row for row, with the same column names and alignment.
- The tiers in section 8 match `README.md`: every model named in a tier has a row in `README.md`, and every tier model appears in the assignment matrix (section 4) or the escalation ladder (section 5).
- The escalation ladder in section 5 uses current models.
- Each datasheet in `model/` matches `README.md` for context and prices.
- The cross-provider table in `model/README.md` matches `README.md`.

---

## Step 6: Report

Summarize the changes by file: added, removed, changed (old value to new value), unverified values, suggestions I did not apply, and broken links. Keep the report short. Give it in your chat reply, not in a file.

---

## Constraints

- Edit in place. Do not rewrite whole files.
- If this run changed any file, set the comment on line 1 to today's date in YYMMDD format, for example `<-- Last updated 261114 -->`.
- Do not edit `agent/README.md`. `README.md` (the model reference) and `model/README.md` are in scope.
- Do not create new files, and do not commit to git.
