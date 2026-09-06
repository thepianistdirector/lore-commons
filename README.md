# Lore Commons

> Turn documents into connected notes whose citations always reopen the exact source.

**Status:** Planning repository. No application has been implemented yet. There are no releases, usage claims, funding claims, or completed roadmap items.

Lore Commons is an open research and knowledge workbench for people who want their notes to remain accountable to the documents behind them. It combines portable local workspaces, source-linked writing, and local search; later, contributors can add optional user-chosen model adapters that suggest connections or drafts without replacing citations, changing notes silently, or making the core workflow depend on a provider.

[Project on Tanduna](https://tanduna.com/projects/lore-commons) · [Current roadmap and publication status](https://tanduna.com/projects/lore-commons/roadmap)

![AI-generated concept reference for Lore Commons](https://tanduna.com/project-references/lore-commons-concept.png)

*AI-generated reference for what we want to build. This is not a screenshot of working software.*

## Why build this

We want notes to remain useful when a source changes, a workspace moves or a model provider disappears. A citation should reopen the source version and location it actually refers to. This is a product hypothesis to test with real research workflows; we are not claiming existing users or validated demand.

## First useful result

Create a local workspace, import lawful PDF and Markdown samples, write a note, attach a citation, reopen its supported source context, find it through local search, then export and reopen the workspace without silently changing what the citation means.

## Proposed technical starting point

Use a Tauri 2 desktop shell with a React/TypeScript/Vite interface and a Rust workspace for domain rules, imports, storage, search, and bundles. Persist each workspace in a user-selected directory containing an application-managed SQLite database, immutable imported source-version blobs, and versioned metadata; use SQLite transactions and FTS5 for local indexing. Render and extract supported PDFs with a pinned PDF.js build in the webview while Rust owns file ingestion, identifiers, validation, and durable anchor records. Parse Markdown into a normalized structural representation with byte/line ranges. Keep source identity distinct from source-version identity; citations bind to one immutable version plus a typed page, heading, or text-span anchor and never retarget silently. Store Markdown notes with stable IDs and derive backlinks/search indexes so they can be rebuilt. Export a versioned, validated workspace bundle without implying redistribution rights. Ship the first useful release with no account, server, telemetry, model, or network requirement. Optional AI suggestions are a later extension behind an explicit user action and review boundary; they may propose content but cannot mutate notes, create evidence claims, or replace citation health.

Wave 1 must ratify the architecture, exact versions, supported platforms, licenses and verification commands. No product dependencies are installed in this repository yet.

## Expanded development plan

The new plan contains **10 waves and 36 tasks**. It is undergoing Tanduna's written-plan review and maintainer approval, including explicit repository/base bindings, model choices, tests and downloadable skills. It is not an implementation or release claim.

| Wave | Outcome area | Tasks |
| --- | --- | --- |
| 1 | Ground truth and buildable skeleton | 4 |
| 2 | Durable local workspace | 4 |
| 3 | Sources that stay findable | 4 |
| 4 | Citations that reopen evidence | 4 |
| 5 | Notes that remain grounded | 4 |
| 6 | Local discovery | 4 |
| 7 | Knowledge that travels and recovers | 4 |
| 8 | Trustworthy complete workflow | 4 |
| 9 | Releasable first version | 3 |
| 10 | Optional suggestion boundary | 1 |

Start with the foundation. Later work requires its prerequisites to be merged and accepted, and an execution revision pinned to the actual integrated base. A planning snapshot of today's documentation-only commit cannot prove that a future feature is ready to implement.

[ROADMAP.md](ROADMAP.md) preserves the original six-task outline as historical context. Use the expanded Tanduna plan and its current approval status for new work. Earlier rejected or replaced task versions remain history.

## Contribute through a reviewable task

1. Read the current Tanduna task and [CONTRIBUTING.md](CONTRIBUTING.md). Discuss open decisions before implementation. A GitHub issue can link the approved task and record any needed scope clarification.
2. Check its repository, exact base commit or resolved branch, dependencies, preferred model and explicitly allowed fallback, writable paths, required skill version, acceptance criteria and testing steps. Missing or provisional execution fields must be resolved before starting dependent work.
3. Use only a permitted model and effort. Record the actual tool/model evidence available; distinguish a requested model or self-declaration from a runtime-observed model. A result from an unapproved model is not an accepted contribution.
4. Make one bounded change, run the agreed checks and report passed, failed and untested behavior. A zero-test filtered command does not satisfy a testing requirement.
5. Return the work through a GitHub pull request with the task link and evidence. Lucas reviews and merges contributor PRs; choosing a task does not start an agent, merge code or publish a release automatically.

Code, design, documentation, testing and lawful assets can all be useful contributions. Do not invent users, test results, completed features or performance evidence.

## Public contribution skill

Read or download [lore-commons-contribution](skills/lore-commons-contribution/SKILL.md). The complete skill is a single public `SKILL.md` file and does not require private prompts or credentials. Use the commit-pinned download URL recorded in your task; the branch link below shows the latest document and is not an immutable execution binding.

[Download the current skill](https://raw.githubusercontent.com/thepianistdirector/lore-commons/main/skills/lore-commons-contribution/SKILL.md)

The skill explains project-specific invariants and evidence requirements. The task revision remains authoritative for the actual model, base, scope, permissions and checks. See [AGENT-WORK.md](AGENT-WORK.md) and [AGENTS.md](AGENTS.md) for the contribution boundaries.

## License

Repository documentation and future source code are licensed under AGPL-3.0-only. Imported user documents retain their own rights and are not relicensed by this repository.

See [LICENSE](LICENSE) for the full GNU Affero General Public License version 3 text. SPDX identifier: `AGPL-3.0-only`.
