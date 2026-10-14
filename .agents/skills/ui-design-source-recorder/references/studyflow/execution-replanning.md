# StudyFlow execution, re-planning, and conflicts

Read when changing Check-in → Re-plan → Review → Apply or manual overrides. Evidence: transcribed design context with recorded verification date **2026-10-14**, not newly verified business rules; see [authority and limitations](index.md).

1. [Calendar](screens/02-weekly-calendar.md) or [dashboard](screens/05-dashboard.md) opens [session details](screens/11-session-editor.md).
2. [Check-in](screens/12-check-in.md) records Completed, Partial with actual time, or Missed.
3. Actual progress updates outstanding work; missed work remains outstanding. Keep planned allocation separate from actual logged effort; the remaining-effort semantic conflict requires a domain decision.
4. Suggested or user-triggered [Re-plan](screens/04-replanning-review.md) changes future incomplete sessions. Preserve completed/past sessions and optionally locked sessions when supported.
5. Review old versus proposed schedule, then explicitly Apply. How much feasible existing work should stay stable is unresolved; the diff is not an optimization specification.

## Manual conflicts

- Recorded BR-USER-003 context: a human may override a busy-time conflict only after a specific warning and explicit confirmation. See [conflict screen](screens/13-conflicts.md) and consult the approved rule before changing behavior.
- AI-generated planning must not violate busy intervals or other hard constraints; a human override path does not authorize AI exceptions.
- AI must not silently rename tasks or change deadlines. Enforce overlap, daily maximum, duration, break, and deadline checks deterministically.
- Use the relevant local timezone and unambiguous 24-hour times; specimen dates are illustrative. Show conflicts, partial completion, and overload reasons with words as well as color.
- Prioritize this core journey before polish. Warning dialogs alone do not prove working confirmation, persistence, or recovery.
