---
title: "SumizAI vs Standard Notes: encrypted notes or AI notes"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-standard-notes.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "Standard Notes encrypts every note end to end and syncs everywhere. SumizAI writes AI notes from your chats and keeps them as Markdown on your Mac. Compared."
---

# SumizAI vs Standard Notes: a locked notebook or a vault the AI fills

Standard Notes exists for one promise: notes encrypted end to end, readable by nobody but you, on macOS, Windows, Linux, iOS, Android and the web. SumizAI exists for a different one. The answers you get from an AI model turn into AI notes with a title, a summary and a chapter, without you writing them.

Privacy is where this comparison has to start, because the two apps make opposite trade-offs. Facts about Standard Notes come from standardnotes.com, its plans page and its self-hosting guide, read on 23 October 2026.

## Where your words go

In Standard Notes a note is encrypted on your device (the site names XChaCha20-Poly1305) before it syncs, and only you hold the keys. The company calls it zero-knowledge encryption and says its apps are open and audited. You can even run the sync server yourself with Docker.

The vault app works differently, and you should know exactly how. Notes are plain `.md` files on your Mac, unencrypted by the app, next to a local database used as an index. Nothing syncs and there is no server holding notes. But every question you ask goes, together with the table of contents and up to five relevant notes (24,000 characters at most), to the AI provider you picked: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter or your own OpenAI-compatible server. The app asks for consent before sending. Only a local Ollama model keeps the whole loop on your machine.

So: if the threat you care about is anyone reading your notes in transit or on a server, Standard Notes is built for you. An AI notes tool that talks to a cloud model cannot match it.

## Feature by feature

|  | SumizAI | Standard Notes |
|---|---|---|
| Who writes the note | The model, from your chat | You |
| Price | 7 days free, then 1 USD a month, one plan | Free; Productivity 90 USD a year; Professional 120 USD a year |
| Source code | Closed | Published on GitHub |
| Platforms | macOS first, coming to the Mac App Store; Windows, iOS, Android in preparation | macOS, Windows, Linux, iOS, Android, web |
| Encryption | None added by the app; files on your disk | End-to-end for every note, on all plans |
| Sync | None | Unlimited devices, even on the free plan; self-hosting with Docker |
| Note types | Markdown notes with title, summary, body and source | Plain text free; Super notes (Markdown, rich text, checklists, code) on Productivity |
| Organisation | Table of contents up to six levels, filled by the model | Tags; folders from Productivity |
| AI | Built in, seven providers on your own key | None listed on the plans page |
| Files | Imports `.md`, `.markdown`, `.txt`, `.pdf` | 100 GB encrypted file storage on Professional |
| Export | ZIP with `base.md` and `notes/`, PDF, PowerPoint deck with 15 themes | Full export, encrypted or plaintext; daily encrypted email backups |

## Choose Standard Notes when privacy is the job

- You keep passwords, health records, ID scans or a journal. Standard Notes lists exactly these uses, and encryption is the point.
- You want the code in public and the option to host the server yourself.
- You need the same notes on a Linux laptop, an Android phone and a browser today.
- You want to pay nothing: the free plan already encrypts and syncs without a device limit.
- You prefer a company funded by its users, with no venture capital, as Standard Notes describes itself.

Nobody should move a diary or a password list into an AI-driven vault. Keep those where they are.

## Choose the vault app when the notes come from AI chats

A Tuesday evening, revising for a Spanish exam. You ask Claude to explain the difference between *por* and *para*, then ask for ten examples, then for the exceptions. In Standard Notes you would copy the useful parts into a note and tag it “spanish”, if you had the energy.

In the vault each answer becomes one of your AI notes: titled, summarised in a line, filed under “2. Grammar > 2.3 Prepositions”, with the original exchange kept underneath. Ask about *para* again next week and the duplicate check, a second model scoring 0 to 1, offers to merge instead of making a twin. Before the exam you export the chapter as a PDF of summaries only, or as an editable `.pptx` deck.

That is the use case. You bring your own model, from any of seven providers. The interface comes in 16 languages, and the language of your notes is independent of it.

Provider settings: pick one of seven providers and paste your own key, or point to Ollama.

The [AI notes app](https://sumizai.com/) overview explains each step from chat to filed note.

## Moving notes out of Standard Notes

Standard Notes offers a full export in plaintext as well as encrypted. Choose plaintext. The importer here reads `.md`, `.markdown`, `.txt` and `.pdf`, single files or a whole folder, one at a time, so check the extensions in the unpacked backup first. Each file becomes an AI note, the original text attached as its source, and the table of contents is rebuilt after every file.

Think twice before importing anything sensitive: the import sends each file's text to your AI provider. With Ollama, it stays local.

Out of the vault, you get a ZIP with `base.md` and the `notes/` folder.

## SumizAI as an Obsidian alternative, and Standard Notes users

Some Standard Notes users want local Markdown files and look at Obsidian. The page about [an Obsidian alternative that writes AI notes from chats](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html) explains how an exported vault opens in Obsidian unchanged, relative links included.

## Standard Notes or an AI notes vault: questions

### Is SumizAI end-to-end encrypted like Standard Notes?

No. It does not sync, so there is no transfer to encrypt, but notes are ordinary files on your Mac, and questions go to the AI provider you chose. Standard Notes encrypts every note on every plan.

### Does Standard Notes have AI?

Its plans page lists no AI features. If you want a model to write and file notes, that is the job of the other app.

### Can I self-host either one?

Standard Notes supports self-hosting its sync server with Docker. The vault app has no server to host: everything runs on your Mac, and only the AI requests leave it.

### Which is cheaper?

Standard Notes is free for encrypted plain-text notes; Productivity is 90 USD a year. Here the plan is 1 USD a month, plus model usage billed by your provider.

### Can I use it on Linux or Android?

Not yet. The Mac version comes first; Windows, iOS and Android are in preparation. Standard Notes runs on all of those plus Linux.

Sources, read on 23 October 2026: [Standard Notes plans](https://standardnotes.com/plans), [Standard Notes downloads](https://standardnotes.com/download) and [the self-hosting guide](https://standardnotes.com/help/self-hosting/getting-started), plus standardnotes.com. Statements about the vault app were checked in its code and App Store metadata.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Capacities](https://sumizai.com/alternative-to/sumizai-alternative-to-capacities.html)
- [SumizAI vs Nuclino](https://sumizai.com/alternative-to/sumizai-alternative-to-nuclino.html)
- [SumizAI vs Craft](https://sumizai.com/alternative-to/sumizai-alternative-to-craft-do.html)
- [SumizAI vs Roam Research](https://sumizai.com/alternative-to/sumizai-alternative-to-roam-by-roam-research.html)
- [SumizAI vs DEVONthink](https://sumizai.com/alternative-to/sumizai-alternative-to-devonthink.html)
- [SumizAI vs UpNote](https://sumizai.com/alternative-to/sumizai-alternative-to-upnote.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Secrets in Standard Notes, answers in a vault

The Mac version is coming to the Mac App Store with seven days free. Use it for what you learn from AI, and keep your private records where they are encrypted.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
