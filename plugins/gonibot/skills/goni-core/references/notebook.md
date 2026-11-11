# GoniBot's notebook (where memory lives)

GoniBot doesn't remember between chats on its own. Everything it needs to know about the practice
lives in a small set of files: the notebook.

## Where the notebook is

1. **Preferred: the owner's GoniBot folder on their computer.** The dashboard's Settings, then
   GoniBot page lets students set a GoniBot folder so every trick from the Goni button opens in
   it. If a folder is connected to this session, look there for a `GoniBot` notebook (or the
   files below at the folder's top level). Create the files there if they don't exist.
2. **If no folder is connected:** ask the owner to connect their GoniBot folder (any folder they
   like, for example Documents/GoniBot) and explain it takes one click to approve. If they'd
   rather not, fall back to Google Drive: keep a Drive folder named "GoniBot" and save new
   dated copies of files instead of editing (the Drive connector can create files but may not be
   able to update them). Always read the newest copy.
3. Never store notebook files only in this chat. A chat doesn't carry over.

## Files

| File | What's in it | Written by |
|---|---|---|
| `practice-profile.md` | Everything from the interview (see template below) | `/gonibot:goni-interview`, updated as things change |
| `voice-samples.md` | 3 to 5 samples of the owner's writing or speech, plus "Notes from edits" | `/gonibot:goni-interview`, every draft edit |
| `duties.md` | Each duty: on/off, schedule, scheduled task name, runs reviewed (0 to 3), trusted yes/no | `/gonibot:goni-interview`, `/gonibot:goni-train`, `/gonibot:goni-hours` |
| `sops/` | One SOP per duty or trick taught, named `sop-<duty>.md` | `/gonibot:goni-train` |
| `logs/lead-log.md` | Date, first name or initials, source, what they asked about (leads only) | `/gonibot:goni-wrap`, lead log duty |
| `logs/time-log.md` | Time audit entries by bucket | `/gonibot:goni-log` |
| `logs/wins.md` | Dated wins: evals booked, reviews, posts, first-evers, hours handed off | every trick that spots a win |
| `logs/hours.md` | Starting estimate per task and monthly hours check results | `/gonibot:goni-interview`, `/gonibot:goni-hours` |
| `logs/focus.md` | The one thing picked in Snuffle Mat, Stay or Fetch, with the check-back date | `/gonibot:goni-snuffle`, `/gonibot:goni-stay`, `/gonibot:goni-fetch` |
| `badges.md` | Badges announced (id, date) | any trick |
| `camp.md` | Training Camp day logs and collected links | `/gonibot:goni-camp` |
| `drafts/` | Dated copies of posts, newsletters and briefs | content duties |

Keep files short and skimmable. Newest entries at the top of logs. Never put patient health
information in any file (see ground rules).

## practice-profile.md template

The `interview:` line is what unlocks every other trick and duty (see goni-core, "Before any
trick or duty"). A profile written before this line existed counts as `done` if it already has the
practice name, offers and at least one voice sample; add the line the next time you save it.

```markdown
# Practice profile
interview: started / done
Last updated: YYYY-MM-DD

## The owner
- Name (what to call them):
- Practice name:
- Program: Foundations (phase _) / Legacy / CEO Club
- Coach:
- Time zone:
- Work computer stays on? (for scheduled duties):

## The practice
- Practice model (in-clinic, mobile, gym-based, telehealth, hybrid):
- Who they help (niche):
- Offers and prices (eval, packages, memberships, wellness):
- Back pocket offers ready? (eval / discovery call / lead magnet / follow me):
- Lead magnet (name + link):
- Booking link and how they prefer to book people:
- Google review link:
- Typical weekly schedule (clinical days and hours, Power Hour time, CEO time):
- Max visits per week they want:

## Systems
- CRM: dashboard CRM / Google Sheet (link) / GHL / other:
- Task list: Notion database (link) / TickTick / Todoist / GHL tasks / tell GoniBot:
- Data tracker (link):
- Roadmap or coaching folder (link):
- Email platform (Wix, Squarespace, ActiveCampaign, other):
- Calendars to read (and any to skip):
- Connectors set up: Gmail / Calendar / Drive / GHL / Notion / other:

## Lead sources
- Where leads come from most (in their words):

## What they want off their plate
- Dreaded tasks, with a rough weekly time guess for each:
- Starting estimate of weekly admin hours:

## Preferences
- Best time for the morning list:
- Days off / no-message days:
- Reporting helpers switched on (P&R, EOW, EOM, EOQ, benchmarks):
- Anything GoniBot should never do or say:
```

## duties.md template

```markdown
# Duties
| Duty | On? | Schedule | Scheduled task name | Runs reviewed | Trusted |
|---|---|---|---|---|---|
| Power Hour list | off | weekdays 7:00am | | 0 | no |
```

Add one row per duty as the owner switches it on. Use the duty names from `duties.md` in this
reference folder.
