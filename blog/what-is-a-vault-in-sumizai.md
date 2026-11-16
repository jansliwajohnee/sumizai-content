---
title: "What is a vault, and why is it a boundary?"
url: "https://sumizai.com/blog/what-is-a-vault-in-sumizai.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "A vault holds your AI notes, their table of contents and duplicate settings, and it marks the edge of what the model sees when you ask a question."
tags: ["ai notes vault", "sumizai vault", "knowledge vault", "ai context boundary", "markdown vault", "sumizai"]
---

# What is a vault, and why is it a boundary?

In most apps a notebook or folder is there to keep the sidebar tidy. In SumizAI the container has a job. **A vault decides what the model sees**, what the duplicate check compares, what the table of contents describes and what lands in an export. Get the vaults right and your AI notes stay useful at note 300.

## What exactly is a vault?

A named space that owns four things: its notes, its table of contents, its conversations and its settings. You make one with **Create vault**, give it a name, and every answer you keep from a chat inside it becomes one of its AI notes.

On disk it is a plain directory in the folder you chose for your notes. Inside sits `base.md`, the generated table of contents, next to a `notes/` directory holding one `.md` file per note. A local database indexes those files for search and for the tree, but the files are the notes. If you know Obsidian, the word is familiar: there, too, a vault is a folder of Markdown files, and that shared idea is why this app works as an alternative to Obsidian without any conversion step.

The demo vault Home garden: numbered chapters, each note filed under one of them.

The vault is also the unit the app thinks in. A question, a duplicate check, a rebuild of the contents: each one runs on exactly one vault.

## What does the boundary mean for AI notes in practice?

When you ask a question inside a vault, the model gets that vault's table of contents plus the full text of at most 5 of its most relevant notes, capped at 24,000 characters. **Notes from other vaults are never included.** No cross-vault ranking, no "related from elsewhere" surprise.

Picture two vaults. In _Home garden_, "beds" means raised beds and a question about them pulls in your notes on compost and spacing. In a vault for a hospital IT contract, the same word means something else entirely. Neither vault's AI notes leak into the other's answers.

It is a privacy property you can reason about, too. A request goes straight from your computer to the provider you connected, the app asks for consent before sending, and material in a vault you are not asking in is simply not part of that request.

## How should you draw the lines between vaults?

Do not ask what a note is about. Ask **what should be in the room when you ask about it**.

That question gives you fewer, larger vaults than sorting by topic, and that is the right result. Context is what makes answers good. A vault with four AI notes gives the model nothing a folder would not.

A quick test for any single note: would you be annoyed by an answer that ignored it? Then it belongs in the vault where you ask that question. Would you be annoyed by an answer that _used_ it? Then it belongs somewhere else.

## Which settings live on the vault?

Open **Vault settings** and you find two groups.

**Duplicates.** The mode (ask, always merge or always create) and the similarity threshold. Before a note is saved, full-text search and trigrams find candidates in the same vault and a second model scores each one from 0 to 1. Above the threshold the mode decides. In ask mode, notes waiting for your decision are listed on the vault page, not only in the chat.**Note language.** Notes are written in the vault's language whatever the language of what you paste; _Automatic_ follows the notes already in the vault. The interface language is separate, with 16 to choose from.

A study vault full of AI notes and a diary-style vault want different answers to the duplicate question, which is exactly why the setting sits on the vault and not on your account.

## How do you get a note from one vault into another?

Through files, because that is what notes are. Press **Download vault** to get a ZIP with `base.md` and `notes/`, take the `.md` file you want, and import it into the other vault. Import accepts `.md`, `.markdown`, `.txt` and `.pdf`, one file at a time, and the imported text is kept as the new note's source while the table of contents updates after each note.

The same ZIP goes back in whole, too. A vault archive imported into the app always becomes a new vault, and a name that already exists gets a suffix instead of overwriting anything.

This is also where the app meets Obsidian. The ZIP uses ordinary Markdown links, `[Title](file.md)`, not wiki-links, so the unpacked folder opens as an Obsidian vault with the links working. People looking for an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) that writes the AI notes for them can keep Obsidian as the reader for the same files.

## How many vaults should you have?

Fewer than you think. One vault per project is the classic mistake: twenty containers with four notes each, none of which can answer anything.

What works is one vault per _area of thinking_ that outlasts a single project. Your work. A field you are studying. A long hobby, like the garden. Projects become chapters inside them, which is what a table of contents up to six levels deep (`1.`, `1.1`, `a)`, `a.1)`) is built for.

Splitting later is a file operation, not a migration. Export, pick the notes, import them where they belong.

## What happens to your vaults when you stop paying?

They stay readable. After you cancel, the app still opens your vaults and exports them; it only stops starting new conversations. And since every AI note is a `.md` file in your own folder, any text editor opens them even without the app. That is the first thing to check in any Obsidian alternative: what happens to your files on the day you leave.

The licence is a signed token valid for 7 days, so a week offline is normal work, not a lockout. Deleting your account does not touch vaults either: they and their files stay on your computer. Deleting a vault is the one destructive action, which is why the app makes you type the vault's name to confirm.

## Is a vault shared, or yours alone?

Yours alone. No shared vaults, no sharing links, no co-editing, and no sync between devices. There is no server holding notes, and SumizAI does not collect notes, questions or documents.

What you share is output: the ZIP of Markdown, a PDF (summaries only, or full notes) or an editable `.pptx` deck with 15 themes in table-of-contents order. For a team wiki with sync and plugins, pick a tool built for that; no Obsidian alternative focused on personal AI notes replaces one.

One practical note: nothing is downloadable yet. The macOS app is coming to the Mac App Store, other platforms are in preparation, and after a 7-day trial it costs 1 USD a month. For the full overview, read the page about the [AI notes app](/).

