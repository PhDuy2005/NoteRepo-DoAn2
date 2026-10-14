---
name: ui-design-source-recorder
description: Create, update, or remove draft UI design source records, especially Figma records, with traceable screen links and evidence status. Use for documenting design sources and consulting recorded StudyFlow screen context during UI review or edits.
metadata:
  short-description: Record UI design sources
---

# UI Design Source Recorder

Use this skill when asked to document, inventory, or refresh the source and evidence for a project's UI design. Keep the record searchable and useful for implementation and review.

## Workflow

1. Inspect repository guidance and existing design or requirements records. Update the established record when one exists; otherwise create a clearly named Markdown file in the project's documentation area. For StudyFlow, use the bundled references below as the established design record; update only the relevant references unless the user requests another output location.
2. Inspect the design source when access is available. Record the file name/key and canonical URL, page names, relevant frame/node links, screen dimensions when verified, and the date checked. Prefer direct links to individual screens over links to the file alone.
3. Build a screen inventory that maps stable local IDs to the exact frame, its visible scope, and related approved requirements or use cases when those links are known. Label UX concepts without an approved requirement as proposals.
4. Record design-system evidence that helps implementation: semantic color roles, typography, spacing, components/variants, and important interaction states. Distinguish values inspected in the source from suggested implementation conventions.
5. Capture key user flows and decision points only as represented by the design. Note missing prototype behavior, responsive variants, accessibility review, persistence, or backend behavior rather than inferring them from static frames.
6. Add concise caveats and source references. Keep unresolved decisions visible and identify which authoritative document or owner must resolve them.
7. Review links, IDs, and status wording against the source and repository files. Do not describe an inaccessible or uninspected source as verified.

## Removing a draft design document

This skill also applies when the user asks to remove a draft UI design source record or related draft design document. Before deleting, verify the exact file and confirm from its location or contents that it is a draft. Delete only the requested draft file; do not remove approved records or other drafts as cleanup. Search for direct links to the file and remove or update only links that would become stale, preserving surrounding content. If the target's draft status or intended file is ambiguous, ask which document to remove. Report the deleted path and any references updated.

## Internal preferences

- When reviewing or changing StudyFlow presentation conventions, consult [`references/studyflow-ui-preferences.md`](references/studyflow-ui-preferences.md). It is optional for a task limited to finding a screen or correcting its source link.
- When recording another project's design, derive preferences from that project's sources and keep them separate from requirements. Record each preference with supporting frames/components, evidence type, confidence, and scope. Treat a single isolated detail as a candidate, not a general preference.

## Authority and evidence

- Approved requirements and business rules govern product behavior. A design record describes the UI representation and candidate interactions; it does not approve new behavior.
- When a design conflicts with an approved rule, record the conflict and point to the rule. Do not silently change the rule or present the mockup as authority.
- Label claims by evidence: inspected in the editable design, transcribed from a project document, proposed for implementation, or still unverified. Include a last-verified date for mutable source details.
- Keep preference statements about presentation or interaction style separate from product rules. Do not turn inferred preferences into acceptance criteria or behavior constraints without approval.
- Do not infer a clickable prototype, responsive behavior, implementation status, API contract, or persisted state from editable frames alone.
- Preserve existing user-authored content and unrelated documents. Change only the requested design-source record, its relevant bundled references, and directly necessary links.

## StudyFlow references: load by task

Start with the short [StudyFlow index](references/studyflow/index.md) for provenance, authority, and screen lookup. Its bundled snapshots are sufficient without a separate draft knowledge document.

- **One screen:** read only its linked file in `references/studyflow/screens/`. Use its exact node URL to inspect the current design when the task requires live evidence. Follow related-screen links only when the requested change affects that interaction.
- **Colors, typography, spacing, or shell sizing:** read [foundations](references/studyflow/foundations.md).
- **Shared components or variants:** read [components](references/studyflow/components.md).
- **Generate → Review → Apply:** read [planning flow](references/studyflow/planning-flow.md) when changing that journey.
- **Check-in, Re-plan, or manual conflicts:** read [execution and re-planning](references/studyflow/execution-replanning.md) when changing those interactions.
- **Presentation preferences:** read [preferences](references/studyflow-ui-preferences.md) when needed.

Do not preload every screen, both flow references, or the entire reference directory for a single-screen task. Refresh mutable details from the actual Figma source when available; otherwise label them as recorded snapshot evidence. Update a screen's coverage, caveats, and provenance together when it changes. Keep shared specifications in their shared reference rather than copying them into every screen.
