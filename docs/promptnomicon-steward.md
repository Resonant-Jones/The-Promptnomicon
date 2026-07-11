# Promptnomicon Steward

The Promptnomicon Steward turns this methodology into a repo-local agent a developer can talk to.

It is designed for projects where the hard part is no longer inventing ideas, but keeping work bounded, reviewable, validated, and aligned with reality.

## What It Is

A lightweight process companion for AI-assisted development.

It helps teams:

- define smallest coherent tasks
- separate planning from execution
- classify claims by proof surface
- generate receipts
- add project reality footers to dev logs and changelogs
- detect documentation drift
- identify bottlenecks without blaming people

## What It Is Not

The Steward is not a replacement for engineering judgment.

It is not a magic project manager.

It should not become another reporting burden.

Its purpose is to reduce coordination load by making the current project state easier to see.

## Install Into Another Repo

Copy these files into the target repository:

```text
agents/promptnomicon-steward.md
templates/promptnomicon-steward-session.md
templates/promptnomicon-steward-invocation.md
templates/project-reality-footer.md
```

Recommended target layout:

```text
.promptnomicon/
  promptnomicon-steward.md
  promptnomicon-steward-session.md
  promptnomicon-steward-invocation.md
  project-reality-footer.md
```

Then open the target repo in a repo-aware assistant.

## Invoke the Steward

Recommended first invocation:

```text
Invoke the Promptnomicon Steward.

Read .promptnomicon/promptnomicon-steward.md,
.promptnomicon/promptnomicon-steward-session.md,
and .promptnomicon/promptnomicon-steward-invocation.md.

Begin the project interview.
Do not modify implementation files.
Do not recommend a coding task until the interview distinguishes current reality from aspiration.
After the interview, create or update docs/promptnomicon/project-reality.md only with my approval.
```

A compatible short form is:

```text
Invoke the Promptnomicon Steward and begin the project interview.
```

## What Happens on First Invocation

The Steward begins in read-only mode and asks one focused question at a time. The interview establishes:

1. the project's ultimate goal
2. who it is for and what problem it solves
3. what is already implemented or directly observed
4. what remains planned, experimental, or aspirational
5. the next meaningful milestone
6. protected boundaries that require explicit approval
7. the proof surfaces that count as completion
8. operating constraints such as platform, budget, compatibility, privacy, or deployment limits

The interview contract lives in `templates/promptnomicon-steward-invocation.md`.

## Project Reality Artifact

After the interview, the Steward proposes a durable project-reality record at:

```text
docs/promptnomicon/project-reality.md
```

The artifact separates implemented behavior, test evidence, runtime proof, plans, constraints, protected boundaries, uncertainty, and the smallest coherent next task.

The Steward must request explicit approval before writing or replacing this file.

## Returning Sessions

When `docs/promptnomicon/project-reality.md` already exists, use the normal session template:

```text
Use .promptnomicon/promptnomicon-steward-session.md as your operating instructions for this session. Do not modify files yet. Compare the repository against the existing project-reality record, report any drift, and give me the smallest coherent next task.
```

## Best Use Cases

- before starting a coding session
- after a large roadmap or architecture dump
- before beta/release planning
- after an agent modifies files
- when one person is becoming the bottleneck
- when docs, tests, and implementation may be drifting

## Design Principle

The Steward is a rail to grab onto.

It should make the repo feel less scattered, not make the developer feel managed by a haunted clipboard.
