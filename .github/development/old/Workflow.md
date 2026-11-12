# AI-Assisted Software Engineering Workflow

## Purpose

Use AI as a practical engineering assistant to improve software quality,
maintainability, documentation, and development efficiency. AI supports
engineering work; it does not replace developer judgment, ownership,
review, or validation.

For the complete principles, procedures, and expectations, see
**[WorkflowStrategy.md](WorkflowStrategy.md)**.

## Development Context

-   **Language:** C#
-   **Target frameworks:** .NET 10 and .NET Framework 4.8
-   **Engineering practices:** Incremental development, continuous
    refactoring, and technical-debt reduction
-   **Documentation:** XML documentation, technical references, and
    software manuals
-   **Additional activities:** Rapid prototyping, experimentation, and
    repository maintenance

Always confirm the project's target framework, language version,
dependencies, and conventions before recommending or changing code. Do
not assume modern .NET APIs are available in .NET Framework 4.8.

## Core Expectations

1.  **Developer ownership:** The developer makes final decisions and is
    responsible for the resulting software.
2.  **Correctness first:** Prefer reliable, understandable solutions
    over speed or unnecessary complexity.
3.  **Understand before changing:** Inspect relevant code, tests,
    project structure, and conventions before making substantial
    changes.
4.  **Keep changes focused:** Make small, coherent, reviewable changes
    and avoid unrelated cleanup.
5.  **Respect the codebase:** Follow established architecture and
    conventions unless there is a clear reason to change them.
6.  **Maintain quality continuously:** Consider tests, documentation,
    maintainability, and repository hygiene part of normal development.
7.  **Be transparent:** Distinguish verified facts from assumptions,
    explain risks, and never claim checks were performed when they were
    not.

## AI's Role in the Development Lifecycle

  -----------------------------------------------------------------------
  Activity                            How AI should help
  ----------------------------------- -----------------------------------
  Understanding                       Explain code, trace dependencies,
                                      and summarize existing behavior

  Planning                            Clarify requirements, identify edge
                                      cases, and propose implementation
                                      steps

  Implementation                      Produce focused code, tests,
                                      scripts, and configuration changes

  Validation                          Suggest tests, analyze failures,
                                      and review diagnostics

  Refactoring                         Identify duplication, complexity,
                                      code smells, and technical debt

  Documentation                       Draft and maintain XML comments,
                                      technical documents, manuals, and
                                      diagrams

  Repository maintenance              Review organization, consistency,
                                      obsolete files, and unnecessary
                                      artifacts

  Experimentation                     Explore ideas and create small
                                      proofs of concept
  -----------------------------------------------------------------------

Use AI where it provides meaningful value; it does not need to
participate in every routine task.

## Model Selection

Select models according to task requirements rather than relying on one
model for everything.

-   Use fast, capable coding models for small, well-defined changes.
-   Prefer strong reasoning and code comprehension for complex
    debugging, architecture, and refactoring.
-   Prefer clear technical writing and factual discipline for
    documentation.
-   Use models with suitable context and agentic capabilities for
    repository-wide, multi-step work.
-   Consider an independent second-model review for important or
    uncertain changes.

Account for capability, context, latency, cost, privacy, and available
tools. Model agreement is not proof of correctness.

## Code Changes and Refactoring

Before changing code, inspect the relevant solution, projects, source
files, tests, configuration, and documentation. Establish the scope and
identify framework-specific constraints.

During implementation:

-   Make the smallest coherent change that satisfies the requirement.
-   Preserve existing behavior and compatibility unless a change is
    requested.
-   Avoid unnecessary abstractions, dependencies, and broad rewrites.
-   Add or update tests when behavior changes or defects are fixed.
-   Keep secrets and sensitive values out of prompts, source code, and
    generated artifacts.

Refactor incrementally and intentionally. Explain the problem, expected
benefit, scope, and risk of proposed improvements. Prefer
behavior-preserving refactoring, with appropriate tests before and after
the change.

## Testing and Verification

Treat AI-generated code as unverified until reviewed and tested. Run
relevant builds, targeted tests, broader test suites, analyzers,
formatting checks, and compatibility checks as appropriate.

Clearly report:

-   Which checks were actually performed and their results.
-   Which checks were not performed.
-   Known limitations, risks, and assumptions.

Never imply that code compiles, runs, or passes tests without evidence.

## Documentation and Repository Hygiene

Keep documentation consistent with the actual implementation. Update
relevant XML comments, technical documentation, manuals, setup
instructions, and diagrams when changes affect them.

Keep repositories clear and maintainable. Before moving, renaming, or
deleting files, check project references, build scripts, CI workflows,
packaging, and tooling. Avoid committing temporary experiments, build
output, or generated files unless required by the repository.

## Experimental Development

Use AI to explore ideas quickly through small, clearly scoped
prototypes. Label shortcuts, mocks, assumptions, and limitations. Keep
experiments separate from production code where practical.

Before promoting a prototype, review its design, security, error
handling, performance, tests, dependencies, maintainability, and
documentation. A successful demonstration is not automatically
production-ready.

## Security and Approval

Use only data permitted by the selected AI service and its data-handling
terms. Minimize shared context and redact credentials, tokens, private
keys, personal information, and other sensitive data as appropriate.

Apply careful human review to security-sensitive code. Obtain explicit
developer approval before high-impact or irreversible actions, including
destructive file changes, production modifications, publishing packages,
or changing access controls.

## Communication and Completion

For non-trivial work, AI should communicate:

1.  **Understanding:** The requested outcome and relevant constraints.
2.  **Approach:** The plan, when the task has meaningful complexity.
3.  **Changes:** Files changed and important decisions.
4.  **Validation:** Checks performed and their results.
5.  **Remaining work:** Risks, assumptions, limitations, and checks
    still needed.

Before accepting work, confirm that the scope is met, changes are
focused, framework constraints are respected, relevant validation is
complete or disclosed, affected documentation is updated, and the
developer has reviewed the result.

## Further Guidance

This file is a concise workflow reference.
**[WorkflowStrategy.md](WorkflowStrategy.md)** is the authoritative,
detailed guide and should be consulted whenever additional context,
procedures, or clarification is needed.

Supporting documents may define more specific requirements for model
selection, C# development, code review, documentation, repository
organization, and AI agent behavior. Follow those specialized standards
when they apply.
