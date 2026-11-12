# AI Model Reference

> **Last verified:** November 12, 2026
> **Scope:** The models on your list, grouped by provider, with specs, pricing, use cases, strengths, and weaknesses for C#/.NET engineering work.

## Files

| File | Covers |
|---|---|
| [OpenAI-Models.md](OpenAI-Models.md) | GPT-6 family, GPT-5.6 family, deprecated GPT-5.3-Codex and GPT-5.4 nano |
| [Anthropic-Models.md](Anthropic-Models.md) | Claude Fable 5.2, Opus 5.5, Sonnet 5.5, Haiku 5.5, and earlier versions |
| [Google-Models.md](Google-Models.md) | Gemini 3.8 Flash, Gemini 4 Argon |
| [Grok-Models.md](Grok-Models.md) | Grok 4.5, 4.6, 4.7 |
| [Microsoft-MAI-Models.md](Microsoft-MAI-Models.md) | MAI-Code-1.1-Flash |
| [Moonshot-Models.md](Moonshot-Models.md) | Kimi K3 |

---

## Cross-provider comparison

Prices are per 1M tokens, input / output. Figures change often. See the provider docs before budgeting.

| Model | Provider | Context | Input | Output | Tier |
|---|---|---|---|---|---|
| Claude Fable 5.2 | Anthropic | 1M | $8 | $40 | Top reasoning |
| GPT-6 Astra | OpenAI | 1.05M | $10 | $50 | Top reasoning |
| Claude Opus 5.5 | Anthropic | 1M | $4 | $20 | Flagship (recommended default) |
| GPT-5.6 Sol | OpenAI | 1.05M | $4 | $20 | Flagship |
| GPT-6.1 Sol | OpenAI | 1.05M | $2 | $10 | Balanced flagship |
| Claude Sonnet 5.5 | Anthropic | 1M | $2 | $10 | Speed and intelligence balance |
| Kimi K3 | Moonshot | 1M | $3 | $15 | Long-horizon agentic |
| Grok 4.7 | xAI | 500K | $2 (disputed) | $6 (disputed) | Coding and agents |
| Gemini 3.8 Flash | Google | 1.05M | $0.75 (intro) | $3.75 (intro) | Fast, large context |
| GPT-6.1 Terra | OpenAI | 1.05M | $1 | $5 | Fast and efficient |
| MAI-Code-1.1-Flash | Microsoft | 256K | $0.20 | $1.20 | Low-cost coding in Copilot |
| GPT-6 Luna | OpenAI | 1.05M | $0.10 | $0.50 | High-volume |
| Claude Haiku 5.5 | Anthropic | 1M | from $0.10 | from $0.50 | Fastest, high-volume |

---

## Recommended starting setup for your workflow

| Workflow | Model | Fallback |
|---|---|---|
| Large C# refactors, architecture | Claude Opus 5.5 | Claude Fable 5.2 or GPT-6.1 Sol |
| Routine refactors, code review | Claude Sonnet 5.5 | GPT-6.1 Terra |
| XML doc comments and manuals | Claude Sonnet 5.5 or GPT-6.1 Terra | Gemini 3.8 Flash |
| Bulk doc generation across a repo | Claude Haiku 5.5 or GPT-6 Luna | MAI-Code-1.1-Flash |
| Repo hygiene and build scripting | GPT-6.1 Terra | Grok 4.7 |
| Vibe-coding experiments | Gemini 3.8 Flash or MAI-Code-1.1-Flash | Kimi K3 |
| Analysis of a whole solution in one prompt | Gemini 3.8 Flash or Kimi K3 | Claude Opus 5.5 |

**Suggested evaluation approach:** Pick one real task from your repositories, such as converting a .NET Framework 4.8 class to .NET 10 or writing doc comments for a module. Run it against three or four candidates and compare results, cost, and time.

---

## Action items from the research

1. **Retire or migrate deprecated models before April 1, 2027:** GPT-5.3-Codex and GPT-5.4 nano (and GPT-5.1 if used).
2. **Check Fable access before production use.** Anthropic suspended Claude Fable 5 and Mythos 5 from June 12 to July 1, 2026, due to export controls.
3. **Plan for the Gemini 3.8 Flash price step-up** after December 31, 2026.
4. **Confirm Grok 4.7 pricing** on xAI's site. Sources disagree.
5. **Re-check GPT-5.6 pricing.** OpenAI cut prices on July 30, 2026, and some sources still show launch prices.

---

## Gaps and verification notes

These items could not be fully verified from the sources available on November 12, 2026. Check the provider pages before relying on them.

| Item | Gap |
|---|---|
| Claude Opus 4.8 (fast mode) | Price and terms not confirmed |
| Gemini 4 Argon | Per-token pricing not confirmed |
| Grok 4.6 | Current pricing not confirmed |
| GPT-6 Sol | Shows as an alias for GPT-6.1 Sol. Confirm pricing on the pricing page. |
| GPT-5.3-Codex | Pricing not confirmed. Deprecated. |
| Strengths and weaknesses | Synthesized from vendor descriptions, model cards, and third-party reporting. Treat as a starting point and validate with your own tests. |
| Benchmarks | Mostly vendor-reported. Not independently reproduced. |

**Note on your list:** Your list includes "Claude Fable 5" and "Claude Fable 5.1", which are covered. Anthropic's current catalog also includes Claude Fable 5.2, which is the recommended Fable model, and the restricted Mythos tier.
