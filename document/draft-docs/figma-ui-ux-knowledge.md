# StudyFlow — Figma UI/UX Knowledge Base

> **Project:** DoAn2 — Multi-Agent AI Personalized Study Planner for UIT students  
> **Status:** Design reference / low-fidelity, **NOT** an approved business specification  
> **Last verified:** 2026-10-14  
> **Figma source:** https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq  
> **Source repository:** https://github.com/PhDuy2005/NoteRepo-DoAn2

## 1. Purpose, authority and project constraints

This document is a durable, searchable index of the current StudyFlow user-interface work. Use it to align future discussions, Vue/TypeScript implementation, acceptance criteria and demo preparation with the actual editable Figma file.

**Authority precedence:** approved requirements / business rules in `document/approved-application-docs/` control behavior; this UI document describes representations and candidate interactions. If the Figma illustration contradicts an approved rule, amend the Figma design, **not** the rule without explicit approval.

Context: one developer, approximately 13 weeks and limited evenings; prioritize practical MVP over speculative enterprise-scale UI. Frontend direction: Vue + TypeScript; backend: Java/Spring Boot; MySQL. Do not assume Python, automated UIT portal integration, LMS, native mobile apps, or Google Calendar synchronization.

**Deliverable status:** Wireframes and edit-ready Figma layers exist. A wired, clickable prototype, responsive/mobile variants, production Vue components, API behavior, full accessibility audit and high-fidelity visual polish have **not** been established merely by these designs.

## 2. Figma structure and screen inventory (16 screens)

Figma file key: `84aoXZTWzvPkJu7qZerZrq`. Page: **MVP Wireframes**. Standard screen size: **1280 × 860 px**, desktop-first. Left app navigation approximately **218 px**; top header approximately **80–84 px**.

| ID | Figma frame | Design coverage | Main approved requirement / use-case |
| --- | --- | --- | --- |
| 01 | [Quản lý công việc](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=4-3) | Task list, estimated/remaining effort, priority, deadline, task creation form | FR-TASK, UC-04 |
| 02 | [Lịch học tuần](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=4-110) | Seven-day timeline; busy blocks, AI study sessions, weekly capacity | FR-SCHEDULE, FR-PLAN, UC-02/05 |
| 03 | [AI Planner — duyệt kế hoạch](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=5-16) | Generate/Review/Draft/Apply; candidate sessions, overload warning, availability totals | FR-PLAN, FR-EXPLAIN, UC-05/06 |
| 04 | [Re-plan — đề xuất điều chỉnh](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=5-109) | Before/after plan comparison, moved/preserved sessions, explicit Apply | FR-REPLAN, UC-09 |
| 05 | [Tổng quan học tập](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=20-94) | Today’s sessions, deadlines, workload risks and progress snapshot | Cross-feature dashboard; proposed UX aggregation |
| 06 | [Quản lý thời gian rảnh](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=20-168) | Recurring weekly busy times, manual edit, day-specific exception | FR-SCHEDULE, UC-02 |
| 07 | [Theo dõi tiến độ](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=20-266) | Completion ratio, actual hours, missed sessions, check-in controls and re-plan suggestion | FR-PROGRESS, UC-08 |
| 08 | [Hồ sơ & sở thích học tập](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=28-123) | Profile; study-session target, daily study cap, preferred daypart | FR-PROFILE, UC-01 |
| 09 | [Quản lý môn học](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=28-196) | Courses, code, color coding, course editor; course weight is a UX proposal requiring rule alignment | FR-TASK-001, UC-03 |
| 10 | [Onboarding / Thiết lập ban đầu](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=28-279) | Guided setup: Profile → Busy schedule → Courses → Tasks | Combines UC-01 through UC-04; proposed UX |
| 11 | [Chi tiết & chỉnh sửa phiên học](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=29-143) | Inspect/change session task/date/time, delete; optional pinned session | FR-MODIFY, optional FR-PLAN-005 |
| 12 | [Check-in & ghi nhận tiến độ](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=29-256) | Completed / Partial / Missed and actual duration input | FR-PROGRESS, BR-PROGRESS |
| 13 | [Cảnh báo xung đột lịch](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=29-361) | Conflict details; choose alternative versus explicit manual override | FR-MODIFY, BR-USER-003 |
| 14 | [Giải thích quyết định của AI](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=31-151) | Per-session short Vietnamese reasoning: deadline, priority, availability, preferences | FR-EXPLAIN, UC-10 |
| 15 | [Cấu hình trước khi sinh kế hoạch](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=31-199) | Week selector, input readiness, preferences, generate flow | FR-PLAN, UC-05 |
| 16 | [Empty / Loading / Error / Overload](https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq?node-id=31-255) | No tasks, AI generation pending, AI/API failure fallback, insufficient capacity | Error UX and NFR graceful degradation |

### Additional design-system areas

- **FOUNDATIONS — Colors / Typography / Tokens:** reusable values, color roles and usage conventions.
- **SHARED COMPONENTS — Reusable UI Kit:** editable instances and specimen states.
- **COMPONENT MASTERS — Assets:** source native component sets/variants; avoid detaching when reusing.

## 3. Color and typography conventions

The palette is intentionally sparse and suitable for low-fidelity visual separation. Semantic role is more important than raw HEX; implement via CSS variables or theme tokens.

| Role | Reference HEX | Use |
| --- | --- | --- |
| Primary / AI / interactive | `#4765BC` | Generate, Apply, active navigation, focus/action emphasis |
| Canvas background | `#F5F7FA` | Overall work area |
| Card / surface | `#FFFFFF` | Sidebar, cards, forms, dialogs |
| Main text | `#1C2938` | Body and headings |
| Secondary text | `#647386` | Descriptions, timestamps |
| Subtle border | `#DDE3EA` | Frames and separators |
| Busy / neutral background | `#EFF2F6` | Fixed busy slots, non-semantic neutral surfaces |
| AI draft background | `#EAF0FF` | AI proposals and draft state |
| Success background | `#EAF5ED` | Completed and validation success |
| Success text | `#2B7951` | Completion label |
| Warning background | `#FFF3DF` | Overload, deadline risk, partial status |
| Warning text | `#956011` | Warning label |
| Danger background | `#FAEEEE` | Missed, overdue and failure states |
| Danger text | `#BA454F` | Errors and destructive actions |

**Semantic token structure:** `bg/*`, `text/*`, `border/*`, `action/*`; 21 semantic color variables were created as aliases to base palette variables. There are separate spacing/radius variables. This is a proposed naming system for frontend alignment, not proof of existing CSS source.

**Typography:** Inter. H1 28 Bold; H2 20 SemiBold; H3 16 SemiBold; Body 13 Regular; Label 12 Medium; Caption 11 Regular. Base spacing: **4, 8, 12, 16, 24, 32px**. Radii: **6, 10, 14px**.

Color usage rules:
- Draft (blue) does **not** mean Active; only explicit Apply can activate a generated plan.
- Success means a task/session is complete or validation passed; distinguish completion from scheduled.
- Warning means review needed (overload, risk, partial). Danger means missed/overdue/failed/destructive.
- Busy blocks use neutral grey; conflicts must show textual detail, not rely on color alone.
- Reserve one visually dominant primary CTA per action area, and label status in words.

## 4. Reusable components in the current Figma kit

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

## 5. Critical product flows

**Planning:**
1. Onboarding/Profile, recurring and exceptional unavailability, Courses and Tasks supply inputs.
2. Generate config checks prerequisites and user preferences.
3. Orchestrator runs Profile Agent → Planning Agent → Review Agent, up to approved iteration limit; deterministic validation checks hard constraints.
4. User sees **Draft** plus sessions, explanations and warnings.
5. Explicit **Apply** makes the plan active; otherwise prior plan remains unchanged.

**Execution + Re-planning:**
1. Calendar or Dashboard opens study-session details.
2. User checks in **Completed**, **Partial with actual time**, or **Missed**.
3. Progress updates outstanding work; missed sessions remain outstanding.
4. Suggested or user-triggered Re-plan changes **future incomplete sessions only**.
5. User reviews old versus proposed schedule, then explicitly confirms Apply.

**Manual conflict:**
- Planner/AI is forbidden from proposing busy-time overlap and other hard-constraint violations.
- Human may manually override a busy-time conflict **only after a specific warning and explicit confirmation** (BR-USER-003).
- Completed and past sessions are preserved during automatic Re-plan; locked sessions preserved where the optional locking feature is implemented.
- AI must not silently rename tasks or alter task deadlines.

## 6. Open design decisions / caveats

1. **Remaining effort semantic conflict:** Some approved functional descriptions suggest decreasing remaining effort when a session is scheduled, while progress rules use actual time spent. Recommendation: separate **work_remaining_minutes** from **unscheduled_minutes**; only actual work should reduce real outstanding effort. Requires explicit domain sign-off.
2. **Duration bounds:** Preferred session target 30–120 min; BR plan upper bound 180 min. Treat these as separate preference versus allowed session cap until harmonized.
3. **Scheduling stability:** Specify how much of a feasible existing future plan should remain unchanged during Re-plan; the before/after diff currently illustrates preservation but is not an optimization specification.
4. **Manual override policy:** Keep one explicit-confirmation path for user overrides; never allow AI-generated plan to violate busy intervals.
5. **Course weight:** The course-management specimen exposes weight, but its exact data type, ranking rules and edit rights must be verified against approved requirements before implementation.
6. **Onboarding, dashboard and several forms** are UX proposals built to support approved use cases; they do not imply new formal FRs.
7. **Prototype state:** Button labels and dialogs are editable visuals. Do not infer click-through navigation, persisted state or backend operations from an artboard alone.
8. **Accessibility/responsive:** Pending separate review of contrast, keyboard focus, labels, mobile layout and Vietnamese line wrapping.

## 7. Implementation and review checklist

- Match approved FR/BR first, not mock sample values. Render all times in the user's relevant local timezone, using an unambiguous 24-hour format; mock dates are illustrative.
- Separate schedule entries (planned allocations), real task remaining effort and actual logged progress.
- Validate busy overlaps, daily maximum, session duration, break intervals, and task deadline **deterministically**; do not delegate hard rules to an LLM.
- Keep plan states explicit: Draft, Active, historical/completed; do not implicitly Apply.
- Support loading, empty, recoverable AI outage, timeout and overload states; preserve entered data on failure.
- UI should show actual available hours, allocated hours, per-session details, conflicts, partial completion and overload reasons.
- Use semantic tokens and native component instances wherever possible when editing Figma. Avoid creating detached rasterized copies of whole screens.
- Implement the core MVP journeys before polish: **Generate → Review → Apply** and **Check-in → Re-plan → Review → Apply**.
- Do not claim this document is an approved requirements artifact unless the project owner explicitly approves it.

## 8. Reference sources

- **Current editable Figma:** https://www.figma.com/design/84aoXZTWzvPkJu7qZerZrq
- **Approved requirements directory:** https://github.com/PhDuy2005/NoteRepo-DoAn2/tree/main/document/approved-application-docs
- **Functional requirements:** https://github.com/PhDuy2005/NoteRepo-DoAn2/tree/main/document/approved-application-docs/functional-requirement
- **Business rules:** https://github.com/PhDuy2005/NoteRepo-DoAn2/tree/main/document/approved-application-docs/business-rule
- **Technology decisions:** https://github.com/PhDuy2005/NoteRepo-DoAn2/blob/main/document/approved-application-docs/technical-decision/technology-stack.md

**For ChatGPT Project knowledge:** This Markdown should be added as a Project file/knowledge source via the ChatGPT Project interface. Saving to GitHub alone does not guarantee that Project knowledge has been directly updated or indexed.
