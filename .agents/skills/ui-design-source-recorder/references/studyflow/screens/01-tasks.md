# 01 — Quản lý công việc

- Figma frame: [Quản lý công việc](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=4-3)
- Recorded coverage: Task list, estimated/remaining effort, priority, deadline, task creation form.
- Recorded requirement/use-case mapping: FR-TASK, UC-04.
- Authority to consult for behavior changes: [approved project document](../../../../../../document/approved-application-docs/functional-requirement/course-task-management.md). The mapping above is transcribed, not revalidated approval evidence.
- Evidence: migrated local snapshot, recorded verification date **2026-10-14**; current Figma not re-inspected during migration. See [source and limitations](../index.md).

## Screen-specific review context

- Estimated effort, actual work remaining, and unscheduled allocations are separate concepts. The recorded FR/BR descriptions disagree about when remaining effort decreases; `work_remaining_minutes` versus `unscheduled_minutes` is a proposal requiring domain approval.
- Mock dates and task values are illustrative. AI must not silently rename tasks or alter their deadlines.

## Related screens, only if the interaction changes

[07](./07-progress.md).
