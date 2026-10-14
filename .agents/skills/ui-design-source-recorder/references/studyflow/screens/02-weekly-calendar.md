# 02 — Lịch học tuần

- Figma frame: [Lịch học tuần](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=4-110)
- Recorded coverage: Seven-day timeline; busy blocks, AI study sessions, weekly capacity.
- Recorded requirement/use-case mapping: FR-SCHEDULE, FR-PLAN, UC-02/05.
- Authority to consult for behavior changes: [approved project document](../../../../../../document/approved-application-docs/functional-requirement/schedule-availability.md). The mapping above is transcribed, not revalidated approval evidence.
- Evidence: migrated local snapshot, recorded verification date **2026-10-14**; current Figma not re-inspected during migration. See [source and limitations](../index.md).

## Screen-specific review context

- Show available and allocated hours and distinguish busy blocks from planned study sessions. Render times in the relevant local timezone with an unambiguous 24-hour format.
- Busy overlap, daily maximum, duration, breaks, and deadline validation belong to deterministic rules; a frame does not prove enforcement.

## Related screens, only if the interaction changes

[06](./06-availability.md), [11](./11-session-editor.md).
