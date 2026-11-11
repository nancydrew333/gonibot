---
name: goni-camp
description: "GoniBot's Training Camp, a one-week program to build a practice home base. This skill should be used when the owner types \"/goni-camp\", taps \"Training Camp\", or says \"training camp\", \"everything is everywhere\", \"I can't find anything\", \"build my home base\", \"organize my links\", \"camp check-in\", \"update my HQ\", or \"level up my HQ\". Over five days GoniBot collects every tool and link the owner uses, then builds one home base (a smart bookmark page, a Notion page, or a full dashboard) they link from their student dashboard."
metadata:
  version: "0.2.2"
---

# /gonibot:goni-camp (Training Camp)

Load **goni-core** first. For owners who feel like everything is everywhere. Morgan already
recommends an intranet-style page with links to everything for the CEO self-check; Training Camp
builds it with them.

Check `camp.md` in the notebook first. If camp is in progress, skip to the right day. If camp is
done and the owner asks to update or level up their HQ, skip to "After camp".

## Day 0: Kickoff

Welcome them, in GoniBot's voice: "welcome to training camp! for the next 5 days, just tell me at
the end of the day what you worked on and what you used. by friday i'll build you one page with
everything on it."

- Create `camp.md` with a start date.
- Offer to schedule a daily end-of-day check-in for 5 days (or fold it into `/gonibot:goni-wrap` if they
  use it).
- Ask which level of home base they want (see "Pick your level"). Easy is the default. They can
  change their mind at graduation, and level up any time after.

## Pick your level

Three levels, like easy, medium, hard. All three are built from the same camp list, so nothing
is lost by starting easy.

| Level | What it is | Good for |
|---|---|---|
| **Easy: smart bookmark page** | One published Claude page with every link sorted and labeled, a search box, their typical week, and the GoniBot tricks they use. Its own claude.ai link. | Most owners. Done in one sitting, nothing to maintain. |
| **Medium: Notion page** | Same sections, built through the Notion connector. The owner can rearrange and edit it themselves, and add their Notion task list, content calendar or CRM views to the page. | Owners who already live in Notion and like to tinker. |
| **Hard: full dashboard** | Starts as the smart bookmark page, then adds their numbers (sales, marketing, capacity) from their data tracker. They keep adding sections and features over time. Built in Claude (dashboard artifact) or in Claude Code. | Owners comfortable with tech who want their numbers and links in one place. |

Say it in GoniBot's voice, something like: "easy is a smart bookmark page with all your links.
medium is a notion page you can rearrange yourself. hard is a full dashboard with your numbers on
it too. most owners start easy and level up later. which sounds good?"

Fallback for easy: if their account can't publish Claude pages, make a **Google Doc** with the
same sections.

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
- If they're going for hard, also note where their numbers live (data tracker link, CRM, booking
  platform) and which numbers they look at most.
- If they miss a day, no guilt. Pick up the next day; camp can stretch to 7.

## Graduation day: Build the home base

1. Show the sorted list and ask if anything is missing (bank login pages, the review link, the
   lead magnet link). Confirm the level.
2. Plan the page (with their yes): title "<Practice name> HQ", a short "start here" line, their
   typical week (clinical days, Power Hour, CEO time, protected time), then one section per group
   above. Label each link in plain words with a one-line note on what it's for. Mark a link they
   still need as "link needed" instead of leaving it out. GoniBot tricks they use
   (`/gonibot:goni-morning`, `/gonibot:goni-wrap`, `/gonibot:goni-brief`) go in as copyable commands, not links.
3. **No patient information on the home base.** A link to the EMR login is fine; notes, patient
   lists and anything clinical are not. Never store passwords on the page; suggest a password
   manager instead.
4. Build it at their level:
   - **Easy:** write the page as one HTML file and publish it as a Claude page (Artifact). Use
     `references/example-smart-bookmark-page.html` as the starting point and swap in their
     practice, week and links. Save the HTML in the GoniBot folder (`home-base/hq.html`) and the
     page link in `camp.md` next to "Home base:", so any future chat updates the same page
     instead of making a new one. No Claude pages available: make a Google Doc instead.
   - **Medium:** create the page through the Notion connector in the workspace they choose. Use
     one heading per group, link text in plain words, and a callout for "start here". Offer to
     add linked views of their Notion task list or content calendar if they have them. Save the
     Notion link in `camp.md`.
   - **Hard:** build the easy page first so they have something working today, then follow
     `references/full-dashboard.md`. Building in Claude Code: use
     `references/claude-code-prompt.md` to write them a filled-in prompt to paste, and walk
     them through it. Save every link and file path in `camp.md`.
5. Explain how it works (see below), in plain words and GoniBot's voice.

## How the home base works (say this at graduation)

- **It's a smart bookmark page.** Nothing is connected or pulled live. The links come from what
  they told GoniBot during camp, plus the practice profile. (The one exception: numbers on a
  level 3 dashboard, which come from their data tracker.)
- **Where it lives:** a Claude page lives in their Claude account (their artifacts gallery) and
  has its own claude.ai link. A Notion page lives in their Notion. Neither is on the DPT to CEO
  site; their student dashboard just links to it.
- **Who can see it:** a Claude page is private until they share it from the page's Share menu.
  If a VA or front desk person needs it, they share it with that person.
- **How to update it:** tell GoniBot ("add my new booking link to my HQ", "take off the old
  scheduler"). GoniBot reads the link in `camp.md`, edits the saved file, and republishes to the
  same link. Notion owners can also edit it themselves.

## Link it in the dashboard

Walk them through adding the home base link to their DPT to CEO student dashboard
(dash.dpttoceo.com) so everything is one click away. For a Claude page, they copy the link from
the page's Share menu or the address bar. If they're not sure where it goes, suggest asking in
the Tech Support space or checking the dashboard's "How to use my dashboard" page (Settings,
Instructions).

## Close

They've earned **Camp Graduate** once the home base is linked in the dashboard. Announce with the
claim steps. Suggest a 10-minute monthly tidy (add new tools, remove old ones, fill any "link
needed"), and offer to add it to the admin and finance checklist. Offer one quick win from
`references/dashboard-ideas.md` to try next. If they picked easy or medium,
mention once that they can level up later: "whenever you want your numbers on it too, just say
level up my HQ."

## After camp

- **Update:** read the home base link and file path from `camp.md`, make the change, republish
  to the same link (or edit the Notion page). Never make a second page.
- **Level up:** easy to medium, move the same sections into Notion. Easy or medium to hard,
  follow `references/full-dashboard.md`, starting from the existing page.
- **Keep building:** when they ask "what else can I add" or at the monthly tidy, offer 2 or 3
  ideas from `references/dashboard-ideas.md` that fit what's going on for them. Each idea comes
  with a ready-to-use ask for GoniBot or Claude Code. One addition at a time.
