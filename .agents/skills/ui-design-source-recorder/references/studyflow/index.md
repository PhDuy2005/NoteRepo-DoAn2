# StudyFlow design lookup

## Source, authority, and limits

- Editable source: [StudyFlow Figma](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq), page **MVP Wireframes**, file key `84aoXZTWzvPkJu7qZerZrq`.
- Provenance: migrated from the project's local UI/UX design record on **2026-10-14**. That record states last verified **2026-10-14**; this migration did not inspect live Figma or revalidate requirement mappings. Bundled references retain the useful snapshot and do not require the original draft document.
- [Approved project documents](../../../../../document/approved-application-docs/) govern behavior; screen mappings and flow descriptions here are recorded design context. Check the relevant approved FR/BR when behavior changes or a conflict appears.
- Recorded coverage: editable low-fidelity wireframes. Clickable prototype, responsive/mobile variants, production Vue components, API/persistence behavior, accessibility conformance, and high-fidelity polish are unverified. Review contrast, focus, labels, mobile layout, and Vietnamese line wrapping when relevant.
- Project context at capture: one developer, about 13 weeks, limited evenings; practical MVP. Recorded stack direction: Vue/TypeScript, Java/Spring Boot, MySQL; verify [technology decisions](../../../../../document/approved-application-docs/technical-decision/technology-stack.md) for implementation. Do not infer automated UIT portal integration, LMS, native mobile, Python, or Google Calendar synchronization from these designs.

## Find one screen

Read the matching screen file only. Each contains its exact Figma node URL, recorded scope, requirement mapping, and relevant caveats. Follow related screens only if their interaction is affected.

| ID | Screen reference | Figma node |
| --- | --- | --- |
| 01 | [Quản lý công việc](screens/01-tasks.md) | `4-3` |
| 02 | [Lịch học tuần](screens/02-weekly-calendar.md) | `4-110` |
| 03 | [AI Planner — duyệt kế hoạch](screens/03-planner-review.md) | `5-16` |
| 04 | [Re-plan — đề xuất điều chỉnh](screens/04-replanning-review.md) | `5-109` |
| 05 | [Tổng quan học tập](screens/05-dashboard.md) | `20-94` |
| 06 | [Quản lý thời gian rảnh](screens/06-availability.md) | `20-168` |
| 07 | [Theo dõi tiến độ](screens/07-progress.md) | `20-266` |
| 08 | [Hồ sơ & sở thích học tập](screens/08-profile.md) | `28-123` |
| 09 | [Quản lý môn học](screens/09-courses.md) | `28-196` |
| 10 | [Onboarding / Thiết lập ban đầu](screens/10-onboarding.md) | `28-279` |
| 11 | [Chi tiết & chỉnh sửa phiên học](screens/11-session-editor.md) | `29-143` |
| 12 | [Check-in & ghi nhận tiến độ](screens/12-check-in.md) | `29-256` |
| 13 | [Cảnh báo xung đột lịch](screens/13-conflicts.md) | `29-361` |
| 14 | [Giải thích quyết định của AI](screens/14-ai-explanation.md) | `31-151` |
| 15 | [Cấu hình trước khi sinh kế hoạch](screens/15-generation-config.md) | `31-199` |
| 16 | [Empty / Loading / Error / Overload](screens/16-feedback-states.md) | `31-255` |

## Shared references, only when needed

- [Foundations](foundations.md): colors/tokens, typography, spacing, radii, shell measurements.
- [Components](components.md): reusable kit, variants, proposed Vue boundaries.
- [Planning flow](planning-flow.md): generation, review, explicit Apply, validation context.
- [Execution and re-planning](execution-replanning.md): progress, future changes, conflict overrides.
- [Preferences](../studyflow-ui-preferences.md): evidence-backed presentation direction.

Shared references are optional; a screen-link lookup does not require the palette, component inventory, or all journey details. After live inspection, update the affected reference's date and evidence status; do not imply that every screen was rechecked.
