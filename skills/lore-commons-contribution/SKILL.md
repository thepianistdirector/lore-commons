---
name: lore-commons-contribution
description: Implement or review Lore Commons contributions involving local sources, citations, notes, search, workspace portability, recovery, or optional suggestion boundaries.
---

# Lore Commons contribution

Build research tooling whose claims can be reopened against the exact local evidence that produced them. Apply this skill to Lore Commons implementation, review, migration, documentation, and release-validation tasks.

## Start from the task revision

Treat the current task revision and repository source as authority. Before editing, inspect the repository root, branch, HEAD, status, relevant instructions, and active writers. Read the task's goal, dependencies, acceptance criteria, repository/base binding, allowed and prohibited paths, commands, network policy, secret scope, execution permissions, and model requirement. Do not substitute a global model choice or expand permissions. If a required binding, dependency, fixture, or command is absent, report that exact gap instead of inventing an executable scope.

Preserve existing work. Change only task-owned paths. Do not install dependencies, use network or credentials, commit, push, publish, sign, or deploy unless the task revision and current user authority explicitly permit that action.

## Preserve the evidence contract

- Keep logical source identity separate from immutable source-version identity. Preserve original imported bytes and extraction provenance. Re-importing changed bytes creates a new version; it never rewrites the version cited by existing notes.
- Bind every citation to one source version and a typed supported anchor: PDF page and optional text range, or Markdown heading occurrence and text span. Reopening shows the cited location with bounded adjacent context. Missing, changed, corrupt, partially extracted, or unresolvable evidence must remain visibly unhealthy; never fuzzy-match or silently retarget it.
- User-authored Markdown notes are authority. Stable note IDs survive rename. Links and citation tokens are explicit authored records. Suggestions, health checks, imports, and migrations cannot silently edit prose or claim that a source proves a note.
- Treat search indexes, snippets, backlinks, and cached extraction views as derived projections. Make them disposable and rebuildable from authoritative sources, versions, notes, links, and citations. Search relevance is not evidence strength.
- Keep the useful path local. Imported content, notes, paths, and diagnostics must not be uploaded, fetched, logged, or sent to a model without a separate explicit user action and task authority. Remote content embedded in documents stays inert. Optional AI output is a labeled proposal requiring user review; it cannot write workspace state or manufacture citations.

## Implement recoverably

Use bounded parsing, validated paths, explicit cancellation, and transactional state changes. Unsupported, encrypted, scanned-only, malformed, oversized, interrupted, and disk-full cases must not appear complete. Clean only operation-owned staging data.

For schema, extraction, note-token, or bundle changes, define version compatibility before mutation. Preserve a recoverable pre-migration state, validate before activation, and leave the original untouched on failure. Test fresh, populated, corrupt, interrupted, and newer-than-supported cases where relevant. Portable exports use stable IDs and relative internal paths, distinguish embedded-source from metadata-only records, rebuild derived data after reopen, and do not imply redistribution rights.

## Prove the task's behavior

Run the task's required commands after implementing the smallest coherent slice. Add tests for failure-prone invariants, not wording or implementation shape. A citation change normally needs first/middle/final anchors, changed and missing versions, and keyboard reopen. Persistence work needs close/reopen plus injected interruption. Search work needs source/note origin labels, stale-index rejection, and rebuild equivalence. User-facing work needs rendered primary and failure flows, keyboard/focus behavior, narrow layout, accessibility checks, and console/network inspection as applicable.

For a consequential invariant change, check that a representative defect makes its test fail, then restore the intended implementation. Report exact files, checks, observed runtime behavior, failures, and untested boundaries.

Use evidence-level language: proposed, implemented, automated pass, runtime observed, user validated, or release verified. A prototype, fixture, green unit test, screenshot, or local package proves only its own level. Never upgrade that evidence into claims of complete, secure, accessible, portable, or releasable behavior.
