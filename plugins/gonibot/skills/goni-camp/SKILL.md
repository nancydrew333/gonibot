---
name: goni-camp
description: "GoniBot's Training Camp, a one-week program to build a practice home base. This skill should be used when the owner types \"/goni-camp\", taps \"Training Camp\", or says \"training camp\", \"everything is everywhere\", \"I can't find anything\", \"build my home base\", \"organize my links\", or \"camp check-in\". Over five days GoniBot collects every tool and link the owner uses, then builds one home base page they link from their student dashboard."
metadata:
  version: "0.1.0"
---

# /goni-camp (Training Camp)

Load **goni-core** first. For owners who feel like everything is everywhere. Morgan already
recommends an intranet-style page with links to everything for the CEO self-check; Training Camp
builds it with them.

Check `camp.md` in the notebook first. If camp is in progress, skip to the right day.

## Day 0: Kickoff

Welcome them, in GoniBot's voice: "welcome to training camp! for the next 5 days, just tell me at
the end of the day what you worked on and what you used. by friday i'll build you one page with
everything on it."

- Create `camp.md` with a start date.
- Offer to schedule a daily end-of-day check-in for 5 days (or fold it into `/goni-wrap` if they
  use it).
- Ask where they want the home base: **Notion** (default, built through the Notion connector) or,
  for owners comfortable with tech, a small dashboard in Claude Code, or a Google Doc.

## Days 1 to 5: Report in

Each check-in: "what did you work on today, and what did you use?" Tools, logins, docs,
spreadsheets, forms, folders. A voice note is fine.

- Pull out each tool or link. Ask for the URL only if it's missing and it matters.
- Sort as you go, by how they actually work:
  - **Daily:** Power Hour, CRM, inbox, calendar, scheduling, messaging
  - **Weekly:** Weekly Reset, content tools, outreach lists, social scheduler
  - **Monthly:** data tracker, EOM report form, finances and bookkeeping, content calendar
  - **SOPs and how-tos:** SOP library, policies and procedures manual, GoniBot's `sops/`
  - **Client delivery:** booking link, intake forms, exercise program platform, EMR login link
  - **DPT to CEO:** dashboard, courses, Circle, coaching folder, Prep and Reflect, EOM form
- Log each day in `camp.md`. Keep each check-in under 5 minutes.
- If they miss a day, no guilt. Pick up the next day; camp can stretch to 7.

## Graduation day: Build the home base

1. Show the sorted list and ask if anything is missing (bank login pages, the review link, the
   lead magnet link).
2. Build the page (with their yes): title "<Practice name> HQ", a short "start here" line, then
   one section per group above, each link labeled in plain words.
3. **No patient information on the home base.** A link to the EMR login is fine; notes, patient
   lists and anything clinical are not. Never store passwords on the page; suggest a password
   manager instead.
4. Notion: create the page through the Notion connector in the workspace they choose. Google Doc
   or a markdown file in the GoniBot folder works as a fallback.

## Link it in the dashboard

Walk them through adding the home base link to their DPT to CEO student dashboard
(dash.dpttoceo.com) so everything is one click away. If they're not sure where it goes, suggest
asking in the Tech Support space or checking the dashboard's "How to use my dashboard" page
(Settings, Instructions).

## Close

They've earned **Camp Graduate** once the home base is linked in the dashboard. Announce with the
claim steps. Suggest a 10-minute monthly tidy (add new tools, remove old ones), and offer to add
it to the admin and finance checklist.
