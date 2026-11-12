# OpenAI Models

> **Last verified:** November 12, 2026
> **Primary sources:** [OpenAI model catalog](https://developers.openai.com/api/docs/models), [OpenAI deprecations](https://developers.openai.com/api/docs/deprecations), plus third-party aggregators where noted.
> **Pricing caveat:** OpenAI changed GPT-5.6 prices on July 30, 2026. Figures below use the most recent reported rates. Confirm against the [OpenAI pricing page](https://developers.openai.com/api/docs/pricing) before budgeting.

---

## At a glance

| Model | Tier | Status | Context | Max output | Input $/1M | Output $/1M | Best for |
|---|---|---|---|---|---|---|---|
| **GPT-6 Astra** | Flagship | Active | 1.05M | 128K | $10.00 | $50.00 | Hardest reasoning and coding |
| **GPT-6.1 Sol** | Balanced flagship | Active | 1.05M | 128K | $2.00 | $10.00 | Complex work at lower cost than Astra |
| **GPT-6.1 Terra** | Fast/efficient | Active | 1.05M | 128K | $1.00 | $5.00 | Visual reasoning, computer use, writing |
| **GPT-6 Luna** | Efficient | Active | 1.05M | 128K | $0.10 | $0.50 | High-volume, focused tasks |
| **GPT-6 Sol** | Flagship (alias) | Active | 1.05M | 128K | see note | see note | Routes to GPT-6.1 Sol (see below) |
| **GPT-5.6 Sol** | Flagship | Active | 1.05M | 128K | $4.00 | $20.00 | Agentic coding, long-horizon work |
| **GPT-5.6 Terra** | Balanced | Active | 1.05M | 128K | $2.00 | $12.00 | Everyday engineering tasks |
| **GPT-5.6 Luna** | Efficient | Active | 1.05M | 128K | $0.20 | $1.20 | Cheap, high-volume automation |
| **GPT-5.3-Codex** | Coding agent | **Deprecated** | 400K | n/a | n/a | n/a | Shuts down April 1, 2027 |
| **GPT-5.4 nano** | Small | **Deprecated** | n/a | n/a | ~$0.20 | ~$1.25 | Shuts down April 1, 2027 |

---

## Recommended picks for your workflow

| Task | Recommended | Why |
|---|---|---|
| Large C# refactors across many files | GPT-6 Astra or GPT-6.1 Sol | Strongest reasoning; large context holds whole solution |
| Generating XML doc comments and manuals | GPT-6.1 Terra | Clear, natural writing at low cost |
| Bulk doc/comment generation across a repo | GPT-6 Luna | Lowest cost for high-volume, repetitive output |
| Vibe-coding experiments | GPT-5.6 Terra | Good balance of speed and capability |
| Repo hygiene scripts (PowerShell, build, CI) | GPT-6.1 Terra or GPT-5.6 Terra | Solid tool use and computer-use support |

---

## Model details

### GPT-6 Astra

| Attribute | Value |
|---|---|
| Model ID | `gpt-6-astra` |
| Context window | 1,050,000 tokens |
| Max output | 128K tokens |
| Pricing | $10.00 input / $50.00 output per 1M tokens |
| Knowledge cutoff | April 30, 2026 |
| Reasoning effort | low, medium, high, xhigh, max |
| Tools | Functions, web search, file search, computer use |
| Modalities | Text and image input, text output |

**Description (OpenAI):** The most capable model for the most demanding work. OpenAI recommends it as the default for complex reasoning and coding.

**Use cases:** Multi-file architecture changes, difficult debugging, long agentic coding sessions, complex technical document synthesis.

**Strengths:**
- Top-tier reasoning and coding depth
- Full tool set, including computer use
- Large context suits whole-solution analysis

**Weaknesses:**
- Highest cost in the GPT-6 family (about 5x Sol per token)
- Overkill for routine refactors or simple comments
- Higher latency at high reasoning effort

---

### GPT-6.1 Sol

| Attribute | Value |
|---|---|
| Model ID | `gpt-6.1-sol` |
| Context window | 1,050,000 tokens |
| Max output | 128K tokens |
| Pricing | $2.00 input / $10.00 output per 1M tokens |
| Knowledge cutoff | April 30, 2026 |
| Reasoning effort | low, medium, high, xhigh, max |
| Tools | Functions, web search, file search, computer use |

**Description (OpenAI):** Near-Astra performance for complex work at a lower cost.

**Use cases:** Most professional coding work where Astra is more than needed: feature implementation, code review, migration planning.

**Strengths:**
- Strong balance of capability and cost
- Same context and tool support as Astra
- Good default for daily engineering work

**Weaknesses:**
- Trails Astra on the hardest multi-step problems
- Reasoning-heavy tasks at high effort still cost more than Luna or Terra

---

### GPT-6.1 Terra

| Attribute | Value |
|---|---|
| Model ID | `gpt-6.1-terra` |
| Context window | 1,050,000 tokens |
| Max output | 128K tokens |
| Pricing | $1.00 input / $5.00 output per 1M tokens |
| Knowledge cutoff | June 1, 2026 |
| Reasoning effort | none, low, medium, high, xhigh, max |
| Tools | Functions, web search, file search, computer use |

**Description (OpenAI):** A fast, efficient model for visual reasoning, precise computer use, and clear, natural writing.

**Use cases:** Documentation and manual writing, UI-related tasks from screenshots, scripted desktop automation, everyday refactoring.

**Strengths:**
- Strong natural-language writing (good for manuals)
- Visual reasoning and computer use
- Reasoning can be turned off (`none`) for fast responses

**Weaknesses:**
- Less depth than Sol or Astra on complex architectural problems
- Newer cutoff than some siblings but still a general model, not code-specialized

---

### GPT-6 Luna

| Attribute | Value |
|---|---|
| Model ID | `gpt-6-luna` |
| Context window | 1,050,000 tokens |
| Max output | 128K tokens |
| Pricing | $0.10 input / $0.50 output per 1M tokens |
| Knowledge cutoff | May 18, 2026 |
| Reasoning effort | none, low, medium, high, xhigh, max |
| Tools | Functions, web search, file search, computer use |

**Description (OpenAI):** The most efficient model for focused, high-volume tasks.

**Use cases:** Bulk XML doc comment generation, classification of commits or issues, extraction tasks, routing, linting-style checks.

**Strengths:**
- Very low cost; suitable for running across an entire repository
- Full tool support and large context
- Fast with reasoning off

**Weaknesses:**
- Not suited to subtle design or refactoring decisions
- Output quality on hard problems drops noticeably versus Sol or Astra

---

### GPT-6 Sol (alias)

| Attribute | Value |
|---|---|
| Model ID | `gpt-6-sol` |
| Status | Active; OpenAI's page redirects readers to GPT-6.1 Sol |
| Pricing | Verify on pricing page; the GPT-6.1 Sol rate ($2/$10) is the current Sol-tier reference |

**Note:** Treat `gpt-6-sol` as the Sol-tier entry point. OpenAI's own page points readers to GPT-6.1 Sol as the newer Sol model. OpenAI also names `gpt-6-sol` as the replacement for the deprecated GPT-5.3-Codex and GPT-5.1.

---

### GPT-5.6 Sol

| Attribute | Value |
|---|---|
| Model ID | `gpt-5.6-sol` (alias `gpt-5.6`) |
| Context window | 1,050,000 tokens |
| Max output | 128K tokens |
| Pricing | $4.00 input / $20.00 output per 1M (after July 30, 2026 cut; launch price was $5 / $30) |
| Knowledge cutoff | February 16, 2026 |

**Use cases:** Agentic coding, long-horizon terminal tasks, hard engineering problems where GPT-6 is not available in your account.

**Strengths:** Strong agentic and terminal performance; supports subagents and programmatic tool calling via the Responses API.

**Weaknesses:** Older cutoff than GPT-6 models; superseded in OpenAI's own catalog by GPT-6.1 Sol at lower cost.

---

### GPT-5.6 Terra

| Attribute | Value |
|---|---|
| Model ID | `gpt-5.6-terra` |
| Context window | 1,050,000 tokens |
| Max output | 128K tokens |
| Pricing | $2.00 input / $12.00 output per 1M (after July 30 cut; launch was $2.50 / $15) |
| Knowledge cutoff | February 16, 2026 |

**Use cases:** Everyday coding, scripting, mid-complexity refactors, documentation drafts.

**Strengths:** Good price-to-capability balance; same context and output limits as Sol.

**Weaknesses:** Superseded by GPT-6.1 Terra, which is newer and cheaper. Consider it mainly if you need the 5.6 behavior.

---

### GPT-5.6 Luna

| Attribute | Value |
|---|---|
| Model ID | `gpt-5.6-luna` |
| Context window | 1,050,000 tokens |
| Max output | 128K tokens |
| Pricing | $0.20 input / $1.20 output per 1M (after July 30 cut; launch was $1 / $6) |
| Knowledge cutoff | February 16, 2026 |

**Use cases:** High-volume automation, repository-wide batch jobs.

**Strengths:** Very low cost; same context as the larger tiers.

**Weaknesses:** Superseded by GPT-6 Luna. Quality on difficult tasks is limited.

---

### GPT-5.3-Codex (deprecated)

| Attribute | Value |
|---|---|
| Model ID | `gpt-5.3-codex` |
| Released | February 5, 2026 |
| Context window | 400,000 tokens (third-party listing) |
| Status | **Deprecated** October 1, 2026; API shutdown **April 1, 2027** |
| Replacement | `gpt-6-sol` (per OpenAI) |

**Description:** A coding-specialized agent model built for long-running agentic work in Codex, with CLI and IDE integration.

**Strengths (when current):** Strong autonomous software tasks, CLI and IDE integration.

**Weaknesses:** Narrower general use; already removed from Codex for ChatGPT sign-in. Plan migration now.

**Migration:** Search your code and config for `gpt-5.3-codex`, then re-run your evaluation set against `gpt-6-sol` before switching.

---

### GPT-5.4 nano (deprecated)

| Attribute | Value |
|---|---|
| Model ID | `gpt-5.4-nano` |
| Status | **Deprecated** October 1, 2026; shutdown **April 1, 2027** |
| Replacement | `gpt-6-luna` (per OpenAI) |
| Pricing (last reported) | ~$0.20 input / ~$1.25 output per 1M |

**Note:** Your list includes "GPT-5.4 nano 1". Replace it with GPT-6 Luna before the shutdown date.

---

## Specialized OpenAI models (not on your list, for reference)

| Model | Purpose |
|---|---|
| `gpt-6-cyber` / `gpt-5.6-cyber` | Authorized security research; access is restricted |
| `gpt-image-2.6-*` / `gpt-image-2.5-*` | Image generation and editing |
| `gpt-live-1`, `gpt-realtime-*` | Realtime voice |
| `gpt-transcribe`, `gpt-realtime-whisper` | Speech-to-text |

---

## Notes and caveats

- **All GPT-5.6 and GPT-6 models share a 1.05M-token context window and 128K max output,** so context size is not a reason to pick one over another. Choose by capability and cost.
- **Long-context surcharge:** Requests above about 272K input tokens on GPT-5.6 may be billed at higher rates. Check the pricing page before sending large codebases.
- **Use the Responses API** for the full tool set (multi-agent, programmatic tool calling). Chat Completions has fewer tools.
- **Knowledge cutoffs differ** (February to June 2026). Give newer models current context in prompts when working with recent frameworks.
