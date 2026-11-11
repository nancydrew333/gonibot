---
name: goni-eom
description: "GoniBot's end of month report trick. This skill should be used when the owner types \"/goni-eom\", taps \"EOM report\", or says \"do my EOM\", \"end of month report\", \"EOM prep\", \"fill out my EOM\", or when the GoniBot EOM scheduled task runs (last 2 days of the month). Pulls the month's numbers from the owner's connected tools, asks the reflection questions one at a time, and writes every answer into a Google Doc in the same order as the DPT to CEO End of Month Report form, ready to paste. Requires goni-core first."
metadata:
  version: "0.1.0"
---

# GoniBot EOM report

Load **goni-core** first and read the practice profile. This trick does the boring half of the End of Month Report (pulling and adding up the numbers) and leaves the thinking to the owner. The output is a Google Doc with every form question in order and an answer under each, so they can paste it into the Notion form in about 10 minutes.

**Never submit the form.** GoniBot drafts, the owner pastes and submits. The report is due by the end of the day on the 1st.

## Step 1: Say hi and set expectations

One short message in GoniBot's voice: "ok, EOM time. i'll grab your numbers first, then ask you a few questions. voice notes are totally fine. about 15 minutes." Then get started.

## Step 2: Connect what we can

Check connectors (see goni-core). For each one that's missing, say in one line what it would fill in, then keep going with what's there.

| Connector | What it fills in |
|---|---|
| Google Drive / Sheets | Their data tracker (link in the profile): revenue, expenses, appointments, calls, leads, touchpoints. Also where the finished doc gets saved. |
| Google Calendar | Total appointments and discovery calls / evals booked, if they're not in the tracker |
| GHL (if they use it) | Discovery calls and evals booked, showed, closed; new leads; lead sources |
| Gmail | Reviews and testimonials received; Stripe, Square or Jane payment emails if revenue isn't in the tracker |
| Notion | Last month's EOM answers, to compare (only if they've shared it) |

**The tracker comes first.** The form says the data tracker must be updated before the report. If this month's tracker row is blank or half done, offer to fill it with them first: ask for the missing numbers in one batch, then write them into their tracker only after they say yes.

No EMR access, ever (goni-core ground rules). For appointment counts, use the calendar or ask.

## Step 3: Pull and calculate

Use the metric names from their own tracker. Show the math whenever you calculate:
- Profit = revenue − expenses; margin = profit ÷ revenue (the form asks for both a $ and a %)
- Average income per appointment = revenue ÷ total appointments
- Show rate = showed ÷ booked; close rate = closed ÷ showed

Don't guess a blank. If a number isn't anywhere, put it on the question list. "not tracked this month" is a fine answer; imperfect data beats no data.

Compare to their own goals and their own last month only. Never to other students. Lead with what moved in the right direction. Never frame a number as a shortfall or a failure.

## Step 4: Ask the questions

Ask **one at a time** (or two short ones together), in GoniBot's voice, and wait for each answer. Take voice-note answers as they come and clean up the typos, but keep their words. Before each one, offer a nudge from the data: "your top source looks like instagram (4 of 6 calls). does that match what you saw?"

The owner answers in their own words:
1. Primary marketing focus: online/digital, in person, or both
2. Strategy used: what did you actually do this month, with quantities (reels, DMs, gym convos, workshops, referral asks)?
3. Results of marketing: where did it start paying off? what dots did you connect?
4. Top 1–3 referral sources, with a count for each if you have it
5. Biggest win this month
6. Based on your data, what's working well and what could use an adjustment?
7. Top 1–3 priorities for the new month
8. CEO Self Check: 1–10, where 1 is "my heart just isn't in this" and 10 is "i'm showing up as the best version of myself." What score, and why? (**7 isn't allowed.** If they say 7, ask "6 or 8?" with a smile.)
9. Any questions for your coach?
10. Did you receive any reviews or testimonials? How many? Did you actively ask for them?

GoniBot can draft 2–6 from the data and their wins log (`logs/wins.md`) as a starting point, but always shows the draft and asks "does this sound like you?" Number 8 is never drafted: that one is theirs.

If the owner says they're having a rough month, don't push through the list. Offer `/gonibot:goni-boost` first, and remind them their coach would love to hear about it.

## Step 5: Write the Google Doc

Create the doc with Google Drive `create_file` (`contentMimeType: "text/html"` so headings and bold convert). Name it `EOM Report – [Month YYYY] – [First Last]`, and save it in the folder from the profile if there is one.

Write the questions in this exact order, matching the Notion form, with the question in bold and the answer as plain text under it. Leave a blank answer as "—" so nothing gets skipped when pasting.

1. Full Name
2. Email
3. Program (DPT to CEO / DTC Continuity/All Access / CEO Club)
4. Your Primary Coach
5. Link to data tracker
6. Total Revenue
7. Total Expenses
8. Total Profit ($ and margin %)
9. Total number of appointments
10. Average income per appointment
11. Discovery Calls or Consultations Booked (total number)
12. Evaluations or Sales Calls Booked (total number)
13. Evaluations or Sales Calls Showed (total number)
14. Evaluations or Sales Calls Closed (New Clients) (total number)
15. Total leads generated
16. Total connections/touchpoints
17. Did you receive any reviews/testimonials this month? (Yes / No)
18. If yes, how many?
19. Did you actively ask for reviews/testimonials? (Yes / No)
20. Primary marketing focus (Online/digital / In person / Both)
21. Strategy used
22. Results of marketing
23. What are your top 1–3 referral sources?
24. What was your biggest win this month?
25. Based on your data, what's working well? What could use improvement or adjustment?
26. What are your top 1–3 priorities going into the new month?
27. CEO Self Check: Are you showing up like the business owner you want to be?
28. Any questions for the coaches?
29. CEO Club students: EOQ Report link. Only in March, June, September and December, and only for CEO Club; otherwise write "not this month".
30. Mailing address update. Only if it changed; otherwise "no change".

Put the math under the numbers it applies to, in small italic text (e.g. "$8,450 − $2,310 = $6,140 profit, 72.7% margin"), so the owner can check it.

Name, email, program and coach come from the profile. Confirm them once; don't ask every month.

Fallback: if Drive isn't connected, put the same content in a Gmail draft to themselves with the subject `EOM Report – [Month]`. If Gmail isn't connected either, paste it in the chat in one block.

## Step 6: Hand it off

Short message in GoniBot's voice: the doc link, "it's in the same order as the form, so it's top to bottom copy and paste," the due date (end of day on the 1st), and the form link if it's in the profile. Then one line of what moved in the right direction this month.

Log the run in the notebook. For the first three runs, ask what to change and fold it into this duty's SOP (goni-core "Training").

## Scheduled duty

When switched on, schedule this for the 2nd-to-last day of each month, mid-morning in the owner's time zone. The scheduled run does Steps 2–3 and drafts the doc with the numbers filled in and the reflection questions left as prompts. Then it sends one nudge: "your EOM numbers are in your doc. just need your answers to a few questions, about 10 minutes."
