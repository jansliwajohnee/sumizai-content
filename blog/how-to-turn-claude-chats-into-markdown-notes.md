---
title: "How to turn Claude chats into Markdown notes"
url: "https://sumizai.com/blog/how-to-turn-claude-chats-into-markdown-notes.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Claude models on your own Anthropic key, each useful answer saved as one of your AI notes in a plain .md file, plus what to do with chats already on claude.ai."
tags: ["claude to markdown", "claude chat notes", "export claude conversation", "anthropic api key notes", "claude answers as md files", "save claude chats", "sumizai"]
---

# How to turn Claude chats into Markdown notes

Claude writes its answers in Markdown already: headings, lists, code blocks. What a chat window lacks is a file per idea, filed somewhere you will find it again. In SumizAI you talk to Claude models on your own Anthropic key and the useful answers become **AI notes**, each one a `.md` file in a folder on your Mac. The app does not connect to claude.ai, so older chats come in by paste or import.

## Which Claude does SumizAI talk to?

The Claude models offered through the Anthropic API, called with a key you create in the Anthropic Console. The key starts with `sk-ant-`; you paste it in Settings, click _Save key_ and then _Test connection_, and the app replies that Claude answered correctly when it works. It is stored encrypted and never shown in full again.

Two things this is not. It is not your claude.ai account: no login, no access to your Projects or chat list there. And it is not covered by a Claude Pro or Max plan, because API calls are billed by Anthropic separately, per token, under your own account.

After the key, choose the _Model answering in chat_. A second, cheaper model does the supporting work (titles, summaries, topic matching), which keeps a long session from costing more than the conversation itself.

## What turns a Claude reply into one of your AI notes?

A short pipeline that starts after the answer finishes streaming. A draft is written with a title, a summary and an expansion. The draft is matched to a chapter. Full-text search and trigrams look for a note that already covers the topic, and a second model scores the match from 0 to 1 with a reason.

Above the vault's threshold, the app asks: merge or keep both. You can also set a vault to always merge or always create. A merge only appends, so nothing you saved earlier disappears.

Then the AI note is written to disk. You do not press anything for this; the switch to stop it lives on the conversation, for sessions you know are throwaway.

## What is inside an AI note's .md file?

Open one in any text editor and you see four parts, top to bottom:

YAML front matter: `id`, `title`, `summary`, `section` (the chapter), `created` and `updated`;the title as a `#` heading, followed by the expansion in Claude's own Markdown structure: sub-headings, bullet points, fenced code;for material longer than 6 000 characters, a separate full-content section that is told not to summarise;a sources section with the original question and Claude's complete reply, verbatim.

The boundaries between those parts are HTML comments such as `<!-- sumizai:sources -->`. They are invisible in any Markdown preview, and the app uses them instead of headings because Claude's answers are full of headings themselves.

The note list: every row is a separate Markdown file on disk.

Links between files are standard `[Title](file.md)` syntax. The model is handed a map of the titles and filenames that exist in the vault and can only link to those, so a renamed or invented target never survives. Each note also lists its backlinks underneath. No `[[wiki-links]]`, on purpose: plain links render on GitHub and in VS Code without any plugin.

## How do I bring in chats I already had on claude.ai?

One at a time, by hand, and that is fine. Under each Claude reply there is a copy button; for a whole exchange, select the text from your question down. Paste it in the vault's Import tab, in the _Import a conversation_ field, and it becomes AI notes the same way a live chat does.

_Import text_ lets the model rewrite the material into a structured note and keeps your paste as the source. _Add without AI_ stores it exactly as pasted, which suits a reply you already consider final, like a finished checklist or a block of code you do not want touched.

Already saved Claude replies as files? _Choose files or folder_ accepts `.md`, `.markdown`, `.txt` and `.pdf`, and it works through a folder one file after another, so each new note sees the ones before it. A PDF always comes in word for word, without the model.

Claude's own data export (Settings, Privacy, Export data, on the web or in Claude Desktop) sends a download link by email that expires after 24 hours. It is an account archive rather than a set of notes, and it is not a format the importer reads. Use it as a backup and a place to copy from.

## Does Claude see my older notes when I ask something new?

Some of your AI notes, and the app tells you which. Each question goes out with the vault's table of contents and the full text of at most 5 notes that match it best, inside a budget of 24 000 characters.

Under the answer, _Answered using your notes_ lists them. That is the honest version of a "second brain": Claude never reads the whole vault, so a vault of 3 000 AI notes costs the same per question as one of 30.

Vaults are hard walls. A question in your work vault cannot pull in a note from the one about your garden.

## Where do the files go, and is this an alternative to Obsidian?

Into the notes folder you chose in Settings, one subfolder per vault. A local database sits next to them as an index for search; the `.md` files are the record. There is no sync and no server copy, and the app does not collect your notes or questions.

Obsidian opens them as they are. That is the point where SumizAI and Obsidian meet: one writes AI notes from your Claude chats, the other is a hand-written editor with plugins. If you are weighing it as an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html), the comparison page goes through prices, sync and plugins point by point. An Obsidian alternative in this sense means less typing, not a different editor: the files stay readable in both.

For sharing outside Markdown tools, a vault exports as a ZIP (`base.md` plus `notes/`), as PDF with summaries only or full notes, or as an editable PowerPoint deck with 15 themes.

## Can I start today?

Not yet. No version is available to download. The Mac build for Apple silicon and Intel is coming to the Mac App Store; Windows, iOS and Android are being prepared.

When it arrives: 7 days free, then 1 USD a month on a single plan. Claude usage goes on your Anthropic bill and nothing is added to it. If you stop paying, your AI notes still open and export; only new conversations stop. The [AI notes app](/) page has the rest of the details.

