---
title: "How do you actually work with SumizAI day to day?"
url: "https://sumizai.com/blog/how-to-work-with-sumizai.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Connect a provider key, create a vault, ask questions and let AI notes file themselves. The daily rhythm, from the first question to an exported PDF or deck."
tags: ["ai notes workflow", "how to use sumizai", "ai note taking workflow", "vault setup", "markdown notes workflow", "sumizai"]
---

# How do you actually work with SumizAI day to day?

SumizAI has very few settings, and the ones it has matter. **Setup takes a few minutes.** The useful part is knowing which three or four decisions to make on purpose, and which ones to leave to the app that writes your AI notes.

## What do the first five minutes look like?

Five steps, in this order: create an account with your e-mail, connect an AI provider, create a vault, ask one real question, open the table of contents. After step four you already have your first AI notes, and step five shows you where they went.

Connecting a provider means pasting your own API key in the settings. Seven providers are on the list: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local Ollama and any server that speaks the OpenAI API. Press **Test connection** before you close the screen. It makes a real call, so a typo in the key shows up now and not in the middle of your first conversation.

Provider settings: pick one of the seven providers, paste your key, press Test connection.

Then ask something you actually want to know. Not a test prompt. The answer streams in, a note is saved shortly after, and the table of contents already shows it under a numbered chapter.

## How do you decide what becomes a vault?

One question settles it: **when I ask about this, what else should the model be allowed to see?** Everything that should be in view goes into the same vault. Everything that should stay out goes somewhere else.

A vault is a hard edge. A question asked inside it travels with that vault's table of contents and with its notes, and with nothing from any other vault. That is exactly what you want when a client project and a hobby both talk about "beds" and mean flower beds in one and hospital beds in the other.

Go broad. A vault with forty AI notes gives the model material to work with; a vault with three is a folder with a fancy name.

## Should you change the duplicate settings?

Not in the first weeks. The default asks you each time a new note looks like an existing one, and those questions teach you what the app treats as the same topic while your vault of AI notes is still small enough to fix.

Each vault has two settings. The **mode**: ask, always merge, or always create. And the **threshold** for the 0 to 1 similarity score a second model gives each candidate. The threshold counts in every mode, because it defines what "the same topic" means.

Switch a vault to _always merge_ when it is a long study of one subject and you want one growing note per concept. Switch it to _always create_ when it works like a diary, where two entries on the same subject really are two entries. A merge never deletes anything: the original question and answer of both notes stay underneath.

## How should you ask so the AI notes come out well?

Ask one thing at a time. A note is written per exchange, so a question that hides four questions gives one note about four things: hard to file, hard to merge, hard to find in May.

Give the model the frame you want back. "Explain hardening off" and "Compare hardening off over 7 days and over 14 days for tomato seedlings, by risk and effort" produce very different expansions. The second one is a note you will reread next spring.

Say it out loud when you decide something. Answers that record what you chose, what you dropped and why are the AI notes that pay for the whole setup later, because a scrolled-away chat is precisely where that reasoning gets lost.

## What should you do with the table of contents?

Mostly nothing. Each AI note is filed at the moment it is written, with only that note in view: a good decision that cannot see next month.

So once in a while, press **Rebuild contents** in the vault bar. It reads all the notes, in batches of 60, and lays out the chapters again from scratch. A failed run leaves the old tree untouched. Do it after a busy week, when what you know has changed shape and the shelves have not caught up.

You can also edit the tree by hand: rename, reorder, add, nest or delete chapters. Deleting a chapter moves its notes up to the parent chapter.

## When is it worth renaming a note?

When the title stops describing the note, which happens to AI notes after two or three merges.

A rename is more than cosmetic. The file name follows the title, so renaming moves the `.md` file and rewrites every `[Title](file.md)` link to it in the other notes of the vault. The order is fixed: new file, then links, then the old file is removed, and if any step fails the change is rolled back. Your folder stays readable from outside: `hardening-off-seedlings.md` is the note about hardening off seedlings. It is also the link format Obsidian reads, so for anyone using the app as an alternative to Obsidian a link that breaks here would break in the export too.

## How do you get things back out?

Three ways to get AI notes back, for three situations.

**Search**, when you roughly remember what was said. It looks through titles, summaries, note text and the original question and answer, ignores diacritics, and shows the matching fragment with the phrase highlighted.**A question to the vault**, when you do not know where the answer sits. It goes out with the table of contents and the full text of at most 5 relevant notes, within 24,000 characters, and the reply lists the notes it used.**Export**, when the reader is someone else: a ZIP of Markdown, a PDF with summaries only or full notes, or an editable `.pptx` in table-of-contents order with 15 themes.

The ZIP holds `base.md` and a `notes/` folder with relative links. That is also the practical answer for anyone treating the app as an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html): the notes are written for you, and the exported folder opens in Obsidian with every link working.

## What does a realistic week look like?

Monday to Thursday you work as you already do, asking a model about things you need. AI notes pile up without you thinking about them, and twice a day or so you answer a merge question with one click.

Friday, ten minutes. Open the vault, skim the table of contents, rebuild it if the shape has drifted, rename the two notes whose titles no longer fit.

When something is due, search for the thread, export to PDF or a deck, and cut it down. That last step is short because the structure was decided forty conversations earlier, one note at a time. Nothing in this week involves plugins, sync or a graph view. That is the honest trade of an Obsidian alternative built this way: you give up all three and get notes that write themselves.

## What are the two most common mistakes?

The first: treating the vault as an archive. Two hundred notes in a fortnight, zero questions asked back, and the verdict that it is a fancy way to store chat logs. The value shows on the way back in, the first time an answer is built from five notes you saved and lists them.

The second: one huge vault for everything. Each question then carries a less focused set of notes, and the duplicate check compares material that was never related. Split early.

And a note on expectations, since this page describes the working rhythm and not a download: no version is available yet. The macOS app is coming to the Mac App Store, Windows, iOS and Android are in preparation, and the plan is 7 days free, then 1 USD a month. If you would rather compare it with other Obsidian alternatives first, the comparison pages are a good start; for the overview, see the [AI notes app](/) home page.

