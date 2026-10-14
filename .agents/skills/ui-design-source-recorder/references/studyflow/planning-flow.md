# StudyFlow planning journey

Read when changing Generate → Review → Apply. Evidence: transcribed design context with recorded verification date **2026-10-14**, not newly verified product rules; see [authority and limitations](index.md).

1. Onboarding/profile, recurring and exceptional unavailability, courses, and tasks supply inputs.
2. [Generation config](screens/15-generation-config.md) checks prerequisites and preferences.
3. Recorded orchestration: Profile Agent → Planning Agent → Review Agent, up to the approved iteration limit. Verify against current approved requirements before implementing orchestration.
4. [Review](screens/03-planner-review.md) shows Draft sessions, [explanations](screens/14-ai-explanation.md), availability/allocation totals, and warnings.
5. Explicit Apply activates the proposal; before Apply, the previous active plan remains unchanged. Keep Draft, Active, and historical/completed states distinct.

## Constraints to check against approved rules

- Deterministically validate busy overlaps, daily maximum, duration, breaks, and deadlines; hard rules are not delegated to an LLM. AI must not silently rename tasks or change deadlines.
- Preferred target 30–120 minutes versus recorded rule cap 180 minutes remains a preference/cap harmonization question; do not invent a single default.
- Real outstanding effort, unscheduled allocation, and actual logged progress are distinct. The recorded FR/BR disagreement about effort reduced on scheduling versus actual work requires explicit domain sign-off; `work_remaining_minutes` / `unscheduled_minutes` is only a proposal.
- [Failure states](screens/16-feedback-states.md) include empty, loading, recoverable AI outage, timeout, and overload; preserve entered data. Show actual availability, allocations, session details, and overload reasons.
- Prioritize the core journey before visual polish. Static frames do not prove navigation, persistence, transactions, or deterministic validation.
