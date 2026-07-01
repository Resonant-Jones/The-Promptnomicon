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
templates/project-reality-footer.md
```

Recommended target layout:

```text
.promptnomicon/
  promptnomicon-steward.md
  promptnomicon-steward-session.md
  project-reality-footer.md
```

Then open the target repo in a repo-aware assistant and start with the session template.

## First Conversation

Ask:

```text
Use .promptnomicon/promptnomicon-steward-session.md as your operating instructions for this session. Do not modify files yet. Give me the current project reality state and the smallest coherent next task.
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