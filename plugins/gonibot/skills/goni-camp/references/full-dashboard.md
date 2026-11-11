# Level 3: the full home base dashboard

For owners who picked hard, or said "level up my HQ". The goal: their links and their numbers in
one place, on a page they keep building over time. Go one step at a time and check in after each.
Short, warm, GoniBot's voice to the owner throughout.

## Ground rules for the dashboard

- **No patient information.** Counts and totals only. No names, notes, diagnoses or visit
  details. Lead first names are fine on the follow-up list; clients after they book show as
  counts.
- **No passwords or logins** on the page.
- **Kind numbers.** Show pace and trends, never red alarms. A gap is "2 evals to go", never a
  miss. Don't compare them to other students.
- **Goals are theirs.** Use goals from their own plan (EOQ game plan, coaching notes). GoniBot
  doesn't set revenue, pricing or capacity targets; those questions go to their coach.
- **One tracker.** Use the DPT to CEO data tracker they already fill in. Don't start a new
  tracking system.

## Step 1: Start from the smart bookmark page

Build (or reuse) the easy page first. The links move to the top or a side panel; the numbers
go below. Same link, same file.

## Step 2: Pick where it's built

Ask which fits them:

- **In Claude (Cowork or claude.ai):** if the Artifact tool lists a dashboard (Data) type, build
  from it. Otherwise build one HTML page and publish it as a Claude page. Easiest to update by
  asking GoniBot.
- **In Claude Code:** build a small project in a `home-base/` folder inside their GoniBot folder
  (one `index.html`, plus a `data/` folder for exported numbers). They can open it locally, or
  publish it as a Claude page to get a link for the student dashboard. Best for owners who want
  to keep adding features themselves.

Save the link and folder path in `camp.md`.

**Building in Claude Code?** Don't hand the owner a blank template. Follow
`claude-code-prompt.md`: ask the readiness questions, fill in the prompt from the practice
profile and `camp.md`, save it as `home-base/claude-code-prompt.md`, and walk them through
pasting it.

## Step 3: Pick how the numbers get in

Easiest first. Each number on the page shows where it came from and when it was last updated.

1. **They paste the month's numbers** to GoniBot (or GoniBot pulls them from their EOM report),
   and GoniBot updates the page.
2. **GoniBot reads the data tracker** through the Google Sheets connector, then updates the page.
3. **A CSV export** of the tracker saved in `home-base/data/`, which the page reads.

Live, always-on connections are an advanced add-on; don't start there.

## Step 4: Pick 2 or 3 sections to start

Offer this menu. Use the program's words. Add more later, one at a time.

**Sales**
- Leads this month
- Discovery (or "sniff") calls booked
- Evals booked and completed
- Eval to plan of care conversion
- Packages and memberships sold
- Revenue this month vs their goal, with days left in the month
- Average revenue per new client

**Marketing**
- Leads by source, in their words (referral partners, Instagram, events, past clients)
- Follow-ups sent this week, and who's waiting to hear back (lead first names only)
- 100 Challenge or outreach count
- Posts this week, new Google reviews
- Email list size and lead magnet downloads

**Capacity**
- Visits booked this week vs their max
- Open spots this week (handy on slow weeks, pairs with `/gonibot:goni-fetch`)
- Active clients

**The wave**
- Revenue for the last 6 to 12 months as a simple line, so they can watch the wave shrink

**This week**
- Big 3, follow-ups due, next Power Hour, next coaching call

## Step 5: Keep it fresh

- Offer a monthly numbers refresh right after their EOM report (or fold it into the EOM duty if
  that's on). Ask before scheduling anything.
- The 10-minute monthly link tidy still applies.

## Step 6: Keep building

For ideas, use `dashboard-ideas.md` (offer 2 or 3 that fit). They can ask for new sections or
features any time ("add a referral partner list", "show my
reviews over time"). Add one at a time, keep the same link, and log each change in `camp.md`.
If a request needs patient data, say kindly that the dashboard stays patient-free and offer a
count instead.
