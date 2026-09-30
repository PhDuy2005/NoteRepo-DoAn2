---
name: document-approval-workflow
description: Manage section-by-section review of documents in docs/ and consolidate only explicitly approved sections in approved-docs/.
metadata:
  short-description: Review and consolidate approved docs
---

# Document Approval Workflow

Use this skill when the user is reviewing project documentation in `docs/` and asks to approve, organize, or consolidate approved parts.

## Source and approval rules

- Treat files in `docs/` as drafts. Do not move, rename, or rewrite a source document just because one part was approved.
- Approval applies only to the specific section or item the user explicitly names as approved. A request to review, revise, or prepare a section is not approval.
- Copy approved content into the shared document under `approved-docs/`. Preserve its meaning and identify its source document and section. Never imply neighboring content was approved.
- If it is unclear which exact section was approved, ask before changing approved documentation. Keep the review moving on independent, unambiguous work.
- Preserve existing approved content when updating the shared document. Do not overwrite user edits or remove sections without explicit direction.

## Shared approved document

- Keep one main Markdown document in `approved-docs/` for the project's approved requirements and analysis content. Reuse an existing main file if present; otherwise create a clearly named file such as `requirements_analysis.md`.
- Maintain a top-level table of contents with links to each approved section. Update it whenever sections are added, renamed, or reordered, and use valid Markdown anchors.
- Use a clear hierarchy for document parts, retain useful source numbering/IDs, and avoid duplicating an already-approved section.
- At the beginning of each distinct information type (for example, User Needs or Use Cases), include a compact summary table with the stable ID, name, concise summary, actor/audience where relevant, and approval/source reference. Tailor columns to the content rather than forcing irrelevant fields.
- Keep detailed approved content after its type's summary table. Make TBDs, assumptions, and unresolved decisions visible; do not turn draft proposals into approved facts.

## First approved Use Case

When the first Use Case is explicitly approved and added:

1. Add it to the shared approved document and create or update a `use-case/` folder inside `approved-docs/`.
2. Add a reusable Use Case template in that folder, based on the structure and level of detail of the approved UC. Name it `use-case-template.md` unless a local naming convention already exists.
3. Mark template-only fields with placeholders; do not copy scenario-specific facts into the template as defaults.
4. Link the template from the Use Cases section or its summary in the shared document.

Do not create a Use Case template before a Use Case is approved. For later UCs, follow the established template and flag any missing decisions instead of inventing behavior.

## Before editing

Inspect the relevant source sections, existing contents of `approved-docs/`, and repository guidance such as `AGENTS.md`. Keep the edit limited to the approved material and the indexes/templates required by this workflow. Report what was approved, which files changed, and any items that remain draft or unresolved.
