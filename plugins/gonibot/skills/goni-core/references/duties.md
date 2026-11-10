# GoniBot's duties

Every job GoniBot can do on a schedule, which skill runs it, and who it's for.
Programs: F = Foundations (Phase 5 on), L = Legacy, C = CEO Club. "All" = F, L and C.

## Daily

| Duty | When | Skill | What GoniBot does | Owner's part | Programs |
|---|---|---|---|---|---|
| Power Hour list | Weekdays, owner's Power Hour time (default 7:00am) | goni-leads (also inside `/goni-morning`) | Reads calendar, inbox, task list and tracker, lists today's top 3 business tasks | Reads it in 2 minutes, picks where to start | All |
| Lead follow-ups and pipeline check | Weekdays 7:00am | goni-leads | Finds leads with no reply in 2+ days (GHL: conversations inbox incl. Instagram/Facebook DMs, plus open opportunities), drafts a follow-up for each | Edits if needed, sends | All |
| Inbox triage | Weekdays noon | goni-leads | Labels new inquiries, flags urgent ones, drafts replies to common questions | Approves or tweaks drafts | All |
| Lead log | Weekdays 6:00pm (also inside `/goni-wrap`) | goni-leads | Asks who reached out today and from where, adds it to the lead log and tracker | Answers in a sentence or voice note | All |

## Weekly

| Duty | When | Skill | What GoniBot does | Programs |
|---|---|---|---|---|
| Weekly Reset brief | Mon 7:30am (or `/goni-brief`) | goni-brief | Follow-ups first, then last week recap, anything stuck, suggested Big 3 | All |
| Calendar guard | Mon 7:30am, inside the brief | goni-brief | Suggests Power Hour and CEO time blocks, flags weeks where clinical hours crowd them out | All |
| Content batch | Mon, after the owner's voice note | goni-content | One voice note into 3 to 5 posts, captions and stories, plus a newsletter draft (Waterfall Method) | All |
| Google Business Profile post | Mon, with the content batch | goni-content | Turns the voice note into a short GBP post | All |
| Outreach list | Wed 7:30am | goni-outreach | Short list of past clients, referral partners and warm leads, a drafted message for each | All |
| 100 Challenge tracker | Wed | goni-outreach | Counts touches toward the 100, drafts the next batch | F |
| Review asks | Thu 7:30am | goni-content | Drafts review or testimonial asks for clients the owner names as wins | All |
| End-of-week KPI post (opt-in) | Fri 2:00pm | goni-reports | Drafts the weekly KPI post for Circle | All |
| Friday wins | Fri 3:00pm | goni-content | Pulls the week's wins into a short Circle post | All |
| Weekly numbers report | Fri 3:00pm | goni-reports | Instagram, website and GBP numbers, what to do more of (screenshots fine) | All |
| Weekly project review | Fri | goni-reports | 15-minute weekly project review against the project hub | C |

## Monthly

| Duty | When | Skill | What GoniBot does | Programs |
|---|---|---|---|---|
| Admin and finance checklist | 1st of the month | goni-reports | Walks through unpaid invoices, upcoming expenses, transfers to tax and savings | All |
| Mid-month pace check | Around the 15th | goni-reports | A kind look at where the month stands; checks back on the one thing from Snuffle Mat | All |
| Referral partner nurture | Mid-month | goni-outreach | Drafts a monthly check-in for each referral partner | All |
| Past-client reactivation list | Monthly | goni-outreach | 30 to 90 day check-ins for past clients the owner names, first names only | All |
| Content calendar | Last week of the month | goni-content | Next month's themes, promotions and email topics from goals | All |
| EOM report prep (opt-in) | Last 2 days of the month | goni-reports | Reads the tracker, does the math, emails every EOM answer as a draft | All |
| Hours check | End of month (or `/goni-hours`) | goni-hours | Hours handed off versus the starting estimate | All |
| EOQ data prep (opt-in) | End of each quarter | goni-reports | Gathers the quarter's numbers for the EOQ review | C |
| Annual planning data pull | December | goni-reports | 12 months from the tracker into a summary | F, L |

## As needed

| Duty | When | Skill | Programs |
|---|---|---|---|
| Prep and Reflect pre-fill (opt-in) | 24 hours before each coaching call | goni-reports | All |
| Benchmark form prep (opt-in) | Before each benchmark | goni-reports | F |
| Discovery call prep | Before each discovery call | goni-leads | All |
| Hesitation follow-ups | After a call that didn't book | goni-leads | All |
| Sales Gym nudge | After a call that didn't book | goni-leads | All |
| FAQ library | As questions repeat | goni-leads | All |
| Event assistant | When planning an event | goni-content | All |
| Email nurture builder | When launching a lead magnet | goni-content | F |
| First-hire kit | When ready to hire | goni-train | L, C |
| Busy-week mode | `/goni-stay` | goni-stay | All |
| Slow-week mode | `/goni-fetch` | goni-fetch | All |
| Training Camp | `/goni-camp` | goni-camp | All |
| Pick-me-up | `/goni-boost` | goni-boost | All |

## Switching a duty on

Duties unlock one at a time, never all at once. Start with the 2 or 3 the owner picks in the
hiring report. Before a duty switches on:

1. Write its SOP with `/goni-train` (4 to 5 questions). A short SOP is fine.
2. Schedule it (below).
3. Add or update its row in the notebook's `duties.md` (on, schedule, task name, runs reviewed 0).
4. If this is the owner's first duty, they've earned **First Fetch** (see badges.md).

## Scheduling a duty

Use Cowork's scheduled task feature to create one task per duty. If a scheduling tool is
available in this session, create the task directly after the owner says yes to the time. If not,
walk the owner through adding it from Scheduled in the Claude desktop app sidebar, and give them
the exact prompt to paste.

- **Name:** "GoniBot: <duty name>" (for example "GoniBot: Power Hour list")
- **Schedule:** the time from the table, adjusted to the owner's schedule and time zone. Skip
  their days off.
- **Prompt (copy exactly, filling in the duty):**
  "Run GoniBot's <duty name> duty. Load the goni-core skill first, read my practice profile and
  duties list in my GoniBot notebook, then follow the <skill name> skill for this duty. Drafts
  only, nothing gets sent."
- **Folder:** attach the owner's GoniBot folder if they have one, so the notebook is available.

Tell the owner once: scheduled duties only run while the computer is on and the Claude desktop
app is open, so a desk computer that stays on works best. If a run is missed, GoniBot picks up at
the next one. Nothing to catch up on.

## Switching a duty off

If the owner says a duty isn't helping, pause it (disable the scheduled task or walk them through
it), mark it "off" in `duties.md` with a one-line reason, and don't bring it up again unless they
ask.
