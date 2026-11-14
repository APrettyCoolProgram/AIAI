<-- Last updated 261114 -->
<div align="center">

  <img src="./.github/logo/AIAI-448x672.png" alt="AIAI">

   <br>
   <br>

  ![RELEASE](https://img.shields.io/badge/November_2026-teal)&nbsp;

## [Model assignment matrix](./workflow/workflow.md#4-model-assignment-matrix)

| Task | Primary | Secondary | Escalate | Review |
|--:|---|---|---|---|
| Design | Claude Opus 5.5 | GPT-6.1 Sol | Claude Fable 5.2 | GPT-6.1 Sol |
| Feature (small) | Claude Sonnet 5.5 | GPT-6.1 Terra | Claude Opus 5.5 | Tests and build |
| Feature (large) | Claude Opus 5.5 | Claude Sonnet 5.5 | Claude Fable 5.2 | GPT-6.1 Sol |
| Refactor (mechanical) | Claude Haiku 5.5 | GPT-6 Luna | Claude Sonnet 5.5 | Compiler |
| Refactor (design) | Claude Opus 5.5 | Claude Sonnet 5.5 | Claude Fable 5.2 | Tests and review |
| Unit tests | GPT-6.1 Terra | Claude Sonnet 5.5 | GPT-6.1 Sol | Mutation testing |
| XML docs | Claude Haiku 5.5 | GPT-6 Luna | Claude Sonnet 5.5 | `CS1591` build check |
| Code comments | Claude Sonnet 5.5 | Claude Haiku 5.5 | Claude Opus 5.5 | Human review |
| User manual | Claude Opus 5.5 | GPT-6.1 Terra | GPT-6.1 Sol | Compile samples |
| Code review | GPT-6.1 Sol | Gemini 3.8 Flash | Claude Opus 5.5 | Human for risky code |
| Repo or CI config | GPT-6.1 Terra | Claude Haiku 5.5 | Claude Sonnet 5.5 | CI on clean clone |
| .NET Framework migration plan | Claude Opus 5.5 | GPT-6.1 Sol | Claude Fable 5.2 | Second model review |
| Quick legacy fix | MAI-Code-1.1-Flash | Gemini 3.8 Flash | Claude Sonnet 5.5 | Tests |
| Experiment | Gemini 3.8 Flash | MAI-Code-1.1-Flash | Kimi K3 | Spending cap |
| Classification or routing | Claude Haiku 5.5 | GPT-6 Luna | Claude Sonnet 5.5 | Spot checks |

---

## Models

| Model | Provider | Context | Input $/1M | Output $/1M | Cost | Summary |
|-------|----------|:-------:|:----------:|:-----------:|:----:|---------|
| [GPT-6 Astra](model/OpenAI-Models.md) | OpenAI | 1.05M | $10 | $50 | Highest | Most capable model for hard reasoning and coding |
| [GPT-6.1 Sol](model/OpenAI-Models.md) | OpenAI | 1.05M | $2 | $10 | 7 | Near-Astra capability at a lower price |
| [GPT-6.1 Terra](model/OpenAI-Models.md) | OpenAI | 1.05M | $1 | $5 | 6 | Fast, efficient model for writing and computer use |
| [GPT-6 Luna](model/OpenAI-Models.md) | OpenAI | 1.05M | $0.10 | $0.50 | Lowest | Cheapest GPT-6 model, for high-volume focused tasks |
| [GPT-5.6 Sol](model/OpenAI-Models.md) | OpenAI | 1.05M | $4 | $20 | 8 | Earlier flagship for agentic coding and long tasks |
| [GPT-5.6 Terra](model/OpenAI-Models.md) | OpenAI | 1.05M | $2 | $12 | 7 | Earlier balanced tier for everyday engineering; deprecated in Copilot Nov 16, 2026 |
| [GPT-5.6 Luna](model/OpenAI-Models.md) | OpenAI | 1.05M | $0.20 | $1.20 | 3 | Earlier low-cost tier for automation |
| [GPT-5.3-Codex](model/OpenAI-Models.md) | OpenAI | 400K | — | — | — | Coding agent; deprecated, shuts down April 1, 2027 |
| [GPT-5.4 nano](model/OpenAI-Models.md) | OpenAI | — | ~$0.20 | ~$1.25 | 3 | Small model; deprecated, shuts down April 1, 2027 |
| [Claude Fable 5.2](model/Anthropic-Models.md) | Anthropic | 1M | $8 | $40 | 9 | Top reasoning model for long agentic work |
| [Claude Opus 5.5](model/Anthropic-Models.md) | Anthropic | 1M | $4 | $20 | 8 | Recommended default for long coding and knowledge work |
| [Claude Sonnet 5.5](model/Anthropic-Models.md) | Anthropic | 1M | $2 | $10 | 7 | Best balance of speed and intelligence |
| [Claude Haiku 5.5](model/Anthropic-Models.md) | Anthropic | 1M | from $0.10 | from $0.50 | Lowest | Fastest and cheapest; classification and routing |
| [Claude Fable 5.1](model/Anthropic-Models.md) | Anthropic | 1M | $10 | $50 | Highest | Earlier Fable generation |
| [Claude Fable 5](model/Anthropic-Models.md) | Anthropic | 1M | $10 | $50 | Highest | Earlier Fable; access was suspended June to July 2026 |
| [Claude Opus 5](model/Anthropic-Models.md) | Anthropic | 1M | $5 | $25 | 8 | Earlier Opus generation; deprecated in Copilot Nov 16, 2026 |
| [Claude Opus 4.8](model/Anthropic-Models.md) | Anthropic | 1M | $5 | $25 | 8 | Stable earlier Opus; fast-mode variant listed; deprecated in Copilot Nov 16, 2026 (annual individual plans excepted) |
| [Claude Sonnet 5](model/Anthropic-Models.md) | Anthropic | 1M | $2 | $10 | 7 | Earlier Sonnet at the same price as 5.5 |
| [Claude Sonnet 4.6](model/Anthropic-Models.md) | Anthropic | 1M | $3 | $15 | 7 | Older, pricier Sonnet; retired from Copilot Sep 1, 2026 (annual individual plans excepted) |
| [Claude Haiku 4.5](model/Anthropic-Models.md) | Anthropic | 200K | $1 | $5 | 6 | Older small model with 200K context |
| [Gemini 4 Argon](model/Google-Models.md) | Google | 1.05M (input + output) | — | — | — | Google's frontier model for deep, multi-domain work |
| [Gemini 3.8 Flash](model/Google-Models.md) | Google | 1.05M | $0.75 (intro) | $3.75 (intro) | 5 | Fast, large-context model with multimodal input |
| [Grok 4.7](model/Grok-Models.md) | xAI | 500K | $2 (sources differ) | $6 (sources differ) | 6 | Newest Grok; coding and agentic focus |
| [Grok 4.6](model/Grok-Models.md) | xAI | 500K | — | — | — | Earlier Grok coding model |
| [MAI-Code-1.1-Flash](model/Microsoft-MAI-Models.md) | Microsoft | 256K | $0.20 | $1.20 | 3 | Low-cost coding model in GitHub Copilot |
| [Kimi K3](model/Moonshot-Models.md) | Moonshot | 1M | $3 | $15 | 7 | Open-weight, 1M-context model for long agentic tasks |

<br>

***

> <sub>**Last updated:** November 14, 2026</sub>
