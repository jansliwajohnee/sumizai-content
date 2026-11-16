---
title: "SumizAI vs SiYuan: block references or AI notes from chats"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-siyuan.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "SiYuan is an open-source, local-first block editor with references, databases and flashcards. SumizAI writes AI notes from your chats. Compared."
---

# SiYuan or SumizAI: blocks you link, or notes that file themselves

SiYuan is a local-first knowledge base built around blocks: every paragraph, heading or list item has its own ID, so you can reference or embed a single block anywhere, and a backlinks panel and graph show where it is used. It is open source under AGPL-3.0, free for local use, and full of power tools. SumizAI is far smaller in scope. It writes AI notes from the answers in your model conversations and files them into a table of contents.

If you enjoy building a dense web of references by hand, SiYuan rewards that effort like few other tools. If you mostly want last week's good AI answers to be findable, the trade-offs look different. SiYuan facts below come from b3log.org and its GitHub page, read on 23 October 2026.

Chapters numbered 1., 1.1, a) and a.1), filled by the model rather than by dragging blocks.

## Ten rows, two philosophies

|  | SumizAI | SiYuan |
|---|---|---|
| Unit of content | A whole note: title, summary, body, original chat | A block with its own ID |
| Who writes | The AI model, from a reply you keep | You; AI helps with writing and Q&A via the OpenAI API |
| Price | 7 days free, then 1 USD a month | Free locally; PRO features 64 USD once; subscription 148 USD with 8 GB official cloud |
| Licence | Proprietary | Open source, AGPL-3.0 |
| Platforms | macOS first, coming to the Mac App Store; Windows, iOS, Android in preparation | Windows, macOS, Linux, Android, iOS and iPadOS, HarmonyOS; Docker in the browser |
| Files on disk | One `.md` per note, readable anywhere | `.sy` files in JSON, SQLite index |
| Links | Markdown links to existing notes; backlinks | Block references, two-way links, graph |
| Extras | Duplicate check with merge offer | Databases with relations and rollups; FSRS flashcards |
| Sync | None | End-to-end encrypted sync (paid); S3 or WebDAV with PRO |
| Export | Vault ZIP, PDF in two levels, PowerPoint with 15 themes | Markdown with assets, PDF, Word, HTML |

## Planning a trip to Japan in each app

Two weeks before a trip you ask a model a dozen questions: whether a rail pass still pays off for Tokyo, Kyoto and Hiroshima, how IC cards work on buses, what to do with luggage between hotels.

SiYuan is great at the assembly. You keep a page per topic, then write an itinerary doc that pulls in single blocks with `((block reference))`: the luggage-forwarding paragraph shows up on day 4 without being copied. A database lists hotels with check-in dates and a relation to each city. Everything connects, but each block got there because you put it there.

With AI notes, the questions are the input. The rail pass answer becomes one of them, titled “Rail pass vs single tickets for three cities”, filed under `2.` “Transport”, with a summary on top and the model's full reply underneath, word for word. When you later ask about the Hiroshima day trip, the app sends the table of contents plus up to five relevant notes, within 24,000 characters, and names the notes it used. No itinerary doc, no hotel table. A tidy folder of AI notes instead.

Neither result is a full travel plan. One is a hand-built dashboard, the other a well-filed archive.

## Moving material between SiYuan and the app

SiYuan stores documents as `.sy` JSON, so do not point the importer at the workspace folder. Export first: SiYuan offers Markdown with assets, PDF, Word and HTML. Take the Markdown.

Then open the import panel and pick the exported files or their folder. The importer reads `.md`, `.markdown`, `.txt` and `.pdf`, handles one file at a time and rebuilds the table of contents after each. Every file becomes one of your AI notes, and its original text is kept as the source. Block references and database views turn into plain text, since there is nothing here to resolve them.

Going back is easier. The vault ZIP contains `base.md`, a `notes/` folder and relative Markdown links; SiYuan's import list includes Markdown, so the AI notes arrive as documents you can start referencing block by block.

## SiYuan is the stronger choice if

- you think in fragments and want to reuse one paragraph across ten documents;
- you want databases next to your notes, with relations, rollups and templates;
- you want spaced-repetition flashcards (SiYuan uses FSRS);
- you need Linux, Android, iOS, HarmonyOS or a self-hosted Docker setup now;
- you want encrypted sync between devices, or your own S3 or WebDAV storage;
- you want open-source code under AGPL-3.0.

Six reasons, and each is real. On features alone SiYuan is the bigger tool by a wide margin.

## And the app with AI notes wins if

Your bottleneck is writing, not linking. SiYuan's AI helps you continue a paragraph or answer questions, but you still decide which block goes where. Here the model writes the AI note, picks a chapter by its number (or asks for a new subchapter), and can only link to notes that exist, because it receives a map of titles and files.

You care about plain files. A SiYuan workspace is JSON plus SQLite; a vault here is ordinary `.md` files plus a local index. That difference matters most for people leaving Obsidian. Anyone looking for an Obsidian alternative that still writes Markdown can read the [Obsidian alternative page](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html): the app writes notes from your chats, and the exported folder opens in Obsidian unchanged.

You want duplicates caught. Before saving, a full-text and trigram search finds candidates, a second model scores similarity from 0 to 1, and above the vault's threshold you choose: merge or keep both. Merging only appends.

And you want AI costs in your hands: seven providers on your own key, including a local Ollama or an OpenAI-compatible server, for 1 USD a month on top of what the provider bills.

## SiYuan and AI notes: common questions

### Is SiYuan free?

Local use is free. The pricing page lists PRO features (third-party S3 and WebDAV sync) for 64 USD once and a 148 USD subscription with 8 GB of official cloud storage; the page is not consistent about whether that subscription is yearly or lifetime.

### Does SiYuan have AI?

Yes, through the OpenAI API: continued writing, translation, abstracts, brainstorming, grammar fixes and Q&A chat.

### Can I sync SiYuan through Dropbox or iCloud?

SiYuan's own documentation warns against syncing through third-party sync disks because data can be corrupted. Use its sync or S3 or WebDAV instead.

### Does this app have block references?

No. A note is the smallest unit, and links are ordinary Markdown links like `[Rail pass](rail-pass.md)`.

SiYuan: [b3log.org/siyuan](https://b3log.org/siyuan/en/) (features and download list), [pricing page](https://b3log.org/siyuan/en/pricing.html) and the [siyuan-note/siyuan repository](https://github.com/siyuan-note/siyuan) (licence, data format, import and export), all read on 2026-10-23. The other column relies on the app's source code; a plain overview lives on the [AI notes app](https://sumizai.com/) home page.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Craft](https://sumizai.com/alternative-to/sumizai-alternative-to-craft-do.html)
- [SumizAI vs Roam Research](https://sumizai.com/alternative-to/sumizai-alternative-to-roam-by-roam-research.html)
- [SumizAI vs DEVONthink](https://sumizai.com/alternative-to/sumizai-alternative-to-devonthink.html)
- [SumizAI vs UpNote](https://sumizai.com/alternative-to/sumizai-alternative-to-upnote.html)
- [SumizAI vs Heptabase](https://sumizai.com/alternative-to/sumizai-alternative-to-heptabase.html)
- [SumizAI vs GoodNotes](https://sumizai.com/alternative-to/sumizai-alternative-to-goodnotes.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Skip the block wiring for a week

Seven days free. Ask your usual questions and see how many AI notes are waiting in their chapters on day seven.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
