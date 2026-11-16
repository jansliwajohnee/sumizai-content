---
title: "What does SumizAI search when you search?"
url: "https://sumizai.com/blog/how-search-works-in-sumizai.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "How search in your AI notes works: title, summary, body and the original chat, ranked by weight, typo-tolerant, plus a chat mode that finds a note by meaning."
tags: ["note search", "full text search notes", "search AI notes", "search by meaning", "find notes", "sumizai"]
---

# What does SumizAI search when you search?

SumizAI gives you three ways to find something in your AI notes, and they answer different questions. The _Search notes_ field finds a word. The _Search notes_ chat mode finds a note when you only remember what it was about. _Find in note_ (Cmd+F) finds a phrase inside the note you have open.

## Which parts of an AI note does the search field read?

Four, and each has its own weight in the ranking: the **title** (10), the **summary** (5), the **body** (2) and the **source material** (1), which is your original question and the model's answer, kept word for word under the note.

The fourth one matters more than its weight suggests. You rarely remember what a note is called. You remember an example from the conversation, a number, a product name the model mentioned once. That text is in the index too, so a note about compost turns up when you type _nitrogen_, even if that word sits only in the answer you got three weeks ago.

The weights keep order. A hit in the title still beats a passing mention deep in the source.

## What do I see when I search my AI notes?

Each result shows the title, the one-line summary and, when the match is in the body, a short fragment of about 40 words with your words highlighted.

The notes list of the demo vault. The placeholder says what the field is best at: a title or a word from the summary.

With a few dozen AI notes on one subject, that fragment saves you from opening five of them to find the right one. You can tell from the list whether this is the note where the watering schedule was worked out or one where it came up in passing. The same field sits above the table of contents on the vault page, so you can search without leaving the chapter view.

## Does it cope with accents, word endings and typos?

Accents, yes. The index strips diacritics, so _pomidor_ and _pomidór_ are the same word and typing Polish or French without accents is not a mistake.

Word endings are handled with prefix matching. Every word you type is treated as the start of a word, so _compost_ also finds _composting_ and _composted_. There is no stemming dictionary behind it.

Typos get a second pass. When the word index does not fill the page, the app compares your query with titles and summaries by trigram similarity and adds notes that score above 0.6. They land below the exact hits, because a rescued typo should not outrank a real match.

One more rule: words in the field are joined with AND. Type _tomato seedlings_ and you get notes that contain both.

## How does search by meaning work?

This is the chat mode, and it exists for the case where the word search has nothing to grab. The example that started it: someone asks for "the Java Spring library for FHIR", while the note says _HAPI FHIR_ and never uses the word _library_.

A helper model turns your question into 3 to 8 search terms, adding English equivalents and obvious proper names, since library and tool names are written in English even in Polish notes.Your question plus those terms go to the same search as the field, 6 results per term. A note hit by several terms ranks higher.The main model sees up to 12 candidates (title, filename, summary, a fragment of up to 400 characters) and answers in 2 to 4 sentences, then lists the notes that hold the answer as links.

It is told to answer only from those notes, to say plainly when none fits and to skip a candidate that is unrelated. Links in the answer are checked against the vault, so you cannot be sent to a file that does not exist. This mode does not create new AI notes: you are looking, not writing.

No embeddings, no vector database. The meaning comes from a model writing the search terms and a model reading the shortlist, which costs two calls to your own AI provider (Claude, GPT, Gemini or any of the 7 supported) and keeps every step inspectable.

## How is search connected to what the model reads?

The same index picks the context for a normal question. When you ask something in a vault, the model gets the table of contents and the full text of at most 5 of the most relevant notes, within a 24,000-character budget, and the app shows which notes it used.

So the model never reads the whole vault. If an answer ignores one of your AI notes you expected, search for it yourself: when the field cannot find it either, the problem is the wording of the note, not the model.

## Is search limited to one vault?

Yes. Every query carries the vault, for the field, the chat mode and the context alike. A vault about the garden and a vault about work never mix in results.

In practice this keeps results short. Fifty AI notes about one subject are easy to search; five hundred about everything are not, so I would rather open the right vault first. Obsidian users know the idea: a vault there is a folder too, which is part of why this app works as an alternative to Obsidian rather than a new format to learn.

## What if search misses a note I know is there?

Open the vault settings and run _Check and repair_. The index is derived data: the searchable text is computed from the `.md` files, and the files win every disagreement.

The check finds files that went missing from the index, restores notes from files that the index lost, and aligns filenames with titles. It never deletes an AI note that still has its file.

## Where do my AI notes live while I search?

On your Mac, as ordinary Markdown files, with a local database next to them as the index. Nothing about your searches leaves the computer, except the two model calls of the chat mode, which go straight to the provider whose key you entered.

That also makes SumizAI a practical Obsidian alternative for one specific job: the AI writes and files the notes, you search them here, and the same folder still opens in Obsidian when you want plugins or a graph. If you came here comparing Obsidian alternatives, weigh this part: search is built around notes the AI wrote, with the source chat inside each one. The trade-offs, including no sync, are in the [Obsidian alternative comparison](/alternative-to/sumizai-alternative-to-obsidian.html).

If you are new here, the [AI notes app](/) overview shows the whole path from a chat answer to a note. The Mac version is coming to the Mac App Store; after a 7-day trial it costs 1 USD a month.

## And Find in note?

Cmd+F opens a find bar over the open note with a counter ("3 of 7"), next and previous buttons and highlighting. The app takes over the shortcut on purpose, because the window it runs in has no find bar of its own.

Long notes rebuilt from a PDF or a big import are where this earns its place.

