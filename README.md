# GoniBot, your first hire

GoniBot is a Claude plugin for DPT to CEO, Legacy and CEO Club practice owners. It works like a
first admin hire: it learns how your practice runs, then drafts your follow-ups, content, reports
and weekly plans and hands them back for a quick review. Nothing goes out without you.

It's included in your program. You'll need your own paid Claude plan (Pro or higher) and the
Claude desktop app.

## Install GoniBot (about 5 minutes)

1. Open the **Claude desktop app** and sign in.
2. Select **Customize** in the sidebar, then **Plugins**.
3. Select **Add marketplace** and paste: `nancydrew333/gonibot`
4. Find **gonibot** in the list and select **Install**.
5. On the **dpt-to-ceo** marketplace, turn on **Sync automatically**, so you always have the
   newest version of GoniBot.

Then connect your apps (the Toy Bin on your dashboard walks you through it) and type
`/gonibot:goni-interview` in a new task. The interview comes first: GoniBot's other tricks unlock once
it's done.

Full guide: your DPT to CEO dashboard, under **Settings, GoniBot**.

## What's in here

| Folder | What it is |
|---|---|
| `.claude-plugin/marketplace.json` | The catalog Claude reads when you add this marketplace |
| `plugins/gonibot/` | The GoniBot plugin: one skill per trick, plus GoniBot's core rules |

## Releasing an update (for Morgan)

Edit the files in `plugins/gonibot/`, add a line to the changelog in `plugins/gonibot/README.md`,
then commit and push to `main` in GitHub Desktop. The plugin has no version number on purpose:
every push counts as a new version. Students with **Sync automatically** on get it on their
own; anyone else gets it when they select **Check for updates** on the marketplace.

---

© 2026 Morgan Meese, DPT to CEO. All rights reserved. This repository is public so DPT to CEO
students can install GoniBot. It isn't licensed for reuse, copying or redistribution.
