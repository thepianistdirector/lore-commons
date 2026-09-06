# Contributing to Lore Commons

Lore Commons is at the planning stage. Contributions are welcome, but the first useful work is to turn the expanded Tanduna plan into approved, bounded task revisions and linked GitHub issues. Do not infer a technology stack, command, file path, or completed feature from the plan.

## Contribution flow

1. Read the [current Tanduna plan](https://tanduna.com/projects/lore-commons/roadmap), check task approval and dependencies, and read the [required contribution skill](skills/lore-commons-contribution/SKILL.md). [ROADMAP.md](ROADMAP.md) preserves the historical outline.
2. Open or join a GitHub issue. State the problem, proposed scope, acceptance criteria, and any unresolved product decision.
3. Wait for a maintainer to confirm the implementation approach and validation before writing a substantial change.
4. Create a focused branch and keep unrelated work out of the pull request.
5. Run the agreed checks and record the exact results.
6. Open a pull request that links the issue, explains the behavior changed, lists validation evidence, and names known limitations.
7. A human maintainer reviews, requests changes, or accepts the contribution. Nothing merges automatically.

## Working with coding agents

Coding agents may help with design, implementation, tests, documentation, and review. The human contributor remains responsible for the scope and the submitted result. Use [AGENT-WORK.md](AGENT-WORK.md) to give an agent a bounded task.

In the pull request, distinguish what the agent generated from what you personally verified. Report commands that actually ran and outcomes actually observed. Never claim a test, build, review, release, or remote GitHub action that did not occur. Do not include credentials, local machine paths, private prompts, or unrelated repository data.

## Quality expectations

- Satisfy the issue's acceptance criteria with the smallest coherent change.
- Add focused validation for behavior that can fail.
- Preserve portable project data and explicit failure states.
- Update documentation when user-visible behavior or a stable contract changes.
- Keep accessibility and keyboard use in scope for user-facing work.
- Do not add a production dependency without a maintainer-approved reason and review of its maintenance, license, and runtime impact.

## Licensing contributions

By submitting a contribution, you agree that it may be distributed under `AGPL-3.0-only`, the repository license. Do not submit third-party code or assets unless their provenance and license are documented and compatible with this repository.
