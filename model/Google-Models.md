# Google Gemini Models

> **Last verified:** November 12, 2026
> **Primary source:** [Google models catalog (Gemini Enterprise Agent Platform)](https://docs.cloud.google.com/gemini-enterprise-agent-platform/data/models/google-models)
> **Pricing caveat:** Gemini 3.8 Flash is at an introductory rate through December 31, 2026. Confirm the rate on the [Gemini API pricing page](https://ai.google.dev/gemini-api/docs/pricing) before budgeting.

---

## At a glance

| Model | API ID | Context | Max output | Input $/1M | Output $/1M | Tier | Best for |
|---|---|---|---|---|---|---|---|
| **Gemini 4 Argon** | See Google's docs | 1,048,576 unified (input + output) | Shared with input | Verify | Verify | Frontier | Deep multi-step work across coding, legal, finance, science |
| **Gemini 3.8 Flash** | `gemini-3.8-flash` | 1,048,576 | 65,536 | $0.75 (intro) | $3.75 (intro) | Flash | Fast, large-context coding and agentic work |

**Your list includes:** Gemini 3.8 Flash and Gemini 4 Argon.

---

## Recommended picks for your workflow

| Task | Recommended | Why |
|---|---|---|
| Hardest refactor or design analysis | Gemini 4 Argon | Frontier-level, configurable thinking depth |
| Fast daily coding and doc drafts | Gemini 3.8 Flash | Low cost, large context, quick responses |
| Analyzing a whole repository in one prompt | Gemini 3.8 Flash | 1M-token window for large inputs |
| Screenshot-to-UI or diagram-based work | Gemini 3.8 Flash | Accepts image, audio, and video input |

---

## Model details

### Gemini 4 Argon

| Attribute | Value |
|---|---|
| Positioning | Google's frontier model for deep work in complex, real-world tasks |
| Context | Unified limit of 1,048,576 tokens covering input **and** output |
| Output | Includes thinking, function calls, and the final response, so long reasoning uses up the same budget as your prompt |
| Thinking | Configurable thinking levels |
| Variants | Gemini 4 Argon, plus **Gemini 4 Argon Cyber Permissive** for cybersecurity work (gated) |

**Description (Google):** Excels across coding, finance, legal, cybersecurity, and science. Supports deep multi-step reasoning with configurable thinking levels, and long-output generation.

**Use cases:** Complex refactors that need deep reasoning, architectural trade-off analysis, long-form technical documentation, security analysis (with the cyber variant where access is granted).

**Strengths:**
- Frontier-class reasoning across many domains
- Configurable thinking lets you trade cost and latency for depth
- Long output capability

**Weaknesses:**
- **Unified token budget:** Heavy thinking plus a large answer can consume the whole 1M window. Plan prompt size with output in mind.
- The cyber variant is restricted and not available to general users
- I could not confirm per-token pricing from the docs I retrieved. Check the pricing page.

**Migration note:** Google's documentation includes a "Get started with Gemini 4" guide and a migration path from Gemini 3.x.

---

### Gemini 3.8 Flash

| Attribute | Value |
|---|---|
| API ID | `gemini-3.8-flash` (dots, not dashes) |
| Released | September 2, 2026 (general availability) |
| Context | 1,048,576 tokens |
| Max output | 65,536 tokens |
| Pricing | $0.75 input / $3.75 output per 1M tokens (introductory through December 31, 2026) |
| Input modalities | Text, image, audio, video |
| Output | Text |
| Caching | Supported; cached input is much cheaper |

**Description (Google):** Google's most intelligent Flash model, with significant gains over 3.7 Flash in software engineering, agentic tasks, and multi-step reasoning.

**Use cases:** Agentic coding, code review, document and chart analysis, multi-file refactoring with large context, screenshot-to-web-layout generation.

**Strengths:**
- Strong quality for its price and speed
- 1M-token context at a low introductory rate
- Broad multimodal input (audio and video as well as images)
- Good value for high-throughput work

**Weaknesses:**
- Introductory pricing ends December 31, 2026. Budget for the step-up.
- Output capped at 65K tokens, lower than the 128K limits on Claude and OpenAI models
- Long context does not guarantee equal attention to every part. Retrieval still matters.
- A gated **Gemini 3.8 Flash Cyber** variant exists for security work

---

## Related Gemini models (not on your list, for reference)

| Model | Notes |
|---|---|
| Gemini 4 Carbon | Another 4-generation model in the catalog |
| Gemini 3.1 Pro, 2.5 Pro | Earlier Pro-tier models |
| Gemini 3.8 Live, 3.8 Flash TTS | Realtime voice and text-to-speech |
| Gemini Embedding 2 | Embeddings for search and retrieval |
| Veo 3.1, Lyria 3, Nano Banana models | Video, music, and image generation |

---

## Notes and caveats

- **Model IDs use dots**, for example `gemini-3.8-flash`. Dashed forms appear only in page URLs.
- **Access route matters.** Pricing and features can differ between Google AI Studio, the Gemini API, and Google Cloud's Agent Platform. Check the route your organization uses.
- **Context pricing:** Some Gemini tiers charge more above a context threshold. Verify on the pricing page for large prompts.
- **OpenAI-compatible endpoints** are available, which makes it easier to test Gemini alongside GPT models.
