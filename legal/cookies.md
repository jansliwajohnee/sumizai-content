---
title: "Cookie policy"
url: "https://sumizai.com/legal/cookies.html"
date: "2026-10-17T00:00:00+02:00"
modified: "2026-10-17T00:00:00+02:00"
description: "What sumizai.com stores on your device, when, and for how long. Nothing is stored before you choose. The apps set no cookies."
tags: ["sumizai", "legal", "cookies"]
---

# Cookie policy

This page lists everything SumizAI stores on your device through a browser, what it is for, and how to switch it off. Before you choose, page views are counted without storing anything on your device; cookies are written only after you say yes. The SumizAI applications set no cookies at all.

## What this covers

Two different things carry the name SumizAI, and they store very different amounts on your device. This document is precise about which is which.

- **The website, `sumizai.com`** — the pages you are reading now, including the blog and these legal documents. This is the only place where analytics exist.
- **The SumizAI application** on your computer. It sets **no cookies** and carries no analytics, no telemetry and no crash reporting.

"Cookies" here is shorthand for anything written to your device by a website: cookies proper, and also `localStorage` entries. Storing anything that is not strictly necessary for a service you asked for requires your consent under the ePrivacy rules as implemented in Polish law; the personal data that analytics then collect is processed on the basis of that consent, Article 6(1)(a) GDPR. What happens to data more broadly is in the [Privacy Policy](https://sumizai.com/legal/privacy.html).

## Our approach: nothing is stored before you choose

Google Analytics and Microsoft Clarity are not in the page source. They are injected by one first-party script, `/assets/consent.js`, which runs on every page.

**Before you answer, and if you refuse, both tools run in cookieless mode.** They count that a page was opened and send us that fact. What they do _not_ do is write anything to your device: no cookie, no local storage, no session storage, no identifier that would let anyone recognise you on your next visit. Google calls this state _Consent Mode advanced_ and marks the measurement as modelled; Microsoft calls it _cookieless mode_ and gives each page view its own throwaway number. Consent law in Poland — art. 398 of the Electronic Communications Law, implementing art. 5(3) of the ePrivacy Directive — governs storing and reading data on your device, and in this state we do neither.

**Only if you accept** do the cookies in the table below get written and does session replay start.

**Your choice is not stored in a cookie.** It lives in your browser's `localStorage`, under the key `sumizai.consent`, first-party, and it never leaves your device. The record holds three things: a version number, whether you accepted analytics, and the timestamp of the choice.

If `localStorage` is unavailable — private browsing, storage disabled — the choice cannot be remembered, so the banner appears again on your next visit and, until you answer, measurement stays cookieless. That failure mode is deliberately the quiet one.

There are **no advertising cookies on this site**: no ad network, no remarketing tag, no conversion pixel, no data broker, no fingerprinting, and no cookie wall. Rejecting costs you nothing — the whole site works exactly the same.

## Strictly necessary storage

These cannot be switched off in the panel, because switching them off would break the thing you asked for. They need no consent.

| Name | Where | What it does | Lifetime |
|---|---|---|---|
| `sumizai.consent` | sumizai.com — `localStorage`, not a cookie | Remembers the answer you gave the cookie banner, so you are not asked on every page. This is the record of consent itself. | Until you clear this site's data, or until we bump the record's version number and ask again. |

That is the only strictly necessary item. The website has no sign-in and sets no session cookie.

## Analytics cookies (only after consent)

If you accept analytics, two tools load: **Google Analytics 4** (property `G-RKZ7HS09BS`) and **Microsoft Clarity** (project `y23mz3osxm`). We use them to see which pages are read, which are abandoned, and where a page confuses people. They are the only third-party services on this website.

| Cookie | Set by | Purpose | Lifetime (vendor default) |
|---|---|---|---|
| `_ga` | Google Analytics 4 | Distinguishes one browser from another, so a person who returns is not counted as a new one. | 2 years |
| `_ga_RKZ7HS09BS` (the `_ga_*` pattern) | Google Analytics 4 | Holds the session state for this specific Analytics property. | 2 years |
| `_clck` | Microsoft Clarity | Attaches a Clarity identifier to the browser, so several page views belong to one recorded visitor. | 1 year |
| `_clsk` | Microsoft Clarity | Joins the page views of a single visit into one session recording. | 1 day |
| `MUID` | Microsoft | A Microsoft identifier used across Microsoft's own services; written where Microsoft's domains are reachable from your browser. | 1 year |
| `CLID` | Microsoft Clarity | A Clarity identifier marking the first time Clarity saw this browser. | 1 year |
| `ANONCHK` | Microsoft | A short-lived Microsoft cookie tied to how `MUID` is handled; Microsoft's own list, linked below, describes it. | 10 minutes |

**The names, purposes and lifetimes in that table are the vendors' own, as they documented them when this page was written — none of them are values we set.** Google and Microsoft can change any of it without telling us, and `MUID`, `CLID` and `ANONCHK` are set on Microsoft's own domains, not ours, so whether they appear at all depends on your browser's third-party cookie settings. Treat the vendors' always-current cookie lists, linked further down, as the authority; if you want a guarantee rather than a documented default, reject analytics — then none of these rows exists.

Our withdrawal routine also clears `_gid`, `_gat` and `SM` if a vendor happens to set them.

**Where this data goes.** Google and Microsoft run global infrastructure, so what their scripts collect may be processed outside the European Economic Area, under the safeguards those companies publish for their own services — we have no private arrangement with either of them beyond their standard terms. We also keep no copy: the statistics stay inside Google Analytics and Clarity, for as long as those services retain them, and we cannot delete one visitor's history there. Declining analytics, or withdrawing later, means the scripts never load and there is nothing to transfer. The [Privacy Policy](https://sumizai.com/legal/privacy.html) sets this out in full.

## What Microsoft Clarity actually records

You deserve to know this in plain words rather than find it in a vendor's documentation: **Clarity records your visit as a replayable session**. By Microsoft's own description of the product it captures interaction signals — pointer movement, scrolling, clicks and taps, window size, the sequence of pages — and reconstructs them as a playback of the page you saw, and it aggregates the same signals into **heatmaps**. What exactly is captured is Microsoft's design, not ours; its documentation, linked below, is the accurate and current description.

So yes: if you accepted analytics, your scrolling on this page can be played back. Two things bound it.

- We install Clarity as it comes and leave its default masking of page text and form input in place; we do not use Clarity's APIs to attach an identity, an e-mail address or any custom tag to a session. What that masking does and does not cover is Microsoft's to define, not ours to promise.
- This is the public marketing site. There is no sign-in on `sumizai.com`, so no account content and no note content can appear in a recording. Your notes never touch this website at all.

Nothing is recorded before you consent, and nothing is recorded after you withdraw. What Microsoft does with the data it collects — including where it stores it and for how long — is governed by Microsoft's own notice, linked below; we do not control it and will not paraphrase it here.

## Google Consent Mode: denied by default

Before any Google script can exist on the page, our consent script sets Google Consent Mode v2 defaults. Denied is the starting position, not the fallback.

| Signal | Default | After you accept analytics |
|---|---|---|
| `analytics_storage` | denied | granted |
| `ad_storage` | denied | stays denied |
| `ad_user_data` | denied | stays denied |
| `ad_personalization` | denied | stays denied |
| `functionality_storage` | granted | granted |
| `security_storage` | granted | granted |

The three advertising signals stay denied permanently, because we run no advertising and there is nothing for them to enable. Accepting flips exactly one switch. Rejecting, or withdrawing later, sets `analytics_storage` back to denied.

## Changing or withdrawing your consent

Withdrawing must be as easy as consenting, so it is the same panel, reachable from the same place on every page.

- Open **"Cookie settings"** in the footer of any page.
- Switch **Analytics** on or off.
- Press **Save choices**.

**Withdrawing does not just stop future tracking — it deletes what was already set.** When you turn analytics off, the script immediately expires the analytics cookies on this site's domain: `_ga`, `_ga_*`, `_gid`, `_gat`, `_clck`, `_clsk`, `CLID`, `MUID`, `ANONCHK` and `SM`, in their host-only and dot-domain variants.

What it cannot do is reach cookies stored on Google's or Microsoft's own domains — no website can delete another domain's cookies. For those, use your browser's controls or the vendors' opt-outs below.

Withdrawal works forward in time. It does not undo measurements already taken and already sent to the vendors, and it does not affect the lawfulness of what happened while consent was in force. If you want those earlier records dealt with, write to us and read the [Privacy Policy](https://sumizai.com/legal/privacy.html), which sets out your rights of access and erasure.

## Browser controls

Your browser can do more than our panel can, and it applies to every site, not just this one. In Chrome, Firefox, Safari or Edge you can block cookies entirely, block third-party cookies only, delete stored data for a single site, or browse in a private window where everything is discarded when you close it. The browser's own help pages are the accurate instructions; they change too often for us to reprint them here.

Two consequences worth knowing:

- Clearing this site's data also clears the `sumizai.consent` record, so the banner comes back and you are asked again. That is the record disappearing, not us ignoring you.
- Nothing on `sumizai.com` breaks if you block everything; you are only asked about cookies again on each visit.

Honestly stated: we do **not** currently act on the browser's "Do Not Track" header or on a Global Privacy Control signal. The signal we act on is the choice you make in the panel, which is why the panel defaults to nothing running.

## The applications

**The SumizAI applications set no cookies at all.** They are native applications, and they carry no analytics, no telemetry and no crash reporting — there is no consent banner in them because there is nothing on the device to consent to. Your vaults, notes and conversations stay in a local SQLite database and in Markdown files in a folder you pick; requests to the AI provider you chose go straight from your computer to that provider and never pass through any server of ours.

To sign in and to check your subscription, the application talks to our account server, `api.sumizai.com`. It does so with session tokens kept in the system keychain, not with cookies, and it never sends notes, questions or documents there. What that server stores is described in the [Privacy Policy](https://sumizai.com/legal/privacy.html).

## The vendors' own notices

These are the vendors' current documents. They are the authoritative source for the cookies those vendors set and for what they then do with the data. We do not control these pages and cannot promise the links stay valid forever.

**Google**

- [Google Privacy Policy](https://policies.google.com/privacy)
- [How Google uses cookies](https://policies.google.com/technologies/cookies)
- [Google Analytics 4 cookie usage](https://support.google.com/analytics/answer/11397207)
- [Google Analytics opt-out browser add-on](https://tools.google.com/dlpage/gaoptout)

**Microsoft**

- [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement)
- [Microsoft Clarity cookie list](https://learn.microsoft.com/clarity/setup-and-installation/cookie-list)

There are no other third-party services on this website. No fonts, maps, videos, chat widgets or embeds are loaded from anyone else.

## Changes to this policy

The version number and the date at the top of this page are the whole change record. We update this document whenever the site's tooling changes — a tool added, a tool removed, a cookie renamed by its vendor.

If a change means the consent you gave no longer matches what would run, we do not quietly rely on the old answer. We raise the version number stored in the consent record, which invalidates every saved choice, brings the banner back, and asks everyone again. Until that new answer arrives, nothing beyond the strictly necessary runs.

## Contact

The controller of the personal data that this website's analytics collect — and of the account data on `api.sumizai.com` — is the operator named here, within the meaning of Article 4(7) GDPR. Notes from the applications never reach us. Questions about anything on this page, or a request about data already collected, go to a person, not a form.

**Operator**
10UP Jan Śliwa, sole proprietorship registered in Poland (CEIDG)

**Address**
Kminkowa 26, 72-003 Bezrzecze, Poland

**NIP**
8521091009

**E-mail**
[contact@sumizai.com](mailto:contact@sumizai.com)

We publish no telephone number, so e-mail is the channel. Your rights of access, erasure, restriction and objection, and how to exercise them, are set out in the [Privacy Policy](https://sumizai.com/legal/privacy.html). You may also complain to the Polish supervisory authority, the President of the Personal Data Protection Office (Prezes Urzędu Ochrony Danych Osobowych), ul. Stawki 2, 00-193 Warsaw. Consumers and sole traders treated as consumers keep every statutory right Polish and EU law gives them; nothing here limits it. This page describes what the site does — it is not legal advice.

