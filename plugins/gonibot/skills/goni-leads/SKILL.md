---
name: goni-leads
description: "GoniBot's lead and inbox duties. This skill should be used when a GoniBot scheduled task or the owner asks for the \"Power Hour list\", \"lead follow-ups\", \"pipeline check\", \"who do I need to follow up with\", \"inbox triage\", \"sort my inbox\", \"lead log\", \"who reached out today\", \"discovery call prep\", \"hesitation follow-ups\", \"they didn't book\", \"Sales Gym nudge\", or \"FAQ library\" / \"saved replies\". Requires the goni-core skill to be loaded first."
metadata:
  version: "0.1.0"
---

# GoniBot lead duties

Load **goni-core** first and follow its voice, ground rules and notebook steps. All drafts are in
the owner's voice (goni-core `references/owner-voice.md`). Nothing gets sent.

Find leads wherever the owner keeps them (from `practice-profile.md`, "CRM"):
- **GHL:** conversations inbox (includes Instagram and Facebook DMs) and open pipeline
  opportunities. New leads and open opportunities only; skip existing patients' threads.
- **Google Sheet CRM:** read it through Google Drive.
- **Dashboard CRM:** no connector yet. Ask the owner to paste or screenshot the lead list, or
  read an exported sheet if they keep one.
- **Gmail:** inquiries in the inbox from the last 7 days.
- **Notion CRM:** query the database they named.

If nothing is connected, ask: "who's waiting to hear back from you? first names and where they
reached out is plenty."

## Power Hour list

Phase 5, Lesson 2: Daily Power Hour.
1. Read today's calendar (every calendar listed in the profile, minus any they skip), the inbox
   for new inquiries, open tasks from their task list, and the lead list.
2. Pick the **top 3 business tasks** for today. Priority order: anyone waiting on a reply, then
   the one thing from `logs/focus.md` if any, then content or outreach that's due, then the Big 3
   from the week's brief.
3. Fit the list to the day. If the calendar is packed with clinical hours, offer a 20 or 30
   minute version.
4. Message (GoniBot voice): a greeting, the 3 tasks as a numbered list with drafts noted as
   ready, and "i'd probably start with ___" plus why in a few words.

## Lead follow-ups and pipeline check

Phase 3: Developing Your Sales Process. Phase 5, Lesson 6: Build Your CRM.
1. Find every lead with no reply from the owner in 2+ days, and open opportunities with no touch
   in 7+ days.
2. For each, check how many touches they've had (CRM notes, thread history). Leads usually
   convert between the 3rd and 7th follow-up, so a quiet lead isn't a lost lead.
3. Draft a follow-up per lead in the owner's voice. Each touch gives something: a question
   about them, a quick tip, a link, or the next back pocket offer down if they hesitated
   (eval, discovery call, lead magnet, follow me).
4. Email leads: Gmail drafts. DM or GHL leads: drafts in the chat, first name above each.
5. Message: how many people are waiting, drafts ready, who to send first. Never frame the count
   as a problem.

## Inbox triage

Phase 5, Lesson 6: Build Your CRM.
1. Scan unread Gmail from the last 24 hours (or since the last run).
2. Sort into: new inquiry, urgent (time-sensitive or upset person), common question, everything
   else. Apply Gmail labels only if the owner has said yes to labels (ask once, note in profile).
3. Draft replies to common questions (pricing, location, superbills, what to expect, insurance)
   using the FAQ library in the notebook if it exists.
4. Report in 2 to 4 lines: urgent first, then drafts ready, then anything only they can answer.

## Lead log

Phase 2: Data Tracking.
1. Ask: "who reached out today and from where?" A sentence or voice note is fine.
2. Explain on the spot what counts if they hesitate: a lead is anyone whose info is now in their
   world (the big four: name, email, phone, Instagram). Everybody counts: providers, past
   clients, friends, neighbors. A connection is any outbound touch related to the business.
3. Add each lead to `logs/lead-log.md` (date, first name or initials, source, what they asked
   about) and to the CRM if connected and the owner says yes.
4. Tally the week so far and remind them it rolls into the tracker at month end.

## Discovery call prep

Phase 3: Cold Lead Sales and Developing Your Sales Process.
Write a one-page brief before a discovery call: who they are (first name, source), what they
said in their inquiry in their own words, 3 to 5 suggested questions (open-ended, about the
emotional driver: why now, what it's costing them), the three-part call structure (pre-frame,
listen and summarize, present and close on the eval), and the back pocket offer to drop to if
they hesitate. Keep it under one screen.

## Hesitation follow-ups and Sales Gym nudge

Phase 3: Handling Hesitations. Phase 3: Train in the DTC Sales Gym.
After a call that didn't book:
1. Ask what they said ("too expensive", "talk to my spouse", "think about it", timing).
2. Draft a follow-up that validates the hesitation and offers one next step, with a set time to
   reconnect. Never "okay, let me know!"
3. Suggest the matching Sales Gym lab: DM Lab (DM conversations), Social Conversion Lab,
   Discovery Call Lab (most hesitations on calls), Evaluation Pitch Lab (said no after an eval).
   One line, as an offer, not homework.

## FAQ library

Phase 5, Lesson 6: Build Your CRM.
When the same question shows up 3 or more times in inquiries, draft a saved reply in the owner's
voice and offer to add it to `faq-library.md` in the notebook. Use the library during inbox
triage.
