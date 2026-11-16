---
title: "Which AI models does SumizAI work with?"
url: "https://sumizai.com/blog/which-ai-models-sumizai-works-with.html"
date: "2026-08-14T00:00:00+02:00"
modified: "2026-08-14T00:00:00+02:00"
description: "AI notes written by Claude, GPT, Gemini, Groq, OpenRouter, a local Ollama or your own server, always on your own API key and with the model list read live."
tags: ["byok ai app", "claude notes app", "openai notes", "ollama local ai notes", "openrouter", "sumizai"]
---

# Which AI models does SumizAI work with?

Every AI note in SumizAI is written by a model you connect yourself. The app sells no tokens and ships no model of its own: you pick one of **seven providers**, paste your API key or a server address, and each request travels from your Mac straight to that provider.

## Which providers can write your AI notes?

Seven: Anthropic, OpenAI, Google Gemini, Groq, OpenRouter, a local Ollama, and a custom server that speaks the OpenAI API. Any of them can draft your AI notes, and you can connect several at once.

Behind those names sit only two clients. Anthropic gets its own, because its Messages API is shaped differently. The other six accept OpenAI-style requests: the app sends `/chat/completions`, reads `/models`, and reaches Gemini through Google's OpenAI-compatible endpoint. That is why the seventh slot, _Custom server_, needs no dedicated integration.

Setup lives in Settings, under Providers. Choose one, paste the key, press _Connect_, then _Test_. Three labels follow: _Connected_ (the provider answered with this key), _Not verified_ (saved, never called) and _Not connected_. The middle one exists so a mistyped key never looks like a working one.

## Why your own key?

Reselling tokens means a margin on every one of them. A margin does not fit into 1 USD a month. SumizAI charges for the app; the model bill goes from your provider to you, at its rate, with any credits or free tier you already have.

Groq has a free tier and OpenRouter lists free models, while Anthropic and OpenAI bill per token. The model picker marks each entry _Free_, _Free tier_ or _Paid_, so you see the cost before the first question. The key is stored encrypted and never shown in full again.

## What leaves your Mac, and when?

Nothing, until you agree. Before a provider receives anything, a window titled _Send data to Anthropic?_ (or whichever one you picked) lists what goes out: your questions and the conversation history, excerpts of notes used as context, and imported documents. Refuse, and the call does not happen. Disconnecting the provider withdraws the consent; reconnecting asks again.

Context has a ceiling. A question carries the vault's table of contents plus the full text of at most five relevant AI notes, within 24,000 characters, and the chat shows _Answered using your notes_ with the list. The model never reads the whole vault, and SumizAI's own servers receive none of it.

## Where does the list of models come from?

From the provider, asked with your key. No catalogue is baked into the code.

A hard-coded list goes stale within a month: it offers a retired model, and you find out when a note fails to save. So the app reads the provider's `/models` endpoint and filters it. Embedding, image, speech and transcription models go, because you cannot chat with them. A dated snapshot like `-001` next to the same model without a suffix appears once, and an older generation next to a newer one in the same family is hidden.

What remains is sorted in two groups, _Free_ above _Paid_, strongest first. On OpenRouter, with hundreds of raw entries, that order is what makes the dropdown usable.

## How many model calls does one AI note take?

Three or four. The answer streams first, up to 4,096 tokens. Then, in the background, the app drafts the note (title, summary, expanded text), scores it against similar notes for duplicates with about 800 tokens of output, and picks a chapter with around 300.

Everything runs on the model under _Model answering in chat_. Settings also names the model for supporting work (titles, summaries, topic matching); in the Mac app it is the same one. A cheaper helper would save money and write thinner summaries, and the summary is the line of an AI note you read most.

## Which provider is fastest from your desk?

Measure it. _Run speed test_ in Settings sends a short request to every connected provider and times the real reply from this machine, right now. Published benchmarks average other people's networks; your latency to Groq on a Tuesday evening is the number you feel.

Results show a bar for time and separate quality stars, which are our editorial rating rather than a measurement. The _recommended_ label goes to the best-quality provider among those that answered in comparable time.

## What happens when a provider refuses?

You get the real reason. A 401 or 403 becomes _The provider rejected your API key_, and the app does not retry it. A 404 means the model is gone, and it drops off your list.

A daily limit (HTTP 429) is different. The model is marked _limit reached · back at_ a given hour for the next 24 hours, and a window offers another model with resources left, so the interrupted job continues there.

One trap if you build something similar: Anthropic rejects direct calls from a desktop app without an explicit opt-in header, and the refusal reads like a bad key. The app sends that header.

## Can everything stay on your machine?

Yes, with Ollama. Its default address, `127.0.0.1:11434`, is filled in and no key is needed. Type a bare `host:port` for another machine on your network and the app adds `http://` and `/v1`.

With a local model the question, the context and the answer never touch a third-party server, and the AI notes land as plain `.md` files in the vault folder you chose.

## Do notes from different models mix in one vault?

They do. Switch from Claude to a Groq model midweek and the next note simply has another author. The format stays the same, the original question and answer sit word for word underneath, and links are ordinary Markdown links to real files.

That plain folder is why this setup works as an Obsidian alternative for people who are tired of writing every page by hand: the model drafts and files, and Obsidian still opens the result. The page [SumizAI as an Obsidian alternative](/alternative-to/sumizai-alternative-to-obsidian.html) walks through that split, and the [AI notes app](/) overview explains the rest of the app.

Providers in Settings: Connected, Not verified or Not connected, and a chat model picked from the provider's own list.

## Is my material used for training?

Not by SumizAI. There is no training pipeline and no server holding your notes.

What a provider does with API traffic is set by your agreement with it, which is one more reason the key should be yours: read the terms, choose, and switch provider without moving your AI notes anywhere. It is also the plain answer for anyone shopping for an Obsidian alternative with AI built in: the model is yours to pick from seven providers, and swapping it changes nothing in the folder.

