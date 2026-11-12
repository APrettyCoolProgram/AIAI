# Model Documentation

This document contains the prompts/responses for:

* `Model-Description.md`
* `Model-Description-Detailed.md`
* 'Model-Suggestion.md
* 'Model-Suggestion-Detailed.md

## Model files

### Prompt

```text
I'm a software engineer that would like to start incorporating AI into my 
workflow.

My current workflow includes:

- Writing software in C# using both .NET 10 and the .NET Framework 4.8
- Continuously refactoring to keep technical debt at a minimum
- Creating technical documentation/manuals for the software I write
- Occasionally experimenting with vibe-coding weird ideas
- Ensuring that my code repositories are clean and well organized.

This is the current list of models that I have available:

OpenAI/GPT (https://developers.openai.com/api/docs/models)
- GPT‑5.3‑Codex
- GPT‑5.4 nano 1
- GPT‑5.6 Luna
- GPT‑5.6 Sol
- GPT‑5.6 Terra
- GPT‑6 Astra
- GPT‑6 Luna
- GPT‑6 Sol
- GPT‑6.1 Sol
- GPT‑6.1 Terra

Anthropic/Claude (https://platform.claude.com/docs/en/data/models/overview)
- Claude Fable 5
- Claude Fable 5.1
- Claude Haiku 4.5
- Claude Haiku 5.5
- Claude Opus 4.8
- Claude Opus 4.8 (fast mode)
- Claude Opus 5
- Claude Opus 5.5
- Claude Sonnet 4.6
- Claude Sonnet 5
- Claude Sonnet 5.5

Google/Gemini (https://docs.cloud.google.com/gemini-enterprise-agent-platform/data/models/google-models)
- Gemini 3.8 Flash
- Gemini 4 Argon

Grok (https://docs.x.ai/developers/models)
- Grok 4.5
- Grok 4.6
- Grok 4.7

Microsoft/MAI (https://microsoft.ai/data/models/mai-code-1-flash/))
- MAI‑Code‑1.1‑Flash

Moonshot/Kimi
- Kimi K3 (https://github.com/MoonshotAI/Kimi-K3)

We will use this information to create a number of documents.

Create documentation for each group (e.g. `OpenAI-Models.md`, `Anthropic-Models.md`, etc.) that has detailed informtion for each model in that group (e.g., "Claude Fable 5", "Claude Haiku 4.5", etc.).

Include the use-cases for each model, the strengths and weaknesses, and any other relevant information.

The documentation should be formatted nicely (use tables, etc.), and be easy to read.

Write the documentation to `Projects/data/models/*
```

### Response

```text
 I'll start by pulling the official model pages you linked so the documentation reflects current specs rather than my memory.

The OpenAI page lists a few models that differ from your list (for example, it shows GPT-6.1 Terra and GPT-6 Astra, but not GPT-5.6 or GPT-6 Sol). I'll note that in the docs. Next, the Anthropic page.

Anthropic's page has full specs. Next, Google's Gemini models.

The Gemini overview was cut off before the model details, so I'll fetch the specific Gemini 4 Argon and 3.8 Flash pages, plus the remaining provider pages.

The Google pages are very large, so I'll switch to targeted searches for the remaining models rather than fetching full pages.

Grok 4.7 pricing varies by source ($1.60/$4.80 vs $2/$6), so I'll flag that in the doc. Next, Kimi K3 and Microsoft's MAI model.

Kimi K3 is well documented. Next, Microsoft's MAI model.

Next, the OpenAI models that weren't on the models page (GPT-5.x and GPT-6 Sol).

Next, Gemini 3.8 Flash and the GPT-5.3-Codex and GPT-6 Sol models.

I have enough on Gemini. One more search for GPT-5.3-Codex and GPT-6 Sol, the two OpenAI entries I still lack details for.

I have enough verified detail to write the docs. First I'll create the output folder, then save the durable facts about your workflow to this project's memory.

Now the documentation files, one per provider group, starting with OpenAI.

Next, the Anthropic document.

Next, the Google Gemini document.

I left a typo in the Gemini 4 Argon context cell. Fixing it now.

I wrote a sloppy phrase in the Grok 4.7 benchmark line. Correcting it.

Next, the Kimi document.

One claim in the Kimi weaknesses is wrong: Kimi's $15 output price is above Sonnet 5.5's $10, not equal to it. Fixing that.

I'll also tighten one awkward phrase in the Kimi recommendations table.

Last, a README that ties the six documents together with a cross-provider comparison and a list of what I couldn't verify.

I wrote seven documents to `Projects/data/models/`: one README and one file per provider group. Each has spec tables, pricing, recommended uses for C#/.NET work, and strengths and weaknesses for every model.

**What's in the folder**
- `README.md`: a cross-provider comparison table, recommended picks for your workflow, and action items.
- `OpenAI-Models.md`, `Anthropic-Models.md`, `Google-Models.md`, `Grok-Models.md`, `Microsoft-MAI-Models.md`, `Moonshot-Models.md`.

**Things you should act on**
- **Deprecated models:** GPT-5.3-Codex and GPT-5.4 nano shut down on April 1, 2027. OpenAI points to GPT-6 Sol and GPT-6 Luna as replacements.
- **Claude Fable access:** Anthropic suspended Fable 5 and Mythos 5 from June 12 to July 1, 2026, due to U.S. export controls. Check the status before relying on Fable in production.
- **Pricing changes:** OpenAI cut GPT-5.6 prices on July 30, so some sources still show launch prices. Gemini 3.8 Flash is at an introductory rate through December 31, 2026. Grok 4.7's price varies by source ($2/$6 vs $1.60/$4.80).
- **Your list vs. current catalogs:** Anthropic's catalog now includes Claude Fable 5.2 and the restricted Mythos tier. OpenAI's page doesn't list GPT-5.6 or GPT-6 Sol under those names; GPT-6 Sol redirects to GPT-6.1 Sol.

**Gaps and caveats**
- I couldn't confirm pricing for Claude Opus 4.8 fast mode, Gemini 4 Argon, Grok 4.6, or GPT-5.3-Codex. Each file says so.
- Benchmark numbers are vendor-reported. The strengths and weaknesses are my synthesis from vendor descriptions, model cards, and third-party reporting, so validate them on your own code before committing.
- The Kimi and MAI documents include a few details from third-party sources (Kimi's license, MAI's post-training emphasis on .NET). Check those against the primary pages.

I also saved your workflow and the project's scope to memory for this project, so future model or tooling questions can build on it.
```

## project/README.md (Part 1)

### Prompt

```text
The project/README.md file is going to be the main document for this project.

Add a very brief summary to project/README.mdthat uses a table to give a very high-level description of each model in project/data/models/*
```

### Result

```text
The `project/` folder doesn't exist. The main project README is `Projects/data/models/README.md`, so I'll add the summary there.

I added a "Model summary" table to `Projects/data/models/README.md`. There's no `project/` folder, so I assumed you meant this README, which is the project's main document.

The table has one row per model (29 in total) across the six providers, each with a one-line description. It sits above the cross-provider comparison.
```

## project/README.md (Part 2)

### Prompt

```text
Make the following modifications to `project/README.md`:

* Remove the "Files", "Action items" and "Gaps and verification notes" sections
* Combine the "Model summary" and "Cross-provider comparison" tables, when applicable
* The "Model" in the "Model summary" table should link to the relevant documentation in `project/data/models/` (e.g., "GPT-6 Astra" should link to `project/data/models/OpenAI-Models.md).
```

### Result

```text
I've updated the README as requested:

- **Removed** the "Files," "Action items," and "Gaps and verification notes" sections.
- **Merged** the "Model summary" and "Cross-provider comparison" into one table. Each row has the model, provider, context window, input and output prices, and a one-line summary. Models without verified prices show "—".
- **Linked** each model name to its provider file in `data/models/`, for example `[GPT-6 Astra](data/models/OpenAI-Models.md)`.

The "Recommended starting setup" and "Suggested evaluation approach" sections are unchanged.

Removing the gaps section also removed the notes on unverified figures. The table still marks those with "—" or "sources differ," and the provider files explain the gaps in more detail..
```

## project/README.md (Part 3)

### Prompt

```text
Please design a workflow that ensures that I am being as efficient as possible, and utilizing the right model for each part of the workflow.

For example:

* Should I be using one model to plan a project/feature/etc., another model to implement that plan/create the source code, and yet another model to write documentation?

I'm sure there are other parts of the workflow I'll need to document, such as:

* Source code comments/documentation (including XML documentation)
* Creating Unit Tests
* etc.

The document should be formatted nicely, and be easy to follow/read.

Use compontents like tables, Mermaid charts, etc. when applicable.

Put all of this into a document named `project/Workflow.md`
```

### Response

```text
I'll put the workflow in `Projects/data/models/Workflow.md`, next to the README, since that's where the project's main documents live.

I wrote the workflow to `Projects/data/models/Workflow.md`, next to the README. I put it there rather than in a separate `project/` folder because that's where the other project documents live.

**The core answer to your example:** Yes, use separate models for planning, implementation, and documentation. The default path is:

- **Plan:** Claude Opus 5.5, reviewed by GPT-6.1 Sol.
- **Implement:** Claude Sonnet 5.5, with Opus 5.5 for multi-file changes.
- **Unit tests:** GPT-6.1 Terra, so the tests aren't written by the same model that wrote the code.
- **XML docs:** Haiku 5.5 drafts, Sonnet 5.5 reviews.
- **Manuals:** Opus 5.5 or GPT-6.1 Terra.
- **Code review:** A model that didn't write the change, such as GPT-6.1 Sol.

**What the document covers**

- **Principles:** The compiler and tests decide, not the model. Start cheap and escalate after real failures. A different model reviews the work.
- **A Mermaid flowchart** of the default feature path, and a Mermaid diagram of the escalation tiers.
- **Phase-by-phase sections** for planning, implementation, refactoring (mechanical vs. design-level), unit tests, XML docs and comments, manuals, code review, repo hygiene, .NET Framework 4.8 to .NET 10 migration, and experiments.
- **A model assignment matrix** with a primary model, a cheaper option, an escalation target, and a reviewer for each task.
- **Efficiency techniques** (spec files as handoffs, a new session per task, prompt caching, batch processing for bulk docs) and **verification gates** (build with warnings as errors, `CS1591`, mutation testing, formatting checks).
- **A spec file template** and a quick-start checklist.

**Things to check**

- The model choices are reasoned from the model docs, not tested on your code. The weekly review in Section 10 is there so you can adjust them based on your own results.
- Tool commands like `dotnet build -warnaserror` and Stryker.NET are standard, but confirm they fit your CI setup.
- The workflow avoids the deprecated GPT-5.3-Codex and GPT-5.4 nano, and treats Fable 5.2 as the only Fable model for new work.
```























