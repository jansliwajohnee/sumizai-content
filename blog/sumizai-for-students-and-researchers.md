---
title: "How do students and researchers use SumizAI?"
url: "https://sumizai.com/blog/sumizai-for-students-and-researchers.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "AI notes for a whole semester: one vault per subject, questions that make good notes, imported lecture PDFs and a revision PDF built from the contents."
tags: ["ai notes for students", "study notes app", "research notes", "literature notes", "revision ai notes", "sumizai"]
---

# How do students and researchers use SumizAI?

A model can explain the Krebs cycle at eleven at night better than your textbook, and by June that chat is buried under two hundred others. SumizAI keeps the part you needed: an answer worth keeping becomes one of your **AI notes**, with a title, a summary, an expanded body and the original question and answer saved word for word underneath. This is the setup I would use for a degree.

## One vault per subject, not per assignment

A vault in SumizAI is a boundary. When you ask a question inside it, the model sees the AI notes of that vault and nothing from any other one.

That makes the subject the right unit. Take two courses that both talk about regression, say Statistics 2 and Econometrics. In one shared vault, a question about residuals pulls in notes from the wrong course and the answer mixes two notations. In two vaults, each answer stays inside one lecturer's vocabulary.

An essay or a lab report is smaller than that. Make it a chapter in the subject's vault, so the AI notes you collected for it are still there in week eleven when the exam covers the same ground.

## Which questions turn into good AI notes?

Questions that ask for structure.

“Explain the central limit theorem” gives a correct answer and a flat note. “Explain the central limit theorem, the assumptions it needs, and two cases where it fails” gives a note with an argument in it: something you can test yourself on, not only reread.

Ask one thing per message. A note is written from one exchange, so a message holding four questions produces one note about four topics. That note lands in a vague chapter, and later it matches half the vault during the duplicate check.

The interface comes in 16 languages, and the note language does not depend on it: run the app in English, keep German literature notes in German.

## Lecture slides and papers: importing PDF and Markdown

Not everything starts as a conversation. The import takes single files or a whole folder in four formats: `.md`, `.markdown`, `.txt` and `.pdf`.

Files go in one at a time. Each one becomes a note, with its original text attached as the source, and the table of contents is rebuilt after every note, so a folder of weekly lecture PDFs arrives already sorted into chapters. Your own Markdown notes from first year come in the same way, and so does a folder of `.md` files from Obsidian if you are trying SumizAI as an alternative to Obsidian.

## Revision from the table of contents

The table of contents is a tree of chapters up to six levels deep, numbered `1.`, `1.1`, `a)`, `a.1)`. You never write it; the model files each new note into an existing chapter by its number, or asks for a new subchapter when nothing fits. After a term it reads like a syllabus of what you actually covered, with each of your AI notes sitting under the lecture topic it belongs to.

## Three exports for exam season

The Contents view of the demo vault “Home garden”. A Statistics vault gets the same numbered tree.

**PDF** prints the titles and summaries of your AI notes and nothing else. That is the revision sheet: a term on a few pages, read in one sitting, and you find the three topics you have forgotten.

**PDF+** prints the full notes, still without the original questions and answers. Use it for the chapters you got wrong.

**PowerPoint** (`.pptx`) gives editable slides with 15 themes, in the order of the contents, without the source exchanges. A first draft for a seminar talk.

When the tree starts to feel crowded around week eight, the **Rebuild contents** button lays all chapters out again from the notes in the vault.

## What researchers get from the source material

Every note keeps the full original question and answer, and the source is only ever appended to. Nothing rewrites it.

For research that matters. AI notes without a trail are paraphrases. When a note says a method breaks down with small samples, you can open the source and read what was said and in what context, instead of trusting a paraphrase written by a model months ago.

Duplicates are handled the same careful way. Before a note is saved, full-text search and trigram matching find candidates, and a second model scores the overlap from 0 to 1 with a reason. Above the vault's threshold you choose **Merge with this one**, **Keep as a new note** or **Decide later**. A merge only adds; a concept you return to over a year becomes one note that grew, with every contributing conversation still readable below it.

Links between notes are plain Markdown links like `[Survivorship bias](survivorship-bias.md)`. The model gets a map of existing titles and files and can link only to those, and the panel **Notes that link here** under each note shows the reverse direction.

## Asking your AI notes instead of rereading them

This is the habit that pays. Ask the vault “what did I conclude about heteroskedasticity?” and the question goes out with the table of contents and the full text of at most five of the most relevant notes, inside a budget of 24 000 characters.

The model does not read the whole vault, and the app says which notes it used under **Answered using your notes**. If the answer leans on the wrong note, you see it at once. Search works by meaning across titles, summaries and content, so “the thing about biased samples” finds the note even when its title says survivorship bias.

## Plain files, and where Obsidian fits

Your AI notes are ordinary `.md` files on your own disk, with a local database as the index. There is no sync and no server holding them, and SumizAI does not collect your notes, questions or documents.

**Download vault** produces a ZIP with `base.md` (the contents) and a `notes/` folder, with relative links. It opens in Obsidian, VS Code or on GitHub. If you already keep a study vault in Obsidian, SumizAI works as an [Obsidian alternative for the writing part](/alternative-to/sumizai-alternative-to-obsidian.html): the model writes and files the notes, and the exported files still open in the editor you know. Students who want a full Obsidian alternative with sync and plugins will not find them here; the app has neither.

## What it costs on a student budget

Seven days free, then 1 USD a month, one plan. The model is billed separately by the provider you connect, on your own API key, and SumizAI adds nothing on top.

Two ways to keep that bill near zero. Connect OpenRouter, where the model picker lists free models above paid ones, or run Ollama on your own computer. Five other providers are there too: Anthropic, OpenAI, Google Gemini, Groq and any server that speaks the OpenAI API.

If you stop paying over the summer, your AI notes still open and still export; chat, imports and rebuilds wait until you subscribe again.

One honest limit: no version can be downloaded yet. The Mac edition is coming to the Mac App Store, and Windows, iOS and Android are in preparation. The [AI notes app](/) page shows the current state.

