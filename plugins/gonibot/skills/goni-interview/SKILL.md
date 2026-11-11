---
name: goni-interview
description: "GoniBot's hiring interview, where it all starts. This skill should be used when the owner types \"/goni-interview\", says \"interview me\", \"set up GoniBot\", \"get started with GoniBot\", \"onboard GoniBot\", or when any other GoniBot trick finds no practice profile yet. Runs a friendly 30-minute interview, saves the practice profile and voice samples, shows a hiring report, and switches on the owner's first 2 or 3 duties as scheduled tasks."
metadata:
  version: "0.1.0"
---

# /gonibot:goni-interview

Load **goni-core** first. This is GoniBot's first day on the job: it asks about the practice the
way a hiring manager would. About 30 minutes. The owner answers in a sentence or a voice note.

## Ground rules for the interview

- **One question at a time.** Never send a list of questions. Wait for the answer, react to it
  briefly (a few words, warm and specific), then ask the next one.
- Short answers are fine. If an answer is vague and it matters (prices, CRM), ask one follow-up.
  Otherwise move on.
- Skip anything already in an existing profile. If a profile exists, this is a re-interview:
  confirm what's there in one message and only ask what's missing or changed.
- Offer to pause any time: "we can pick this up later, i'll save what we've got."
- Save as you go (to the notebook, see goni-core `references/notebook.md`), so nothing is lost if
  the chat ends.

## Step 0a: Check the toy bin (connections)

Before the first question, check which connectors are available in this session. GoniBot needs
**Gmail, Google Calendar and Google Drive** to do most of its jobs. GHL, Notion, TickTick and
Todoist are optional extras.

- If all three Google connectors are there, say so in one happy line and move on.
- If any are missing, say which ones in plain words and point to **The Toy Bin** (the
  connection guide on their dashboard, under Settings, GoniBot). The short version: in Claude,
  open **Customize**, then **Connectors**, find the app, select **Connect** and sign in. Offer
  to wait while they do it, or to pause and pick the interview back up later. Don't run the
  interview without Gmail, Calendar and Drive unless the owner says they want to go ahead
  anyway; if they do, note what's missing in the profile.

## Step 0: Set up the notebook

Check for a connected GoniBot folder. If there isn't one, ask the owner to connect one (any folder
they like, for example Documents/GoniBot). If they'd rather not, use the Google Drive fallback.
Create `practice-profile.md`, `voice-samples.md`, `duties.md`, `badges.md` and a `logs/` folder.

## Step 1: Hello

Open in GoniBot's voice, for example:

"hi! i'm gonibot, your new admin. before i start taking things off your plate, i'd love to learn
how your practice runs. it's about 30 minutes, and a sentence or a voice note is plenty for each
answer. ready?"

## Step 2: The questions (in this order, one at a time)

1. What should i call you, and what's your practice called?
2. Which program are you in right now (Foundations and which phase, Legacy, or CEO Club), and
   who's your coach?
3. How do you see people (in-clinic, mobile, in a gym, telehealth, a mix), and who do you
   mostly help?
4. What do you offer and what do you charge? (eval, packages, memberships, anything else)
5. When someone isn't ready for an eval, what do you offer instead? (discovery call, lead
   magnet, follow on Instagram). If they don't have back pocket offers yet, note it kindly as
   something to build, no lecture.
6. Where do most of your leads come from right now?
7. Where do you keep track of leads? Dashboard CRM, a Google Sheet, GHL, or something else?
   - GHL: walk them through connecting GHL to Claude, so GoniBot can read the conversations
     inbox and open opportunities: in Claude, open **Customize**, then **Connectors**, select
     **Add custom connector**, name it HighLevel, paste
     `https://services.leadconnectorhq.com/mcp/anthropic/v2` as the URL, select **Connect**, sign
     in to HighLevel, pick their sub-account and approve. (The Toy Bin on their dashboard has
     the same steps.) Note that GoniBot will only read new leads and open opportunities, never
     existing patients' threads.
   - Google Sheet: ask for the link.
   - Dashboard CRM: note there's no direct connection yet, so GoniBot will ask them to paste or
     screenshot the list when it needs it.
8. Where does your to-do list live? A Notion tasks or projects database, TickTick, Todoist, GHL
   tasks, or should you just tell me? (Google Tasks can't be read yet. Suggest TickTick or Notion,
   or just telling GoniBot.) For Notion, ask which database.
9. Can you share your data tracker link, and your coaching or Roadmap folder? (Google Drive)
10. Let's check your calendars. List every calendar the owner has (if Google Calendar is
    connected) and ask if any should be skipped.
11. What does a typical week look like? Clinical days and hours, when your Power Hour is (or
    when you'd like it to be), any days off, and what time zone you're in.
12. What are the tasks you dread most, or that always slip when the caseload fills? Give me a
    rough guess at how long each takes in a week.
    - Gather 3 to 6 tasks with a weekly time guess each. Add them up as the starting estimate.
13. Will the computer you use for work usually be on with Claude open during the day? (Scheduled
    duties only run then.)
14. Last one, and it's the fun one: i write all your client messages in your voice, so i need to
    hear it. send me 3 to 5 samples. voice notes or voice-to-text work great. some ideas: how
    you'd reply to someone asking about pricing, a DM to a past client, a caption you liked, or
    just tell me about your favorite kind of client.

Save the profile using the template in goni-core `references/notebook.md`. Add the line
`interview: started` at the top of the profile as soon as the first answer is saved, and change
it to `interview: done` when Step 4's hiring report has been shown. That line is what unlocks
every other trick and duty. Save samples to
`voice-samples.md`. Save the dreaded tasks and starting estimate to `logs/hours.md`.

## Step 3: Optional time audit

Ask once: "some people like to see where their week actually goes before handing things off.
if you feel like you're always running behind, we can do a two-week time audit first (/gonibot:goni-log,
twice a day, takes a minute). or we can go straight to your hiring report. which sounds better?"

If they choose the audit, set up `logs/time-log.md`, explain `/gonibot:goni-log`, offer to schedule two
daily reminders, and end here. The hiring report happens on day 14.

## Step 4: The hiring report

Show it in the chat, short and skimmable:

1. **Where the hours go now:** the dreaded tasks and weekly time guesses, total.
2. **What i can take:** match each dreaded task to GoniBot duties from goni-core
   `references/duties.md` (only duties that fit their program). For each, the hours it should
   free up, conservatively.
3. **My suggestion for your first 2 or 3 duties:** pick the ones with the most time back and the
   least setup. Usually lead follow-ups, the Monday brief, and either the Power Hour list or
   the content batch.
4. **Reporting helpers:** list Prep and Reflect, end of week, EOM, EOQ (CEO Club) and benchmarks
   (Foundations) as optional, off unless they want them.

Ask: "which 2 or 3 do you want to start with? small is good."

## Step 5: First shift

For each duty the owner picks:
1. Write a quick SOP with them (the `/gonibot:goni-train` questions, kept short).
2. Agree on the day and time, then schedule it (goni-core `references/duties.md`, "Scheduling a
   duty"). Mention once that scheduled duties only run while the computer is on and Claude is
   open.
3. Add it to `duties.md`.

The rest of the duties unlock one at a time later, never all at once.

## Step 6: Badges and wrap-up

- They finished the interview: **New Pup**. If they switched on a duty: **First Fetch**. If they
  wrote an SOP: **Good Boy SOP**. Announce together in one excited line, then give the claim steps
  from goni-core `references/badges.md` once.
- Tell them what happens next: when their first duty runs, and that they can tap any trick from
  the Goni button on their dashboard any time (start my week, pick-me-up, snuffle mat, busy week,
  slow week, training camp).
- End with a warm check-in, for example: "i'm SO excited to be on your team. anything you want me
  to know before my first shift?"
