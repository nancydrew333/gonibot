---
name: goni-reports
description: "GoniBot's reporting and admin duties. This skill should be used when a GoniBot scheduled task or the owner asks for \"Prep and Reflect\", \"P&R answers\", \"benchmark form\", \"end of week post\", \"KPI post\", \"EOQ data\", \"quarter numbers\", \"weekly numbers report\", \"admin and finance checklist\", \"mid-month pace check\", \"how's the month going\", \"weekly project review\", or \"annual planning data\". Requires goni-core first."
metadata:
  version: "0.1.0"
---

# GoniBot reporting and admin duties

Load **goni-core** first. Reporting helpers (Prep and Reflect, end of week KPI post, EOM, EOQ,
benchmarks) are **opt-in**: only run them if they're switched on in the profile or the owner asks
directly. Forms don't save drafts, so GoniBot drafts the answers in an email to the owner
(a Gmail draft addressed to themselves) to copy in. Never submit a form.

## Reading the data tracker

Read the All Data Tracker from the link in the profile (Google Drive). Use the metric names it
uses. When a field is blank, don't guess: ask the owner for it in one batch, and explain what
counts if it's a field people often leave blank (leads, connections, touchpoints). Imperfect data
beats no data, so it's fine to write "not tracked this month."

Show the math when you calculate:
- Show rate = evals attended / evals booked
- Close rate = plans of care started / evals completed (also discovery call to eval if tracked)
- Revenue per eval = total sales / new clients (evals)
- Average income per appointment = total sales / total appointments
- Profit margin = (revenue - expenses) / revenue, only if expenses are tracked

Never frame a number as a shortfall. Compare to their own goals and their own past months, never
to other students. Lead with what moved in the right direction.

## EOM report

The End of Month Report has its own trick now: **goni-eom** (`/goni-eom`). If the owner asks for
EOM help, or the EOM scheduled task runs, use that skill instead of drafting it here. The math
above still applies.

## Prep and Reflect pre-fill (24 hours before each coaching call)

Welcome, Lesson 1: Your Orientation. Find the next coaching call on the calendar. Draft: the
week's numbers (leads, calls, evals, plans started, revenue if tracked), wins since the last
call, what they worked on, where they're stuck (using the stuck format), and 1 to 3 questions for
their coach. Email as a draft to the owner.

## Benchmark form prep (Foundations)

Welcome: Benchmark Check-Ins. Onboarding, 6-Week, Midpoint, 6-Month, Graduation. Pull numbers
since they started (discovery calls, evals, revenue, monthly trend) and draft answers. Email as a
draft.

## End-of-week KPI post (Friday)

Draft the weekly Circle post: what went well, what didn't, what needs to change. Owner's voice,
honest and kind, clients by initials. Message the owner the draft.

## Weekly numbers report (Friday)

Phase 2: Data Tracking. One short report on Instagram, website and Google Business Profile.
GHL users can pull Instagram stats through GHL. No Google Analytics or Business Profile connector
exists yet, so ask the owner to drop in screenshots or exports, and read those. Report 3 to 5
numbers, one thing that worked, and "i'd do more of ___ next week." Under 8 lines.

## Admin and finance checklist (1st of the month)

Phase 5, Lesson 4: Monthly Admin and Finance Routine.
Walk through, one at a time, as a checklist the owner ticks off: unpaid invoices to follow up,
upcoming expenses, transfers to tax and profit savings (their percentages if set, Profit First
style), revenue for the month, update the tracker, set next month's goals. GoniBot reminds and
asks; the owner does every money move.

## Mid-month pace check (around the 15th)

A quick, kind look at where the month stands so the EOM is never a surprise: leads, calls, evals
and sales so far compared to their own monthly goal, read against the 90-day runway (this month's
leads came from what they did three months ago). Check back on the one thing in `logs/focus.md`.
End with one small step for the second half of the month. Not weekly, to avoid overload.

## Weekly project review (CEO Club)

CEO Club Project Management module. Read their project hub (Notion or wherever the profile
says). List projects in motion, what moved, what's stuck, next milestone. 15 minutes. Ask which
one gets their CEO time next week.

## EOQ data prep (CEO Club)

CEO Club EOQ review. Gather the quarter's numbers month by month (revenue, leads, evals, plans,
average income per appointment, hours), flag missing months, and save a clean summary to the
notebook so the EOQ review starts with clean data. Don't write the review itself.

## Annual planning data pull (December, Foundations and Legacy)

Phase 7: Annual Planning With Data. Pull 12 months from the tracker into a summary covering top
marketing channels, best referral sources, conversion rates, average income per appointment,
customer lifetime value if trackable, and time by bucket. Save to the notebook. Suggest they
bring it to their coach.
