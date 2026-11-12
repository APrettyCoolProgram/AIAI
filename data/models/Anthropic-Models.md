# Anthropic Claude Models

> **Last verified:** November 12, 2026
> **Primary source:** [Claude Platform models overview](https://platform.claude.com/docs/en/data/models/overview)
> **Model IDs** shown are the API strings. Use them exactly as written.

---

## At a glance

| Model | Line | API ID | Context | Max output | Input $/1M | Output $/1M | Speed | Best for |
|---|---|---|---|---|---|---|---|---|
| **Claude Fable 5.2** | Fable | `claude-fable-5-2` | 1M | 128K | $8 | $40 | Moderate | Demanding reasoning, long-horizon agentic work |
| **Claude Opus 5.5** | Opus | `claude-opus-5-5` | 1M | 128K | $4 | $20 | Moderate | **Default recommendation**; long agentic coding and knowledge work |
| **Claude Sonnet 5.5** | Sonnet | `claude-sonnet-5-5` | 1M | 128K | $2 | $10 | Fast | Best speed/intelligence balance |
| **Claude Haiku 5.5** | Haiku | `claude-haiku-5-5` | 1M | 128K | from $0.10 | from $0.50 | Fastest | Classification, extraction, routing, high volume |
| Claude Fable 5.1 | Fable | `claude-fable-5-1` | 1M | 128K | $10 | $50 | Moderate | Previous Fable generation |
| Claude Fable 5 | Fable | `claude-fable-5` | 1M | 128K | $10 | $50 | Moderate | See availability note below |
| Claude Opus 5 | Opus | `claude-opus-5` | 1M | 128K | $5 | $25 | Moderate | Previous Opus generation |
| Claude Opus 4.8 | Opus | `claude-opus-4-8` | 1M | 128K | $5 | $25 | Moderate | Stable, widely used |
| Claude Sonnet 5 | Sonnet | `claude-sonnet-5` | 1M | 128K | $2 | $10 | Fast | Previous Sonnet generation |
| Claude Sonnet 4.6 | Sonnet | `claude-sonnet-4-6` | 1M | 128K | $3 | $15 | Fast | Older, pricier than Sonnet 5 |
| Claude Haiku 4.5 | Haiku | `claude-haiku-4-5` | 200K | 64K | $1 | $5 | Fast | Smaller context; legacy small model |

---

## Recommended picks for your workflow

| Task | Recommended | Why |
|---|---|---|
| Large C# refactors and architectural changes | Opus 5.5 (escalate to Fable 5.2) | Long-running agentic coding; Fable for the hardest cases |
| Routine refactors and code review | Sonnet 5.5 | Fast and capable at lower cost than Opus |
| Generating XML doc comments and manuals | Sonnet 5.5 | Strong writing at a good price |
| Bulk doc comments or classifying a whole repo | Haiku 5.5 | Lowest cost for high-volume work |
| Vibe-coding experiments | Sonnet 5.5 | Quick iterations without high cost |
| Hard debugging across a whole solution | Fable 5.2 | Strongest reasoning in the lineup |

**Quick rule:** Start with **Opus 5.5** for most work, drop to **Sonnet 5.5** for speed and cost, and move to **Fable 5.2** when your evals on Opus 5.5 at higher effort still fall short.

---

## Shared capabilities (all current models)

- Text and image input, text output, multilingual, vision, tool use
- **Adaptive thinking.** Fable 5.2 and Opus 5.5 always think; Sonnet 5.5 and Haiku 5.5 adapt.
- **Effort control.** Default effort: Fable 5.2 `high`, Opus 5.5 `medium`, Sonnet 5.5 `high`, Haiku 5.5 `medium`.
- **Reliable knowledge cutoff:** June 2026 for all current models.

---

## Model details

### Claude Fable 5.2

| Attribute | Value |
|---|---|
| API ID | `claude-fable-5-2` |
| Pricing | $8 input / $40 output per 1M tokens |
| Context / output | 1M / 128K |
| Thinking | Adaptive, always on; default effort `high` |
| Latency | Moderate |
| Safety | Includes additional safeguards for biology and cybersecurity (see Mythos note) |

**Description (Anthropic):** For demanding reasoning and long-horizon agentic work, or when evals on Opus 5.5 at higher effort still fall short.

**Use cases:** Hardest debugging, deep architectural analysis, multi-day agentic refactors, complex specification work.

**Strengths:**
- Top reasoning in the current public lineup
- Built for long agentic runs
- Full 1M context

**Weaknesses:**
- Most expensive current model per token among the general line
- Moderate latency; overkill for routine edits
- Additional safety measures may occasionally affect security-related coding tasks

---

### Claude Opus 5.5

| Attribute | Value |
|---|---|
| API ID | `claude-opus-5-5` |
| Pricing | $4 input / $20 output per 1M tokens |
| Context / output | 1M / 128K |
| Thinking | Adaptive, always on; default effort `medium` |
| Latency | Moderate |

**Description (Anthropic):** For long-running agentic coding and knowledge work. Anthropic's recommended starting point for most workloads.

**Use cases:** Large refactors, codebase-wide documentation, technical manuals, multi-step agent workflows.

**Strengths:**
- Excellent for sustained agentic coding
- Strong at long documents and detailed technical writing
- Better value than Opus 5 and Opus 4.8 at a lower price

**Weaknesses:**
- Moderate latency compared with Sonnet and Haiku
- Costs more per token than Sonnet 5.5 for routine work

---

### Claude Sonnet 5.5

| Attribute | Value |
|---|---|
| API ID | `claude-sonnet-5-5` |
| Pricing | $2 input / $10 output per 1M tokens |
| Context / output | 1M / 128K |
| Thinking | Adaptive; default effort `high` |
| Latency | Fast |

**Description (Anthropic):** The best combination of speed and intelligence.

**Use cases:** Daily coding, code review, unit test generation, documentation, refactoring of individual classes or modules.

**Strengths:**
- Fast and capable at low cost
- Strong all-round choice for C# work
- Good for interactive, back-and-forth sessions

**Weaknesses:**
- Less depth than Opus or Fable on very large, cross-cutting changes
- May need explicit prompting to reason through complex design tradeoffs

---

### Claude Haiku 5.5

| Attribute | Value |
|---|---|
| API ID | `claude-haiku-5-5` |
| Pricing | From $0.10 input / $0.50 output per 1M tokens |
| Context / output | 1M / 128K |
| Thinking | Adaptive; default effort `medium` |
| Latency | Fastest |

**Description (Anthropic):** For high-volume, latency-sensitive tasks such as classification, extraction, and routing.

**Use cases:** Tagging commits, classifying issues, extracting API signatures for docs, routing tasks to larger models.

**Strengths:**
- Very low cost and very fast
- Large 1M context for its tier
- Good for pipelines that call the model thousands of times

**Weaknesses:**
- Not suited to subtle refactoring or design decisions
- Quality drops on complex multi-file reasoning

---

### Claude Fable 5.1 and Fable 5

| Attribute | Value |
|---|---|
| API IDs | `claude-fable-5-1`, `claude-fable-5` |
| Pricing | $10 input / $50 output per 1M tokens |
| Context / output | 1M / 128K |

**Description:** Earlier generations in the Fable line. Fable 5.2 is cheaper and newer; prefer it unless you need a pinned earlier version.

**Availability note:** Anthropic suspended access to Claude Fable 5 and Claude Mythos 5 on June 12, 2026 to comply with U.S. Department of Commerce export controls. The controls were lifted June 30, and access was restored July 1, 2026. Check Anthropic's [statement](https://www.anthropic.com/news/fable-mythos-access) for the latest status before depending on any Fable model in production.

---

### Claude Opus 5, Opus 4.8, and Opus 4.8 fast mode

| Attribute | Value |
|---|---|
| API IDs | `claude-opus-5`, `claude-opus-4-8` |
| Pricing | $5 input / $25 output per 1M tokens |
| Context / output | 1M / 128K |

**Description:** Earlier Opus generations. Opus 5.5 is the recommended successor.

**Opus 4.8 (fast mode):** Your list includes a fast-mode variant. Fast mode is a speed-optimized option for Opus 4.8. I could not confirm its current price from the models page, so check the [pricing page](https://platform.claude.com/docs/en/about-claude/pricing) before use.

---

### Claude Sonnet 5 and Sonnet 4.6

| Attribute | Value |
|---|---|
| API IDs | `claude-sonnet-5`, `claude-sonnet-4-6` |
| Pricing | Sonnet 5: $2 / $10. Sonnet 4.6: $3 / $15 per 1M tokens |
| Context / output | 1M / 128K |

**Description:** Sonnet 5 matches Sonnet 5.5's price and is an earlier generation. Sonnet 4.6 costs more than Sonnet 5 and is older. Move to Sonnet 5.5 where possible.

---

### Claude Haiku 4.5

| Attribute | Value |
|---|---|
| API ID | `claude-haiku-4-5` |
| Pricing | $1 input / $5 output per 1M tokens |
| Context / output | 200K / 64K |

**Description:** Previous-generation small model. Smaller context than the 5.x line. Use Haiku 5.5 for new work.

---

## Specialized and restricted models (not on your list)

| Model | Notes |
|---|---|
| **Claude Mythos 5.2** / **Mythos 5.1** / **Mythos 5** | Anthropic's top tier above Opus. Mythos Preview is limited to a small number of trusted organizations under Project Glasswing. See [anthropic.com/glasswing](https://www.anthropic.com/glasswing). |
| **Claude Opus 4.5**, **Opus 4.6**, **Opus 4.7** | Earlier Opus versions still listed. Prefer the 5.x line. |
| **Claude Sonnet 4.5**, **Sonnet 4** | Older versions with 200K context. |

---

## Notes and caveats

- **Use the API ID exactly** (for example, `claude-opus-5-5`). Anthropic also documents aliases and snapshots in [Model IDs and versioning](https://platform.claude.com/docs/en/about-claude/data/models/model-ids-and-versions).
- **Check retirements.** Deprecated models are listed in [Model deprecations](https://platform.claude.com/docs/en/about-claude/model-deprecations).
- **Cost tip:** Batch processing and prompt caching reduce cost substantially for repetitive work such as doc generation. See [Pricing](https://platform.claude.com/docs/en/about-claude/pricing).
- **Long-context prompts:** A 1M context window does not mean every part of a large codebase is equally attended to. Give the model relevant files and clear instructions rather than dumping an entire solution.
