# Model Suggestions

**Purpose:** A compact five-model toolbox for C# software engineering,
refactoring, technical documentation, repository maintenance, and
experimentation.

The goal is not to use the most powerful model for every prompt. Use a
fast or well-balanced model for routine work, reserve the most capable
model for difficult decisions, and bring in a different model when an
independent perspective is valuable.

## Recommended five-model toolbox

  --------------------------------------------------------------------------
  Model               Role in the       Use it for        Why keep it
                      toolbox                             
  ------------------- ----------------- ----------------- ------------------
  **GPT-5.3-Codex**   Coding and        Multi-file        A coding-oriented
                      repository agent  implementation,   choice for
                                        debugging, test   structured,
                                        creation,         repository-level
                                        repository-wide   engineering work
                                        refactoring, and  
                                        changes that      
                                        require           
                                        inspecting and    
                                        editing a         
                                        codebase          

  **Claude Sonnet     Everyday          Normal C#         The best single
  5.5**               workhorse         development,      all-rounder in
                                        focused           this shortlist;
                                        refactoring, code broad enough to
                                        review, XML       handle most daily
                                        documentation,    tasks without
                                        manuals, and      routinely
                                        technical         escalating to a
                                        explanations      premium model

  **Claude Opus 5.5** Deep reasoning    Difficult bugs,   Keep it available
                      and critical      architectural     for problems where
                      review            trade-offs,       an extra level of
                                        complex           analysis may
                                        refactoring,      prevent expensive
                                        root-cause        mistakes
                                        analysis, and     
                                        review of         
                                        high-risk changes 

  **Claude Haiku      Fast, lightweight Simple code       Avoids spending
  5.5**               assistant         questions, small  time and resources
                                        methods,          on a heavyweight
                                        straightforward   model when the
                                        edits, summaries, task is simple
                                        basic test        
                                        scaffolding, and  
                                        routine           
                                        documentation     
                                        changes           

  **Kimi K3**         Independent       Reviewing another Adds a different
                      second opinion    model's proposed  model family and
                                        design or         can expose blind
                                        implementation,   spots that may be
                                        exploring         missed when asking
                                        alternatives, and the same model to
                                        challenging       review its own
                                        assumptions       work
  --------------------------------------------------------------------------

## Which model should I use?

  -----------------------------------------------------------------------
  Task                    Start with              Escalate or cross-check
                                                  when
  ----------------------- ----------------------- -----------------------
  Implement a feature     **GPT-5.3-Codex**       Use **Claude Opus 5.5**
  across several files                            if the design or
                                                  debugging problem
                                                  becomes unusually
                                                  difficult

  Everyday C#             **Claude Sonnet 5.5**   Use **GPT-5.3-Codex**
  implementation                                  when repository
                                                  inspection and
                                                  coordinated file
                                                  changes are central

  Refactor code and       **Claude Sonnet 5.5**   Ask **Claude Opus 5.5**
  reduce technical debt                           to assess broad, risky,
                                                  or behavior-sensitive
                                                  refactoring

  Debug a difficult or    **Claude Opus 5.5**     Ask **Kimi K3** for an
  intermittent issue                              independent diagnosis
                                                  if the cause is unclear

  Review architecture or  **Claude Opus 5.5**     Use **Kimi K3** as a
  a high-impact change                            separate reviewer
                                                  rather than asking Opus
                                                  to review itself

  Write XML               **Claude Sonnet 5.5**   Use **Claude Haiku
  documentation, manuals,                         5.5** for small,
  and technical                                   routine documentation
  explanations                                    edits

  Make a small code       **Claude Haiku 5.5**    Move to **Claude Sonnet
  change or get a quick                           5.5** if the task
  explanation                                     requires broader
                                                  context or more
                                                  reasoning

  Explore an alternative  **Kimi K3**             Compare its proposal
  design                                          with **Claude Sonnet
                                                  5.5** or **Claude Opus
                                                  5.5** before adopting
                                                  it

  Clean up or reorganize  **GPT-5.3-Codex**       Have **Claude Sonnet
  a repository                                    5.5** review the plan
                                                  and resulting changes
  -----------------------------------------------------------------------

## A practical switching strategy

1.  **Default to Claude Sonnet 5.5** for ordinary development,
    refactoring, and documentation.
2.  **Use Claude Haiku 5.5** when the task is small, clear, and low
    risk.
3.  **Switch to GPT-5.3-Codex** when the work is primarily
    repository-aware coding: inspecting files, changing multiple files,
    implementing features, or coordinating tests.
4.  **Escalate to Claude Opus 5.5** when the problem is difficult, the
    change is high risk, or the cost of a wrong answer is significant.
5.  **Use Kimi K3** when you want a genuinely separate perspective on a
    design, diagnosis, or proposed change.

You do not need to run every task through multiple models. A second
opinion is most valuable for architectural decisions, subtle bugs,
public API changes, security-sensitive code, and large refactors.

## Important .NET instructions

For every coding task, explicitly identify the target framework:

-   **.NET 10**
-   **.NET Framework 4.8**

Do not let the model assume that APIs, runtime behavior, language
features, or library versions are interchangeable between these targets.
Ask it to identify compatibility assumptions and avoid APIs unavailable
to the target framework.

For repository-level work, ask the model to:

-   Inspect existing patterns and project structure before proposing
    changes.
-   Keep changes focused and avoid unnecessary abstractions.
-   Preserve existing behavior and public APIs unless a breaking change
    is requested.
-   Add or update tests where appropriate.
-   Run, or clearly specify, the relevant build and test commands.
-   Summarize changed files, assumptions, risks, and anything it could
    not verify.

## How to validate the shortlist

Treat this as a practical starting lineup, not a permanent ranking.
Model names and versions alone do not establish guaranteed performance,
speed, cost, or tool reliability. In particular, verify the capabilities
and pricing shown by the provider or model-hosting application.

Try the five models on a small set of representative tasks from your own
repositories. Compare:

  -----------------------------------------------------------------------
  Evaluation area                     What to look for
  ----------------------------------- -----------------------------------
  Correctness                         Does the code compile and meet the
                                      requirements?

  .NET compatibility                  Does it respect the specified
                                      target framework?

  Repository awareness                Does it follow existing
                                      architecture and conventions?

  Refactoring quality                 Does it improve maintainability
                                      without introducing needless
                                      complexity?

  Documentation quality               Is the documentation accurate and
                                      consistent with the implementation?

  Tool reliability                    Does it inspect and modify the
                                      intended files, and accurately
                                      report what it did?

  Efficiency                          Is the quality worth the response
                                      time and usage cost?
  -----------------------------------------------------------------------

If one model consistently performs poorly or duplicates another model's
role, replace it. The best toolbox is the smallest set that reliably
covers your actual work.
