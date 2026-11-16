---
title: "SumizAI vs CherryTree: a node tree or AI notes in Markdown"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-cherrytree.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "CherryTree keeps rich-text nodes in one XML or SQLite file, free under GPL. SumizAI writes AI notes from model chats as .md files. Storage, export and import compared."
---

# SumizAI vs CherryTree: one file full of nodes, or AI notes in a folder of Markdown

CherryTree is a free hierarchical notebook by Giuseppe Penone and Evgenii Gurianov: every note is a node in a tree, with rich text, syntax-highlighted code and images, all saved in a single XML or SQLite file if you want. SumizAI also thinks in a tree, but it fills that tree with AI notes written from your chats with a model, and it saves them as separate Markdown files.

Version 1.7.2 of CherryTree, dated 22 August 2026, was the stable release when I read its site on 23 October 2026. All details about it below come from that page.

Every note in the list is a separate .md file; CherryTree would keep its nodes in one document.

## One portable file against a folder of plain files

The biggest practical difference is not the AI. It is where your notes physically live.

CherryTree lets you store a whole knowledge base in one SQLite or XML file, or spread it over multiple files and directories. One file is easy to copy to a USB stick, and only the single-file mode can be password protected, through 7-Zip. The site is candid that an unprotected copy is extracted to a temporary folder while the document is open.

Here each note is its own `.md` file on your disk, with a local database next to it as an index for search. You can read the notes in any text editor, put the folder under Git or open the exported vault on GitHub. There is no password option and no sync.

If a single encrypted file is what you need, CherryTree already solved it.

## CherryTree and the AI notes app, row by row

|  | SumizAI | CherryTree |
|---|---|---|
| Who writes | The model writes, from a chat answer you keep; you can correct it | You, in a rich-text editor |
| Price | 7 days free, then 1 USD a month; tokens billed by your AI provider | Free; donations through GitHub Sponsors, Ko-fi, PayPal |
| Licence | Proprietary | GPLv3+ |
| Platforms | macOS, coming to the Mac App Store; Windows, iOS and Android in preparation | Linux (PPA, Debian, Fedora, AppImage, Flatpak, Snap), macOS (installer, Homebrew, MacPorts), Windows (installer, portable) |
| Storage | Separate `.md` files plus a local index | One XML or SQLite file, or multiple files and directories |
| Tree | Table of contents up to 6 levels; the model picks the chapter | Node tree you build by hand and drag around |
| Links | Markdown links to notes that exist; backlinks under each note | Links to web pages, nodes, files and folders; `[[node name]]` auto links |
| Code | Code blocks as Markdown inside notes | Syntax highlighting, codeboxes, code execution |
| AI | 7 providers on your own API key | None mentioned on the site |
| Export | ZIP of Markdown, PDF in two levels, `.pptx` with 15 themes | PDF, HTML, plain text, CherryTree file; per node, node with subnodes, or whole tree |
| Import | `.md`, `.markdown`, `.txt`, `.pdf` | HTML, plain text, and files from Zim, KeepNote, Tomboy, Gnote, Treepad Lite and others |

## A Wednesday of shell scripts

You are writing a backup script. In CherryTree you have a node “Scripts”, a child node “rsync flags”, and inside it a codebox with the command, which you can run from the note. When something breaks you add a line of text below the codebox. Precise, and entirely manual.

Same Wednesday with AI notes: you ask Claude why `rsync --delete` removed a folder you wanted. The answer explains the trailing slash. You keep it. The model titles the note, adds a two-sentence summary, files it under chapter `5.1` (backups) and links it to an older note about exclude patterns. Your exact question and Claude’s exact answer sit at the bottom as the source, never overwritten.

On Friday you ask again, slightly differently. Before anything is saved, the app finds the Wednesday note, a second model rates the overlap on a 0 to 1 scale, and you get the choice to merge or keep both.

## When AI notes are the better choice

When the notes you care about come out of conversations, and you no longer have the patience to copy them into nodes. The app writes them up as AI notes, files them, avoids duplicates and links only to files that exist.

Also when you want later questions to use earlier answers. A question is sent with the vault’s table of contents and the full text of at most five relevant AI notes, capped at 24,000 characters, and you see which ones were used. Search works by meaning, not only by exact words.

And when the notes must leave the app in a modern format: Markdown in a ZIP, a PDF of summaries or full notes, or an editable PowerPoint deck.

People who arrive here from Obsidian are looking at the same trade. This app is an Obsidian alternative for collecting answers, and its exported vault opens in Obsidian as it is; the [Obsidian alternative with AI notes](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html) page goes through that comparison.

## When CherryTree is the better choice

- You want one file, optionally password protected, that you carry between machines.
- You run Linux, or need Windows or a portable build today.
- You keep code snippets you execute, LaTeX formulas, tables and embedded files inside notes.
- You pay nothing and want GPL software you can build from source.
- You write your notes yourself and like the control of a drag-and-drop tree.
- You are migrating from KeepNote, Tomboy or Treepad: CherryTree imports them directly.

That is a long list, and it is meant to be. For a classic personal notebook, CherryTree is the safer pick; the AI app only makes sense if most of your material is chat answers.

## Moving notes in either direction

**CherryTree to Mac app.** Export the tree, or one node with its subnodes, as plain text or PDF. The importer reads `.txt` and `.pdf` (as well as `.md` and `.markdown`), one file at a time, and turns each file into a note with the original text kept as its source. Your node hierarchy is not copied: the model places each note into chapters again, and the table of contents is rebuilt after every file.

**Mac app to CherryTree.** Export the vault as a ZIP: `base.md` with the table of contents and a `notes/` folder. CherryTree’s import menu lists plain text files and folders of them, and Markdown is plain text, so that is the route to test on a few files first. Expect the Markdown symbols to arrive as typed characters, not formatting.

## Before you choose: five questions

### Is CherryTree free?

Yes. The source code is GPLv3+, and the site asks only for optional donations.

### Can SumizAI password-protect a vault like CherryTree does?

No. Notes are plain files on your Mac with no password layer; use macOS disk encryption if you need it. CherryTree offers password protection for single-file documents.

### Does the Mac app run code blocks?

No. Code stays as text inside one of your AI notes. CherryTree can execute codeboxes and code nodes.

### Which AI models can write the notes?

Models from Anthropic, OpenAI, Google Gemini, Groq and OpenRouter, a local Ollama, or your own OpenAI-compatible server. You supply the key, approve the request, and pay the provider directly.

### What if I stop paying?

Your AI notes still open and export. Only starting new conversations stops.

CherryTree description, storage, export and import formats, platforms, version 1.7.2 and licence: [giuspen.net/cherrytree](https://www.giuspen.net/cherrytree/), read on 2026-10-23. Statements about the Mac app rest on its code and App Store metadata; the [AI notes app](https://sumizai.com/) page sums it up.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Craft](https://sumizai.com/alternative-to/sumizai-alternative-to-craft-do.html)
- [SumizAI vs Roam Research](https://sumizai.com/alternative-to/sumizai-alternative-to-roam-by-roam-research.html)
- [SumizAI vs DEVONthink](https://sumizai.com/alternative-to/sumizai-alternative-to-devonthink.html)
- [SumizAI vs UpNote](https://sumizai.com/alternative-to/sumizai-alternative-to-upnote.html)
- [SumizAI vs Heptabase](https://sumizai.com/alternative-to/sumizai-alternative-to-heptabase.html)
- [SumizAI vs GoodNotes](https://sumizai.com/alternative-to/sumizai-alternative-to-goodnotes.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Write the tree yourself, or let the model file it

The Mac release is being prepared for the Mac App Store: 7 days free, then 1 USD a month. The Mac page has the details.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
