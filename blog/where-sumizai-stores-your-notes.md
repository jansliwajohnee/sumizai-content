---
title: "Where does SumizAI store your notes?"
url: "https://sumizai.com/blog/where-sumizai-stores-your-notes.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Your AI notes are plain .md files in a folder you choose: one directory per vault, base.md for the contents, notes/ for the notes. The database is only an index."
tags: ["local markdown notes", "AI notes on disk", "note file format", "no vendor lock-in", "export notes zip", "sumizai"]
---

# Where does SumizAI store your notes?

Every one of your AI notes is a plain `.md` file in a folder on your Mac. You pick the folder, you can open it in Finder, and it holds everything the app knows about your notes. The local database is an index built from those files, so if the two ever disagree, the file wins.

## What does the folder with my AI notes look like?

You choose it in Settings, under _Notes folder_: "Every vault keeps its .md files in this folder on your computer." Inside, each vault gets its own directory named after the vault. The demo vault _Home garden_ becomes `home-garden/`:

`base.md`: the table of contents, chapters numbered `1.`, `1.1`, `a)` and so on, with links to the notes;`sumi.md`: a short digest of the vault the model uses to pick the right chapter for a new note without reading everything;`notes/`: one `.md` file per note, such as `sowing-tomatoes-indoors.md`;`documents/`: files you imported, kept next to the note made from each of them.

No hidden metadata directory, no proprietary container. _Change folder_ moves the files to the new place for you. If the folder disappears (an unplugged drive, a rename in Finder), the app says it has no access and asks you to point to it again. Your notes are not lost.

## What is inside a single AI note file?

Open `sowing-tomatoes-indoors.md` in any editor and you see, from top to bottom:

front matter between `---` lines: `id`, `title`, `summary`, `section` (its chapter), `created`, `updated`, the note language and up to three follow-up questions;the title as a `# heading` and the note body, written as bullet points;an optional `## Full text` section with the longer version;`## Source material`: your original question and the model's answer, word for word, each entry stamped with its date.

The same note in the app. On disk it is `home-garden/notes/sowing-tomatoes-indoors.md`.

The source section is only ever appended to. When a duplicate gets merged into the note, its question and answer go below the old ones. Nothing is overwritten.

Links to other notes are ordinary Markdown links inside the body, `[Checking soil pH](checking-soil-ph.md)`, so the file reads and navigates properly in any editor.

## If the files hold everything, what is the database for?

Speed. The local database stores titles, summaries, the location of each file, the searchable text and the list of link targets. It answers questions the files cannot answer cheaply, like "which notes link here?" or "which five notes fit this question best?".

It is an index, not a second copy. In _Vault settings_, _Check and repair_ compares it with the folder: files found under another name go back into the index, notes are restored from files, filenames are aligned with titles, and an entry whose file is gone leaves the table of contents.

So you can edit your AI notes in another editor. After the check, the app reads what is actually on disk.

## Do filenames change?

Yes, when a title changes. The filename is a slug of the title: lowercase, no diacritics, at most 60 characters. Rename an AI note and its file moves, and every link to it in the other notes of the vault is rewritten.

Two titles with the same slug get a suffix, `(1)`, `(2)`, decided by what already exists in the folder. A ZIP you downloaded before the rename keeps the old names. I think that is the right price for a folder whose names describe what is in the files.

## How do I take a vault with me?

Click _Download vault_ on the vault page. You get a ZIP with `base.md` and the `notes/` folder, the vault exactly as it is, with relative links between files.

Unzip it and open it in Obsidian, in VS Code or push it to a GitHub repository. The links work at once, and Obsidian's graph shows them with no plugin and no migration script. For anyone weighing an alternative to Obsidian, that export is the safety net: if you leave, the vault goes with you as a folder Obsidian already understands.

This is the main reason people look at SumizAI as an Obsidian alternative: the AI notes write themselves from your chats, yet what you own at the end is still local files Obsidian can open. What you give up (plugins, Canvas, sync) is laid out on the [SumizAI as an Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) page.

Besides the ZIP there is PDF in two levels (summaries only, or full notes) and an editable PowerPoint `.pptx` with 15 themes, its slides in table of contents order.

## What should I back up?

The notes folder. It holds all your AI notes, in an open format.

Time Machine or a plain copy covers it. The database is rebuilt from the files, so losing it costs a run of _Check and repair_, not your notes.

## Where does my AI provider key live?

In the macOS Keychain, not in the notes folder. That is deliberate: the folder is the thing you copy, back up and maybe keep in a cloud drive, and an API key has no business travelling with it. If you are comparing Obsidian alternatives with AI built in, ask each one where the key is kept.

The key is yours (bring your own key). The app works with 7 providers: Anthropic (Claude), OpenAI (GPT), Google Gemini, Groq, OpenRouter, a local Ollama and your own OpenAI-compatible server. Requests go straight from your computer to that provider, after the app asks for your consent, and you pay the provider for the model. SumizAI adds nothing on top.

## What is not stored, and what is not synced?

There is no server holding your AI notes. SumizAI does not collect notes, questions or documents. The account (an e-mail address) exists for the subscription: 7 days free without a card, then 1 USD a month, one plan for all your Macs.

There is **no sync between devices**. Two Macs hold two separate folders. I would rather say that here than have you find out after two weeks of writing on the wrong machine.

If you cancel, nothing is locked away. The notes still open and export; the app only stops starting new conversations. The Mac version is coming to the Mac App Store, and no build is downloadable yet. For the bigger picture, see the [AI notes app](/) page.

