---
title: "How do you turn a vault into a PDF or a PowerPoint deck?"
url: "https://sumizai.com/blog/export-notes-to-pdf-and-powerpoint.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Turn a vault of AI notes into a ZIP of Markdown files, a PDF with summaries or full notes, or an editable .pptx deck with 15 templates."
tags: ["export notes to pdf", "notes to powerpoint", "markdown to pptx", "knowledge base presentation", "pdf export", "sumizai"]
---

# How do you turn a vault into a PDF or a PowerPoint deck?

A vault of AI notes that grew out of forty conversations already has an order: every note picked its chapter on the day it was written. **Export turns that order into a file** in one click, and you choose which file.

## Which formats can a vault of AI notes become?

Three, behind four buttons in the _Export_ bar above the vault: _Download vault_, _PDF_, _PDF+_ and _PowerPoint_. Each one takes all the AI notes in the vault at once.

_Download vault_ saves a ZIP with the files exactly as they sit on your disk. _PDF_ and _PDF+_ produce one document at two levels of detail. _PowerPoint_ writes a `.pptx` deck you can open and edit like any other.

## What is inside the ZIP?

A folder named after the vault, with `base.md` on top and every note in `notes/`. The layout matches the folder on your disk byte for byte, so nothing is converted on the way out.

`base.md` is the table of contents as Markdown: chapters with their numbers (`1.`, `1.1`, `a)`) and under each one a link such as `[Sowing tomatoes indoors](notes/sowing-tomatoes-indoors.md)`. Notes the model has not filed yet get their own list, so no file goes missing from the index.

All links are relative. Unpack the archive and the folder works in VS Code, on GitHub and in Obsidian, which is the usual route for people who keep SumizAI as an Obsidian alternative for the writing and still read in Obsidian. The page on [SumizAI as an Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) covers that setup.

## PDF or PDF+: which one?

_PDF_ gives one slide-shaped page per note with its title and summary. _PDF+_ gives the same page per note with the full text: summary plus the expanded part.

They are two different documents, not one with a font change. Take the _Home garden_ demo vault: the short version is a briefing you read in ten minutes, a list of what you learned about seedlings, soil and watering. The long one is the reference you keep open while doing the work.

In both, pages follow the table of contents, and each note keeps the number it has in the app. The first page carries the vault name.

## Why do Polish letters survive the PDF?

Because the font travels inside the file. The fourteen standard PDF fonts have no Polish characters at all, and a font borrowed from the reader's system would produce a different document on every machine. So the app embeds the whole DejaVu font file in each PDF.

That is why the PDF is the safer format for anything leaving your organisation. A PowerPoint file plays by PowerPoint's rules and uses whatever fonts the opening computer has, like every deck does.

## What does the deck look like?

One slide per note, in table-of-contents order, with the title and summary of each AI note. Before exporting you pick a _Template_: fifteen of them, in three groups of five.

**Plain**: Classic, Warm, Cool, Night, Forest. Text on a solid background.**With graphics**: Indigo (side bar), Slate (header band), Teal (split), Amber (corner), Plum (card).**With illustration**: Semiconductors, Industry, Laboratory, Caribbean, Medical. A banner with a drawn motif: a chip with circuit traces, a factory skyline, flasks and test tubes, sea and palms, an ECG line.

The illustrations are drawn in code as shapes, not pasted stock photos, so the motif looks identical on slide 3 and slide 43. Every text and background colour pair meets the WCAG contrast thresholds (4.5:1 for body text, 3:1 for large type), which matters once a projector washes the colours out. Classic, graphite on white, is the default.

## Does the original conversation end up on a slide?

No, in neither PDF nor PowerPoint. The question you asked and the model's raw answer stay in the note as its source, untouched, but no export puts them in front of an audience. A transcript on a slide is worse than an empty slide.

Markdown markup is also cleaned for slides: `##` and `**` disappear, list items turn into bullets, and code fences are dropped.

## Why does the export come out in a sensible order?

Because the ordering was done long before, one note at a time. When an AI note is saved, the model chooses an existing chapter by its number or asks for a new subchapter, and the tree goes down to six levels.

Export is only rendering. Apps that store flat notes have to invent an order at export time, which is why their output reads like a list sorted by date.

The practical rule: **fix the table of contents, not the slides**. If the chapters come out in the wrong order, correct the table of contents in the app, or rebuild it, and export again. That beats dragging forty slides around.

The table of contents of the Home garden vault. The PDF pages and the slides follow this numbering exactly.

## How much editing does the result need?

Plan to cut. You get a complete, correctly ordered draft of every AI note in the vault, and a good talk uses part of it.

What you skip is the evening of work: choosing the order, writing a line of summary per section, and getting forty slides formatted alike. The `.pptx` is a real PowerPoint file, so trimming happens in Keynote, PowerPoint or Google Slides.

## Can I export only part of a vault?

Not directly. Export works on the whole vault, so a subset means editing the output or splitting the vault.

For a one-off, delete the slides you do not need. A vault of sixty AI notes gives sixty slides; keep the ones your audience needs. If you keep exporting the same chapter for the same audience, it wants to be its own vault, since a vault is also the boundary of what a question can see. More on how notes are written, filed and searched in the [AI notes app](/) overview.

## Do I keep my exports if I stop paying?

Yes. After you cancel, AI notes stay readable and every export button keeps working; the app only stops starting new conversations. Your `.md` files were on your disk all along, and the ZIP is the same folder in an envelope. Few other exits from a note app are that short, and it is part of why the plain-files approach holds up as an Obsidian alternative: leaving costs you nothing.

