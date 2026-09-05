# Lore Commons roadmap

This is a proposed plan for a project starting from zero. Every item below is unimplemented. The order expresses dependencies, not dates or delivery promises. No token or developer-time estimates are configured.

## Before implementation

- Confirm the first implementation approach and repository structure in a GitHub issue.
- Convert the selected task into a bounded issue with affected paths, validation commands, and review evidence.
- Preserve the dependency order unless a maintainer records a reason to change it.
- Keep task state honest: documentation alone does not complete an implementation task.

## Wave 1: Sources that stay findable

**Outcome:** Imported PDF and Markdown sources receive durable identities and citations that reopen exact context.

### LC-01 — Create the local source library

**Status:** Planned; implementation has not started.  
**Dependencies:** No preceding task in this draft plan; repository setup and maintainer scoping still come first.  
**Goal:** Import bounded PDF and Markdown documents into a local workspace with durable source identity, visible metadata, and extraction status.

**Acceptance criteria**

- [ ] Each imported source keeps its original filename, media type, source identity, and import time.
- [ ] PDF pages and Markdown headings remain distinguishable in extracted content.
- [ ] Unsupported or partially readable documents show an exact limitation and never appear fully imported.
- [ ] Re-importing an unchanged source does not create a second indistinguishable source record.

Before work starts, a maintainer must turn this plan into a scoped GitHub issue with the chosen implementation approach, affected paths, and validation commands. Estimates are not configured.

### LC-02 — Make citations reopen exact context

**Status:** Planned; implementation has not started.  
**Dependencies:** LC-01  
**Goal:** Define citation anchors for PDF pages and text regions plus Markdown headings and text spans, then reopen them in a source viewer.

**Acceptance criteria**

- [ ] A citation identifies one source version and the smallest supported page, heading, or text-span context.
- [ ] Opening a citation highlights or focuses the cited context without hiding adjacent source material.
- [ ] Changed or missing sources produce a visible unresolved citation rather than redirecting to a guess.
- [ ] Citation labels remain readable and keyboard reachable in notes and search results.

Before work starts, a maintainer must turn this plan into a scoped GitHub issue with the chosen implementation approach, affected paths, and validation commands. Estimates are not configured.

## Wave 2: Notes that remain grounded

**Outcome:** Researchers can write connected notes and find relevant source and note passages locally.

### LC-03 — Build source-linked notes and backlinks

**Status:** Planned; implementation has not started.  
**Dependencies:** LC-02  
**Goal:** Create a Markdown note editor that inserts citations from selected source context and shows which notes cite a source or another note.

**Acceptance criteria**

- [ ] A researcher can create, edit, rename, and link notes without breaking stable note identity.
- [ ] Inserting a citation records the selected source anchor and a readable label.
- [ ] Source and note backlinks update from saved links and never infer a relationship that was not recorded.
- [ ] Closing and reopening the workspace preserves note text, links, citations, and selection state.

Before work starts, a maintainer must turn this plan into a scoped GitHub issue with the chosen implementation approach, affected paths, and validation commands. Estimates are not configured.

### LC-04 — Add local search across sources and notes

**Status:** Planned; implementation has not started.  
**Dependencies:** LC-01, LC-03  
**Goal:** Index extracted source text and saved notes locally, returning results with object type, context, and a direct path to the matched passage.

**Acceptance criteria**

- [ ] Search distinguishes source passages from note passages and labels their origin.
- [ ] Each result opens the matching note or supported source context.
- [ ] Index updates after a note edit or source re-import without displaying stale text as current.
- [ ] No model or network service is required for the first-milestone search path.

Before work starts, a maintainer must turn this plan into a scoped GitHub issue with the chosen implementation approach, affected paths, and validation commands. Estimates are not configured.

## Wave 3: Knowledge that travels

**Outcome:** Workspaces export, reopen, and explain citation problems without losing original evidence or note history.

### LC-05 — Export and reopen a portable workspace

**Status:** Planned; implementation has not started.  
**Dependencies:** LC-01, LC-02, LC-03, LC-04  
**Goal:** Export sources, notes, links, citations, metadata, and index-rebuild instructions into a documented bundle that can reopen on another local installation.

**Acceptance criteria**

- [ ] The bundle format is versioned and contains the records required to rebuild search locally.
- [ ] Reopening preserves source and note identities, links, citation anchors, and unresolved states.
- [ ] An incomplete or incompatible bundle fails before replacing an existing workspace.
- [ ] The export does not imply publication or permission to redistribute imported documents.

Before work starts, a maintainer must turn this plan into a scoped GitHub issue with the chosen implementation approach, affected paths, and validation commands. Estimates are not configured.

### LC-06 — Show citation health and teach the workflow

**Status:** Planned; implementation has not started.  
**Dependencies:** LC-02, LC-03, LC-05  
**Goal:** Add a citation-health view plus a lawful sample research packet that teaches import, citation, notes, search, export, and recovery.

**Acceptance criteria**

- [ ] The health view distinguishes current, version-bound, missing-source, and unresolved citations.
- [ ] Health findings never rewrite note text, replace a citation, or claim a source proves the note.
- [ ] The sample packet uses redistributable sources and can be completed without a model or network service.
- [ ] Contributor documentation explains how a future importer or optional model adapter must preserve citation authority.

Before work starts, a maintainer must turn this plan into a scoped GitHub issue with the chosen implementation approach, affected paths, and validation commands. Estimates are not configured.


## Completion evidence

A task can be marked complete only after its acceptance criteria are demonstrated in the repository, the relevant checks pass, and a human maintainer accepts the pull request. A generated patch, agent report, or local claim is not completion evidence by itself.
