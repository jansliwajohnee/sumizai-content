---
title: "What is Markdown, and why does it matter?"
url: "https://sumizai.com/blog/markdown.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "Markdown explained with real examples: core syntax, CommonMark and GFM, how a .md file renders, and what AI notes look like when saved as Markdown."
tags: ["what is markdown", "markdown syntax", "markdown format", "commonmark", "github flavored markdown", "md file", "ai notes markdown", "sumizai"]
---

# What is Markdown, and why does it matter?

Markdown is a way to format plain text with a handful of keyboard characters: `#` for a heading, `**` for bold, `-` for a list item. The file stays readable in any text editor and turns into clean HTML when something renders it. It is also how SumizAI stores AI notes, so after the syntax, the dialects and the pitfalls this guide takes one real note file apart.

## Where did Markdown come from?

John Gruber published it in 2004, with Aaron Swartz as a sounding board for the syntax. The first implementation was one Perl script, `Markdown.pl`, that read a text file and wrote HTML.

Gruber's goal fits in a sentence: a Markdown document should be publishable as plain text without looking as if somebody had marked it up with tags. The name is a pun on exactly that. You write less markup and the tool produces the markup for you.

It has held up: any `README.md` on GitHub reads fine in raw view.

## What does the syntax look like in practice?

Small. The part you will use daily takes ten minutes to learn, and it is the same set that Claude or GPT already use when they format a chat answer, so AI notes built from those answers need nothing else:

`# Heading` down to `###### Heading` for six heading levels;`**bold**` and `_italic_`;`- item` or `1. item` for lists, indented to nest;`[text](https://example.com)` for a link, the same with a leading `!` for an image;`> line` for a quotation;single backticks for `inline code`, three backticks on their own line to open and close a code block, with an optional language name such as `python` after the opening fence;`---` alone on a line for a horizontal rule.

One rule catches nearly everyone. A single line break inside a paragraph does nothing, because the renderer joins the two lines into one, so to force a break you end the line with two spaces or a backslash, or you leave an empty line and start a new paragraph.

## Why did plain text win over .docx for this kind of writing?

A `.md` file needs no particular program. TextEdit, Notepad, Vim and VS Code all open it, on any operating system, and show the same content.

Three practical things follow from that. Git compares it line by line, so a changed sentence shows up as a one-line diff instead of a modified binary blob. Ordinary tools like `grep` or Spotlight search it. And with no renderer at all you still read the text, with a few asterisks visible.

A `.docx`, by contrast, is a ZIP archive of XML files: fine for machines, opaque to people, and tied to software that understands Word's layout model. For notes you want to read again in ten years, that difference settles the question. It is also why file format comes up in every serious comparison of Obsidian alternatives: when a tool stores your notes as `.md` files, leaving it costs you nothing.

## One Markdown or many? CommonMark, GFM and the rest

Many. Gruber's 2004 description was prose plus a Perl script, and it left edge cases open (nested emphasis, list items that continue without indentation, blank lines inside lists). Each parser settled them its own way, so one file could render three different ways.

**CommonMark** answered that in 2014. John MacFarlane, Jeff Atwood and a few others wrote a precise specification with more than 600 test examples, and a compliant parser gives the same HTML for the same input. Most current tools start from it.

**GitHub Flavored Markdown** is CommonMark plus tables, strikethrough with `~~text~~`, task lists with `- [ ]` and `- [x]`, and bare URLs that become links. Pandoc's Markdown and MultiMarkdown go further, with footnotes, citations and definition lists for academic writing.

What this means for you: a GFM table looks fine on GitHub and appears as a row of pipe characters in a strict CommonMark viewer. Check your tools' dialect first.

## How does a .md file become a page?

In two steps. A parser turns the text into a tree of headings, paragraphs, list items and inline spans; a renderer then walks that tree and writes HTML, or a PDF through Pandoc, or slides through yet another tool. SumizAI shows your AI notes rendered in this way, while the file underneath stays plain text.

The tree in the middle is what makes extensions possible. Libraries such as `remark` in JavaScript and `cmark` in C let a plugin change the tree instead of running regular expressions over raw text, which keeps the core syntax intact.

A warning for anyone rendering Markdown that strangers wrote. Most parsers pass raw HTML through by default, and a `<script>` tag inside a comment field is a textbook XSS hole. Sanitize the output.

## Front matter, escaping and the details you learn later

YAML front matter is a block between two `---` lines at the very top of a file. Renderers hide it and tools read it as data: Hugo and Jekyll take the title and date from it, note apps store IDs and timestamps there. Each AI note in SumizAI starts with such a block, shown further down.

Escaping is the next lesson. Write the file name `my_draft_v2.md` in a sentence and half of it can turn italic, because underscores mean emphasis. A backslash before the character, or backticks around the whole name, fixes it.

Footnotes are the third surprise: they work in GFM and Pandoc, not in plain CommonMark.

## When is Markdown the wrong tool?

For layout. There are no columns, no page sizes and no control over fonts, so a printed brochure belongs in a layout program.

For data, too. A Markdown table is for people to read; configuration and API payloads belong in JSON, YAML or TOML, which programs parse without guessing.

And for very long technical books. AsciiDoc and reStructuredText have includes, cross-references and admonitions built in, while Markdown gets them only through extensions. For a 400-page manual the stricter syntax pays for itself. None of these limits touch AI notes, which are prose with headings, lists and the occasional table.

## What does an AI note look like as a Markdown file?

When a chat answer is worth keeping, SumizAI saves it as one of your AI notes in the vault folder, and the file is plain Markdown with a little structure on top. A note titled “Sowing tomatoes indoors” is stored as `notes/sowing-tomatoes-indoors.md`: the title in lower case, accents removed, words joined by hyphens.

The note “Sowing tomatoes indoors” in the Home garden vault. On disk it is one .md file.

Read from top to bottom, the file contains:

front matter with `id`, `title`, `summary`, `section` (the chapter in the vault's table of contents), `created` and `updated`;an H1 with the title, followed by the body of the note;a `## Full text` section when the note has an expanded version;`## Source material`, where every exchange appears as **Question** and **Answer**, word for word.

Between the sections sit HTML comments such as `<!-- sumizai:sources -->`. No Markdown preview shows them. They are there because a model's answers are full of their own `##` headings, so a heading could never reliably mark where the source begins.

Links between notes are ordinary Markdown links, `[Watering seedlings](watering-seedlings.md)`, never `[[wiki-links]]`. The model gets a map of the titles and files that exist and can link only to those, so nothing points at a file that is not there. If you are comparing Obsidian alternatives, this detail matters: Obsidian creates `[[wiki-links]]` by default but reads standard links just as well.

## Why Markdown is a safe home for AI notes

Because nothing in that file belongs to the app. The vault folder opens in Obsidian as it is, and that is the practical sense in which SumizAI works as an [Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html): it writes the AI notes from your conversations, and Obsidian, VS Code or GitHub can read the same files afterwards.

The local database is only an index for search. The `.md` files are the record, and the vault's table of contents is itself a file, `base.md`. Exporting a vault gives you a ZIP with `base.md` and a `notes/` folder, links kept relative.

If you are looking for an alternative to Obsidian that fills the vault for you, this is the property to check first. More on how the [AI notes app](/) turns a chat into a file is in the related articles below.

