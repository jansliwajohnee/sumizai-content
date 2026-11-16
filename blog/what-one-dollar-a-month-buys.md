---
title: "What does one dollar a month actually buy?"
url: "https://sumizai.com/blog/what-one-dollar-a-month-buys.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "What 1 USD a month pays for in an AI notes app: one plan after a 7-day trial, your own AI key billed by the provider, and notes that stay yours if you stop."
tags: ["sumizai pricing", "cheap note app", "one dollar subscription", "free trial notes app", "byok pricing", "sumizai"]
---

# What does one dollar a month actually buy?

SumizAI has one plan: 7 days free, then 1 USD a month. The number is small on purpose, and the interesting part is the split behind it. **The dollar pays for the app that writes your AI notes; the model is paid separately**, by you, to a provider you choose.

## What the trial includes

The whole app. There is one edition, so there is no reduced trial version, and the AI notes you write in those seven days stay yours whatever you decide.

For seven days you create vaults, chat, let AI notes file themselves into the table of contents, merge duplicates, import `.md`, `.txt` and `.pdf` files, search, and export to ZIP, PDF and PowerPoint. Whatever the app does after you pay, it does during the trial.

The trial and the subscription run through the App Store. The app needs an account (an e-mail address), and that account lets one subscription work on all your Macs.

## What the dollar pays for

Everything that happens between the model's answer and finished AI notes on your disk: the title, summary and expanded body, filing into a chapter tree six levels deep, the duplicate check with its merge dialog, Markdown links between notes, search by meaning, import, and the three exports.

There are no tiers. No feature sits behind a higher plan, because there is no higher plan.

The renewal is the standard App Store one: the subscription renews at 1.00 USD a month unless you cancel at least 24 hours before the period ends, and you manage it in your Apple Account settings. The App Store shows the price in your local currency before you buy, and it can differ by country.

## What the dollar does not pay for: the model

SumizAI runs on **your own API key**. You connect one or more of seven providers: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local Ollama, or your own server compatible with the OpenAI API. Requests go straight from your computer to that provider, which bills your account. SumizAI adds nothing on top.

Provider settings. Free and paid models are marked, and you pick which one answers in chat.

This is the trade that keeps the price at a dollar. Reselling the model would mean a margin on every token. Instead, the rate you pay is the provider's own, on your own credits.

## How to estimate the total

1 USD plus your provider bill. The second number depends on which model you pick and how much you ask, and you control both.

Two facts from the app help with the estimate. One question means three or four model calls: the answer itself, then in the background a note draft, a duplicate score and a chapter choice. And the context sent with a question is capped: the table of contents plus the full text of at most five of the most relevant notes, within 24 000 characters. A vault with 50 AI notes and one with 500 send prompts of roughly the same size.

If the provider bill is the worry, there are two near-free routes. OpenRouter's free models appear above the paid ones in the model picker. A local Ollama costs you electricity and nothing else.

## What happens to your AI notes if you stop paying

They stay readable and exportable. Without an active subscription, the app still opens your vaults and still downloads them as ZIP, PDF or `.pptx`; what stops is new conversations, imports and rebuilds.

There is a stronger guarantee under that one. Your notes are ordinary `.md` files in a folder on your disk, with a local database as the index. With no subscription, or no app at all, they open in any text editor, and the links between them, plain Markdown like `[Watering schedule](watering-schedule.md)`, work in any Markdown tool, Obsidian included. When you weigh any Obsidian alternative against Obsidian itself, this is the question to ask first, and here the answer is that the files never depended on the subscription.

Deleting your account removes it from the server; your vaults and `.md` files stay on the computer. It does not cancel the App Store subscription, so cancel that first in your Apple Account.

## A week offline is fine

The app checks a signed licence token that is valid for 7 days. That token is also the offline grace period.

So a week on a train, at a conference with bad Wi-Fi or in a cabin without signal is ordinary use, not a lockout. A cloud model needs a connection anyway; a local Ollama does not, and with it the app keeps writing notes for that week without any network.

## Why it is this cheap

Scope. The expensive part of an AI product is running the model, and SumizAI does not resell it. What remains is a desktop app plus a small server for accounts and licences. Your AI notes never pass through that server: there is no sync and nothing stores your notes, questions or documents.

The list of what a dollar does not buy is just as specific: no sync between devices, no team vaults, no collaboration, no plugins, no web app. If you need those, you need a different product.

## Compared with Obsidian, which is free

Obsidian costs nothing for personal use, and people ask why they should pay a dollar instead. The answer is that SumizAI does a different job. It writes notes from your conversations with a model and files them; Obsidian is an editor where you write them yourself, and turning a chat into AI notes there is a copy-and-paste job.

That is why it makes sense as an [Obsidian alternative for notes written by AI](/alternative-to/sumizai-alternative-to-obsidian.html) and also as a companion to it. The exported ZIP has `base.md` and a `notes/` folder with relative links, and it opens in Obsidian as a vault. Paying a dollar for an Obsidian alternative only makes sense if you want the writing done for you.

## When can you pay it?

Not yet. No version is available for download today. The macOS edition, for Apple silicon and Intel, is coming to the Mac App Store; Windows, iOS and Android are in preparation. The [AI notes app](/) page shows the current status.

