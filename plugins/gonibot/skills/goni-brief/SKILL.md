---
name: goni-brief
description: "GoniBot's \"Start my week\" brief (the Weekly Reset brief). This skill should be used when the owner types \"/goni-brief\", taps \"Start my week\", or says \"start my week\", \"Monday brief\", \"weekly reset\", \"plan my week\", \"what's my Big 3 this week\", or when the GoniBot Weekly Reset scheduled task runs. Follow-ups come first, then last week's recap, anything stuck, calendar guard, and a suggested Big 3. Can also run any other GoniBot brief on demand."
metadata:
  version: "0.1.0"
---

# /goni-brief (Start my week)

Load **goni-core** first. Phase 5, Lesson 3: Weekly Reset. This brief turns the Weekly Reset
from "figure out what to do" into "confirm the plan" in about 10 minutes.

## On demand for other briefs

If the owner names a different brief ("/goni-brief eom", "run my outreach list", "pace check"),
run that duty from goni-core `references/duties.md` using its skill instead, then stop.

## Gather (quietly)

- Leads waiting 2+ days and open opportunities (goni-leads, follow-ups section)
- Last week: evals booked, new leads (`logs/lead-log.md`), follow-ups sent, posts, wins
  (`logs/wins.md`)
- This week's calendar (all calendars from the profile), clinical hours, Power Hour and CEO time
- Open and overdue tasks from their task list
- `logs/focus.md` (the one thing from Snuffle Mat, Stay or Fetch) and `duties.md` (what's on)
- If last week was a busy week (`/goni-stay`), check whether the essentials happened

## The brief (one message, then a short back-and-forth)

1. **Follow-ups first.** "happy monday! first up, 4 people are waiting to hear back from you, and
   the follow-ups are drafted." List first names and where each draft is (Gmail drafts or below
   in the chat). This always comes first.
2. **Last week in 3 lines.** Lead with what went well. Numbers only if GoniBot could read them.
   No shortfall framing.
3. **Anything stuck.** One or two items: a lead that's gone quiet after 3 touches (suggest the
   next back pocket offer), a task overdue twice (ask if it still matters), a duty that didn't
   run.
4. **Calendar guard.** If Power Hour or CEO time isn't on the calendar this week, or clinical
   hours crowd it out, suggest specific blocks that fit. Offer to add them (their yes first).
5. **Suggested Big 3 for the week.** One per bucket when possible (sales and revenue,
   visibility, client delivery and the business), plus the one thing from `logs/focus.md` if it
   exists. Phrase it hedged: "if it's cool with you, i'd probably focus on ___."
6. **This week's duties.** One line: what GoniBot will do this week (from `duties.md`) and
   anything it needs from them, like the Monday voice note for the content batch.
7. **Check-in question.** "does that feel doable?"

Keep the whole brief to one screen. Lists only for the follow-ups and the Big 3.

## After they reply

- They confirm or swap the Big 3. Save it to the notebook (top of `logs/focus.md`, under
  "This week's Big 3") so `/goni-morning` can use it.
- If they say the week is already slammed, offer `/goni-stay`. If it's wide open, offer
  `/goni-fetch`.
- If last week was a Stay week and the essentials got done, they've earned **Good Stay**.
- For a scheduled run's first three weeks, ask: "anything you want me to do differently in your
  monday brief?" and update the brief's SOP (`sops/sop-weekly-reset-brief.md`).

## Example opener

"happy monday! first up, 4 people are waiting to hear back from you, and the follow-ups are
drafted. after that, if it's cool with you, i'd probably focus on the workshop flyer and your
voice note this week. does that feel doable?"
