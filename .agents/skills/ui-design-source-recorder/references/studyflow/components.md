# StudyFlow component kit

Read for shared components/variants. Evidence: transcribed snapshot, recorded verification date **2026-10-14**; see [source and limitations](index.md). Current counts and variant availability require live confirmation.

Recorded areas: **SHARED COMPONENTS — Reusable UI Kit** (instances and specimen states), **COMPONENT MASTERS — Assets** (native sources). Exact node URLs were not captured. Locate the relevant component in Figma; prefer semantic tokens and native instances, preserving reuse rather than detaching or rasterizing whole screens.

The file contains **35 native component variants across 10 component families**:

| Component family | Variant coverage | Intended use |
| --- | --- | --- |
| Button | Primary, Secondary, Danger, Ghost × Default/Disabled (8) | Actions, confirmation, cancellation |
| Badge | Pending, In progress, Draft, Completed, Partial, Missed, Overdue (7) | Task and session state |
| Text field | Default, Focus, Error (3) | Data entry and validation |
| Nav item | Default, Selected (2) | App sidebar |
| Tab | Default, Selected (2) | Local view switching |
| Study session card | Planned, Completed, Partial, Missed (4) | Session preview and progress |
| Calendar block | Study, Busy, Completed (3) | Seven-day grid |
| Feedback banner | Info, Success, Warning, Danger (4) | Guidance and failure recovery |
| KPI card | Single reusable component | Summary values |
| Confirmation dialog | Single reusable component | Explicit confirmation |

For Vue implementation, **suggested** boundaries (not yet implemented): AppSidebar, BaseButton, BaseTextField, StatusBadge, WeekCalendar, StudySessionCard, MetricCard, FeedbackBanner, ConfirmationDialog, SessionCheckInDialog, SessionEditDialog and PlanDiffReview. Keep business-rule validation in the domain/backend, not in visual components.
