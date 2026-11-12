# Microsoft MAI Models

> **Last verified:** November 12, 2026
> **Primary sources:** [MAI-Code-1.1-Flash on Microsoft Foundry](https://ai.azure.com/catalog/data/models/MAI-Code-1.1-Flash), [Microsoft AI model card](https://microsoft.ai/pdf/MAI-Code-1.1-Flash-Model-Card.PDF), [Microsoft AI model page](https://microsoft.ai/data/models/mai-code-1-flash/)

---

## At a glance

| Model | Status | Context | Input $/1M | Output $/1M | Cached input $/1M | Best for |
|---|---|---|---|---|---|---|
| **MAI-Code-1.1-Flash** | Active (released Aug 11, 2026) | 256K | $0.20 | $1.20 | $0.02 | Fast, low-cost coding assistance in GitHub Copilot and Foundry |

Pricing is shown as reported for GitHub Copilot. Check the Foundry pricing page for Azure rates.

---

## Recommended picks for your workflow

| Task | Recommended | Why |
|---|---|---|
| Everyday coding in an IDE via Copilot | MAI-Code-1.1-Flash | Low cost, fast, tuned for Copilot workflows |
| Refactoring and repo Q&A | MAI-Code-1.1-Flash | Microsoft lists these as target use cases |
| Screenshot or design to prototype | MAI-Code-1.1-Flash | Native vision support |
| Hard architectural problems | Use a larger model | MAI-Code is a workhorse, not a frontier model |

---

## Model details

### MAI-Code-1.1-Flash

| Attribute | Value |
|---|---|
| Developer | Microsoft AI |
| Model ID | `mai-code-1.1-flash` |
| Released | August 11, 2026 |
| Architecture | Sparse Mixture-of-Experts: 138B total parameters, about 5B active per token (per model card) |
| Context | 256,000 tokens |
| Modalities | Text and image input; text output |
| Pricing (GitHub Copilot) | $0.20 input / $0.02 cached input / $1.20 output per 1M tokens |
| Predecessor | MAI-Code-1-Flash (retired from Copilot September 10, 2026) |
| Post-training focus | CLI tasks and .NET, per third-party reporting of the model card |

**Description (Microsoft):** A coding-focused generative model for fast, efficient assistance in everyday developer workflows. Optimized for low latency and low serving cost.

**Intended use cases (Microsoft):**
- Agentic coding in real repositories
- Repository question answering
- Refactoring
- Tool-using developer scenarios
- Turning screenshots, diagrams, and designs into code

**Vendor-reported results** (Copilot harness, not independently verified):
- SWE-bench Verified: **72.6%**
- Terminal-Bench 2.1: **62.9%**
- Microsoft reports about **25% fewer tokens per task** and **25% faster token streaming** than MAI-Code-1.0

**Strengths:**
- Very low cost. Roughly a quarter of the price of its predecessor.
- Token-efficient, which keeps agent runs cheap
- Native vision for UI and diagram input
- Reported post-training emphasis on .NET, relevant to your stack
- Fast enough for interactive IDE use
- Also available in a quantized on-device version on some Windows hardware

**Weaknesses:**
- Microsoft positions it as an efficient workhorse, not a frontier model. Expect less depth than Claude Opus or GPT-6 Astra on the hardest problems.
- Benchmarks are vendor-reported and from Microsoft's own harness
- Available mainly through GitHub Copilot and Microsoft Foundry, so it is less flexible than direct API access from other providers
- Context is smaller than the 1M-token models in other families

---

## Notes and caveats

- **Access route:** Most users reach MAI-Code-1.1-Flash through GitHub Copilot. Foundry offers API access with Azure billing and governance.
- **Premium request multiplier:** In Copilot, annual subscribers were charged at a reduced premium multiplier for this model at launch. Check current Copilot plan details.
- **.NET fit:** Microsoft's reported focus on .NET makes this a sensible first test for your C# and .NET 4.8 work. Verify the output against your own codebase, especially for legacy Framework APIs.
- **Model naming:** Microsoft uses "MAI-Code" for coding models and "MAI-Thinking" for its general model. MAI-Code-1.1-Flash depends on MAI-Thinking-1.
