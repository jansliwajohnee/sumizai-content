---
title: "How does SumizAI stop your library filling with near-duplicates?"
url: "https://sumizai.com/blog/how-sumizai-handles-duplicate-notes.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Up to 5 candidates from full-text and trigram search, a helper model scoring each from 0 to 1, three vault modes, and merges that keep AI notes append-only."
tags: ["duplicate notes", "merge notes", "similarity threshold", "AI notes duplicates", "note deduplication", "knowledge base clutter", "sumizai"]
---

# How does SumizAI stop your library filling with near-duplicates?

Ask a model about compost ratios in April, again in June and once more in September, and a plain chat log gives you three answers in three places. A folder of **AI notes** would do the same if nothing stopped it: three files, each a little better than the last, none complete. SumizAI puts one check in front of every save to catch exactly that.

## What runs before a new note is saved?

Two passes. Cheap first, expensive second.

The first pass is search. The draft is matched against the vault with full-text search (SQLite FTS5 over titles, summaries, note bodies and source text) and with trigram similarity. Together they return a shortlist of at most 5 existing AI notes. That is database work and takes milliseconds.

The second pass is judgement. A helper model reads the draft next to each candidate and answers with **a score from 0 to 1 and one sentence of reasoning**. It is a short call, capped at 800 tokens, on your own provider key like everything else. You couldn't afford to have a model compare a draft with all 900 notes in a vault, and a database can't tell that two paragraphs make the same point. The split gives each side the job it is good at.

## Why two search methods for the candidates?

They miss different things. Full-text search is exact about words and blind to the ones you didn't use. Trigrams match on three-letter fragments, so they catch typos, inflected forms and near-spellings: _composting_ against _compost_, or a Polish _kompostownik_ against _kompostowanie_.

The index also strips diacritics, and the query goes through the same treatment. People type Polish without accents as a matter of habit (_zrodlo_ for _źródło_), and if only one side were normalised, those AI notes would never meet as candidates.

## What does the score mean?

Whether the two texts are about _the same topic_, not whether they share vocabulary. That is the part no index can do.

The sentence of reasoning matters as much as the number. “Both give the brown-to-green ratio, the new one adds how often to turn the pile” tells you what a merge would add. “Both mention compost, but one is about soil pH” tells you why it shouldn't happen.

The score is then compared with the vault's **Similarity threshold**. A new vault starts at 0.75. Raise it and you get fewer merges and more separate notes; lower it and more drafts count as repeats.

## Which mode should a vault use?

Vault settings offer three, under _When a note looks like a duplicate_.

**Ask me each time** is the default. A dialog titled _This looks like something you already have_ shows the draft, each candidate with its match score, and three buttons: _Merge with this one_, _Keep as a new note_, _Decide later_. Postponed drafts wait on the vault page under _Waiting for your decision_.**Always merge** folds close drafts in on its own, but only above the threshold. Good for a vault that is a long study of a few ideas, where you want ten deep AI notes rather than a hundred thin ones.**Always keep both** never merges. Right for a log, where two entries on the same subject from different weeks really are two entries.

Chat has one twist. Notes from a conversation are written in the background while you keep talking, so in ask mode the chat doesn't interrupt you: the draft goes into the best candidate above the threshold. Tick **Ask before merging** under the question box and that conversation brings the dialog back. Imports also decide without asking, because nobody wants 40 dialogs after dropping in a folder of PDFs.

## What happens to an AI note in a merge?

Material is added, nothing is replaced. The new content joins the existing note, and the new question and answer go into its source block under the ones already there, word for word.

No code path can edit or delete earlier source material, by accident or otherwise. The storage layer simply has no operation for it. In a blank-page editor, merging two notes is your job, and whatever you trim is gone unless you kept a copy. If you are weighing an alternative to Obsidian for notes from AI chats, look at this difference first.

So a merged AI note grows in two layers: on top, the current best version of the idea; underneath, every conversation that fed it, in its own words. Six months on you can still see which answer said the pile should be turned every two weeks, and under what conditions.

Manual merging: tick two or more AI notes in the list and press Merge.

## Can I merge notes myself?

Yes, for duplicates the check didn't catch. Tick the notes in the **Notes** list and press **Merge**, or use **Merge notes** above the table of contents.

The model writes one draft from what the selected notes say today. The result is a new AI note that carries the source material of all of them, in the order they were created. The old notes go away, and every link that pointed at their files is rewritten to the new file. The model is asked first and nothing is touched until it answers, so if the provider refuses, your vault stays exactly as it was.

## What about candidates below the threshold?

They are related, not the same, and related AI notes are what links are for. The draft that becomes a new note gets a short map of existing notes from the same search, titles and file names, and can work ordinary Markdown links to them into the text: `[Checking soil pH](checking-soil-ph.md)`. Links to files outside that map are cut.

That's why the threshold is worth tuning rather than pushing to an extreme. Set it at 0.95 and repeats slip through as new files. Set it at 0.4 and notes that should stay apart get folded together, losing the link that would have connected them.

## What if a merge went wrong?

Nothing is lost, because the source material of both conversations is still in the note, in full. Open the note and use **Rebuild from source material**: it runs that material through the pipeline again, and a long text comes back as several linked notes that replace the merged one.

If you'd rather do it by hand, the note is an ordinary `.md` file in the vault's `notes/` folder, so splitting it is a text-editor job.

Plain files are also why the app sits on the list of [Obsidian alternatives](/alternative-to/sumizai-alternative-to-obsidian.html) at all: the merge logic is SumizAI's, the files are yours, and a vault exported as ZIP opens in Obsidian. As an alternative to Obsidian it trades plugins for notes that write and deduplicate themselves. The rest of the [AI notes app](/) (vaults, search, export to PDF and PowerPoint) is on the main page, and the full path of an answer is in [how a chat answer becomes a note](/blog/how-a-chat-answer-becomes-a-note.html).

