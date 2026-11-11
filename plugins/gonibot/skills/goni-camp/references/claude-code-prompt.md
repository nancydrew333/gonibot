# Prompting Claude Code to build the full dashboard

Use this when the owner picks the hard level and wants to build in Claude Code. GoniBot doesn't
just hand over a blank template. It **fills in the prompt** from the practice profile and
`camp.md`, saves it, and walks the owner through pasting it.

## Step 1: Check they're ready

Ask, one at a time:

1. "do you have claude code on your claude account?" If not sure, point them to the Claude
   desktop app's Code tab, or the Tech Support space. If they don't have it, build the dashboard
   in Claude instead (see `full-dashboard.md`, Step 2) and stop here.
2. "which 2 or 3 sections do you want first?" Offer the menu from `full-dashboard.md`, Step 4.
   Recommend sales and capacity if they don't know.
3. "where do your numbers live?" (data tracker link, or they'll paste them). For the first build,
   last month's numbers pasted in are plenty.
4. "what's your monthly revenue goal right now?" Use only a goal they already have from their own
   plan or their coach. If they don't have one, leave the goal line out and suggest they bring it
   to their coach.

## Step 2: Fill in the prompt

Copy the template below. Replace every `<...>` with real details from `practice-profile.md`,
`camp.md` and their answers. Delete any section they didn't pick. Never put patient names or
clinical details in the prompt.

Save the filled prompt in the GoniBot folder as `home-base/claude-code-prompt.md`, and show it to
the owner in a code block so it's easy to copy.

## Step 3: Walk them through it

Say it in GoniBot's voice, short:

1. Open Claude Code and pick their GoniBot folder as the folder to work in.
2. Paste the prompt and send it.
3. Claude Code may ask a question or two. Answer, then let it build.
4. When it opens the page, look it over and ask Claude Code for changes in plain words
   ("make the revenue chart bigger", "move links to the left").
5. Come back and tell GoniBot it's done so it can log the link in `camp.md` and help link it in
   the student dashboard.

## Prompt template

````
I'm a cash-based physical therapist and a DPT to CEO student. My GoniBot folder (this folder)
has my practice details. Please build my practice home base: one dashboard with all my links
and my key numbers, that I'll keep adding to over time.

Read these first:
- practice-profile.md (my practice, offers, prices, schedule, max visits)
- camp.md (every tool and link I use, already sorted into groups)
- home-base/hq.html, if it exists (my current smart bookmark page; keep its links)

About my practice:
- Practice name: <practice name>
- Who I help: <niche, in their words>
- Model: <in-clinic / mobile / gym-based / telehealth / hybrid>
- Offers: <eval $___, package $___, membership $___/mo, ...>
- Typical week: <clinical days and hours, Power Hour, CEO time, protected time>
- Max visits per week: <number>
- Coach: <coach name>

Build it in a folder called home-base/:
- home-base/index.html: one self-contained page, no build step, opens in any browser
- home-base/data/numbers.csv: the monthly numbers the page reads
- home-base/README.md: plain-language steps for updating numbers and links

Page layout, top to bottom:
1. Header: "<Practice name> HQ", today's date, and a strip showing my typical week with
   today highlighted.
2. Links panel: every link from camp.md, grouped Daily, Weekly, Monthly, Client delivery,
   SOPs and how-tos, DPT to CEO. Each link gets a plain label and a one-line note on what
   it's for. Add a search box. Mark missing links as "link needed".
   GoniBot commands (/gonibot:goni-morning, /gonibot:goni-wrap, /gonibot:goni-brief) show as copy buttons.
3. Numbers sections:
<keep only the sections they picked>
   - Sales this month: leads, discovery calls booked, evals booked and completed,
     eval to plan conversion, packages and memberships sold, revenue vs my goal of
     $<goal> with days left in the month, average revenue per new client
   - Marketing: leads by source (<their top sources>), follow-ups sent this week,
     outreach / 100 Challenge count, posts this week, new Google reviews,
     email list size, lead magnet downloads
   - Capacity: visits booked this week vs my max of <max>, open spots, active clients
   - The wave: a line chart of my last 12 months of revenue
   - This week: my Big 3, follow-ups due (lead first names only), next Power Hour,
     next coaching call

My numbers:
<either: "Here are last month's numbers: ..." or "Read them from my data tracker export at
home-base/data/tracker.csv" or "Put in example numbers I can replace, clearly labeled as examples">

Design (make it something I'm proud to open every morning):
- Feels like my brand: <brand colors, or "pick a calm, professional palette that fits
  a <niche> practice">. One accent color, used sparingly.
- Summary first: big, clear numbers at the top of each section, details below.
- Clean, readable type with a real heading font and body font (Google Fonts is fine).
- Works great on my phone and in both light and dark mode.
- Simple charts with labels I can read. No clutter, no stock icons or emoji everywhere.
- Smooth but subtle: nothing that flashes or moves for no reason.

Rules (please follow these exactly):
- No patient information anywhere. Counts and totals only. Lead first names are ok on the
  follow-up list. No passwords or logins on the page.
- Kind numbers: show pace and trends. No red warning colors. Write gaps as
  "2 evals to go", never as a miss or a failure.
- Every number says where it came from and when it was last updated.
- No outside services or tracking. Everything stays in this folder.

When you're done:
- Open the page so I can see it.
- Tell me in plain words how to update next month's numbers and how to add a link.
- Add a line to camp.md: "Home base leveled up to full dashboard" with the folder path.
- Ask me what I'd like to change or add next.
````

## After the first build

When they want more, offer 2 or 3 ideas from `dashboard-ideas.md` that fit them. Each one has an
ask they can paste straight into Claude Code.
