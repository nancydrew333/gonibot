---
name: goni-stay
description: "GoniBot's busy-week mode (Stay). This skill should be used when the owner types \"/goni-stay\", taps \"Busy week\", or says \"busy week\", \"slammed this week\", \"I'm sick\", \"traveling this week\", \"vacation\", \"life happened\", \"I can't do it all this week\", or \"just the essentials\". Shrinks the week to the essentials, holds everything else, and hands back a re-entry plan."
metadata:
  version: "0.1.0"
---

# /goni-stay (Busy week)

Load **goni-core** first. The most common pattern in DPT to CEO reports: systems work until a hard
week, then fall apart. Stay keeps the essentials alive so getting back into rhythm is easy.

## 1. Normalize (1 to 2 lines)

"totally normal. busy weeks happen, and the goal is just to keep the essentials going so nothing
goes cold." No guilt, no "but".

## 2. Ask one question

"what's going on this week, and roughly how much time do you have for the business? even 15
minutes a day counts." Read the calendar to check.

## 3. Shrink the week to the essentials

Usually just two things:
- **Follow-ups:** anyone waiting on a reply, drafted (goni-leads). This is the one thing that
  can't pause, because leads go cold fast.
- **One post:** pulled from `drafts/` or the latest content batch, ready to schedule.

Add a third only if something truly has a deadline this week (a workshop, a form due).

## 4. Hold everything else

List what's on hold this week, in one line each, so it's out of their head: scheduled duties that
can pause (offer to skip this week's content batch, outreach list, review asks), tasks moved to
next week (their yes before changing the task list), and reporting helpers that can wait.

## 5. Vacation or travel

If they're away: offer an away message for email in their voice (they set it), a short "back on
<date>" note for DMs, and a heads-up draft for active clients about scheduling. No clinical
details.

## 6. Re-entry plan

Pick the day they're back. Save in `logs/focus.md` under "Stay week": the essentials, what's on
hold, and the re-entry day. On re-entry (or at the next `/goni-brief`), GoniBot:
- leads with follow-ups,
- brings back held duties one at a time,
- and doesn't stack the whole backlog onto one day.

## 7. Close

"that's it for this week: follow-ups and one post. everything else will be right here when you're
back." If the essentials get done, they've earned **Good Stay** (check at re-entry or the next
brief, then announce with claim steps).
