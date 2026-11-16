---
title: "SumizAI vs Trilium Notes: a note tree or AI notes"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-trilium-notes.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "Trilium Notes is a free, self-hosted tree of notes you build and script. SumizAI files AI notes from your chats into a table of contents. An honest comparison."
---

# SumizAI vs Trilium Notes: two trees, two gardeners

Trilium Notes is a free, open-source notebook for people who like to build structure: an arbitrarily deep tree of notes, clones that let one note sit in several branches, labels and relations, and scripts on top. SumizAI also arranges everything in a tree, but the model does the arranging, because the content is AI notes written from your chats.

In Trilium you are the gardener. Here the model plants and you prune. Trilium facts on this page come from triliumnotes.org and the project's GitHub repository, read on 23 October 2026.

The vault's table of contents in dark mode. Chapters go up to six levels; numbering runs `1.`, `1.1`, `a)`, `a.1)`.

## How each app grows its tree

Trilium gives you the tree and every tool to shape it. You create a note, drag it under a parent, clone it into a second branch, add a label like `#status=draft` or a relation to another note, and later run a query or a script over those attributes. Nothing moves unless you move it.

In the AI notes app the table of contents is shared between you and the model. When an answer is worth keeping, the model either picks an existing chapter by its number or asks for a new subchapter, up to six levels deep. Delete a chapter and its notes move up to the parent; nothing is lost. There are no clones, labels or scripts.

That makes the trade easy to state. Trilium rewards people who enjoy designing structure. The other tree is for people who would rather never think about where a note goes.

## Feature by feature

|  | SumizAI | Trilium Notes |
|---|---|---|
| Who writes | The model, from your chat; you edit | You |
| Who files | The model chooses or creates the chapter | You, with clones and attributes |
| Price | 7 days free, then 1 USD a month | Free, no premium tier, no sign-up |
| Licence | Proprietary subscription | AGPL-3.0, open source |
| Platforms | macOS first, coming to the Mac App Store; Windows, iOS, Android in preparation | Desktop builds for Windows, macOS and Linux; server reachable in a browser; no official mobile app |
| Storage | Plain `.md` files on your disk, local index | Trilium's own database, on your machine or your server |
| Encryption | None added; notes never go to a server of ours | Per-note protection with a password |
| Note types | Text notes with source, summary and body | Text, code, Canvas (Excalidraw), Mermaid, relation maps and more |
| AI | The core: 7 providers on your own key | Opt-in, disabled by default |
| Sync | None | Through a self-hosted or cloud sync server |
| Import and export | Import `.md`, `.txt`, `.pdf`; export ZIP, PDF, PowerPoint | Markdown, HTML and OPML both ways; Evernote import |

## Bringing a Trilium tree across

Trilium exports to Markdown, HTML and OPML. Choose Markdown, then point the importer at the exported folder. It handles `.md`, `.markdown`, `.txt` and `.pdf`, takes one file at a time, keeps each file's original text as the source of the new note and rebuilds the table of contents after every file.

Be clear about what does not survive. Clones, labels, relations and scripts have no equivalent, and the model builds its own chapter structure instead of copying your branches. HTML and OPML exports are not accepted at all.

Back the other way: the vault exports as a ZIP with `base.md` (the table of contents) and a `notes/` folder, and Trilium imports Markdown.

## Stay with Trilium when

- You want to pay nothing and own the server: Trilium is free with no locked features, and you can host the sync server yourself.
- Structure is the point. Clones, attributes and queries let one note live in three contexts, which a model-chosen table of contents does not attempt.
- You script your notes. Trilium is programmable; there is no scripting here.
- You draw. Canvas based on Excalidraw, Mermaid diagrams and relation maps are built in.
- You need Linux, or a browser on any machine via your own server.

## Choose the AI notes app when your day looks like this

Picture a sysadmin moving a database to a new host. Over one day they ask GPT about `pg_dump` flags, how to keep replication lag low during the switch, and what to check before cutting DNS over. In Trilium each of those answers needs a note, a place in the tree and maybe a label. By evening, two of the three get written down.

With the chat-first app all three land as AI notes under `5. Databases`, each with a title, a one-line summary and the original exchange kept verbatim underneath. When the second question overlaps the first, a second model scores the pair between 0 and 1 and offers a merge. Next month, a question about a failed restore goes out with the table of contents and up to five relevant notes, capped at 24,000 characters, and the screen lists which ones were used.

Price is the other half: 1 USD a month for the [AI notes app](https://sumizai.com/), plus model costs paid straight to Anthropic, OpenAI, Google, Groq or OpenRouter. With local Ollama or your own OpenAI-compatible server, questions never leave your network.

If Obsidian is also on your list, the comparison there runs along the same line: SumizAI works as an [Obsidian alternative that writes AI notes for you](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html), and because the notes are plain Markdown with relative links, the exported vault opens in Obsidian. Few Obsidian alternatives give you that exit.

## Trilium versus AI notes: common questions

### Is Trilium Notes still maintained?

Yes. The project lives on GitHub under the TriliumNext organisation and is published at triliumnotes.org.

### Does Trilium have AI?

Its site says AI features are opt-in and disabled by default. You turn them on; they do not write notes from your outside chats.

### Is there a mobile app?

Trilium has no official one; the site points to its web interface and unofficial apps such as TriliumDroid. The Mac version of the AI notes app comes first, with iOS and Android in preparation.

### Can I keep both?

Yes. Use Trilium for the structured knowledge base you design, and let the model keep the answers from your chats in a separate vault.

Sources: [triliumnotes.org](https://triliumnotes.org/) and the [TriliumNext/Trilium repository](https://github.com/TriliumNext/Trilium) on GitHub (features, platforms, licence), both read on 23 October 2026.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Logseq](https://sumizai.com/alternative-to/sumizai-alternative-to-logseq.html)
- [SumizAI vs Zettlr](https://sumizai.com/alternative-to/sumizai-alternative-to-zettlr.html)
- [SumizAI vs Joplin](https://sumizai.com/alternative-to/sumizai-alternative-to-joplin.html)
- [SumizAI vs Anytype](https://sumizai.com/alternative-to/sumizai-alternative-to-anytype.html)
- [SumizAI vs Notesnook](https://sumizai.com/alternative-to/sumizai-alternative-to-notesnook.html)
- [SumizAI vs Notion](https://sumizai.com/alternative-to/sumizai-alternative-to-notion.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Let the model plant the tree

The app comes to the Mac App Store first: 7 days free, then 1 USD a month.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
