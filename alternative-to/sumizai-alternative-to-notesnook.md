---
title: "SumizAI vs Notesnook: encrypted notes or AI notes"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-notesnook.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "Notesnook encrypts the notes you type. SumizAI writes AI notes from your chats and keeps them as .md files on your Mac. Prices, platforms and migration compared."
---

# SumizAI vs Notesnook: who holds the key, who holds the pen

Notesnook is an open-source, end-to-end encrypted notebook for people who type their own notes and want nobody, not even the company running the sync server, to read them. SumizAI starts somewhere else entirely: the text comes out of your conversations with an AI model, so you end up reviewing AI notes instead of writing every line.

Both apps take privacy seriously, but they protect different things. Everything below about Notesnook was checked on notesnook.com on 23 October 2026. The section on when to stay with Notesnook is meant seriously.

The starting point is a conversation, not an empty page. This answer turns into one of the AI notes in the “Home garden” vault.

## Side by side, as of 23 October 2026

Eleven rows. Where a cell says “none”, the official site lists nothing for it.

|  | SumizAI | Notesnook |
|---|---|---|
| Who writes the note | The AI model drafts AI notes from your chat; you edit the result | You, in an editor with tables, checklists, code blocks and maths |
| Price | 7 days free, then 1 USD a month, one plan | Free forever with unlimited notes; paid plans from 1.67 USD a month add attachment storage |
| Licence | Proprietary subscription | Open source, GPLv3 for the apps and the sync server |
| Platforms | macOS first, coming to the Mac App Store; Windows, iOS and Android in preparation | Windows, macOS, Linux, Android, iOS and the web |
| Storage | Plain `.md` files on your disk plus a local index database | Encrypted notes, synced through Notesnook servers |
| Encryption | Nothing added by the app; no server of ours ever receives your notes | End-to-end, before notes leave the device; a second password for the private vault |
| Organisation | Table of contents up to 6 levels deep, filled in by the model | Notebooks and tags, 50 of each on the free plan |
| Duplicates | Checked before saving, with an offer to merge | Up to you |
| AI | Seven providers on your own API key, including local Ollama | None listed on notesnook.com |
| Sync | None; no collaboration either | Unlimited devices on every plan |
| Export | ZIP of Markdown, PDF at two levels of detail, PowerPoint with 15 themes | PDF, HTML, Markdown, Markdown + Frontmatter, plain text |

## Two kinds of privacy in one evening

Say you spend an evening untangling a rental contract. In Notesnook you type the clauses that worry you, tag the note “flat”, and move it into the vault so it opens only with the second password. It syncs to your phone encrypted. Nobody at Notesnook can read it, and that promise is the reason the app exists.

With the AI app you would ask the model about the notice period instead. Your question, the vault's table of contents and the full text of at most five relevant notes (24,000 characters in total) travel from your Mac straight to the provider you chose, after the app asks for consent. The reply becomes one of your AI notes with a title, a one-line summary and an expanded body. Your original question and the model's answer sit underneath, word for word, as the source.

So the trade is plain. Notesnook shields text from its own servers. The other app has no server for your notes at all, yet the model provider sees what you send, unless you run Ollama locally or point the app at your own OpenAI-compatible server.

## Pick Notesnook if this sounds like you

- You need your notes on a phone or in a browser today. Notesnook runs on six platforms, Linux included; the Mac app is not out yet.
- End-to-end encryption is a hard requirement, for client files, health records or sources.
- You want to pay nothing. The free plan has no time limit and no device cap; paid tiers only raise limits such as 50 MB of attachments a month.
- Writing by hand is how you think, and you want tables, checklists and maths in the editor.

One more point in its favour: cancelling a paid Notesnook plan drops you back to the free tier, and the pricing page says your notes are neither deleted nor locked.

## Where AI notes beat a locked notebook

The case for switching is narrow and specific. Most of what you learn this year comes from asking Claude or GPT, and the good answers sink into a list of 400 chats. Copying them by hand into Notesnook works for a week.

The app does that copying for you and goes further. It files each note into a chapter such as `2.1` or `a)`, links it with plain Markdown links only to notes that exist, and lists backlinks under it. Before saving, a second model scores similarity from 0 to 1 against existing notes; above the vault's threshold you choose between merging and keeping both. A merge only appends, so the source text is never overwritten.

Later questions draw on what you saved, and the app shows which notes it read. Search works by meaning across titles, summaries and bodies. For a presentation, the vault exports to an editable `.pptx` in table-of-contents order.

You also choose the model: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, local Ollama or your own server, each on your key. It is an [AI notes app](https://sumizai.com/) with no markup on model costs.

## Comparing an Obsidian alternative at the same time?

Some readers weigh three tools at once. As an alternative to Obsidian, SumizAI is aimed at the same kind of person as here: someone whose best material comes out of chats. It is an [Obsidian alternative for people who want the notes written for them](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html), and because every note is an ordinary `.md` file with relative links, an exported vault opens in Obsidian without conversion.

## Moving notes in either direction

From Notesnook: open Settings, then Import & export, then Backup & export, and pick Markdown under “Export all notes”. The app asks for your account password and saves a `.zip`. Open the vault when prompted, or locked notes stay out. On desktop and web, PDF export exists only for single notes, so Markdown is the sensible bulk format anyway.

Unzip it and point the importer at the folder. It reads `.md`, `.markdown`, `.txt` and `.pdf`, one file at a time; each file becomes one of your AI notes with its original text kept as the source, and the table of contents is rebuilt after every note. A thousand files take a while.

The other way round, export the vault as a ZIP: `base.md` holds the table of contents and `notes/` holds the files. Notesnook advertises an importer for Obsidian, and since this folder opens in Obsidian unchanged, that is the route I would test first.

## Questions people ask about the two

### Which one is more private?

For typed notes, Notesnook: everything is encrypted before it leaves the device. The AI app keeps notes on your disk and never uploads them to a server of its own, but each question goes to an AI provider unless that provider is Ollama on your machine.

### Does Notesnook write AI notes?

No AI writing feature appears on notesnook.com as of 23 October 2026. You write every note yourself.

### Can I run both?

Yes, and it is a reasonable split: passwords, contracts and journals in Notesnook, AI notes from your chats in the other app. They share no data, so nothing conflicts.

### What does a year cost?

The AI app: 12 USD plus whatever your provider charges for the model. Notesnook: nothing on the free plan, or about 20 USD a year at the cheapest paid rate.

### Is there a Linux version?

No. The Mac version comes first; Windows, iOS and Android are in preparation, and Linux is not on that list.

Sources: [notesnook.com](https://notesnook.com/), [notesnook.com/pricing](https://notesnook.com/pricing) and [the Notesnook help page on exporting](https://notesnook.com/help/export-notes-from-notesnook), all read on 23 October 2026. Facts about our app come from the app itself and its App Store metadata.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs CherryTree](https://sumizai.com/alternative-to/sumizai-alternative-to-cherrytree.html)
- [SumizAI vs AFFiNE](https://sumizai.com/alternative-to/sumizai-alternative-to-affine.html)
- [SumizAI vs SiYuan](https://sumizai.com/alternative-to/sumizai-alternative-to-siyuan.html)
- [SumizAI vs QOwnNotes](https://sumizai.com/alternative-to/sumizai-alternative-to-qownnotes.html)
- [SumizAI vs Bear](https://sumizai.com/alternative-to/sumizai-alternative-to-bear-writer.html)
- [SumizAI vs RemNote](https://sumizai.com/alternative-to/sumizai-alternative-to-remnote.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Try it when the Mac version lands

The Mac App Store comes first: seven days free, then 1 USD a month. Your AI notes stay as files on your own disk.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
