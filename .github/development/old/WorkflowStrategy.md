# AI-Assisted Software Engineering Workflow

## 1. Purpose

This document defines how AI should be incorporated into the software
engineering workflow. AI is a practical engineering assistant for
improving quality, reducing repetitive work, accelerating exploration,
and keeping software and its documentation maintainable.

AI must support sound engineering decisions---not replace engineering
judgment, code ownership, testing, or review.

## 2. Engineering Context

Use the following context when making recommendations or producing work:

  -----------------------------------------------------------------------
  Area                                Environment / expectation
  ----------------------------------- -----------------------------------
  Primary language                    C#

  Modern target                       .NET 10

  Legacy target                       .NET Framework 4.8

  Development practices               Incremental development, continuous
                                      refactoring, and technical-debt
                                      reduction

  Documentation                       Technical documentation, XML
                                      documentation, and user/developer
                                      manuals

  Experimentation                     Occasional rapid prototypes and
                                      exploratory "vibe-coding"

  Repository quality                  Clear structure, consistent
                                      conventions, maintainable history,
                                      and minimal clutter
  -----------------------------------------------------------------------

Always establish which target framework, language version, runtime, and
project type apply before recommending APIs or implementation details.
Do not assume that an API available in modern .NET is available in .NET
Framework 4.8.

## 3. Core Principles

1.  **Human ownership:** The developer remains responsible for
    requirements, architecture, implementation decisions, security, and
    shipped changes.
2.  **Correctness before speed:** Prefer a correct, tested,
    understandable solution over the shortest or fastest generated
    answer.
3.  **Understand before changing:** Inspect relevant code, project
    structure, dependencies, conventions, and tests before proposing
    substantial changes.
4.  **Small, reviewable changes:** Prefer focused changes that are easy
    to understand, validate, and revert.
5.  **Respect existing design:** Follow established architecture and
    conventions unless there is a clear, explained reason to change
    them.
6.  **Continuous quality:** Treat maintainability, tests, documentation,
    and repository hygiene as part of normal development---not cleanup
    tasks for later.
7.  **Evidence over assumptions:** Clearly distinguish facts established
    from the repository from assumptions, hypotheses, and
    recommendations.
8.  **No fabricated completion:** Never claim code was built, tested,
    executed, or verified unless that action actually occurred.

## 4. Where AI Fits in the Development Lifecycle

AI can assist at every stage, with the developer retaining
decision-making authority.

  -----------------------------------------------------------------------
  Stage                   Appropriate AI          Expected developer
                          assistance              responsibility
  ----------------------- ----------------------- -----------------------
  Understand              Explain unfamiliar      Confirm the explanation
                          code, trace call paths, against the actual
                          summarize dependencies, system
                          identify relevant files 

  Plan                    Clarify requirements,   Approve scope,
                          identify edge cases,    constraints, and design
                          propose designs, break  
                          work into steps         

  Implement               Write or modify focused Review changes and
                          code, tests, scripts,   ensure they meet
                          and configuration       requirements

  Validate                Suggest tests, analyze  Run and evaluate the
                          failures, inspect       relevant checks
                          diagnostics, identify   
                          likely regressions      

  Refactor                Identify duplication,   Decide which changes
                          complexity, code        are worthwhile and
                          smells, and safer       preserve behavior
                          improvement             
                          opportunities           

  Document                Draft or update XML     Verify accuracy,
                          comments, technical     completeness, and
                          references, manuals,    audience suitability
                          and diagrams            

  Maintain                Review repository       Approve removals,
                          organization, stale     upgrades, and
                          files, dependencies,    structural changes
                          and consistency         

  Explore                 Prototype ideas,        Decide whether and how
                          compare approaches, and successful experiments
                          build disposable        become production code
                          experiments             
  -----------------------------------------------------------------------

AI should be involved when it offers a meaningful advantage. It need not
be used for every keystroke or routine change.

## 5. Task and Model Selection

Choose a model based on the task rather than defaulting to a single
model for all work.

  -----------------------------------------------------------------------
  Task characteristics                Preferred model qualities
  ----------------------------------- -----------------------------------
  Small, well-defined code changes    Strong coding ability, reliable
                                      instruction following, low latency

  Complex debugging or architecture   Strong reasoning, large-context
                                      comprehension, careful analysis

  Refactoring and code review         Strong code comprehension,
                                      consistency, and ability to explain
                                      trade-offs

  Documentation and manuals           Clear technical writing, factual
                                      discipline, and ability to follow a
                                      specified structure

  Repository-wide work                Strong long-context or agentic
                                      capabilities, tool use, and
                                      disciplined multi-step execution

  Rapid experimentation               Fast iteration, practical coding
                                      ability, and low friction

  High-impact or uncertain changes    Strong reasoning and verification;
                                      consider an independent
                                      second-model review
  -----------------------------------------------------------------------

Model choice should account for capability, context requirements,
latency, cost, privacy, and the tools available in the current
environment. Reassess model recommendations as models and capabilities
change. Do not infer capability solely from a model's name or vendor.

For important work, a second model can provide an independent review,
but agreement between models is not proof of correctness.

## 6. Working with Code and Repositories

Before modifying a repository, AI should:

-   Inspect the relevant solution, projects, source files, tests,
    configuration, and documentation.
-   Identify target frameworks and relevant compatibility constraints.
-   Locate and follow existing naming, formatting, architecture, and
    dependency conventions.
-   Determine the intended scope and avoid unrelated cleanup.
-   Ask for clarification when a missing requirement materially affects
    the implementation.

During implementation, AI should:

-   Make the smallest coherent change that satisfies the requirement.
-   Avoid unnecessary abstractions, dependencies, configuration, and
    generated files.
-   Preserve public behavior and compatibility unless a change is
    explicitly requested.
-   Avoid broad rewrites when a focused change is sufficient.
-   Add or update tests when behavior changes or a defect is fixed.
-   Keep secrets, credentials, tokens, and other sensitive values out of
    source code and generated artifacts.

After implementation, AI should summarize the files changed, explain
important decisions, identify risks, and state exactly which validation
steps were performed and which remain outstanding.

## 7. Refactoring and Technical Debt

Refactoring should be continuous, intentional, and behavior-preserving
unless behavior changes are part of the task.

AI should help identify:

-   Duplication and unnecessary complexity.
-   Poor separation of responsibilities or unclear abstractions.
-   Fragile error handling and edge cases.
-   Inconsistent naming, formatting, and project conventions.
-   Unnecessary dependencies or obsolete code.
-   Missing or ineffective tests.
-   Documentation that no longer matches the implementation.

For each proposed improvement, explain the problem, expected benefit,
scope, and potential risk. Prioritize changes by impact and risk; do not
refactor merely to satisfy stylistic preference.

Keep feature work and unrelated refactoring separate where practical.
Establish or run appropriate tests before and after a
behavior-preserving refactor. If behavior cannot be adequately verified,
state that limitation.

## 8. Testing and Verification

AI-generated code is a proposal until it has been reviewed and
validated.

Use the most relevant available checks, such as:

1.  Build the affected project or solution.
2.  Run targeted unit and integration tests.
3.  Run the broader test suite when the scope or risk warrants it.
4.  Check formatting, analyzers, and static-analysis results where
    configured.
5.  Review compatibility with the actual target framework and supported
    environments.
6.  Inspect the final diff for unintended changes.

AI must not invent test results or imply that generated code compiles.
If it cannot execute a check, it should provide the command or procedure
and mark the check as not run.

For .NET Framework 4.8 projects, verify framework-specific API
availability and toolchain requirements rather than assuming modern .NET
behavior.

## 9. Documentation

Treat documentation as a maintained part of the software.

AI may draft and update:

-   C# XML documentation comments.
-   Architecture and design explanations.
-   Developer setup and build instructions.
-   Technical references and operational procedures.
-   User manuals and troubleshooting guides.
-   Mermaid diagrams and other text-based technical diagrams.

Documentation must be based on verified implementation and agreed
requirements. It should be clear, structured, appropriately detailed for
its audience, and consistent with the repository's existing
documentation style.

When code changes affect documented behavior, configuration, setup, or
interfaces, identify the relevant documentation and update it as part of
the work. Do not add comments that merely restate obvious code or claim
behavior that the implementation does not guarantee.

## 10. Repository Organization and Hygiene

AI should help keep repositories understandable and free of unnecessary
clutter.

Appropriate tasks include reviewing directory structure, identifying
misplaced or duplicate files, checking naming consistency, spotting
obsolete documentation or artifacts, and suggesting improvements to
project and solution organization.

Do not delete, move, rename, or restructure files based only on
assumptions. First determine whether files are referenced by projects,
build scripts, CI workflows, packaging, tooling, or external processes.
Explain potentially disruptive changes and obtain developer approval
before applying them.

Generated output, temporary experiments, local settings, and build
artifacts should remain in appropriate locations and should not be
committed unless the repository explicitly requires them.

## 11. Experimental Development and Vibe-Coding

Use AI to make low-cost exploration easier, while keeping experiments
separate from production engineering.

For experiments:

-   State the question or idea being explored.
-   Prefer a small proof of concept over premature architecture.
-   Clearly label shortcuts, mocks, assumptions, and known limitations.
-   Avoid introducing production dependencies or changing stable code
    unnecessarily.
-   Do not put secrets or real sensitive data into experimental prompts,
    code, or services.
-   Record useful findings and the next steps if the experiment has
    value.

Before promoting an experiment into the main codebase, review its
architecture, error handling, security, performance, tests,
dependencies, maintainability, and documentation. Rewrite or refactor
prototype code as needed; a successful demonstration is not
automatically production-ready.

## 12. Security, Privacy, and Sensitive Changes

Only provide AI systems with code and data that are permitted for the
selected service and its configured data-handling terms. Minimize shared
context and redact credentials, tokens, private keys, personal
information, and proprietary data when appropriate.

AI-generated security-sensitive code---including authentication,
authorization, cryptography, deserialization, input validation, and data
access---requires careful human review and suitable testing. Do not
accept a security claim without evidence.

Require explicit developer approval before high-impact actions such as
deleting data, changing access controls, modifying production systems,
publishing packages, or making irreversible repository changes.

## 13. Communication and Deliverables

AI responses should be practical, direct, and specific. For non-trivial
work, provide:

-   **Understanding:** A concise statement of the requested outcome and
    constraints.
-   **Approach:** The proposed plan when the work has meaningful
    complexity.
-   **Changes:** What was changed and why.
-   **Validation:** Checks actually performed, with results.
-   **Remaining work:** Known limitations, risks, assumptions, and
    checks not performed.

Ask focused clarification questions when proceeding would otherwise
require a consequential guess. For low-risk ambiguity, state a
reasonable assumption and continue.

Prefer actionable recommendations over generic best-practice lists.
Explain trade-offs when more than one reasonable approach exists.

## 14. Definition of Done

AI-assisted work is ready for developer acceptance when the applicable
conditions below are satisfied:

-   [ ] The requested outcome and scope are addressed.
-   [ ] The implementation follows repository conventions and
    target-framework constraints.
-   [ ] Changes are focused and contain no unexplained unrelated
    modifications.
-   [ ] Relevant tests and validation checks have been run, or
    unperformed checks are clearly identified.
-   [ ] Documentation has been updated when affected.
-   [ ] No secrets, unintended generated files, or unnecessary
    dependencies were introduced.
-   [ ] Risks, assumptions, and known limitations are disclosed.
-   [ ] The developer has reviewed and accepted the result.

## 15. Continuous Improvement

Treat this workflow as a living standard. Refine it as development
needs, repositories, tools, and AI models evolve. Capture recurring
failures and successful practices, then incorporate useful lessons into
shared project instructions and supporting standards.

The objective is not to maximize AI usage. It is to use AI deliberately
to produce software that is more reliable, maintainable, understandable,
and efficiently developed.
