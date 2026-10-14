# StudyFlow foundations

Read when changing shared visual values or shell layout. Evidence: transcribed snapshot, recorded verification date **2026-10-14**; see [source and limitations](index.md). Values require live confirmation when current precision matters.

Recorded standard frame: **1280 × 860 px**, desktop-first. Left navigation approximately **218 px**; top header approximately **80–84 px**. These do not establish responsive breakpoints.

Recorded Figma area: **FOUNDATIONS — Colors / Typography / Tokens**. Its exact node URL was not captured; locate it in the editable source before making live edits.

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
