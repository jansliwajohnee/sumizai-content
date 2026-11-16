---
title: "AI Notes from Your AI Chats, Filed as Markdown | SumizAI"
url: "https://sumizai.com/"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "SumizAI is an AI notes app: an answer worth keeping becomes a Markdown note with a title, summary and source, filed for you. 7 days free, then 1 USD/month."
---

# AI notes that write and file themselves

SumizAI turns an answer from Claude or GPT into a Markdown note you own.

AI notes in SumizAI start as an ordinary chat. You ask Claude, GPT or another model you connect, and when an answer is worth keeping, the app writes it up as a note with a title, a summary, an expansion and the original question and answer. Then it files the note into a chapter of your vault. Every note is a plain `.md` file. Seven days are free, then it costs 1 USD a month.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [What a note looks like](#note)

Plain `.md` files · stored on your Mac · your own AI key

A real note from the demo vault “Home garden”, written by Claude from one question.

## What an AI note looks like

Look at the screenshot above. Someone asked how to sow tomatoes indoors. Claude answered, and the answer turned into an AI note called “Sowing tomatoes indoors”. Nobody typed that title.

Each of your AI notes has the same four parts, always in the same order:

01

### Title

Short and specific, so a chapter with forty notes can be scanned in a few seconds.

02

### Summary

One line under the title. Here: start six to eight weeks before the last frost, warm and bright.

03

### Expansion

The useful part of the answer, rewritten with headings and lists: timing, method, hardening off.

04

### Source

Your question and the model's full answer, kept word for word. If the model got something wrong, you can see exactly what it said.

You never copy anything by hand. You keep chatting, and the AI notes collect in the background, already titled and summarised.

## How AI notes get organised

A vault holds one area of your life: work, a thesis, the garden. Each vault has a table of contents with numbered chapters, and when new AI notes arrive, the model picks a chapter for each. You don't drag anything into place.

Duplicates get caught before they are saved. The app looks for a note that already covers the topic, a second model scores the match from 0 to 1 and says why, and above your threshold you get a question: merge, or keep both? A merge only adds to the older note. Its original question and answer are never touched.

AI notes point to each other with ordinary Markdown links such as `[Soil mix](soil-mix.md)`. The model may only link to files that exist, and every note shows what links back to it. Search works by meaning, so “the thing about frost dates” finds the right note even if you never wrote the word frost.

The table of contents fills itself in as the vault grows.

Every note in the vault, with its summary.

## Answers that use what you already know

Ask a question inside a vault and it doesn't travel alone. The app sends the vault's table of contents and the full text of up to five AI notes it judged most relevant, within a budget of 24,000 characters.

When the answer arrives, the app lists which of your AI notes it read. You can check every source. Notes from other vaults are never sent: a vault is a boundary, which is handy when one of them is about a client and another about your health.

## Your AI notes are plain Markdown files

Every note is a `.md` file in a folder on your disk. There is no export step to get your data out, because it never went anywhere else. Download a vault as a ZIP and you get `base.md` with the table of contents and a `notes/` folder. The links are relative, so the whole thing opens in Obsidian, VS Code or on GitHub without the app.

Need to hand something over? A vault exports to PDF, either summaries only or the full notes, and to an editable PowerPoint deck with fifteen themes. It works the other way too: import a PDF or a text file and it becomes one of your AI notes, with the complete original text attached as its source.

That is the whole idea of a second brain you can trust: the files outlive the app.

## Looking for an Obsidian alternative?

Obsidian is a superb editor for notes you write yourself. SumizAI starts from the other end: the model writes the note out of your chat, and you read it, correct it and move on.

If that is what you want from an Obsidian alternative, the comparison page shows where each tool wins, including the cases where you should stay with Obsidian. Your AI notes from SumizAI are plain Markdown, so using both at once is perfectly normal.

[SumizAI as an Obsidian alternative: the full comparison](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)

## AI providers and platforms

SumizAI doesn't resell AI. You paste your own API key from one of seven providers: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local model in Ollama, or your own OpenAI-compatible server. Requests go straight from your Mac to that provider, and the app asks for your consent before anything is sent. No middleman. The provider bills you for what the model uses.

The interface speaks 16 languages. The language of your notes doesn't depend on it.

Seven providers, each on your own key.

| Platform | Status |
|---|---|
| [macOS](https://sumizai.com/mac/) (Apple silicon and Intel) | Coming to the Mac App Store |
| Windows | In preparation |
| iOS | In preparation |
| Android | In preparation |

## Pricing: one dollar a month

Seven days free. After that 1 USD a month, one plan for everybody.

Trial

$0

for 7 days

Through the App Store. Create an account and start.

- Every feature from the first day
- Vaults, questions, notes and exports
- Export to **ZIP**, **PDF** and **PowerPoint**
- Notes from the trial stay yours afterwards

SumizAI

$1

/ month

One plan. Cancel whenever you like.

- Unlimited vaults and notes
- Notes with a title, summary, expansion and the original answer
- Table of contents, duplicate check, links between notes
- Search across every note
- **PDF** in two levels of detail, **PowerPoint** with fifteen themes
- Seven AI providers on your own key
- Notes stay on your disk as **.md** files

**Two things to say plainly.** What the model costs goes to your provider; we add nothing on top. And if you stop paying, your AI notes stay readable and exportable. The app only stops starting new conversations. The licence is a signed token valid for seven days, so a week offline is normal, not an error.

## Frequently asked questions

What is SumizAI?

An AI notes app. You chat with a model on your own API key, and the answers you want to keep become Markdown notes: titled, summarised and filed into the table of contents of a vault.

How are AI notes different from a saved chat?

A saved chat is a transcript. An AI note has a title you can scan, a summary you read in five seconds, an expansion, and the original question and answer kept underneath as evidence. It sits in a chapter next to related notes, not in an endless list of conversations.

Is SumizAI an Obsidian alternative?

For some people, yes. If you want notes written for you out of AI chats, SumizAI does that and a plain Obsidian vault does not. If you live on plugins, the graph view and Canvas, stay with Obsidian and open your SumizAI vault in it whenever you like. The [full comparison](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html) goes through both, point by point.

Where are my notes stored?

On your Mac, in the app's database and as ordinary `.md` files. There is no sync and no server holding your notes. SumizAI does not collect your notes, questions or documents.

Which AI models can I use?

Models from Anthropic, OpenAI, Google Gemini, Groq and OpenRouter, a local model through Ollama, or your own OpenAI-compatible server. You bring the key, and the provider bills you for usage.

What happens to my AI notes if I cancel?

They stay where they are. The app still opens and exports every vault you built. Only new conversations stop.

Can I turn AI notes into slides?

Yes. A vault exports to an editable `.pptx` deck with fifteen themes, in the order of the table of contents. The original question and answer never appear on a slide.

When can I install it?

The Mac version comes first, through the Mac App Store. Windows, iOS and Android are in preparation. The [download page](https://sumizai.com/download/) always shows what you can install today.

### Keep the answers. Skip the filing.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [Read the blog](https://sumizai.com/blog/)

Try it for seven days and count how many AI notes one ordinary week of chatting leaves behind.
