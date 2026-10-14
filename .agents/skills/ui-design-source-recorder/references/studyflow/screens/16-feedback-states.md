# 16 — Empty / Loading / Error / Overload

- Figma frame: [Empty / Loading / Error / Overload](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=31-255)
- Recorded coverage: No tasks, AI generation pending, AI/API failure fallback, insufficient capacity.
- Recorded requirement/use-case mapping: Error UX and NFR graceful degradation.
- Authority to consult for behavior changes: [approved project document](../../../../../../document/approved-application-docs/functional-requirement/functional-requirements.md). The mapping above is transcribed, not revalidated approval evidence.
- Evidence: migrated local snapshot, recorded verification date **2026-10-14**; current Figma not re-inspected during migration. See [source and limitations](../index.md).

## Screen-specific review context

- Recorded states cover no tasks, generation pending, AI/API outage, timeout, and insufficient capacity. Preserve entered data and offer recovery on failure.
- Show overload/conflict reasons and status words as well as color. Do not assume the static frame implements retry, accessibility, or failure recovery.

## Related screens, only if the interaction changes

[15](./15-generation-config.md).
