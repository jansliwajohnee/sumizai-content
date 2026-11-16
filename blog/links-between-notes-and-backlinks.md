---
title: "How do notes link to each other, and what links back?"
url: "https://sumizai.com/blog/links-between-notes-and-backlinks.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "How SumizAI links AI notes: plain Markdown links inside sentences, only to files that exist, a list of backlinks under each note, and renames that fix every link."
tags: ["backlinks", "markdown links between notes", "linked AI notes", "note links", "rebuild links", "sumizai"]
---

# How do notes link to each other, and what links back?

A link between two AI notes in SumizAI is a phrase in a sentence that points to another `.md` file in the same vault. Nothing more. The model that writes the note places the link, the app checks that the target file exists, and every note shows two lists underneath: _Links from this note_ and _Notes that link here_.

## What does a link look like inside an AI note?

Like any Markdown link: `[Sowing tomatoes indoors](sowing-tomatoes-indoors.md)`. The label is the title of the other note, the target is its filename in the vault's `notes/` folder.

There are no wiki-links. You will not find `[[Sowing tomatoes indoors]]` anywhere in the files, because double brackets are a convention of a few editors, while the plain form is read by every Markdown viewer, by GitHub and by VS Code without a plugin.

The link sits where it makes sense in the text. A note about compost says, for example, that finished compost goes into the seed mix described in the tomato note, and the words "tomato note" carry the link. No separate _Related_ block at the end.

An earlier version of the app kept links in a database table and rendered a Related section from it. In real vaults that section stayed empty, because nothing ever filled the table. Moving the link into the text fixed it for good: a link exists in the file, or it does not exist.

## Who decides what gets linked in AI notes?

The model that writes the note. It does not get a free hand, though.

Before writing, it receives a map of **up to 8 existing notes**: title on the left, filename on the right. The candidates come from a search over the vault using the material being written up. When the search finds fewer than 5, the app fills the gap with recently changed notes of the same vault, so the model still has something to choose from. It is asked to weave a link into a sentence where the connection is real, not to produce a list.

Then a filter runs on the way in. Any link to a `.md` file that is not on the map is removed, and its label stays as plain text. External `https://` links are left alone.

## Why not simply trust the model with filenames?

Because it will invent them. Ask for a link to your note on soil acidity and you will get `soil-acidity.md`, a sensible name for a file that does not exist (the real one is `checking-soil-ph.md`).

In a vault of AI notes, a dead link costs more than a missing one. You click, nothing opens, and from then on you distrust every other link in the vault. So the rule is strict on purpose: the model picks the sentence, the app decides which targets are real.

The same check protects the _Search notes_ chat mode, where the answer points to notes with links. Those are checked against the vault before the answer is stored.

## Where do backlinks come from?

Every AI note reads its outgoing list straight from the file. The incoming one cannot be, since answering "who points here?" from text alone would mean opening every file in the vault each time you open a note.

So the app keeps a derived column in its local index with the targets each note links to, and looks the current filename up there. The filename is padded with spaces in that lookup, which is why `gin.md` never matches `login.md`.

That column can be rebuilt from the files at any time. The file stays the source; the index only answers faster.

## What happens to links when I rename a note?

They follow. Renaming an AI note renames its file, because the filename is a slug of the title (lowercase, no diacritics, at most 60 characters). Every `](old-name.md)` in the other notes of the vault is rewritten to the new name.

The order is fixed: write the new file, rewrite the references, delete the old file. If anything fails halfway, the rewritten notes are restored and the new file is removed. Two titles that slug to the same name get a suffix, `(1)`, `(2)`, and a link written with or without that suffix still resolves to the right file.

One cost is known and accepted: a ZIP you downloaded before the rename keeps the old filenames.

## Can I rebuild the links in a whole vault?

Yes. On the vault's contents page there is a _Rebuild links_ button. It goes through every note, removes links that lead nowhere and adds missing ones right inside the sentences. It runs slowly in the background, one note at a time.

The vault toolbar: _Rebuild links_ sits next to _Download vault_ and the PDF and PowerPoint exports.

Use it after an import. AI notes written from a folder of `.md`, `.txt` or `.pdf` files arrive one by one, so the first ones had no neighbours to link to.

For lighter repairs there is _Check and repair_ in the vault settings. It needs no model: a link that says `notes/compost.md` or `../notes/compost.md` is corrected to `compost.md`, because only the filename counts.

## Can I add links by hand?

Yes, and they behave exactly like the links in AI notes the model wrote. A generated link is just a Markdown link, so a link you type is the same kind of thing.

Point it at a real filename from `notes/`, save, and it shows up in the outgoing list. The note on the other end lists yours under _Notes that link here_.

This is why I prefer it to a links table. My edits and the app's edits live in one format, and I can check either with a text editor, or with Obsidian itself. That is why I count the app among Obsidian alternatives without pretending it replaces every part of Obsidian.

## Do the links still work in Obsidian after export?

They do. _Download vault_ gives a ZIP with `base.md` (the table of contents) and the `notes/` folder, and all links between notes are relative filenames. Unzip it, open the folder in Obsidian, and the graph view draws the connections with no plugin and no migration step. If you are comparing Obsidian alternatives, this is the detail to test first: does the export keep links Obsidian understands? Here it does.

That is the honest case for SumizAI as an Obsidian alternative: your notes write themselves from AI chats, and the result is still a folder Obsidian can open. The full comparison, including what you give up (plugins, Canvas, sync), is on the [SumizAI as an Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) page.

If you have not seen how a single answer turns into a note, start with the overview of the [AI notes app](/). The price is one plan at 1 USD a month after a 7-day trial, and the Mac version is coming to the Mac App Store; no build is downloadable yet.

## What do links change for the next question?

Less than you would guess, and that is deliberate. When you ask a question in a vault, the model gets the table of contents plus the full text of at most 5 relevant notes within a 24,000-character budget. It does not follow links to pull in more.

Links are for you. They turn a set of AI notes into something you can walk through: from the compost note to the seed mix, from there to germination temperatures (22 to 25 °C in the demo vault), and back through the backlinks.

