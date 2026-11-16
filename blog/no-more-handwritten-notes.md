---
title: "No more handwritten notes: what changes when AI notes write themselves"
url: "https://sumizai.com/blog/no-more-handwritten-notes.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Manual note-taking breaks down in your busiest weeks. What replaces it: AI notes written from chat answers, filed, checked for duplicates, saved as Markdown."
tags: ["no more handwritten notes", "ai notes", "automatic note taking", "notes from ai chats", "ai note taking", "markdown notes", "sumizai"]
---

# No more handwritten notes: what changes when AI notes write themselves

Nobody minds the pen. The problem is the labour around a note: copying the useful part of an answer, inventing a title, choosing a folder, promising to tidy it all up on Sunday. With AI notes that labour moves to the app, and the note itself stays yours, as a plain `.md` file.

## What does “no more handwritten notes” mean in practice?

The note stops being a task. You talk to a model you already pay for (Claude, GPT, Gemini or any other you connected), and when an answer arrives that you would hate to lose, SumizAI turns it into one of your AI notes. No editor to open, no file to name, no folder to pick.

The promise is narrow. You still do the thinking, in the chat. What disappears is the fifteen minutes of retyping that the thinking used to cost before it counted as written down.

Everything else in this article follows from that one change. If notes appear without you, something has to file them, something has to stop near-copies, and something has to keep the files readable in ten years.

## Why do handwritten notes fail when you need them most?

Because they charge their price when you are busiest. The tense project week, the conversation where something finally made sense: those are the moments worth recording, and they are exactly the ones with no spare quarter of an hour.

The second failure is quiet. A hand-kept archive drifts. One idea lands three times under three titles, the folder structure from March looks odd by September, and you stop trusting the archive before you stop adding to it.

The third is about wording. A handwritten summary keeps what you understood at the time, in the words you had then. The original phrasing, the part you want back when a summary turns out to be too confident, is the first thing it throws away. AI notes keep it, as the next section shows.

## How does an AI note get written if you never write it?

From the exchange you just had. When the answer ends, the app asks the model for a note instead of a reply, and what comes back has four parts: a title, a summary to scan, an expansion for when you need the detail, and the source, meaning your original question and the model's answer, kept word for word underneath.

The source is append-only. A note can gain new material later, but the original question and answer are never rewritten, so six months on you can check what was actually said rather than what the summary claims.

That separation matters more than it looks. Scanning, reading and checking are three different jobs, and a single block of text does none of them well.

## Who decides where each note goes?

The app, at the moment an AI note is created. Each vault has a table of contents: a tree of chapters up to six levels deep, numbered `1.`, `1.1`, `a)`, `a.1)`. The model sees the chapters that exist and picks one by its number, or asks for a new sub-chapter when nothing fits.

The Home garden vault: “Sowing tomatoes indoors” sits at 1.2 under Vegetables, “Checking soil pH” at 2.1 under Soil and compost. Nobody dragged them there.

Picking by number is what keeps the tree sane. A model asked to name a chapter from scratch every time would give you Vegetables, Growing vegetables and Vegetable growing as three branches within a month.

Delete a chapter and its notes move up to the parent, so no note ever ends up outside the tree. When the shape of a vault has changed after a busy stretch, **Rebuild contents** lays the chapters out again.

## What stops AI notes from piling up as near-duplicates?

A check that runs before anything is saved. Full-text search and trigram similarity produce a shortlist of notes in the same vault, then a second model scores each candidate from 0 to 1 and writes down why.

Above the vault's threshold you get a question: merge into the existing note or keep both. A vault can also be set to always merge or always create. A long study of one subject wants merging; a daily log does not.

A merge only adds. The older note keeps its question and answer and gains the new ones beside them, which is the opposite of tidying an archive by hand and losing the longer version in the process.

## How do notes link, and can you question them?

Links sit inside AI notes as ordinary Markdown, `[Watering raised beds](watering-raised-beds.md)`. The model receives a map of existing titles and files and may link only to those, so there are no invented file names. Under each note you see the notes that point back at it.

Then you can ask the vault itself. Your question travels with the table of contents and the full text of at most 5 relevant notes, inside a budget of 24,000 characters, and the answer lists which notes it used. The model never reads the whole vault, and a question in one vault sees nothing from another.

A good answer can become a note in turn, with its own source kept underneath.

## Where do the files live, and how do old notes come along?

In a folder you choose, as plain `.md` files: `base.md` holds the table of contents and `notes/` holds one file per note. The local database is only an index. There is no sync and no server holding your notes, and SumizAI does not collect notes, questions or documents.

Notes you typed before can be imported: single files or a whole folder of `.md`, `.markdown`, `.txt` or `.pdf`, processed one file at a time. Each becomes a note with your original text as its source, and the table of contents is rebuilt after every one. An Obsidian vault is also a folder of `.md` files, so it comes in the same way, which matters if you are weighing alternatives to Obsidian and do not want to start from zero.

This is also why SumizAI fits people looking for an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) that writes the notes for them. The app produces AI notes from your conversations, and because links are relative paths between real files, the same folder opens in Obsidian, VS Code or a Git repository. Export adds a ZIP of the vault, a PDF with summaries only or full notes, and an editable `.pptx` deck in table-of-contents order with 15 themes.

## Which model writes your notes, and what does it cost?

The one you connect, and it writes every AI note in the vault. There are seven providers: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local Ollama, or your own OpenAI-compatible server, always on your own API key. Requests go straight from your computer to the provider, and the app asks for your consent before sending.

You pay the provider for the model; SumizAI adds nothing on top. The app itself is free for 7 days, then 1 USD a month, one plan. Cancel and your notes still open and export; only new conversations stop. The licence is a signed token valid for 7 days, so a week offline is normal use.

## Who should keep writing notes by hand?

Teams. There is no shared vault, no collaboration and no sync between devices.

Anyone who wants meeting notes or transcripts of recordings. SumizAI does neither; it works from conversations you have with a model, typed questions and their answers.

People shopping for Obsidian alternatives because of plugins, the graph or Canvas. Those are Obsidian features, and SumizAI has none of them. Stay where you are, and open the SumizAI folder there if you want both.

If you use Obsidian today, treat SumizAI less as an Obsidian alternative and more as the part that writes the notes.

And anyone who does not think out loud with a model. The app captures conversations you were having anyway; with no conversations, there is nothing to capture.

If you do work that way, the [AI notes app](/) is coming to the Mac App Store for Apple silicon and Intel Macs. No version can be downloaded yet; Windows, iOS and Android are in preparation.

