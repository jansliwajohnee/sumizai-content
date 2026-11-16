---
title: "How does a chat answer become a note?"
url: "https://sumizai.com/blog/how-a-chat-answer-becomes-a-note.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "One question followed from chat to file: how AI notes get a title, summary and chapter, how duplicates are judged, and what lands in notes/."
tags: ["chat to markdown", "AI chat notes", "automatic note generation", "AI notes pipeline", "note summary", "Claude notes", "ChatGPT notes", "sumizai"]
---

# How does a chat answer become a note?

You ask a question, the model answers, and a moment later a line under the answer says _Note saved · Open it_. This article follows one question through that gap, because the work done there decides whether your **AI notes** are still useful a year from now. The example comes from the demo vault _Home garden_: _When should I sow tomatoes indoors?_

## What happens before the model sees the question?

Two things, both on your Mac. First, the question is saved to the conversation. Only then does a request go out, so if the provider rejects the key, hits a rate limit or times out, the turn is marked as failed and you retry it in place. You never type it twice.

Second, the app builds the request. With **Use my notes** ticked below the question box, the question travels with the vault's table of contents and the full text of at most 5 matching AI notes, inside a budget of 24,000 characters, and the chat shows which notes went along. Unticked, the model sees the conversation and nothing else. It never reads the whole vault.

The request goes straight from your computer to your provider: Anthropic for Claude, OpenAI for GPT, Google Gemini, Groq, OpenRouter, a local Ollama, or your own server that speaks the OpenAI API. It runs on your key, and the app asks for your consent before anything leaves the machine.

## Why does the answer arrive before the note?

Because they are separate jobs.

The answer streams in token by token (up to 4,096 tokens) and is stored the moment it ends. The AI note is then queued as background work, on the same queue that file imports use, so you can read the answer or type the next question while it is being written.

In total one question costs three or four model calls: the streamed answer, then a draft of the note, a duplicate judgement and a chapter choice. Your provider bills those at its own rates. SumizAI adds nothing on top of the 1 USD a month subscription.

## What goes into an AI note?

Four parts. A **title**. A **summary** of one or two sentences, short enough to scan in a list. An **expansion** that makes sense without the chat around it. And below them the **source**: your original question and the model's answer, word for word.

For the tomato question the draft came back as _Sowing tomatoes indoors_, summarised as _Start six to eight weeks before the last frost, warm and bright_, with the details you need in March in the expansion: seeds about 5 mm deep, 22 to 25 °C until they sprout, a bright windowsill once the first true leaves show.

The source is append-only. Later operations can add to it; none of them rewrites or deletes it. The summary is the model's reading of the conversation and the source is the conversation itself, so if the two ever disagree you can check which one to trust.

The answer is stored first; the AI note is written in the background.

## How does the note get its chapter?

By picking a number, not by inventing a name. The model receives the vault's chapters as a numbered list (`1.`, `1.1`, `a)` and so on) and answers with one of them, or asks for a new sub-chapter under one. A new branch appears only when nothing fits. Here the answer was `1.` Vegetables, so the note became 1.2, right after _Companion plants for tomatoes_.

The model works from a compact digest of the vault capped at 4,000 characters, not the full outline, so filing AI note number 500 costs about what filing number 5 did. The vault's own name is never used as a chapter, and chapters with the same name written with and without diacritics (_Ogórki_ and _Ogorki_) are merged when the tree is read. In Obsidian this filing is your job; here the model does it, and that is the main reason to treat SumizAI as an Obsidian alternative at all.

More on the tree itself: [how the table of contents files your notes](/blog/how-the-table-of-contents-works.html).

## Is this a note I already have?

Before anything is written, full-text search and trigram matching pick up to 5 candidates from the vault. A second helper model then reads the draft against each one and returns a score between 0 and 1 with a sentence explaining it.

A new vault treats 0.75 as a match. Above the threshold the vault's mode decides: ask, always merge, or always create a separate note. In chat the default is quiet: the draft goes into the best match without stopping you. Tick **Ask before merging** for a conversation and the draft waits for your decision, with candidates and scores listed.

A merge only appends. The new material joins the existing note, and the new question and answer are added under the old ones. Merged AI notes keep every source. The details have their own article on [duplicate notes](/blog/how-sumizai-handles-duplicate-notes.html).

## What lands on disk?

A plain Markdown file in the vault's `notes/` folder, named from the title: `sowing-tomatoes-indoors.md`. If the name is taken the app writes `sowing-tomatoes-indoors(1).md`, and it checks the folder itself, not its own index. Rename the note later and the file is renamed too, with every link to it in the vault rewritten.

The local database is only an index. Everything in it can be rebuilt from the files, and when the two disagree the file wins. `base.md`, the table of contents on disk, is updated in the same step, with relative links into `notes/`.

This is why the app works as an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) for people who want the notes written from their chats: the folder it produces opens in Obsidian, VS Code or on GitHub as it is. There is no sync and no server holding your AI notes.

## Where do the links inside a note come from?

From a short list the model gets while writing the expansion: up to 8 existing notes, title and file name, found by the same search. It can link only to those, using ordinary Markdown such as `[Companion plants for tomatoes](companion-plants-for-tomatoes.md)`. No `[[wiki-links]]`: if you try the app as an alternative to Obsidian, the double brackets are the one habit to drop.

Any `.md` target outside that list is removed when the draft arrives. A link to a file that doesn't exist is worse than no link. Each note lists its backlinks underneath. After importing a pile of files, **Rebuild links** in the vault bar goes over the whole vault at once.

## Can a conversation leave nothing behind?

Yes. Untick **Save notes from this conversation** under the question box.

The chat is still stored, every question and answer in order, but the pipeline doesn't run for it: no draft, no chapter, no duplicate check, no file. The switch belongs to that one conversation, so other chats in the vault keep producing AI notes as before.

My rule: leave it on for anything you'd want to find again in six months, and switch it off for scratch work like testing a prompt or comparing how two models phrase the same reply. If you are comparing Obsidian alternatives, the [AI notes app](/) overview covers vaults, search by meaning and export to ZIP, PDF or PowerPoint. It will arrive in the Mac App Store first; no version can be downloaded yet.

