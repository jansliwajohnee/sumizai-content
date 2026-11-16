---
title: "Why is SumizAI different from every other note editor?"
url: "https://sumizai.com/blog/why-sumizai-is-different-from-other-note-editors.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "A note editor hands you a blank page. SumizAI writes AI notes from your chats, files them in a chapter, checks for duplicates and saves plain .md files."
tags: ["ai notes", "ai note taking app", "note editor alternative", "chat to markdown", "markdown knowledge base", "sumizai"]
---

# Why is SumizAI different from every other note editor?

A note editor opens on an empty page and waits for you to type. SumizAI opens on a conversation with a model such as Claude, GPT or Gemini, and turns the answers you want to keep into AI notes you never wrote by hand. **The editing part is missing on purpose.** What the app does instead is the filing, the deduplication and the linking that a normal editor leaves to you.

## What does a normal editor expect you to do after a good answer?

Count the steps. You select the reply in the chat window, copy it, switch apps, create a page, paste, invent a title, pick a folder, fix the formatting that broke on paste, and maybe add a link to an older page if you remember it exists. That is eight or nine small decisions for one answer, and it is the reason most people never build a library of AI notes out of their chats.

Most people do it twice and then stop.

In SumizAI the count is zero. You keep talking to the model, and when an answer is worth keeping it becomes a note in the vault you are working in. Nobody opens an editor, nobody names a file. The same app also imports material you already have: `.md`, `.markdown`, `.txt` and `.pdf` files, or a whole folder, processed one file at a time.

## What is inside an AI note written from a chat?

Four parts, always in the same order. A **title** that says what the note is about. A **summary** of a few sentences for scanning the list, followed by an **expansion** that holds the detail you will want when you come back to it. And under all of it, the **source**: your original question and the model's original answer, word for word.

The note “Sowing tomatoes indoors” from the demo vault Home garden: title, summary and expansion on top, the original exchange below.

The source is append-only. It is never rewritten, not by a merge, not by a retitle. So when a summary half a year later sounds more certain than you remember, you scroll down and read what the model actually said, and what you actually asked. Of the four parts of an AI note, this is the one that makes it trustworthy.

## Who decides which chapter a note goes into?

The model does, but with a short leash. Every vault has a table of contents: a tree of chapters up to six levels deep, numbered `1.`, `1.1`, `a)`, `a.1)`. When a note is created, the model sees the numbered chapters that already exist and answers with a number, or asks for a new sub-chapter under one of them.

Choosing by number is the trick. If a model had to name a chapter from scratch every time, a gardening vault would grow _Tomatoes_, _Tomato growing_ and _Growing tomatoes_ as three separate branches within a week.

The rule matters more as the vault grows: the fiftieth AI note gets the same list of existing numbers as the first one did. Delete a chapter and its notes move up to the parent. They never end up outside the tree.

## How does it avoid writing the same note twice?

Before a note is saved, full-text search and trigram similarity pull a shortlist of notes in the same vault that look close. A second model then reads each candidate next to the new material and scores the match from 0 to 1, with a written reason.

Above the vault's threshold you get a question: merge into the existing note, or keep both. A vault can also be set to always merge or always create. A merge only adds. The older question and answer stay where they were, and the new pair joins them, so a shorter, later answer cannot quietly replace a longer one you saved in March. Without this check, a vault of AI notes about one hobby would collect five versions of the same answer about watering.

## Why are links plain Markdown instead of wiki-links?

Because plain links survive outside the app. Inside a note body a related note appears as `[Hardening off seedlings](hardening-off-seedlings.md)`, written into a sentence. There are no `[[double brackets]]` that only one program understands.

The model receives a map of the titles and filenames that really exist in the vault and may only link to those. An invented filename would be a dead link, and a dead link is worse than none. Under each note you also see the backlinks: every note that points to this one. Wiki-links are the first thing many people check when they test an alternative to Obsidian, so it is fair to say it plainly: there are none here.

This is also why the app works as an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) for people who want their AI notes to write themselves. Export a vault, open the folder in Obsidian, and the links resolve, because each one is a relative path to a real `.md` file.

## What does the model see when you ask a question?

Not your whole vault. A question travels with the vault's table of contents and the full text of **at most 5** of the most relevant notes, inside a budget of 24,000 characters. Notes from other vaults never join in.

When the reply arrives, the app lists which notes it used. Short list, easy to check. You can open each one and compare the answer with what you saved, which is the whole point of keeping your own AI notes instead of trusting a fresh chat every time.

## Where do the files end up?

On your disk. Each AI note is an ordinary `.md` file; a local database serves as an index for search and the table of contents. There is no sync and no server holding your notes, and SumizAI does not collect notes, questions or documents.

**ZIP**: `base.md` with the table of contents plus a `notes/` folder, relative links, opens in Obsidian, VS Code or on GitHub.**PDF**: summaries only, or full notes.**PowerPoint**: an editable `.pptx` in table-of-contents order, 15 themes, without the original questions and answers on the slides.

Search works by meaning across titles, summaries and note bodies, so "when do I move seedlings outside" finds the note even if it never uses the word _move_. Together with the plain-file export, that is what puts the app on a list of Obsidian alternatives at all: you can leave with every note intact.

## When is a regular editor the better choice?

When you want to write. If your notes are drafts, essays or meeting minutes you type yourself, an editor built for typing is the right tool, and this one has no canvas, no whiteboard and no kanban board. There are no plugins, no graph view and no team workspace either. If you depend on thirty Obsidian plugins, stay with Obsidian; no Obsidian alternative replaces that ecosystem.

The AI is also yours to bring. You connect your own API key from one of 7 providers (Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local Ollama, or your own OpenAI-compatible server) and pay that provider directly. The app asks before it sends anything.

And it is not available yet. The macOS version, for Apple silicon and Intel, is coming to the Mac App Store; Windows, iOS and Android are in preparation. The plan is simple: 7 days free without a card, then 1 USD a month. If you stop paying, your notes still open and export. To see the whole picture first, start on the page about the [AI notes app](/) itself.

