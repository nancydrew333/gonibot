---
name: goni-log
description: "GoniBot's optional two-week time audit. This skill should be used when the owner types \"/goni-log\", or says \"log my time\", \"time audit\", \"here's what I did today\", \"where does my week go\", or \"track my hours\", or when a GoniBot time-audit reminder runs. Sorts each entry into clinical, sales, marketing, admin or client delivery, and on day 14 builds the hiring report."
metadata:
  version: "0.1.0"
---

# /gonibot:goni-log (Optional time audit)

Load **goni-core** first. Optional, for owners who feel like they're always running behind and
want to see where their week actually goes before handing things off. Two weeks, twice a day,
about a minute each time. Phase 2: Data Tracking (time metrics).

If the owner already uses Toggl or the dashboard's time tracker, offer to read their export
instead, and only use `/gonibot:goni-log` to fill gaps.

## Starting the audit

If `logs/time-log.md` doesn't exist or has no active audit:
1. Explain in two lines: "for the next two weeks, just tell me what you did, twice a day. a
   sentence or a voice note is plenty. i'll sort it, and on day 14 you'll see exactly where your
   week goes."
2. Create `logs/time-log.md` with a start date.
3. Offer to schedule two reminders a day (midday and end of day, skipping days off). Or they can
   log during `/gonibot:goni-wrap`.

## Logging an entry

1. Take whatever they say ("saw 6 patients, spent a while on DMs, and redid my booking page").
2. Sort each piece into one of five buckets, with a time estimate (ask only if there's no way to
   guess):
   - **Clinical:** patient care, documentation
   - **Sales:** DMs, discovery calls, follow-ups, consults
   - **Marketing:** content, posting, events, outreach, email
   - **Admin:** email, scheduling, billing, finances, tech
   - **Client delivery:** programs, client check-ins, onboarding (non-clinical)
3. Reply in one or two lines: "got it. i'm logging that as about 6 hours clinical, 45 minutes
   sales and an hour of admin. two more days and we'll have a really clear picture of where your
   week goes."
4. Add the entry to `logs/time-log.md` (date, bucket, minutes, a few words). No patient names or
   clinical details.

Missed a log? No guilt. A rough guess for the missed half-day is fine, or skip it.

## Day 14: The hiring report

Total the two weeks by bucket (hours per week and percent). Show it simply, then build the hiring
report exactly as in `/gonibot:goni-interview`, step 4, using these real numbers instead of guesses. Save
the baseline to `logs/hours.md`. Then continue with the interview's step 5 (first shift) to
switch on their first 2 or 3 duties.
