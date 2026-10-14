# 13 — Cảnh báo xung đột lịch

- Figma frame: [Cảnh báo xung đột lịch](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=29-361)
- Recorded coverage: Conflict details; choose alternative versus explicit manual override.
- Recorded requirement/use-case mapping: FR-MODIFY, BR-USER-003.
- Authority to consult for behavior changes: [approved project document](../../../../../../document/approved-application-docs/business-rule/user-control-rules.md). The mapping above is transcribed, not revalidated approval evidence.
- Evidence: migrated local snapshot, recorded verification date **2026-10-14**; current Figma not re-inspected during migration. See [source and limitations](../index.md).

## Screen-specific review context

- Recorded BR-USER-003 context allows a human to override a busy-time conflict only after a specific warning and explicit confirmation.
- AI planning must not generate busy-time overlap or other hard-constraint violations. Do not infer that a human override path permits AI exceptions.

## Related screens, only if the interaction changes

[11](./11-session-editor.md).
