---
name: ui-design-source-recorder
description: Create or update a project record of UI design sources, especially Figma files, with traceable screen links, verification status, and boundaries between design proposals and approved requirements.
metadata:
  short-description: Record UI design sources
---

# UI Design Source Recorder

Use this skill when asked to document, inventory, or refresh the source and evidence for a project's UI design. Keep the record searchable and useful for implementation and review.

## Workflow

1. Inspect repository guidance and existing design or requirements records. Update the established record when one exists; otherwise create a clearly named Markdown file in the project's documentation area.
2. Inspect the design source when access is available. Record the file name/key and canonical URL, page names, relevant frame/node links, screen dimensions when verified, and the date checked. Prefer direct links to individual screens over links to the file alone.
3. Build a screen inventory that maps stable local IDs to the exact frame, its visible scope, and related approved requirements or use cases when those links are known. Label UX concepts without an approved requirement as proposals.
4. Record design-system evidence that helps implementation: semantic color roles, typography, spacing, components/variants, and important interaction states. Distinguish values inspected in the source from suggested implementation conventions.
5. Capture key user flows and decision points only as represented by the design. Note missing prototype behavior, responsive variants, accessibility review, persistence, or backend behavior rather than inferring them from static frames.
6. Add concise caveats and source references. Keep unresolved decisions visible and identify which authoritative document or owner must resolve them.
7. Review links, IDs, and status wording against the source and repository files. Do not describe an inaccessible or uninspected source as verified.

## Internal preferences

- For StudyFlow tasks, read [`references/studyflow-ui-preferences.md`](references/studyflow-ui-preferences.md) and apply its evidence-backed preferences within their stated scope.
- When recording another project's design, derive preferences from that project's sources and keep them separate from requirements. Record each preference with supporting frames/components, evidence type, confidence, and scope. Treat a single isolated detail as a candidate, not a general preference.

## Authority and evidence

- Approved requirements and business rules govern product behavior. A design record describes the UI representation and candidate interactions; it does not approve new behavior.
- When a design conflicts with an approved rule, record the conflict and point to the rule. Do not silently change the rule or present the mockup as authority.
- Label claims by evidence: inspected in the editable design, transcribed from a project document, proposed for implementation, or still unverified. Include a last-verified date for mutable source details.
- Keep preference statements about presentation or interaction style separate from product rules. Do not turn inferred preferences into acceptance criteria or behavior constraints without approval.
- Do not infer a clickable prototype, responsive behavior, implementation status, API contract, or persisted state from editable frames alone.
- Preserve existing user-authored content and unrelated documents. Change only the requested design-source record and directly necessary index links.

## StudyFlow reference

For work in this repository's StudyFlow project, read [`document/draft-docs/figma-ui-ux-knowledge.md`](../../../document/draft-docs/figma-ui-ux-knowledge.md) before updating its design record. It is a project-specific, low-fidelity design reference, not an approved business specification. Reuse its traceability and caveat patterns where useful; do not carry its product details, measurements, palette, or requirements into another project.
