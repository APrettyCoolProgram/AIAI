# AI Model Reference

## Use cases

| Use case | Model | Fallback |
|---|---|---|
| Large C# refactors, architecture | Claude Opus 5.5 | Claude Fable 5.2 or GPT-6.1 Sol |
| Routine refactors, code review | Claude Sonnet 5.5 | GPT-6.1 Terra |
| XML doc comments and manuals | Claude Sonnet 5.5 or GPT-6.1 Terra | Gemini 3.8 Flash |
| Bulk doc generation across a repo | Claude Haiku 5.5 or GPT-6 Luna | MAI-Code-1.1-Flash |
| Repo hygiene and build scripting | GPT-6.1 Terra | Grok 4.7 |
| Vibe-coding experiments | Gemini 3.8 Flash or MAI-Code-1.1-Flash | Kimi K3 |
| Analysis of a whole solution in one prompt | Gemini 3.8 Flash or Kimi K3 | Claude Opus 5.5 |

---

## Models

| Model | Provider | Context | Input $/1M | Output $/1M | Summary |
|---|---|---|---|---|---|
| [GPT-6 Astra](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $10 | $50 | Most capable model for hard reasoning and coding |
| [GPT-6.1 Sol](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $2 | $10 | Near-Astra capability at a lower price |
| [GPT-6.1 Terra](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $1 | $5 | Fast, efficient model for writing and computer use |
| [GPT-6 Luna](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $0.10 | $0.50 | Cheapest GPT-6 model, for high-volume focused tasks |
| [GPT-6 Sol](data/models/OpenAI-Models.md) | OpenAI | 1.05M | — | — | Alias that routes to GPT-6.1 Sol |
| [GPT-5.6 Sol](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $4 | $20 | Earlier flagship for agentic coding and long tasks |
| [GPT-5.6 Terra](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $2 | $12 | Earlier balanced tier for everyday engineering |
| [GPT-5.6 Luna](data/models/OpenAI-Models.md) | OpenAI | 1.05M | $0.20 | $1.20 | Earlier low-cost tier for automation |
| [GPT-5.3-Codex](data/models/OpenAI-Models.md) | OpenAI | 400K | — | — | Coding agent; deprecated, shuts down April 1, 2027 |
| [GPT-5.4 nano](data/models/OpenAI-Models.md) | OpenAI | — | ~$0.20 | ~$1.25 | Small model; deprecated, shuts down April 1, 2027 |
| [Claude Fable 5.2](data/models/Anthropic-Models.md) | Anthropic | 1M | $8 | $40 | Top reasoning model for long agentic work |
| [Claude Opus 5.5](data/models/Anthropic-Models.md) | Anthropic | 1M | $4 | $20 | Recommended default for long coding and knowledge work |
| [Claude Sonnet 5.5](data/models/Anthropic-Models.md) | Anthropic | 1M | $2 | $10 | Best balance of speed and intelligence |
| [Claude Haiku 5.5](data/models/Anthropic-Models.md) | Anthropic | 1M | from $0.10 | from $0.50 | Fastest and cheapest; classification and routing |
| [Claude Fable 5.1](data/models/Anthropic-Models.md) | Anthropic | 1M | $10 | $50 | Earlier Fable generation |
| [Claude Fable 5](data/models/Anthropic-Models.md) | Anthropic | 1M | $10 | $50 | Earlier Fable; access was suspended June to July 2026 |
| [Claude Opus 5](data/models/Anthropic-Models.md) | Anthropic | 1M | $5 | $25 | Earlier Opus generation |
| [Claude Opus 4.8](data/models/Anthropic-Models.md) | Anthropic | 1M | $5 | $25 | Stable earlier Opus; fast-mode variant listed |
| [Claude Sonnet 5](data/models/Anthropic-Models.md) | Anthropic | 1M | $2 | $10 | Earlier Sonnet at the same price as 5.5 |
| [Claude Sonnet 4.6](data/models/Anthropic-Models.md) | Anthropic | 1M | $3 | $15 | Older, pricier Sonnet |
| [Claude Haiku 4.5](data/models/Anthropic-Models.md) | Anthropic | 200K | $1 | $5 | Older small model with 200K context |
| [Gemini 4 Argon](data/models/Google-Models.md) | Google | 1.05M (input + output) | — | — | Google's frontier model for deep, multi-domain work |
| [Gemini 3.8 Flash](data/models/Google-Models.md) | Google | 1.05M | $0.75 (intro) | $3.75 (intro) | Fast, large-context model with multimodal input |
| [Grok 4.7](data/models/Grok-Models.md) | xAI | 500K | $2 (sources differ) | $6 (sources differ) | Newest Grok; coding and agentic focus |
| [Grok 4.6](data/models/Grok-Models.md) | xAI | 500K | — | — | Earlier Grok coding model |
| [Grok 4.5](data/models/Grok-Models.md) | xAI | 500K | $2 | $6 | Earlier Grok for coding and STEM |
| [MAI-Code-1.1-Flash](data/models/Microsoft-MAI-Models.md) | Microsoft | 256K | $0.20 | $1.20 | Low-cost coding model in GitHub Copilot |
| [Kimi K3](data/models/Moonshot-Models.md) | Moonshot | 1M | $3 | $15 | Open-weight, 1M-context model for long agentic tasks |

<br>

***

> <sub>**Last updated:** November 12, 2026</sub>
