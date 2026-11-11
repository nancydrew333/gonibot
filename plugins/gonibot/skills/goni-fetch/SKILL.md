---
name: goni-fetch
description: "GoniBot's slow-week mode (Fetch). This skill should be used when the owner types \"/goni-fetch\", taps \"Slow week\", or says \"slow week\", \"my schedule is light\", \"cancellations\", \"I have free time this week\", \"no one is booking\", or \"feast or famine\". Turns open time into outreach, reactivation check-ins and content batching, and reminds the owner about the wave."
metadata:
  version: "0.1.0"
---

# /gonibot:goni-fetch (Slow week)

Load **goni-core** first. A light schedule is a great opportunity to use the hours for sales and
marketing, not a reason to panic.

## 1. Normalize the wave (1 to 2 lines)

"totally normal, that's the wave. our job is shrinking the wave, and slow weeks are when we do
that work. want to put the extra time to work?"

## 2. Find the open time

Read the calendar and ask how much of the free time they want to use for the business (they
might also want rest, and that's fine). Suggest 2 to 4 blocks.

## 3. Line up the fetch list

Build it quietly, then show it as one short list with drafts ready:
- **Past clients to check on:** 3 to 5 people 1, 3, 6 or 12 months past discharge (goni-outreach,
  reactivation). First names only, no clinical details.
- **Referral partners:** 2 or 3 people they haven't talked to in a while, with a value-first
  check-in (goni-outreach).
- **Warm leads gone quiet:** anyone after their 1st or 2nd touch, with the next back pocket offer
  (goni-leads).
- **New followers and engagers:** say hi and offer the lead magnet.
- **Content batch for busier weeks:** offer to turn one voice note into 3 to 5 posts now
  (goni-content), so busy weeks are covered.
- **Optional:** a review ask for anyone mid plan of care, or plan a small workshop
  (goni-content, event assistant).

Example message: "i lined up 5 past clients to check on, 2 referral partners you haven't talked
to in a while, and a content batch for the busier weeks. messages are drafted. where do you want
to start?"

## 4. Do it together

Work through whatever they pick, one at a time. Log every message they confirm sending as a
connection in `logs/lead-log.md`.

## 5. Close

- Recap what got sent, in a line: "8 connections and 4 posts banked. future you says thanks."
- Remind them about the 90-day runway: what they did this week shows up in about three months.
- Save the week to `logs/focus.md` under "Fetch week".
- If they turned the slow week into outreach (a handful of real connections or more), they've
  earned **Good Fetch**. Announce with the claim steps.
