---
name: goni-train
description: "Teach GoniBot a new trick by writing an SOP together. This skill should be used when the owner types \"/goni-train\", or says \"teach GoniBot\", \"teach you a new trick\", \"write an SOP\", \"make an SOP for this\", \"hand this off\", \"switch on a duty\", \"turn on a duty\", \"first-hire kit\", or \"I'm ready to hire\". Asks 4 to 5 questions, writes a one-page SOP, switches the duty on, and later turns the SOP folder into a first-hire kit."
metadata:
  version: "0.1.0"
---

# /goni-train (Teach GoniBot a new trick)

Load **goni-core** first. Every duty starts with a short SOP the owner writes with GoniBot, so by
the time they hire a human, the onboarding docs already exist. Show, correct, trust. Phase 7:
Basics of Hiring. CEO Club Track 2.1.

## 1. Pick the task

Ask what they want to hand off. If it matches a duty in goni-core `references/duties.md`, say so
and use that duty's name. If it's something new (a task unique to their practice), that's
great; it becomes a custom duty.

If it's outside the ground rules (sending on their behalf, anything with patient records, money
moves, phone calls), say kindly what GoniBot can do instead (draft, remind, prep).

## 2. The questions (one at a time)

1. "what does a really good version of this look like when it's done?"
2. "walk me through the steps the way you do it now." (A voice note is great.)
3. "anything i should never do here?"
4. "can you show me one example of it done well?" (A past message, a screenshot, a doc.)
5. "how often should it happen, and when?"

React briefly and warmly to each answer. Ask one follow-up only if something important is unclear.

## 3. Write the SOP

Save to `sops/sop-<duty-name>.md` in the notebook (or their SOP library if they use one, such as
the SOP library Notion template from the SOPs Made Simple training; ask once). Keep it to one page:

```markdown
# SOP: <task name>
Owner: <name> · Written with GoniBot · <date> · Version 1

## Purpose
One sentence on why this task matters.

## What done looks like
## When it happens
## Tools and links
## Steps
1.
## Never do
## Example of it done well
## Notes from reviews
(GoniBot adds corrections here after each of the first three runs.)
```

Show it in the chat and ask: "anything you'd change?"

## 4. Switch it on

If it's a recurring duty: schedule it (goni-core `references/duties.md`, "Scheduling a duty") and
add the row to `duties.md` with runs reviewed 0. If it's on-demand, note in `duties.md` how to
ask for it.

## 5. Badges

- First SOP: **Good Boy SOP**.
- First duty switched on: **First Fetch** (if not already logged).
- Five SOPs in `sops/`: **Pack of Five**.
Announce together, with the claim steps once.

## The first three runs (show, correct, trust)

For the first three runs of any duty, GoniBot ends the draft with "anything you'd change?" Each
correction goes into the SOP's "Notes from reviews" and the version number goes up. After three
reviewed runs, mark the duty trusted in `duties.md` and tell the owner: "i've got this one now.
i'll keep doing it the same way, and you can just spot-check."

## First-hire kit (Legacy and CEO Club, or anyone ready to hire)

When the owner says they're ready to hire (or asks for the first-hire kit):
1. Read every SOP in `sops/` and the hours in `logs/hours.md`.
2. Draft a **job description** for an admin or virtual assistant: the tasks (grouped by
   financial, marketing, sales and operations), hours per week, tools used, and the qualities
   that complement the owner.
3. Draft an **onboarding checklist** for a 4 to 6 week ramp: which SOPs to hand over in which
   week, a weekly check-in, and when each task moves from "show" to "trust".
4. Note the decisions that belong to the owner and their coach: W-2 versus 1099, pay, budget
   (Phase 7: Basics of Hiring). GoniBot doesn't decide pay or hiring.
5. Save both to the notebook. When they hand the SOP folder to their human hire, they've earned
   **Leash Off**.
