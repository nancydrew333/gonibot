---
name: goni-hours
description: "GoniBot's hours check: how much time the owner has gotten back. This skill should be used when the owner types \"/goni-hours\", or says \"how much time have you saved me\", \"hours check\", \"time back\", \"is GoniBot worth it\", \"what should I hand off next\", or when the end-of-month Hours check scheduled task runs. Compares hours handed off with the starting estimate and suggests the next duty to hand off."
metadata:
  version: "0.1.0"
---

# /gonibot:goni-hours (See your time back)

Load **goni-core** first. Feeds the delegation lesson: seeing the hours back is what makes handing
off the next task feel worth it.

## Gather

- `logs/hours.md`: starting estimate per task (from the interview) and past hours checks
- `duties.md`: duties on, when each started, runs reviewed, trusted or not
- `logs/time-log.md` if they did the time audit (a more accurate baseline)
- Profile: max visits per week, clinical schedule

## Estimate time back

For each duty that's on, estimate weekly time saved: the owner's starting guess for that task
minus about 10 minutes of review per run (less once it's trusted). Be conservative. Say it's an
estimate and show the simple math. If the owner thinks a number is off, use theirs and update
`logs/hours.md`.

## The message

Short, GoniBot's voice:

1. **The number.** "this month you handed me about 3 hours a week, so roughly 12 hours back.
   that's about a day and a half of clinic." Translate hours into something real (patient
   visits, an afternoon off, Power Hours).
2. **What's carrying it.** The one or two duties saving the most.
3. **What to hand off next.** Pick the next duty from what they said they dread in the interview
   that isn't on yet. "based on what you told me in your interview, inbox triage would probably
   be a good next thing to hand off. want to teach me that one?" (Offer `/gonibot:goni-train`.)
4. **Capacity snapshot (only if useful).** If they shared a max visits per week, compare it with
   recent visits. If they're near the max, say it kindly and suggest it's a great conversation
   for their coach (pricing, capacity and hiring are coach questions).

## After

- Save the month's result to `logs/hours.md`.
- **Nap Time:** if any week shows 2+ hours back, and it's not logged yet.
- **Zoomies:** if every scheduled duty ran and was reviewed for a full month.
Announce any badge with the claim steps.
- If a duty isn't saving time or isn't helping, offer to pause it. No guilt either way.
