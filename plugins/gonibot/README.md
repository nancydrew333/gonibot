# GoniBot, your first hire

A Claude Cowork plugin for DPT to CEO practice owners (Foundations from Phase 5 on, Legacy and CEO
Club). GoniBot works like a first admin hire: it learns how the practice runs, takes repetitive
admin off the owner's plate, and hands everything back as drafts for a quick review. About 2 to 5
hours back a week.

Named after Morgan Meese's dog Goni. Student guide: https://dash.dpttoceo.com/gonibot.html

## Tricks (slash commands)

| Trick | Dashboard label | What it does |
|---|---|---|
| `/gonibot:goni-interview` | | The 30-minute hiring interview. Start here. |
| `/gonibot:goni-morning` | | Guided start of the day (10, 20 or 45 minutes) with a Big 3 |
| `/gonibot:goni-brief` | Start my week | Monday brief: follow-ups first, recap, Big 3 |
| `/gonibot:goni-wrap` | | Guided end of day: lead log, wins, tomorrow |
| `/gonibot:goni-boost` | Pick-me-up | A highlight reel of real wins for rough weeks, pulled from the notebook, Prep and Reflect, EOM reports, Share Your Wins, and what coaches have said |
| `/gonibot:goni-snuffle` | Snuffle Mat | Guided lead gen self-audit: find the leak, pick one thing |
| `/gonibot:goni-stay` | Busy week | Shrink the week to the essentials, plan re-entry |
| `/gonibot:goni-fetch` | Slow week | Turn open time into outreach and content |
| `/gonibot:goni-camp` | Training Camp | One week to build a practice home base |
| `/gonibot:goni-train` | | Teach GoniBot a new trick (writes an SOP), first-hire kit |
| `/gonibot:goni-hours` | | See the time handed off and what to hand off next |
| `/gonibot:goni-log` | | Optional two-week time audit |

## Behind the scenes

| Skill | Purpose |
|---|---|
| goni-core | Personality, voice, ground rules, notebook, duties catalog, badges, Roadmap links |
| goni-leads | Power Hour list, follow-ups, inbox triage, lead log, call prep, hesitations, FAQ |
| goni-content | Content batch, GBP post, review asks, Friday wins, content calendar, events, nurture emails |
| goni-outreach | Outreach list, 100 Challenge, referral partners, past-client reactivation |
| goni-reports | EOM, Prep and Reflect, benchmarks, KPI post, numbers report, admin checklist, pace check, EOQ, annual data |

Scheduled duties are created per owner during `/gonibot:goni-interview` and `/gonibot:goni-train`, one at a time.

## Setup for students

1. Claude Pro (or higher) and the Claude desktop app.
2. Install GoniBot: in the desktop app, **Customize**, then **Plugins**, then **Add marketplace**,
   paste `nancydrew333/gonibot`, install **gonibot**, and turn on **Sync automatically**.
3. Connect Gmail, Google Calendar and Google Drive in Claude (**Customize**, then
   **Connectors**). Optional: GHL, Notion, TickTick or Todoist. The Toy Bin on the dashboard
   has step-by-step instructions.
4. Make a GoniBot folder (for example Documents/GoniBot) and set it on the dashboard under
   Settings, GoniBot, so tricks open in it. This is where GoniBot keeps its notebook.
5. Run `/gonibot:goni-interview`. Every other trick and duty unlocks once the interview is done.

Scheduled duties run while the computer is on and the Claude desktop app is open, because
GoniBot's notebook lives in a folder on the owner's computer.

## Ground rules

Nothing goes out without the owner. No patient records or EMR access. No phones and no money
moves. Forms stay the owner's (answers are emailed as drafts). Pricing, capacity and hiring go to
the coach.

## Changelog

- **November 2026:** tricks are now written with their full plugin name (`/gonibot:goni-interview`),
  which is how Claude names plugin skills. Typing `/gonibot` shows them all.
- **November 2026:** new `/gonibot:goni-eom` trick. GoniBot pulls the month's numbers, asks the
  reflection questions one at a time, and drafts a Google Doc in the same order as the End of
  Month Report form, ready to paste.
- **October 2026, launch:** GoniBot is installed from the `dpt-to-ceo` marketplace
  (github.com/nancydrew333/gonibot) and updates automatically. The interview is now required
  before any other trick or duty runs, including Pick-me-up. The interview checks that Gmail,
  Calendar and Drive are connected first and points to the Toy Bin if they aren't. GHL now
  connects through HighLevel's own Claude connector.
- **0.1.2:** GoniBot's voice is now Goni's own (a loyal sidekick with a little dog flavor), and
  Pick-me-up pulls wins from Prep and Reflect, EOM reports, Share Your Wins, and coach comments.
- **0.1.0:** first build.
