---
title: "SumizAI vs Zettlr: Thesis Writing or AI Notes from Chats"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-zettlr.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "Zettlr is a free open-source Markdown editor for academic writing with Zotero and Pandoc. SumizAI writes AI notes from your chats. Who should use which."
---

# Zettlr writes the thesis, AI notes keep the questions

Zettlr is a free, open-source Markdown editor for people who publish: citations from Zotero, JabRef or Juris-M in over 9,000 styles, export through Pandoc to LaTeX, Word or slides, and a Zettelkasten with IDs and `[[links]]`. SumizAI is not an editor of that kind. It keeps answers from conversations with an AI model as AI notes, with the full exchange saved under each one.

If you are writing a dissertation, the verdict is short: write it in Zettlr. What follows is about the other half of research work, the questions you ask a model along the way, and where those answers should live. Zettlr details were checked on zettlr.com, its download page and its documentation on 23 October 2026.

Chapters numbered 1. → 1.1 → a) → a.1), up to six levels, extended by the model as answers come in.

## Twelve facts side by side

|  | SumizAI | Zettlr |
|---|---|---|
| Purpose | Keep and sort what you learn from AI chats | Write and publish long texts |
| Who writes | The model, from a conversation | You |
| Price | 7 days free, then 1 USD a month | Free, supported by donations |
| Licence | Proprietary subscription | Open source, GNU GPL v3 |
| Platforms | macOS first, coming to the Mac App Store; Windows, iOS, Android in preparation | macOS 12+ (Intel and Apple silicon), Windows 10+, Linux (deb, rpm, AppImage, also ARM) |
| Format | Plain `.md` plus a local index | Markdown |
| Links | Markdown links `[Title](file.md)` to existing notes; backlinks | `[[wiki links]]`, Zettelkasten IDs like `YYYYMMDDHHMMSS`, graph view |
| Citations | None | Zotero, JabRef, Juris-M; 9,000+ citation styles |
| AI | 7 providers on your own key | Not mentioned on zettlr.com |
| Network | Talks only to the AI provider you chose, after asking | No forced cloud sync; the only connection is an update check you can turn off |
| Export | ZIP of Markdown, PDF (summaries or full notes), PowerPoint with 15 themes | Pandoc profiles: LaTeX journal templates, Word, Beamer, reveal.js, PowerPoint |
| Interface languages | 16 | Over a dozen |

## Zettlr is the right tool for

Anything that ends with a bibliography. Zettlr inserts a citation while you type, renders LaTeX maths and Mermaid diagrams in the editor, and sends the same file to a journal template or to a `.docx` for a co-author who refuses LaTeX. Nothing here formats a single reference.

It also wins on cost and openness: it is free, under the GPL, runs on Linux including ARM machines, and needs no account. Researchers who built a Zettelkasten by hand, one atomic note per idea and an ID in every file name, should keep it in Zettlr. That method depends on you writing each note, which is exactly the step the other app removes.

## A Tuesday in chapter three

Picture a PhD student in psychology drafting the methods chapter. Zettlr is open with `03-methods.md`, the Zotero library is connected, and citations go in as `[@barr2013]`. Writing goes fine until the question of random slopes comes up.

So the student asks Claude: should a mixed-effects model include random slopes for every within-subject factor? Then a follow-up on convergence warnings, then one on how to report the model. Forty minutes, three good answers. In Zettlr they would become a pasted block in a scratch file, or nothing.

Here the three answers become AI notes in a vault called "Thesis": "Random slopes in mixed models", "Convergence warnings", "Reporting mixed models", filed under chapter `2.3` Statistics. When the student asks in May about power analysis for the same design, the model reads those notes first and says so on screen.

The thesis text stays in Zettlr, with its citations. The reasoning behind the choices sits in a set of AI notes the student can search by meaning months later.

## What AI notes add to a research workflow

- A record of every useful model answer, with the original question and answer kept verbatim, so you can quote what was actually said.
- Filing without effort: the model picks the chapter, and a duplicate check (a second model, score 0 to 1) catches the question you already asked in February.
- Import of your PDFs and Markdown drafts, file by file, so questions can draw on them.
- A PDF of summaries only, handy before a meeting with a supervisor.

Readers weighing Obsidian alternatives for a thesis ask the same thing: does this replace my editor? No. It feeds it. The [page on this Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html) makes the same point about Obsidian, and the [AI notes app](https://sumizai.com/) overview covers the rest.

## Using both, and moving files

Vault to Zettlr: download the ZIP, unpack it, and you have `base.md` and a `notes/` folder of Markdown, the format Zettlr edits. The links are standard Markdown links, not `[[…]]`, so they stay readable in any editor.

Zettlr to the vault: point the importer at your notes folder. It accepts `.md`, `.markdown`, `.txt` and `.pdf`, processes one file at a time and rebuilds the table of contents after each. Every file becomes one of your AI notes, with your text kept as the source. Citation keys and `[[links]]` stay in that source as plain text.

Import only reference material. Your chapter drafts belong in Zettlr, where Pandoc can turn them into a thesis.

## Zettlr questions from researchers

### Is Zettlr free?

Yes. It is free and open-source software under GPL v3, funded by donations.

### Does Zettlr have AI features?

None are mentioned on zettlr.com. It is an editor; you write.

### Can SumizAI manage citations?

No. There is no reference manager integration and no citation styles. Keep Zotero and Zettlr for that.

### Which should I use for a Zettelkasten?

Zettlr, if you follow the method: you write atomic notes and link them yourself. The AI notes app suits answers from chats, not hand-written slips.

### Will AI notes from the vault open in Zettlr?

Yes, they are Markdown files. Links between them are relative Markdown links.

Zettlr: [zettlr.com](https://www.zettlr.com/) (features, price), [zettlr.com/download](https://www.zettlr.com/download) (platforms, version 4.8.0) and [docs.zettlr.com, The Zettelkasten method](https://docs.zettlr.com/en/pkms/zkn-method/) (IDs, links), read on 23 October 2026; licence and languages from github.com/Zettlr/Zettlr. Facts about the vault are from the shipped app.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Standard Notes](https://sumizai.com/alternative-to/sumizai-alternative-to-standard-notes.html)
- [SumizAI vs Microsoft OneNote](https://sumizai.com/alternative-to/sumizai-alternative-to-microsoft-onenote.html)
- [SumizAI vs AppFlowy](https://sumizai.com/alternative-to/sumizai-alternative-to-appflowy.html)
- [SumizAI vs Trilium Notes](https://sumizai.com/alternative-to/sumizai-alternative-to-trilium-notes.html)
- [SumizAI vs Zim](https://sumizai.com/alternative-to/sumizai-alternative-to-zim---a-desktop-wiki.html)
- [SumizAI vs Simplenote](https://sumizai.com/alternative-to/sumizai-alternative-to-simplenote.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Keep the questions behind your thesis

Seven days free. Write in Zettlr, ask your model, and see what the vault holds after a week.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
