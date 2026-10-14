# StudyFlow UI Preferences

These are reusable preferences inferred from the StudyFlow Figma knowledge record. They describe the current design direction; they are not approved product requirements or proof of implemented behavior.

## Source and confidence

- Source: [`document/draft-docs/figma-ui-ux-knowledge.md`](../../../../document/draft-docs/figma-ui-ux-knowledge.md)
- Design source recorded there: StudyFlow Figma file `84aoXZTWzvPkJu7qZerZrq`, page **MVP Wireframes**.
- Source document last verified: 2026-10-14, as recorded in that document. Recheck the source before relying on mutable details.
- Confidence describes how strongly the current design record supports a preference, not whether the preference has product-owner approval.

## Derived preferences

| Preference | Evidence in the source record | Confidence | Scope |
| --- | --- | --- | --- |
| Use semantic color roles and tokens instead of scattering raw color values through implementation. | The design record documents `bg/*`, `text/*`, `border/*`, and `action/*` token groups, 21 semantic aliases, and says semantic role matters more than raw HEX. | High | StudyFlow frontend alignment; exact CSS token implementation remains to be verified. |
| Communicate status with words as well as color. | The color guidance says to label status in words and not rely on color alone for conflicts; the component inventory includes named status badges. | High | StudyFlow status, warning, conflict, and progress UI. |
| Reserve the strongest visual emphasis for the primary action in an action area. | The color-usage guidance says to reserve one visually dominant primary CTA per action area. | High | StudyFlow screens and dialogs represented by the current design. |
| Keep generated plans visibly in Draft until the user explicitly applies them. | The flow distinguishes Draft from Active and states that explicit Apply activates a generated plan; the color guidance says Draft does not mean Active. | High | StudyFlow planning flow. This is consistent with documented requirements, but behavior authority remains in approved requirements/business rules. |
| Make consequential changes reviewable before applying them. | Planning and re-planning flows show a draft/review step, warnings, before/after comparison, and explicit Apply. | High | StudyFlow plan generation and re-planning. Do not infer exact backend transaction behavior from mockups. |
| Preserve the user's work and offer recovery states when generation or service calls fail. | The empty/loading/error/overload frames and implementation checklist call for recoverable failure states and preserving entered data. | High | StudyFlow forms and AI-assisted planning. Confirm against approved requirements when defining acceptance criteria. |
| Keep schedule constraints and conflict reasons understandable in the UI. | The inventory calls out busy blocks, capacity, overload warnings, conflict details, and alternatives; the checklist calls for actual available/allocated hours and conflict reasons. | High | StudyFlow scheduling and re-planning. Deterministic rule enforcement remains outside this visual preference. |
| Prefer reusable native Figma components and semantic design tokens when extending the design. | The source describes a reusable component kit and advises using semantic tokens and native component instances rather than detached raster copies. | High | Editing the StudyFlow Figma file. |
| Treat the current design as desktop-first and avoid assuming responsive/mobile behavior. | The record names a 1280 x 860 px standard frame and explicitly says responsive/mobile variants have not been established. | High | Current StudyFlow design coverage only; this is a coverage caveat, not a preference to omit responsive design. |

## Do not infer

- The listed preferences do not authorize new functional requirements or override `document/approved-application-docs/`.
- Suggested Vue component boundaries, exact token names, and values described as proposals are not proof of implemented frontend conventions.
- Static frames do not establish clickable navigation, persisted state, API behavior, accessibility conformance, or responsive layouts.
- Open decisions in the source record, including effort semantics, duration bounds, schedule stability, course weight, and manual override details, remain unresolved until authoritative project decisions settle them.
