---
title: "How does the table of contents file your notes?"
url: "https://sumizai.com/blog/how-the-table-of-contents-works.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "A chapter tree up to six levels deep, a model that files AI notes by picking a number, and a rebuild that lays the whole vault out again in batches of 60."
tags: ["automatic table of contents", "AI notes organisation", "note filing", "chapter tree", "markdown outline", "base.md", "sumizai"]
---

# How does the table of contents file your notes?

Capture is easy. What kills a notes folder is the filing: after a few weeks nobody decides where each page belongs, and the folder turns into a pile. In SumizAI that decision is taken by the model for every one of your **AI notes**, inside a structure narrow enough to stay consistent at note number 600. This is how the tree works, what you can change by hand, and when to let the app redo it.

## What shape is the table of contents?

A tree of chapters, at most six levels deep, with one running numbering: `1.` → `1.1` → `a)` → `a.1)` → `a.1.1`. Notes are the leaves and take their number from the same sequence. In the demo vault _Home garden_, _Sowing tomatoes indoors_ sits at 1.2 under _1. Vegetables_, and _Checking soil pH_ at 2.1 under _2. Soil and compost_.

Numbers aren't stored with the AI notes. They are computed from position, so when you move a chapter, everything below it renumbers itself.

This is a real structure the app keeps, not a view assembled from tags on the fly. That matters because a model can be asked to put a note into a structure. It can't be asked to put one into a tag cloud. This is also what sets the app apart as an alternative to Obsidian: Obsidian has folders, tags and links, but no outline kept by anyone except you.

Each AI note gets a number in the same sequence as the chapters, with its summary next to the title.

## How does an AI note find its chapter?

The model sees the chapters as a numbered list and answers with **a number**. It can also ask for a new sub-chapter under an existing one. A new top-level branch appears only when nothing fits anywhere.

Picking instead of naming is the decision the whole design rests on. An earlier version asked the model to name the right chapter for every note, and the tree split into variants of one idea: _Vegetables_, _Growing vegetables_, _Vegetable cultivation_, three siblings meaning the same thing. A number can't be paraphrased.

The model doesn't read the full outline either. It works from a digest of the vault held to 4,000 characters: the chapter map plus short conclusions, trimmed from the deepest levels first when it overflows. Filing cost therefore depends on how many chapters you have, not on how much you've written. The vault's own name is never offered as a chapter, and two chapters with the same name spelled with and without diacritics are merged when the tree is read.

## What if a note lands in the wrong place?

The model files most AI notes sensibly, and you move the rest. The tree is yours to edit: drag a note or a chapter to a new spot, or use **Move up**, **Move down**, **Make it a subchapter of the one above** and **Move out one level**. Rename a chapter, add one with **Add chapter** or **Add subchapter**, delete one.

Deleting a chapter doesn't delete notes. The confirmation says it plainly (_Its notes stay in the vault_) and they move up to the parent chapter.

A note without a chapter isn't lost either. It shows under **Not filed yet** in the app and at the end of `base.md` and of every export.

## Can I keep one conversation inside one chapter?

Yes. A chat can be pinned to a chapter (the tree marks it as _Chat pinned to this chapter_), and from then on the model files that conversation's AI notes only within that chapter's subtree. It doesn't even see the rest of the tree, so it can't drift to the root.

Handy for a month of questions about raised beds: every answer lands under one heading, and new sub-chapters grow there.

## What does Rebuild contents do that filing can't?

It looks at everything at once. Filing at creation time weighs one note against the current tree. That is the right call with what it knows, and it can never fix a structure that grew crooked before the note existed.

**Rebuild contents**, in the vault bar, reads all your AI notes in batches of 60 and lays the chapters out again with your main model, in the background. A note the model skips stays where it was. If a response fails, the tree is left untouched; a rebuild can't stop halfway and leave a mess.

The result has one firm rule: the tree must stay **flat, at most four levels, with no umbrella chapter** that holds everything else. If the model produces one anyway, a guard removes it. A root above the root costs a click and tells you nothing.

## When is a rebuild worth running?

After a burst of work that changed the shape of what you know. Not on a schedule.

The sign is a table of contents you scroll past instead of reading: a chapter that made sense at 20 notes and now holds 60, or two branches you keep mixing up. Run it, look at the result, fix by hand what you disagree with. It is safe to repeat.

Why four levels when the tree allows six? Depth is paid for on every read and earned once, at write time. Six exist so a subject that truly nests that far isn't blocked. Left alone, though, a model will happily build a five-level taxonomy for 40 notes, and you'd only ever click through levels four and five. The rebuild aims at a tree you can scan on one screen and reach in two clicks.

## What does the table of contents look like on disk?

A file called `base.md` in the vault folder: the outline in Markdown, with relative links to each file in `notes/`. It is generated, never hand-written, so it can't drift from the tree in the app.

That file turns an exported vault into a document rather than a bag of `.md` files. Open `base.md` in Obsidian, VS Code or on GitHub and the index works, because the links are relative paths between real files. If you are looking at SumizAI as an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html), this is the practical difference: Obsidian gives you folders and leaves the order to you, while here the order is built from your chats and still opens in Obsidian.

When you import `.md`, `.txt` or `.pdf` files, each one becomes an AI note and is filed like an answer from chat, with the table of contents updated after every single note.

## Is the tree only for browsing?

No. It's the map the model gets. With **Use my notes** ticked, every question travels with the vault's table of contents, and the app uses it together with search to pick at most 5 notes, sent in full within 24,000 characters. A tidy tree makes that choice sharper. A tree that has drifted makes it vaguer, which is the best argument for an occasional rebuild.

It's also the order of every export. The PDF (summaries only, or full AI notes) and the editable PowerPoint deck with its 15 themes follow the table of contents, so improving the tree improves the document you hand to someone else. When I compare Obsidian alternatives, I weigh this more than the editor: the structure is what other people end up reading.

The rest of the [AI notes app](/), from vaults to the AI providers it works with, is described on the main page. How a note reaches this tree in the first place is covered in [how a chat answer becomes a note](/blog/how-a-chat-answer-becomes-a-note.html).

