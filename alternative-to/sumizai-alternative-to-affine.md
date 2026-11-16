---
title: "SumizAI vs AFFiNE: AI notes or a docs-and-whiteboard space"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-affine.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "AFFiNE gives you docs, an edgeless whiteboard and databases to fill yourself. SumizAI writes AI notes from your chats. Prices, platforms and migration."
---

# SumizAI vs AFFiNE: who builds the page?

AFFiNE is an open-source workspace where one document can be read as a page or spread out on an endless whiteboard, with databases for tracking projects and an optional AI assistant on top. SumizAI starts from the other end: you ask an AI model a question, and the answer you want to keep becomes one of your AI notes, written and filed by the model.

So the comparison is less about features and more about where your material comes from. If you draw, plan and write by hand with a small team, AFFiNE is built for you. If most of what you learn arrives as answers from Claude or GPT, read on. Prices and platforms below were checked on 23 October 2026.

The starting point here is a conversation, not a blank page or a canvas.

## The two apps in twelve rows

|  | SumizAI | AFFiNE |
|---|---|---|
| Who writes the note | The AI model, from your chat; you can correct it | You, block by block |
| Price | 7 days free, then 1 USD a month | Free plan; Pro 6.75 USD a month; Team 10 USD per seat a month; Believer 499.99 USD once |
| AI cost | Your own API key, paid to the provider; nothing added | AFFiNE AI add-on 8.9 USD a month, billed yearly |
| Licence | Proprietary subscription | Community Edition under MIT, free to self-host |
| Platforms | macOS first, coming to the Mac App Store; Windows, iOS, Android in preparation | Windows, macOS, Linux, web, iOS, Android |
| Storage | Plain `.md` files on your disk plus a local index | Local-first workspace, optional AFFiNE Cloud |
| Structure | Table of contents up to 6 levels, chosen by the model | Docs, folders, databases, whiteboard |
| Visual work | None: text, chapters and links | Edgeless whiteboard; frames can become slides |
| Links | Markdown links to existing notes, backlinks under each note | Links and references between docs |
| Teamwork | Single user, no sync | Real-time collaboration; Free plan up to 3 members |
| Cloud storage | None | 10 GB on Free, 100 GB on Pro |
| Export | ZIP of Markdown, PDF in two levels, PowerPoint with 15 themes | Markdown, HTML, PDF per doc |

## One research afternoon, two ways

Say you are planning a raised vegetable bed and spend an afternoon asking an AI about soil depth, drainage and which crops tolerate partial shade.

With AFFiNE you would open a doc, paste the answers you liked, then switch to edgeless mode and drag the pieces into a sketch: bed on the left, shade line, a sticky note saying “check pH”. Add a database row per crop with sowing month and spacing. It is a good result. It also took you an hour of arranging, because AFFiNE gives you the blocks and expects you to build.

With AI notes the same afternoon produces something different. Each answer you keep turns into a note with a title such as “Soil depth for raised beds”, a one-line summary, the expanded explanation and your question with the full reply underneath, word for word. The model puts it under a chapter like `2.1` “Soil and drainage” and links it to the earlier note on compost. When you ask about shade crops the next day, the app sends the vault's table of contents and the five most relevant notes, within 24,000 characters, and tells you which ones it used.

No sketch, no crop table. A tidy chapter of text, built without any dragging.

## Pick AFFiNE in these cases

- You think visually. The edgeless whiteboard, with shapes, connectors and frames you can present as slides, has no counterpart here at all.
- Your notes are shared. AFFiNE has real-time editing and member limits per plan; this app has one user per vault and no sync.
- You want structured data next to text: a planning database with views for tasks and projects.
- You need Linux, a browser tab or your phone today. AFFiNE runs on all of them, while the Mac build of this app is still on its way to the App Store.
- You want to self-host. The Community Edition is MIT-licensed and runs in Docker.

If two of those apply, AFFiNE is the better tool and this page will not talk you out of it.

## Pick the AI notes app when answers come from a model

The case for it is narrow and specific. You already spend time in conversations with a model, and the good answers drown in a scrolling chat history. Nobody in that situation needs a better whiteboard; they need the copying, titling and filing done for them.

Three details matter in daily use. First, before saving, the app looks for a near-duplicate with full-text and trigram search, and a second model scores the overlap from 0 to 1; above the vault's threshold it asks whether to merge. Second, a merge only appends, so the original source text is never overwritten. Third, the model can only link to notes that exist, because it receives a map of titles and file names, so you do not get dead links.

Cost works differently too. AFFiNE AI is a fixed add-on. Here you bring a key for one of seven providers (Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local Ollama or your own OpenAI-compatible server) and pay the provider directly, on top of 1 USD a month.

There is also an angle for people coming from Obsidian rather than AFFiNE. The [Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html) page explains it in full: the app writes AI notes from your chats, and because every note is a plain `.md` file, the exported vault opens straight in Obsidian. If you are weighing AFFiNE as an alternative to Obsidian and miss the plain files, that is the gap this app fills.

## Taking your notes from one to the other

**AFFiNE to SumizAI.** AFFiNE documents its export to Markdown, HTML and PDF per doc. Export the docs you care about as Markdown, then open the import panel and pick the files or the whole folder. Accepted formats are `.md`, `.markdown`, `.txt` and `.pdf`, processed one file at a time. Each file becomes one of your AI notes with the original text kept as its source, and the table of contents is rebuilt after every note. Whiteboard drawings and database views do not survive as such; only their text does.

**Back to AFFiNE.** Download the vault as a ZIP. Inside is `base.md` with the table of contents and a `notes/` folder with relative links. AFFiNE accepts Markdown files on import (its Notion route uses an HTML ZIP instead), so the notes come across as text docs. For people who never open AFFiNE, the PDF export in two levels or the editable PowerPoint deck are the quicker hand-off.

## AFFiNE and AI notes: short answers

### Does AFFiNE have AI?

Yes, as AFFiNE AI, an add-on listed at 8.9 USD a month billed yearly. It helps you write, draw and plan inside your docs. It does not turn a chat into filed AI notes.

### Is AFFiNE free?

The Free plan costs nothing and includes 10 GB of cloud storage and up to 3 members per workspace. The self-hosted Community Edition is free under the MIT licence.

### Can this app draw diagrams or whiteboards?

No. It handles text: notes, chapters and Markdown links. For diagrams, AFFiNE's edgeless mode is the right place.

### Can I use both?

Yes. Collect AI notes here, export them as Markdown and pull the ones you want to sketch around into AFFiNE. Changes made in AFFiNE stay there.

### Which one works offline?

Both keep data on your machine. This app needs a connection only for the model call (or none, with a local Ollama), and its licence token stays valid for 7 days offline.

AFFiNE plans and prices: [affine.pro/pricing](https://affine.pro/pricing); features and platforms: [affine.pro](https://affine.pro/); licence: [AFFiNE on GitHub](https://github.com/toeverything/AFFiNE); export formats from AFFiNE's release notes on affine.pro. All read on 2026-10-23. Facts about this app come from its code and documentation; see the [AI notes app](https://sumizai.com/) overview.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Zettlr](https://sumizai.com/alternative-to/sumizai-alternative-to-zettlr.html)
- [SumizAI vs Joplin](https://sumizai.com/alternative-to/sumizai-alternative-to-joplin.html)
- [SumizAI vs Anytype](https://sumizai.com/alternative-to/sumizai-alternative-to-anytype.html)
- [SumizAI vs Notesnook](https://sumizai.com/alternative-to/sumizai-alternative-to-notesnook.html)
- [SumizAI vs Notion](https://sumizai.com/alternative-to/sumizai-alternative-to-notion.html)
- [SumizAI vs Standard Notes](https://sumizai.com/alternative-to/sumizai-alternative-to-standard-notes.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Let the model write the first draft

Seven days free. If a week of questions leaves you with a chapter of AI notes you would not have written yourself, the app has done its job.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
