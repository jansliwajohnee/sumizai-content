---
title: "What does SumizAI do for developers?"
url: "https://sumizai.com/blog/sumizai-for-developers.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "AI notes for engineering work: design decisions and debugging sessions saved as plain Markdown, with the original exchange kept verbatim under each note."
tags: ["developer notes", "architecture decision records", "debugging notes", "engineering knowledge base", "markdown notes for developers", "sumizai"]
---

# What does SumizAI do for developers?

Developers ask models questions all day, and the answers scroll away all day. The code survives in the repository. **The reasoning does not**: why this approach, what was rejected, what the benchmark said. SumizAI turns those exchanges into AI notes in Markdown, filed by topic, with the source kept word for word.

## What is worth keeping as AI notes?

Decisions together with the options you turned down. Most other things already live in the code or are not worth a file.

A note that says “we use RabbitMQ” adds nothing; the config file says that. A note that says “we picked RabbitMQ over Kafka because per-message acknowledgement mattered more than throughput at 2 000 messages a second” is the thing no commit records. Ask the model to lay out the trade-off, keep the answer, and it becomes one of your AI notes with a title, a summary and an expanded body.

Second category: debugging sessions that ended in an explanation. The fix is a commit. Why the bug was possible is a note.

## The source under every note is append-only

Every note keeps the original question and answer verbatim below the summary. Later merges add to that source; nothing edits or deletes it.

Engineering claims expire. When a note says connection pooling did not help, you open the source and see that the exchange was about PostgreSQL 12, a pool of 20 and one specific workload. A summary on its own cannot tell you that, and a summary nobody can audit turns into folklore.

The demo note “Sowing tomatoes indoors”. A note about a queue choice has the same parts: summary on top, source at the bottom.

## Markdown files next to your repository

A vault is ordinary `.md` files in a folder on your disk, with a local database used only as the index. There is no sync and no server holding the notes.

**Download vault** gives you a ZIP: `base.md` with the table of contents and a `notes/` directory. Links are relative, so you can unpack it into `docs/decisions/`, commit it, and the links still resolve in a pull request on GitHub. Diffs of AI notes are as readable as diffs of code. `grep -r` and `rg` work on it, and so does your editor's Markdown preview.

Links inside a note are plain Markdown, like `[Retry policy](retry-policy.md)`, not wiki-links. The model gets a map of existing titles and file names and can link only to those, so you do not end up with references to files that never existed.

## One vault per system

Not one per ticket. A vault is a boundary: a question asked inside it sees only that vault's AI notes. So ask yourself: when I ask about the billing service, should the model see the notes about the mobile app? If no, they belong in separate vaults.

Inside a vault, the table of contents carries the structure. It goes up to six levels, numbered `1.`, `1.1`, `a)`, `a.1)`, and the model files each new note into an existing chapter by number or asks for a subchapter. Subsystems make good chapters. Tickets do not. Delete a chapter and its notes move up to the parent, so restructuring is cheap.

## Local models and the consent step

For code you cannot send to a cloud, connect Ollama on your own machine or a custom server that speaks the OpenAI API (vLLM, LM Studio, an internal gateway). Those are two of the seven providers; the other five are Anthropic, OpenAI, Google Gemini, Groq and OpenRouter.

Every provider runs on your own API key. Requests go straight from your computer to the provider, and before anything is sent the app asks for your consent in a dialog that lists what goes out: your questions, excerpts of notes used as context, imported documents.

Context is bounded. A question travels with the table of contents and the full text of at most five of the most relevant notes, inside 24 000 characters, and the app shows which notes it used. A vault of 800 AI notes does not mean 800 notes in every prompt.

## Code stays in the repo; the why goes in the vault

SumizAI is not a snippet manager, and a note is a poor home for code that has to compile. Short fragments inside AI notes are fine as illustration.

The rule I would use: if it runs, it belongs in the repository. If it explains why the running thing looks the way it does, it belongs in your AI notes.

Existing write-ups come in through import. Point it at a folder of `.md`, `.markdown`, `.txt` or `.pdf` files (old ADRs, a vendor's PDF spec) and each file becomes a note with its original text attached as the source.

## Finding an old decision

Search works by meaning across the titles, summaries and content of your AI notes, so “why not Kafka” finds the queue note even if the word Kafka sits only in the source.

Duplicates are caught before they pile up. Full-text search and trigram matching pick candidates, a second model scores the overlap from 0 to 1 with a reason, and above the vault's **Similarity threshold** you decide whether to merge or keep both. Set the vault to **Always merge** if you revisit the same topics every sprint.

## Where it falls short, and where Obsidian fits

No sync, so a laptop and a desktop hold separate libraries. No shared vaults or team features, so this is a personal tool used inside a team. No plugins, no graph, no wiki-links.

Plenty of developers already keep a Markdown vault in Obsidian and are not shopping for an alternative to Obsidian at all. SumizAI is not trying to replace the editor; it is an [Obsidian alternative for the part where notes get written](/alternative-to/sumizai-alternative-to-obsidian.html). The model writes and files them, and the exported folder opens in Obsidian as it is, relative links included. If your setup depends on thirty plugins, the honest answer is that no Obsidian alternative without plugins will cover it, and this one does not try.

For handing a service over to a colleague, the exports do more than a folder of links: PDF+ prints full notes in table-of-contents order, and the `.pptx` export produces editable slides in one of 15 themes, without the source exchanges.

## Price and availability

Seven days free, then 1 USD a month, one plan. The model is billed by your provider; SumizAI adds nothing. No version can be installed yet: the macOS build (Apple silicon and Intel) is coming to the Mac App Store, and Windows, iOS and Android are in preparation. The [AI notes app](/) overview has the current status.

