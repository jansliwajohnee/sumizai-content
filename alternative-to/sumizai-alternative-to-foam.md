---
title: "SumizAI vs Foam: AI notes or a VS Code knowledge base"
url: "https://sumizai.com/alternative-to/sumizai-alternative-to-foam.html"
lang: "en"
date: "2026-08-22T17:49:32+02:00"
modified: "2026-10-23T11:36:33+02:00"
description: "Foam turns VS Code into a free Markdown knowledge base you write yourself. SumizAI writes AI notes from your model chats. Prices, links, Git and migration compared."
---

# SumizAI vs Foam: a wiki you type in VS Code, or AI notes that write themselves

Foam is a free, MIT-licensed extension that makes Visual Studio Code a personal knowledge base: Markdown files, `[[wikilinks]]`, backlinks, a graph and Git for history. SumizAI comes from the other end. You ask a model a question, and the answer you want to keep turns into one of your AI notes, filed into a chapter without you touching a file.

Both store plain `.md` files on your disk, which makes this an unusually friendly comparison: you can use the two side by side. Foam facts below were read on docs.foam.md and the GitHub repository on 23 October 2026.

A finished note from the demo vault “Home garden”. Foam would show the same file as Markdown in an editor tab.

## Foam next to an AI notes app, row by row

|  | SumizAI | Foam |
|---|---|---|
| Who writes the note | An AI model, from your question and its answer | You, in the VS Code editor |
| Price | 7 days free, then 1 USD a month; model costs paid to your provider | Free, “No subscriptions or vendor lock-in” |
| Licence | Proprietary subscription | MIT, open source |
| Where it runs | macOS first, coming to the Mac App Store; Windows, iOS and Android in preparation | Inside VS Code (extension `foam.foam-vscode`), plus a Foam CLI |
| Files | Plain `.md` files plus a local database as an index | Plain Markdown files in a workspace folder |
| Structure | A table of contents up to 6 levels deep, numbered `1.`, `1.1`, `a)` | Folders, tags, Smart Folders, Foam Queries |
| Links | Markdown links `[Title](file.md)` to existing notes only; backlinks under each note | `[[wikilinks]]`, block anchors, embeds, backlinks |
| Graph | None | Graph visualization |
| AI | Built in: 7 providers on your own API key | Not part of Foam; any AI extension you add to VS Code |
| History and sync | No sync; files stay on the Mac | Git: commits, branches, any remote you choose |
| Publishing | Export only: ZIP, PDF, PowerPoint | GitHub Pages, GitLab Pages, Vercel, Netlify with Eleventy, MkDocs |
| Templates and daily notes | No | Yes, both |

## One afternoon of debugging, two ways to keep the result

Say you spend an hour working out why a Docker build cache keeps missing. You ask Claude four questions; the third answer is the one that fixes it.

With Foam, you open the command palette, create a note, paste the answer, trim it, add a `#docker` tag and type `[[build-cache]]` so it shows up in the graph. If you commit, Git remembers it. Good result. It costs you five minutes and the discipline to do it while the fix is still fresh.

In the AI notes app the same four questions happen inside a vault called “Dev”. You mark the third answer as worth keeping. The model writes a title and a short summary, puts the expanded explanation below, and keeps your question and Claude’s reply word for word as the source. It picks chapter `2.3` (containers) from the table of contents and links the new note to an older one about multi-stage builds, because that file already exists. Before saving it also checks whether you wrote this already in March.

Five minutes against zero, and the AI note is already linked. That is the whole trade.

## Where Foam wins, clearly

- You live in VS Code. Keyboard shortcuts, your theme, Vim mode, the terminal: Foam inherits all of it, and a separate Mac app never will.
- You want Git. Diffs per note, branches, pull requests from a colleague, a private repo as backup. The Mac app here has no version control and no sync.
- You publish. A Foam workspace becomes a website on GitHub Pages or Netlify; your AI notes leave the app only as exported files.
- You think in links. Wikilinks, block anchors, embeds and the graph view are the point of Foam; here the model writes the links and there is no graph.
- You pay nothing and want to keep it that way, on Linux or Windows today.

If three of those five describe you, keep Foam and stop reading the next section.

## Where AI notes beat a hand-built wiki

The case for it is narrow and specific: most of what you learn now arrives as answers from Claude, GPT or Gemini, and your Foam workspace has an `inbox/` folder that keeps growing because nobody files it.

That is the job it takes over. It also sends each new question with the vault’s table of contents and the full text of up to five relevant notes (24,000 characters at most), so the next answer builds on what you saved last month, and the app shows you which notes it used. Search works by meaning across titles, summaries and text. For handing material to someone, a vault exports to a PDF with summaries only or full notes, or to an editable `.pptx` deck with 15 themes.

That makes it a fair Obsidian alternative and a fair Foam alternative for one kind of person: the one who reads more AI answers than they write notes. The longer comparison on the [Obsidian alternative that writes AI notes](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html) page covers the same idea from the Obsidian side, and the exported files open there too.

## Moving notes in both directions

**Out to Foam.** Export the vault as a ZIP. Inside is `base.md` with the table of contents and a `notes/` folder; links are relative. Unzip it into a Foam workspace, open the folder in VS Code and the relative links between notes keep working, because they are plain Markdown links, not wikilinks. Commit it and you have history.

**In from Foam.** In the import panel choose single files or the whole workspace folder. Accepted formats are `.md`, `.markdown`, `.txt` and `.pdf`, processed one file at a time on your own model key. Each file becomes one of your AI notes, with the original text kept as its source, and the table of contents is rebuilt after every one. Your `[[wikilinks]]` survive inside that source text but are not converted; the new note gets Markdown links written by the model.

Practical tip: import one folder of 20 files first and look at the chapters it builds.

## Questions people ask before choosing

### Can both tools share one folder?

Not live. The app keeps its vault and index to itself; you get the files out by exporting a ZIP. Treat the Foam copy as the one you edit, publish and commit.

### Does SumizAI work inside VS Code?

No. It is its own app, and the first release is for macOS through the Mac App Store. Foam is the option if VS Code is where you want your notes.

### Which one has AI?

The Mac app is built around it: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local Ollama or your own OpenAI-compatible server, each on your own key, with a prompt for consent before anything leaves the Mac. Foam’s documentation lists no AI writer, so in VS Code you would add an AI extension yourself.

### Is Foam really free?

Yes: open source under MIT, no paid tier on its site. Your costs are hosting if you publish and whatever Git remote you push to.

### What happens to my AI notes if I cancel the subscription?

You can still open and export them. The app only stops starting new conversations, and the files were plain Markdown on your disk all along.

Foam features, pricing statement and publishing targets: [docs.foam.md](https://docs.foam.md/); licence and extension ID: [github.com/foambubble/foam](https://github.com/foambubble/foam); both read on 2026-10-23. Facts about the app come from its code and App Store metadata; the [AI notes app](https://sumizai.com/) overview has the rest.

## Other comparisons

- [SumizAI as an Obsidian alternative](https://sumizai.com/alternative-to/sumizai-alternative-to-obsidian.html)
- [SumizAI vs Notability](https://sumizai.com/alternative-to/sumizai-alternative-to-notability.html)
- [SumizAI vs Logseq](https://sumizai.com/alternative-to/sumizai-alternative-to-logseq.html)
- [SumizAI vs Zettlr](https://sumizai.com/alternative-to/sumizai-alternative-to-zettlr.html)
- [SumizAI vs Joplin](https://sumizai.com/alternative-to/sumizai-alternative-to-joplin.html)
- [SumizAI vs Anytype](https://sumizai.com/alternative-to/sumizai-alternative-to-anytype.html)
- [SumizAI vs Notesnook](https://sumizai.com/alternative-to/sumizai-alternative-to-notesnook.html)
- [All comparisons](https://sumizai.com/alternative-to/)

## Keep Foam for writing, let SumizAI catch the answers

The Mac version is on its way to the Mac App Store: 7 days free, then 1 USD a month. Until then, the Mac page explains what the first release includes.

- [SumizAI for Mac](https://sumizai.com/mac/)
- [All comparisons](https://sumizai.com/alternative-to/)
