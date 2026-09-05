# Agent work guide

This repository welcomes coding-agent assistance within human-reviewed GitHub work. It does not yet contain an implemented product, so an agent must not invent a stack, source path, command, remote action, or completion claim.

## Minimum task brief

A maintainer-approved GitHub issue should provide:

- **Objective:** the observable result to produce.
- **Scope:** files or modules the task may change once they exist.
- **Dependencies:** earlier roadmap tasks or decisions that must already be complete.
- **Acceptance criteria:** concrete behavior and evidence required.
- **Validation:** exact commands or manual checks appropriate to the chosen stack.
- **Boundaries:** prohibited paths, external actions, data, and credentials.
- **Expected result:** patch, documentation, test evidence, or another reviewable artifact.

If a required field is unknown, the agent should surface the gap and continue only with work that does not depend on it.

## Agent workflow

1. Read [AGENTS.md](AGENTS.md), the linked issue, and only the roadmap context needed for the task.
2. Confirm the task's dependencies and current repository state from source.
3. Make the smallest coherent change that satisfies the approved scope.
4. Run the agreed validation. Fix relevant failures before reporting.
5. Return a concise summary of changed files, checks run, results, limitations, and follow-up work.
6. Leave commit, push, pull-request creation, merge, release, publication, credentials, and other external changes to the authorized human unless the task explicitly grants that exact action.

## Evidence language

Use precise states: **planned**, **implemented**, **checked locally**, **reviewed**, **merged**, and **released** mean different things. A generated file is not a passing build. A local passing test is not a merged contribution. A merged contribution is not a release.

## Pull-request handoff template

```markdown
## What changed

## Why

## Validation
- [ ] Command or check — result

## Agent assistance
- Tool or agent used:
- Human verification performed:

## Known limitations
```
