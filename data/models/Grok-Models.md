<-- Last updated 261114 -->
# xAI Grok Models

> **Last verified:** November 14, 2026
> **Primary source:** [xAI model documentation](https://docs.x.ai/developers/models)
> **Pricing caveat:** Third-party aggregators disagree on Grok 4.7 pricing. The figures below show both. Check [docs.x.ai](https://docs.x.ai/developers/models) before budgeting.

---

## At a glance

| Model | Status | Context | Released | Input $/1M | Output $/1M | Knowledge cutoff | Best for |
|---|---|---|---|---|---|---|---|
| **Grok 4.7** | Active | 500K | Sept 21, 2026 | $1.60 to $2.00 (see note) | $4.80 to $6.00 (see note) | ~May to June 2026 | Coding, agentic tasks, knowledge work |
| **Grok 4.6** | Active | 500K | (earlier 2026) | Not verified | Not verified | January 2026 | Earlier frontier coding model |
| **Grok 4.5** | Deprecated in Copilot Oct 19, 2026 (unverified) | 500K | (early 2026) | $2.00 | $6.00 | February 2026 | Coding, knowledge work, STEM |

---

## Recommended picks for your workflow

| Task | Recommended | Why |
|---|---|---|
| Multi-file coding and agentic tasks | Grok 4.7 | Newest in your list; xAI's stated focus is coding and agents |
| Cost-conscious coding comparisons | Grok 4.5 | Published pricing is clear; compare against 4.7 |
| Tasks with images | Grok 4.7 | Accepts text and image input |

---

## Model details

### Grok 4.7

| Attribute | Value |
|---|---|
| API ID | `grok-4.7` |
| Positioning | xAI's frontier model for coding, agentic tasks, and knowledge work |
| Context | 500,000 tokens |
| Output | Docs state "no text output limit." Third-party listings show about 450K per request. |
| Modalities | Text and image input; text output |
| Reasoning efforts | `low`, `medium`, `high` (default), `xhigh` |
| Features | Function calling, structured outputs, reasoning, prompt caching, web search, code execution |
| Architecture | Trained on a new, larger base model than Grok 4.6, with longer reinforcement learning for multi-hour tasks |
| Weights | Proprietary; hosted API only |

**Pricing (conflicting reports):**
- Public list price shown by several aggregators: **$2.00 input / $6.00 output** per 1M tokens
- One aggregator: **$1.60 input / $4.80 output**, with cached reads at $0.40 per 1M
- Pricing tiers exist above a **200K-token** threshold, so a request in the upper half of the window may cost roughly double. Confirm on xAI's pricing page.

**Vendor-reported benchmarks** (not independently verified): CursorBench 4.0 at 46.3%, DeepSWE v1.1 at 71.0% (high effort), Terminal-Bench 4.0 at 37.6%. On the same CursorBench and Terminal-Bench measures, Grok 4.6 scored 40.4% and 20.3%, so 4.7 is a substantial step up.

**Use cases:** Coding and refactoring, agentic workflows with tools, long document analysis up to 500K tokens, knowledge work.

**Strengths:**
- Newest and strongest Grok in your list
- Strong agentic and coding focus
- 500K context suits large files or many related files
- Reasoning effort is adjustable

**Weaknesses:**
- **Pricing tier above 200K tokens** adds cost for large prompts
- Pricing sources disagree, so confirm your rate before committing
- Benchmarks are vendor-reported. Test against your own C# workload.
- Weights are not released, so no self-hosting

---

### Grok 4.6

| Attribute | Value |
|---|---|
| API ID | `grok-4.6` |
| Context | 500,000 tokens |
| Knowledge cutoff | January 2026 |

**Description:** Predecessor to Grok 4.7. xAI's reported gains for 4.7 over 4.6 are substantial on coding and terminal benchmarks, so 4.7 is the better default.

**Use cases:** Coding and agent tasks where 4.7 is not available.

**Strengths:** Same 500K context; mature in production.

**Weaknesses:** Older cutoff; lower scores on xAI's coding benchmarks than 4.7. I could not verify current pricing for 4.6.

---

### Grok 4.5

| Attribute | Value |
|---|---|
| API ID | `grok-4.5` |
| Context | 500,000 tokens |
| Pricing | $2.00 input / $6.00 output per 1M tokens |
| Knowledge cutoff | February 2026 |

**Description (xAI):** A frontier model for coding, knowledge work, and STEM.

**Use cases:** Coding, research, STEM reasoning.

**Strengths:** Clear and stable pricing; same context as 4.7.

**Weaknesses:** Older cutoff and lower coding benchmarks than 4.7.

---

## Related xAI models (not on your list, for reference)

| Model | Notes |
|---|---|
| Grok Build 0.1 | Coding CLI model; 256K context; early access |
| Grok 4.3, Grok 4.20 | Earlier Grok releases |
| Grok Latest | Alias that always points to the newest Grok model |

---

## Notes and caveats

- **Use the exact API ID** (`grok-4.7`). Dashed or aliased forms may route differently.
- **Benchmarks are vendor-reported.** Treat them as a starting point and run your own tests.
- **Knowledge cutoffs** are earlier than some competing models, so give current framework and library details in prompts.
