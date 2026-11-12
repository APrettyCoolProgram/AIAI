# Model Documentation

This document contains the prompts/responses for:

* `Model-Description.md`
* `Model-Description-Detailed.md`
* 'Model-Suggestion.md
* 'Model-Suggestion-Detailed.md

## Initial setup

### Prompt

```text
I'm a software engineer that would like to start incorporating AI into my 
workflow.

My current workflow includes:

- Writing software in C# using both .NET 10 and the .NET Framework 4.8
- Continuously refactoring to keep technical debt at a minimum
- Creating technical documentation/manuals for the software I write
- Occasionally experimenting with vibe-coding weird ideas
- Ensuring that my code repositories are clean and well organized.

This is the current list of models that I have available:

OpenAI/GPT (https://developers.openai.com/api/docs/models)
- GPT‑5.3‑Codex
- GPT‑5.4 nano 1
- GPT‑5.6 Luna
- GPT‑5.6 Sol
- GPT‑5.6 Terra
- GPT‑6 Astra
- GPT‑6 Luna
- GPT‑6 Sol
- GPT‑6.1 Sol
- GPT‑6.1 Terra

Anthropic/Claude (https://platform.claude.com/docs/en/data/models/overview)
- Claude Fable 5
- Claude Fable 5.1
- Claude Haiku 4.5
- Claude Haiku 5.5
- Claude Opus 4.8
- Claude Opus 4.8 (fast mode)
- Claude Opus 5
- Claude Opus 5.5
- Claude Sonnet 4.6
- Claude Sonnet 5
- Claude Sonnet 5.5

Google/Gemini (https://docs.cloud.google.com/gemini-enterprise-agent-platform/data/models/google-models)
- Gemini 3.8 Flash
- Gemini 4 Argon

Grok (https://docs.x.ai/developers/models)
- Grok 4.5
- Grok 4.6
- Grok 4.7

Microsoft/MAI (https://microsoft.ai/data/models/mai-code-1-flash/))
- MAI‑Code‑1.1‑Flash

Moonshot/Kimi
- Kimi K3 (https://github.com/MoonshotAI/Kimi-K3)

We will use this information to create a number of documents.
```

### Response

```text
Excellent. We can use this as the foundation for developing a structured AI-Assisted Software Engineering Workflow tailored to your development environment and working practices.

I suggest we approach this as a collection of related documents rather than trying to put everything into one large set of instructions.

## 1. Your software engineering profile

I'll use the following as our baseline:

| Area                  | Requirements                                                     |
| --------------------- | ---------------------------------------------------------------- |
| Primary language      | C#                                                               |
| Modern framework      | .NET 10                                                          |
| Legacy framework      | .NET Framework 4.8                                               |
| Code quality          | Continuous refactoring and technical-debt reduction              |
| Documentation         | Technical documentation, XML documentation, and software manuals |
| Experimentation       | Vibe-coding and rapid prototyping                                |
| Repository management | Clean structure, organization, maintainability, and consistency  |

## 2. Available AI models

We'll treat your supplied model inventory as our available model pool.

I'll evaluate models across several dimensions:

- Reasoning: Understanding complex code, architecture, and dependencies.
- Coding: Writing, debugging, and modifying C# code.
- Refactoring: Identifying code smells, improving maintainability, and reducing technical debt.
- Documentation: Producing accurate technical documentation and explanations.
- Agentic capabilities: Handling multi-step development tasks and working across repositories.
- Instruction following: Respecting project conventions, constraints, and coding standards.
- Speed and cost: Balancing performance against API usage costs.

One important distinction: the best model for writing code isn't necessarily the best model for reviewing architecture or producing documentation.

We'll avoid assuming that one model should handle everything.

## 3. Proposed document collection

I recommend developing the following documents:

| Document                               | Purpose                                                                     |
| -------------------------------------- | --------------------------------------------------------------------------- |
| 01 – AI Workflow Strategy              | Define how AI fits into your overall development workflow.                  |
| 02 – Model Selection Guide             | Identify the best models for specific engineering tasks.                    |
| 03 – Software Engineering Instructions | Establish general expectations for AI-generated and modified code.          |
| 04 – C# Development Standards          | Define coding, architecture, and framework-specific conventions.            |
| 05 – Code Review & Refactoring         | Establish procedures for identifying and addressing technical debt.         |
| 06 – Technical Documentation Standards | Define how AI should create and maintain documentation.                     |
| 07 – Repository Management             | Establish repository organization, maintenance, and housekeeping practices. |
| 08 – Experimental Development          | Define a workflow for rapid prototyping and vibe-coding.                    |
| 09 – AI Agent Instructions             | Establish reusable instructions for AI agents working within repositories.  |

These are proposed documents, not a commitment to a fixed structure. We can combine or split them as necessary.

## 4. A few guiding principles

I suggest we establish these principles from the beginning:

1. AI is an engineering assistant, not an unquestionable authority.
2. Correctness takes priority over generating code quickly.
3. Existing architecture and conventions should be respected unless there is a good reason to change them.
4. Technical debt should be addressed incrementally rather than continually accumulating.
5. Documentation should reflect the actual implementation, not assumptions about it.
6. AI-generated changes should be reviewable, understandable, and maintainable.
7. Different models should be used where their individual strengths provide meaningful advantages.

My recommendation: Let's develop the documents sequentially, establishing the overall strategy first and allowing that strategy to influence the remaining documents.

I'll also distinguish between verified model capabilities and model names or specifications supplied in your inventory. When we get to model comparisons, I'll check the current official documentation rather than relying on assumptions.

We have a good starting point.
```

## 01 – AI Workflow Strategy (detailed)

### Prompt

Create the `WorkflowStrategy.md` file that defines how AI should fit in my workflow.

Keep it detailed, but concise.

Use tables when it makes sense to do so.

### Response

&#x20;Created

I've created WorkflowStrategy.md as the foundational document for your AI-assisted software engineering workflow.

WorkflowStrategy.md

Markdown · 15 sections · Includes tables and checklists

Download WorkflowStrategy.md

### What's covered

- AI's role throughout the development lifecycle
- Model selection and task allocation
- Repository analysis and code modification
- Refactoring and technical-debt management
- Testing and verification
- Technical documentation
- Repository organization
- Experimental development and vibe-coding
- Security and privacy
- Communication expectations
- Definition of Done
- Continuous improvement

Important: This document establishes the overall philosophy and workflow. It intentionally leaves detailed C# coding standards, model rankings, and repository-specific agent instructions to their own documents.

I'd recommend treating this as the foundational document that the remaining documents build upon.

## 01a – Workflow.md

### Prompt

Create the `WorkflowStrategy.md` file that defines how AI should fit in my workflow.

Keep it detailed, but concise.

Use tables when it makes sense to do so.

### Response

&#x20;Created

Created Workflow\.md as a concise reference to your AI-assisted development workflow.

&#x20;Download Workflow\.md

### Document structure

- Purpose and development context
- Core expectations for AI
- AI's role throughout the development lifecycle
- Model selection principles
- Code changes and refactoring
- Testing and verification
- Documentation and repository hygiene
- Experimental development
- Security and approval
- Communication and completion criteria

### Relationship between the documents

Workflow\.md

Quick reference

Concise workflow and expectations

Detailed guidance

WorkflowStrategy.md

Detailed reference

Full principles, procedures, and guidelines

The two documents are designed to complement each other without unnecessarily duplicating content.

## 01b – Workflow.md

### Prompt

Revise `Workflow.md` so it is significantly more simplified - think 50K foot view - that links back to `WorkflowStrategy.md` for more details about individual topics.

### Response

I can simplify `Workflow.md` substantially, but I couldn't update the downloadable file because the data analysis capability is temporarily unavailable. It should become available again in approximately 23 hours, though that isn't guaranteed.

The intended revision will reduce it to a true 50,000-foot overview:

1. Purpose of AI in software development.
2. Your development environment and activities.
3. General principles for using AI.
4. High-level expectations for validation and developer oversight.
5. Links to `WorkflowStrategy.md` for detailed guidance.

The existing `Workflow.md` remains unchanged. I haven't created or delivered the revised file yet.



























Initial prompt
--------------

When using AI, it's important to me that I'm using the correct and
most effcient model for the task at hand. I don't mind switching
between different models when needed.

Create a document named `Model-Suggestion.md` that suggests
the 5 models I should have in my workflow toolbox.

========
Response
========

Created `Model-Suggestion.md` with a recommended five-model toolbox,
organized around distinct roles:

| Model             | Primary role                                                 |
| ----------------- | ------------------------------------------------------------ |
| GPT-5.3-Codex     | Multi-file coding and repository-level changes               |
| Claude Sonnet 5.5 | Everyday C# development, refactoring, and documentation      |
| Claude Opus 5.5   | Complex reasoning, difficult debugging, and critical reviews |
| Claude Haiku 5.5  | Fast, lightweight tasks                                      |
| Kimi K3           | Independent second opinions and alternative approaches       |

The document also includes a task-to-model recommendation table, a
practical switching strategy, .NET-specific guidance, and criteria
for evaluating whether each model earns its place in your workflow.

Download Model-Suggestion.md

The central recommendation is to use Sonnet as your everyday default,
switch to Codex for repository-heavy coding, and reserve Opus for the
problems that genuinely need deeper reasoning.