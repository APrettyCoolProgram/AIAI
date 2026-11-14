<div align="center">

  <img src="./.github/logo/AIAI-448x672.png" alt="AIAI">

   <br>
   <br>

  ![RELEASE](https://img.shields.io/badge/November_2026-teal)&nbsp;

## Use cases

| Use case | High | Medium | Low |
|---|---|---|---|
| 3.1 Planning and design | Claude Fable 5.2 | Claude Opus 5.5 | GPT-6.1 Sol |
| 3.2 Implementation | Claude Opus 5.5 | — | Claude Sonnet 5.5 or GPT-6.1 Sol |
| 3.3 Refactoring | Claude Opus 5.5 | — | Claude Haiku 5.5 or GPT-6 Luna |
| 3.4 Unit tests | Claude Sonnet 5.5 | — | GPT-6.1 Terra |
| 3.5 XML documentation and code comments | Claude Sonnet 5.5 | — | Claude Haiku 5.5 |
| 3.6 Technical documentation and user manuals | Claude Opus 5.5 | — | GPT-6.1 Terra |
| 3.7 Code review | GPT-6.1 Sol | — | Gemini 3.8 Flash |
| 3.8 Repository hygiene | GPT-6.1 Terra | — | Claude Haiku 5.5 |
| 3.9 Migrating .NET Framework 4.8 to .NET 10 | Claude Fable 5.2 | Claude Opus 5.5, GPT-6.1 Sol, Claude Sonnet 5.5, MAI-Code-1.1-Flash | Claude Haiku 5.5 |
| 3.10 Vibe-coding experiments | Kimi K3 | Gemini 3.8 Flash | MAI-Code-1.1-Flash |

Rows match the phases in `workflow.md`. High, Medium, and Low list the most expensive, middle, and least expensive models in each row, by Cost rating. Ties are joined with "or", and several middle models with commas. "—" means no model fills that position.

---

## Models

| Model | Provider | Context | Input $/1M | Output $/1M | Cost | Summary |
|-------|----------|:-------:|:----------:|:-----------:|:----:|---------|
| [GPT-6 Astra](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $10 | $50 | Highest | Most capable model for hard reasoning and coding |
| [GPT-6.1 Sol](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $2 | $10 | 7 | Near-Astra capability at a lower price |
| [GPT-6.1 Terra](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $1 | $5 | 6 | Fast, efficient model for writing and computer use |
| [GPT-6 Luna](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $0.10 | $0.50 | Lowest | Cheapest GPT-6 model, for high-volume focused tasks |
| [GPT-6 Sol](data/models/OpenAI-Models.md) | OpenAI | 1.05M | — | — | — | Alias that routes to GPT-6.1 Sol |
| [GPT-5.6 Sol](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $4 | $20 | 8 | Earlier flagship for agentic coding and long tasks |
| [GPT-5.6 Terra](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $2 | $12 | 7 | Earlier balanced tier for everyday engineering; deprecated in Copilot Nov 16, 2026 |
| [GPT-5.6 Luna](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $0.20 | $1.20 | 3 | Earlier low-cost tier for automation |
| [GPT-5.3-Codex](data/models/OpenAI-Models.md) | OpenAI | 400K | — | — | — | Coding agent; deprecated, shuts down April 1, 2027 |
| [GPT-5.4 nano](data/models/OpenAI-Models.md) | OpenAI | — | ~$0.20 | ~$1.25 | 3 | Small model; deprecated, shuts down April 1, 2027 |
| [Claude Fable 5.2](data/models/Anthropic-Models.md) | Anthropic | 1M | $8 | $40 | 9 | Top reasoning model for long agentic work |
| [Claude Opus 5.5](data/models/Anthropic-Models.md) | Anthropic | 1M | $4 | $20 | 8 | Recommended default for long coding and knowledge work |
| [Claude Sonnet 5.5](data/models/Anthropic-Models.md) | Anthropic | 1M | $2 | $10 | 7 | Best balance of speed and intelligence |
| [Claude Haiku 5.5](data/models/Anthropic-Models.md) | Anthropic | 1M | from $0.10 | from $0.50 | Lowest | Fastest and cheapest; classification and routing |
| [Claude Fable 5.1](data/models/Anthropic-Models.md) | Anthropic | 1M | $10 | $50 | Highest | Earlier Fable generation |
| [Claude Fable 5](data/models/Anthropic-Models.md) | Anthropic | 1M | $10 | $50 | Highest | Earlier Fable; access was suspended June to July 2026 |
| [Claude Opus 5](data/models/Anthropic-Models.md) | Anthropic | 1M | $5 | $25 | 8 | Earlier Opus generation; deprecated in Copilot Nov 16, 2026 |
| [Claude Opus 4.8](data/models/Anthropic-Models.md) | Anthropic | 1M | $5 | $25 | 8 | Stable earlier Opus; fast-mode variant listed; deprecated in Copilot Nov 16, 2026 (annual individual plans excepted) |
| [Claude Sonnet 5](data/models/Anthropic-Models.md) | Anthropic | 1M | $2 | $10 | 7 | Earlier Sonnet at the same price as 5.5 |
| [Claude Sonnet 4.6](data/models/Anthropic-Models.md) | Anthropic | 1M | $3 | $15 | 7 | Older, pricier Sonnet; retired from Copilot Sep 1, 2026 (unverified) |
| [Claude Haiku 4.5](data/models/Anthropic-Models.md) | Anthropic | 200K | $1 | $5 | 6 | Older small model with 200K context |
| [Gemini 4 Argon](data/models/Google-Models.md) | Google | 1.05M (input + output) | — | — | — | Google's frontier model for deep, multi-domain work |
| [Gemini 3.8 Flash](data/models/Google-Models.md) | Google | 1.05M | $0.75 (intro) | $3.75 (intro) | 5 | Fast, large-context model with multimodal input |
| [Grok 4.7](data/models/Grok-Models.md) | xAI | 500K | $2 (sources differ) | $6 (sources differ) | 6 | Newest Grok; coding and agentic focus |
| [Grok 4.6](data/models/Grok-Models.md) | xAI | 500K | — | — | — | Earlier Grok coding model |
| [Grok 4.5](data/models/Grok-Models.md) | xAI | 500K | $2 | $6 | 6 | Earlier Grok for coding and STEM; deprecated in Copilot Oct 19, 2026 (unverified) |
| [MAI-Code-1.1-Flash](data/models/Microsoft-MAI-Models.md) | Microsoft | 256K | $0.20 | $1.20 | 3 | Low-cost coding model in GitHub Copilot |
| [Kimi K3](data/models/Moonshot-Models.md) | Moonshot | 1M | $3 | $15 | 7 | Open-weight, 1M-context model for long agentic tasks |

<br>

***

> <sub>**Last updated:** November 14, 2026</sub>
