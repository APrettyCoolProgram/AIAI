<-- Last updated 261112 -->

# AIAI Monthly Update

You are maintaining two documents in the AIAI folder:
- models.md: a reference of the AI models available in GitHub Copilot Pro, with use cases.
- workflow.md: the AI-assisted .NET development workflow, which names specific models in its phases, diagrams, matrix, escalation ladder, and cost tiers.

Read models.md, workflow.md, and README.md before changing anything. If I paste a model list below this prompt, treat it as the primary source for what is currently available.

Step 1: Verify current model information
Check the current GitHub Copilot Pro model list, including availability, deprecation and shutdown dates, context window, and pricing. Use official sources first: GitHub Copilot documentation and changelog, and provider pricing pages. Do not guess. If a value cannot be confirmed or sources conflict, keep the existing value, mark it "unverified" in your report, and continue. Record the date you checked.

Step 2: Update models.md
- Add new models to the table under the correct provider, using the same column format and a one-line summary in the same style.
- For deprecated models, add the shutdown date to the summary. Remove models that have already shut down.
- Update context, prices, and summaries that have changed. Keep prices as $ per 1M tokens. Use "—" for unknown values.
- In the use-case table, change a recommendation only if its model was removed, deprecated, or clearly superseded. Otherwise leave it alone.
- Set the "Last updated" line to today's date.
- Do not create the Models/*.md files that the links point to. Report broken links instead.

Step 3: Propagate changes to workflow.md
Search workflow.md for every model that was added, removed, deprecated, or renamed. Check the Mermaid diagrams, phase tables, the assignment matrix (section 4), the deprecation notes, the escalation ladder (section 5), the cost tiers (section 8), and the quick-start checklist.
- If a model was removed or deprecated, replace it with the fallback listed for that use case in models.md, and update the matching diagram node and cost tier.
- If a new model might suit a use case better, do not swap it in. List it as a suggestion in your report. These are judgment calls for me.
- Do not change the principles or the overall structure.
- Keep Mermaid syntax valid and keep the existing table formats.
- Set the "Last updated" line to today's date.

Step 4: Check consistency
- Every model named in workflow.md is either in models.md or listed under "Models not used in this workflow".
- Every fallback named in models.md exists in its table.
- The tiers in section 8 match the models in models.md.
- The escalation ladder in section 5 uses current models.

Step 5: Report
Summarize the changes by file: added, removed, changed (old value to new value), unverified values, suggestions I did not apply, and broken links. Keep the report short.

Constraints:
- Edit in place. Do not rewrite whole files.
- Do not edit README.md, do not create new files, and do not commit to git.
