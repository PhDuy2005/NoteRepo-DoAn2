# 06 — Quản lý thời gian rảnh

- Figma frame: [Quản lý thời gian rảnh](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=20-168)
- Recorded coverage: Recurring weekly busy times, manual edit, day-specific exception.
- Recorded requirement/use-case mapping: FR-SCHEDULE, UC-02.
- Authority to consult for behavior changes: [approved project document](../../../../../../document/approved-application-docs/functional-requirement/schedule-availability.md). The mapping above is transcribed, not revalidated approval evidence.
- Evidence: migrated local snapshot, recorded verification date **2026-10-14**; current Figma not re-inspected during migration. See [source and limitations](../index.md).

## Screen-specific review context

- The recorded form supports recurring busy intervals, manual edits, and day-specific exceptions; do not infer external calendar synchronization.
- Busy-time validation is deterministic. Human override and AI planning have different recorded constraints; consult conflict context only if changing that interaction.

## Related screens, only if the interaction changes

[13](./13-conflicts.md).
