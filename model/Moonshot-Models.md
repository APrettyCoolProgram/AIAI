# Moonshot Kimi Models

> **Last verified:** November 12, 2026
> **Primary sources:** [Kimi K3 on GitHub](https://github.com/MoonshotAI/Kimi-K3), [Kimi API pricing](https://platform.kimi.ai/docs/pricing/chat-k3), plus third-party reporting noted below.

---

## At a glance

| Model | Status | Architecture | Context | Input $/1M | Cached input $/1M | Output $/1M | Open weights | Best for |
|---|---|---|---|---|---|---|---|---|
| **Kimi K3** | Active (released July 16, 2026) | MoE, 2.8T total, ~50B active | 1,048,576 (1M) | $3.00 | $0.30 | $15.00 | Yes (released late July 2026) | Long-horizon agentic coding and knowledge work |

---

## Recommended picks for your workflow

| Task | Recommended | Why |
|---|---|---|
| Long agentic coding sessions | Kimi K3 | Built for long-horizon software tasks |
| Analyzing a large repository in one pass | Kimi K3 | 1M-token context at a flat price |
| Self-hosted or private experiments | Kimi K3 | Open weights, though hardware needs are very large |
| Cost-sensitive production at scale | Compare first | $15 output is not cheap; benchmark against Sonnet 5.5 and GPT-6.1 Terra on your own tasks |

---

## Model details

### Kimi K3

| Attribute | Value |
|---|---|
| Developer | Moonshot AI (Beijing) |
| API ID | `kimi-k3` (check Moonshot's docs for the exact string) |
| Released | July 16, 2026 (API and apps); weights released late July 2026 |
| Architecture | Mixture-of-Experts with Kimi Delta Attention and Attention Residuals |
| Total parameters | 2.8 trillion ("first open model in the 3-trillion-parameter class," per Moonshot) |
| Active parameters | About 50B per token (16 of 896 experts) |
| Context window | 1,048,576 tokens, with flat pricing across the full range |
| Max output | Up to about 131K tokens (third-party listing) |
| Modalities | Text, image, and video input; text output. Native vision. |
| Pricing (API) | $3.00 input / $0.30 cached input / $15.00 output per 1M tokens |
| License | Modified MIT, per initial reporting. Check the license file on the release page. |

**Description (Moonshot):** A long-horizon agent model for software engineering, knowledge work, and multimodal reasoning.

**Vendor-reported benchmarks** (not independently verified):
- Long-horizon tasks: **91.2%** with context compaction at 300K tokens
- **90.4%** on long-horizon tasks with no context management across the full 1M window
- Reported to rank first on Arena's WebDev coding leaderboard at the time of launch
- Third-party ranking: fourth on the Artificial Analysis Intelligence Index at launch

**Use cases:** Multi-hour coding agents, large-codebase analysis, long document synthesis, multimodal work such as diagrams and screenshots, long refactoring plans.

**Strengths:**
- Very large context at a flat price with no tier surcharge above a threshold
- Strong reported results on long-running agent tasks
- Open weights allow self-hosting and inspection
- Cache-hit pricing ($0.30) makes repeated prompts cheap
- Native vision and video input

**Weaknesses:**
- **Output price is high** at $15 per 1M, above Claude Sonnet 5.5 ($10) and GPT-6.1 Terra ($5) on output tokens
- **Self-hosting is demanding.** Moonshot recommends at least 64 accelerators for the full model.
- Benchmarks are vendor-reported. Independent evaluation was still early at launch.
- Some enterprises may have data-residency or vendor-origin policies to review before use
- Smaller ecosystem of third-party tools and integrations than the big US providers

---

## Notes and caveats

- **Cache-aware prompting:** Keep your system prompt and repository context stable between calls. Cached input costs one-tenth of fresh input.
- **Switching models:** When changing models in the Kimi Code CLI, start a new session. Cache from the previous model will not hit.
- **Context setting:** Third-party agents may need the context window set explicitly to 1,048,576 for the full length.
- **Evaluate on your code:** Strong public scores on web and terminal tasks do not guarantee strong results on .NET Framework 4.8 or other legacy stacks. Test before adopting.
