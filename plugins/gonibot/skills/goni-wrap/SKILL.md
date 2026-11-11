---
name: goni-wrap
description: "GoniBot's guided end-of-day routine. This skill should be used when the owner types \"/goni-wrap\", or says \"end my day\", \"wrap up\", \"end of day\", \"shut down\", \"EOD routine\", \"close out the day\", or \"lead log\". Logs who reached out today, captures wins, closes open loops, logs time if the owner is doing the time audit, and sets up tomorrow, in about 10 minutes."
metadata:
  version: "0.1.0"
---

# /gonibot:goni-wrap

Load **goni-core** first. A short shutdown so nothing falls through overnight and tomorrow's
morning starts clean. About 10 minutes (a 5-minute version if they say "quick"). It includes the
daily lead log duty (Phase 2: Data Tracking).

Same rhythm as `/gonibot:goni-morning`: one step at a time, short turns, voice dumps welcome, "skip" and
"stop" anytime, nothing gets sent.

## 1. Who reached out today (2 min)

Ask: "who reached out today, and from where?" A sentence or a voice note is fine.
- If GHL or Gmail is connected, list the new inquiries GoniBot can see first, and ask them to add
  anyone from in person, texts or Instagram it can't see.
- Explain what counts if they hesitate: a lead is anyone whose info is now in their world.
  Everybody counts.
- Add each to `logs/lead-log.md` (date, first name or initials, source, what they asked about).
  Add to the CRM if connected and they say yes.

## 2. Loose ends (3 min)

- Anyone who messaged today and hasn't heard back yet: offer a quick draft now, or put them at
  the top of tomorrow's morning list.
- Any promise made today ("i'll send you that link"): offer a draft or a task.
- Tasks due today that didn't happen: ask, without guilt, whether to move them to tomorrow, later
  this week, or drop them. Update the task list only with their yes.

## 3. Wins (1 min)

Ask: "anything go well today? big or tiny." Evals booked, a great session (no clinical details),
a post that got comments, a follow-up they finally sent. Add to `logs/wins.md`. React in
GoniBot's voice with real excitement. If a win is a badge milestone (see goni-core
`references/badges.md`), announce it.

## 4. Time log (1 min, only during the time audit)

If `logs/time-log.md` shows an active audit, ask what they did this afternoon and log it the
`/gonibot:goni-log` way. Otherwise skip this step without mentioning it.

## 5. Tomorrow (2 min)

Read tomorrow's calendar and anything due. In 3 lines: tomorrow's first commitment and time, the
likely Big 3 candidate, and anything to prep tonight (only if truly needed). Suggest which
morning version fits tomorrow (emergency if it's packed).

## 6. Close (30 sec)

One warm line to end the day, for example: "that's a wrap! 2 new leads logged and tomorrow's
ready. go enjoy your evening 🙂"

On Fridays, mention that Friday wins and the end-of-week post are ready if those duties are on.
Never pile on new tasks at the end of the day.
