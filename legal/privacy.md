---
title: "Privacy Policy"
url: "https://sumizai.com/legal/privacy.html"
date: "2026-10-17T00:00:00+02:00"
modified: "2026-10-17T00:00:00+02:00"
description: "SumizAI keeps your notes on your Mac. Our server holds only your account; the website measures traffic, with cookies only after consent."
tags: ["sumizai", "legal", "privacy"]
---

# Privacy Policy

This policy covers **SumizAI for Mac**, the application distributed through the Mac App Store, the account service it talks to at `api.sumizai.com`, and this website, `sumizai.com`.

The short version: your notes, questions, documents and vaults stay on your Mac. They are never sent to us. Our server stores only what is needed to run your account and subscription. Questions you ask the AI go straight from your Mac to the AI provider you chose, using your own key. There is no analytics, no advertising, no tracking and no crash reporting in the app. The website measures traffic, and sets cookies only after you agree.

## Who is responsible for your data

The controller of the personal data described here is **Jan Śliwa**, Poland, trading as **10UP Jan Śliwa**, a sole proprietorship registered in Poland (CEIDG), tax ID (NIP) 8521091009, Kminkowa 26, 72-003 Bezrzecze, Poland.

Contact for everything in this policy, including requests about your rights: [contact@sumizai.com](mailto:contact@sumizai.com). A human reads every message.

## What this policy covers

This document applies to:

- the **SumizAI application for Mac** from the Mac App Store;
- the **account service** at `api.sumizai.com` that the application uses for sign-in, devices and subscription status;
- the **website** `sumizai.com`, including the contact form on the [Support](https://sumizai.com/support/) page.

The application and the website are different: the website uses analytics (only after you agree to cookies), the application contains no analytics at all. The cookies themselves are listed in the [cookie policy](https://sumizai.com/legal/cookies.html).

## Data that stays on your Mac

Everything you create in SumizAI is stored **only on your computer**:

- **Notes**, as ordinary Markdown (`.md`) files in your notes folder. By default this is a `SumizAI` folder inside the application's own macOS container. You can choose another folder in the app.
- **Vaults, the table of contents, conversations, your questions, the AI answers and imported documents**, in a local SQLite database and files on the same Mac.
- **Your AI provider keys, your session tokens and the installation identifier**, in the macOS keychain on your Mac.

None of this is sent to us. There is no synchronisation and no cloud copy run by us. We cannot read, restore or delete your notes, because we never have them. If you put your notes folder in a place your Mac syncs or backs up (for example iCloud Drive or Time Machine), that copy is handled by Apple or by whatever service you set up, on its terms.

## Your account on api.sumizai.com

You need a SumizAI account to subscribe. You create it in the app with an e-mail address and a password. The account server stores:

| Data | What it is for |
|---|---|
| E-mail address | Your sign-in name and the way we can identify your account when you write to us. We do not send newsletters or marketing. The only e-mail the service sends is a password-reset link, and only when you ask for one. |
| Password-reset link (only if you ask for one) | A one-time link valid for one hour. The server keeps only a SHA-256 hash of it with its expiry time, never the link itself. |
| Password hash (BCrypt) | To check your password at sign-in. We never store the password itself. |
| Account identifier (a random UUID) | Links your account to your devices, your sessions and your App Store subscription. |
| Access status and dates | Whether your access is active, in trial, expired or blocked, where it comes from (App Store subscription or access granted manually by us, e.g. for testers), when it ends, plus an optional internal note explaining a manual grant. |
| Account dates and platform | When the account was created and last updated, the platform it was created on (for example macOS), the platform and time it was last used, and a flag set when a second account is created on the same computer. |
| Referral code | Only if you signed up through a referral link that carried one. Otherwise empty. |
| Session tokens | A short-lived access token (15 minutes) and a refresh token (30 days, rotated each time it is used). The server keeps only a SHA-256 hash of each refresh token, with its issue, expiry and revocation time and the device it belongs to. |

We do not ask for your name, phone number, address, photo or date of birth, and the server has no place to store them.

**Password reset:** in the app choose **Forgot your password?** and enter the account's e-mail address. If an account uses it, our own mail server sends a one-time link to that address; the answer in the app is the same either way, so nobody can use it to find out who has an account. The link opens a page on sumizai.com that loads no analytics, works for one hour and only once, and setting a new password signs out all your devices.

## Device identifiers

One account can be active on up to **three** computers. To enforce that limit, and so that the same computer cannot claim a free trial again and again with new e-mail addresses, the app sends one identifier when you sign in or register:

- **Installation identifier** — a random value the app creates on first use and keeps in your macOS keychain. It is not derived from anything about you or your Mac.

The app does not read any hardware identifier of your Mac (serial number, hardware UUID or network address) and sends none.

For each device the server also stores the platform, a label made of the system name and the first eight characters of the installation identifier (for example `macOS · 1a2b3c4d` — not your computer's name), when it was first and last seen, and when you disconnected it. You can see your devices and disconnect any of them in **Settings → Devices**; disconnecting signs that device out at once.

## Purchases through Apple

The subscription is sold and charged **only by Apple**, through the App Store and StoreKit, using your Apple ID. We never see your card number, bank details or billing address, and we do not process payments.

Apple sends our server signed notifications about your subscription (for example: started, renewed, expired, refunded). From them we keep with your account the **original transaction identifier** of the subscription, the source of access (App Store), the date your access ends and its status. Your purchase is linked to your SumizAI account by your account identifier. We also keep a log of the notifications received: Apple's notification identifier, its type, the environment (production or test), whether it changed your access, and when it arrived. Apple's own handling of your data is described in the [Apple Privacy Policy](https://www.apple.com/legal/privacy/).

## AI providers you choose

SumizAI has no AI of its own. You pick a provider in the app and connect it with **your own API key** (or, for a local Ollama or your own server, possibly with no key at all).

When you use AI features, the app sends from your Mac **directly to that provider**: your question and the conversation, fragments of your notes used as context (the table of contents and the text of up to five most relevant notes), the text of documents you import when you ask the AI to work on them, and a note's source material when you ask the app to translate it into your vault's language. This data does not pass through our servers and we cannot see it.

Before anything is sent to a provider for the first time, the app tells you what will be sent and where, links to the provider's privacy policy and asks for your consent. You withdraw that consent by disconnecting the provider in the app's settings; from then on nothing goes to it.

The provider processes the data under its own terms and its agreement with you, as the owner of the key. Whether it stores the data or uses it to train models depends on those terms and the settings of your account with it, not on us. Their policies:

| Provider | Where the data goes | Their privacy policy |
|---|---|---|
| Anthropic (Claude) | `api.anthropic.com` | [anthropic.com/legal/privacy](https://www.anthropic.com/legal/privacy) |
| OpenAI | `api.openai.com` | [openai.com/policies/privacy-policy](https://openai.com/policies/privacy-policy/) |
| Google Gemini | `generativelanguage.googleapis.com` | [policies.google.com/privacy](https://policies.google.com/privacy) and the [Gemini API Additional Terms](https://ai.google.dev/gemini-api/terms) |
| Groq | `api.groq.com` | [groq.com/privacy-policy](https://groq.com/privacy-policy/) |
| OpenRouter | `openrouter.ai`, which forwards to the model vendor you pick there | [openrouter.ai/privacy](https://openrouter.ai/privacy) |
| Ollama (local) | `127.0.0.1` — your own computer. Nothing leaves the machine. | Not applicable |
| Your own server | The address you type in | Whoever runs that server |

Your provider keys are stored in the macOS keychain on your Mac and are sent only to the provider they belong to. We never receive them.

## What the app does not do

- No analytics or usage statistics in the app.
- No advertising and no advertising identifiers.
- No tracking across apps or websites, and no data brokers.
- No crash reports or telemetry sent anywhere.
- No selling or renting of personal data, to anyone — neither from the app nor from the website.

## The website: sumizai.com

The website is static HTML on our own server. It has no accounts and no login. It has two forms: the contact form described below, and the page that sets a new password from a reset link (see "Your account on api.sumizai.com"), which loads no analytics at all. It loads exactly two third-party services, both for measuring traffic:

- **Google Analytics 4** (property `G-RKZ7HS09BS`) — which pages were opened, roughly where in the world the visit came from, which site sent you here, which device and browser family was used. It is aggregated traffic measurement; it does not tell us who you are.
- **Microsoft Clarity** (project `y23mz3osxm`) — anonymised session replay: pointer movement, clicks, scrolling and the page layout. It is a reconstruction of a page, not a video of your screen, and we attach no identifier of our own to it.

Nothing else: no advertising pixels, no remarketing tags, no chat widget, no fingerprinting.

### Before you consent: measurement without storage

Until you accept cookies in the banner, both tools run in cookieless mode (Google _Consent Mode advanced_, Clarity cookieless mode): they record that a page was opened and store **nothing on your device** — no cookie, no local or session storage, no identifier that survives the page. Each page view is counted on its own. The legal basis is our legitimate interest in knowing which pages are read (Art. 6(1)(f) GDPR); because nothing is stored on or read from your device, consent under art. 398 of the Polish Electronic Communications Law is not required for it. You can object at any time by writing to us.

### After you consent

Accepting switches on the cookies listed in the [cookie policy](https://sumizai.com/legal/cookies.html) and session replay, on the basis of your consent (Art. 6(1)(a) GDPR). Your choice is kept in one entry in your browser's local storage — not a cookie, and the only thing the site stores without asking, because there is no other way to remember that you said no. You can change or withdraw your choice at any time through _Cookie settings_ in the footer; withdrawing deletes the cookies already set.

### IP addresses and the providers' own terms

Every request to a web server carries your IP address. In the analytics reports we use, no IP address is visible to us. Google and Microsoft handle it inside their services under their own terms ([Google](https://policies.google.com/privacy), [Microsoft](https://privacy.microsoft.com/privacystatement)). We do not build profiles, combine this data with anything else, or sell it.

## When you write to us

**By e-mail.** [contact@sumizai.com](mailto:contact@sumizai.com) is a mailbox we run ourselves (Postfix, Dovecot and OpenDKIM on our Hetzner server in Germany). There is no e-mail provider in between.

**Through the contact form** on the [Support](https://sumizai.com/support/) page. The form sends the e-mail address you enter, the subject and the message, together with the page language and the page address, to our account server at `api.sumizai.com` (the same Hetzner machine), which passes the message on to us. Like every request, it is recorded in the access log with your IP address (see [Server logs](#server-logs)), and the IP address is used briefly to limit how many messages can be sent in a row. The form uses no cookies.

We use what you write only to answer you and to deal with the matter. The legal basis is Art. 6(1)(b) GDPR where the message concerns your use of SumizAI, and otherwise Art. 6(1)(f) — our legitimate interest in answering people who write to us. Messages are kept as long as needed to deal with the matter and any related claims.

## Server logs and security

Like any internet service, our servers (the account server and the website) see the IP address of each request. It is used as follows:

- **Access log** of the web server: time, IP address, requested address, response status and the app's user agent. These logs rotate automatically and are kept for at most 90 days.
- **Application log**: technical events and errors. E-mail addresses are masked to the first letter and the domain, and tokens to their last four characters. Application logs are kept for up to 30 days and then deleted.
- **Protection against password guessing**: failed sign-ins are counted per e-mail address and per IP address, in the server's memory only, for 15 minutes.

The app also checks, from time to time, which version is current, so that an outdated version can ask you to update. That request carries only the platform name.

## Why we may process this data (GDPR)

- **Performing the contract** (Art. 6(1)(b) GDPR): your account, sign-in, sessions, devices, the device limit and your subscription status — without these we cannot provide the service you subscribed to.
- **Legitimate interest** (Art. 6(1)(f) GDPR): preventing abuse of the free trial and of the device limit (device identifiers, the record described under [Deleting your account](#deleting-your-account)), protecting the service against attacks (logs, sign-in and form throttling), cookieless traffic measurement on the website, answering messages, and establishing or defending legal claims.
- **Consent** (Art. 6(1)(a) GDPR): analytics cookies and session replay on the website, only after you accept them.
- **Legal obligations** (Art. 6(1)(c) GDPR): where the law requires us to keep or disclose data.

Sending your data to an AI provider is your action, done from your Mac with your key; we do not process that data. The consent the app asks for before the first transfer makes sure you know what goes where.

## Who else receives data

- **Hetzner Online GmbH** (Industriestrasse 25, 91710 Gunzenhausen, Germany) — hosting. The account server, the website and our mailbox run on our own machine in Hetzner's Falkenstein (FSN1) data centre in Germany, EU. Hetzner acts as our processor.
- **Google and Microsoft** — as the website's two analytics services (above). Nothing from the application reaches them. Google may also appear as the AI provider if you choose Gemini.
- **Apple** — sells and charges the subscription and tells us its status. Apple is a separate controller for the purchase.
- **The AI provider you choose** — receives your data directly from your Mac, under your own agreement with it (see above). It does not receive anything from us.
- **Public authorities** — only when the law obliges us.

E-mail you send to [contact@sumizai.com](mailto:contact@sumizai.com) is stored on the same Hetzner machine; there is no third-party e-mail provider.

## Transfers outside the EU

We keep your account data, the website and our mailbox in the European Union and do not transfer them outside the European Economic Area. Apple, the AI provider you choose, and the website's analytics services (Google, Microsoft) may process data in other countries, including the United States; that is governed by their own terms and safeguards. If you prefer to avoid that entirely: use a local Ollama in the app and decline analytics cookies on the website.

## How long we keep data

| Data | Kept until |
|---|---|
| Account, sessions, devices, subscription status | You delete the account. Expired refresh tokens and disconnected devices remain listed with the account until then. |
| Installation identifier of devices that used the free trial | Kept after account deletion, with no link to any account or e-mail address. Deleted 3 years after the entry. |
| Log of notifications received from Apple | Kept after account deletion with the link to the account removed. Deleted 30 days after receipt. |
| Web server access logs | At most 90 days. |
| Application logs | Up to 30 days. |
| Sign-in throttling counters | 15 minutes, in memory. |
| Password-reset link (its hash) | Until it is used or expires (one hour); removed from the database the following night. |
| Your e-mails and contact-form messages | As long as needed to handle the matter and any related claims. |
| Cookie choice on the website | One entry in your browser's local storage, until you clear it or change your choice. |
| Website analytics | Inside Google Analytics and Microsoft Clarity, under the retention those services apply. We keep no separate copy. |
| Notes, vaults, conversations, keys | We never have them. They stay on your Mac until you delete them. |

## Deleting your account

You can delete your account at any time in the app: **Settings → Delete account**. Deletion is immediate and permanent. It removes from our server your account (e-mail, password hash, status and dates), all sessions and all devices. It is a real deletion, not a deactivation. Your subscription status and the original Apple transaction identifier stored with the account are deleted with it; entries in our log of Apple notifications stay, with the link to your account removed.

**One thing remains, and only for one purpose.** The installation identifier of the devices that were linked to the deleted account is kept in a separate table, together with the date of the entry, **with no link to any account and no e-mail address**. It is kept only so that deleting an account and creating a new one on the same computer does not grant a second free trial. The legal basis is our legitimate interest in preventing abuse (Art. 6(1)(f) GDPR). You can object to it by writing to [contact@sumizai.com](mailto:contact@sumizai.com).

**Your vaults and `.md` files stay on your Mac.** Deleting the account never touches them. To remove them, delete the notes folder and the app.

**Deleting the account does not cancel the App Store subscription.** Apple bills it, so cancel it in your Apple ID settings ([how to cancel](https://support.apple.com/en-us/118428)).

## Your rights

Under the GDPR you have the right to:

- **access** your data and get a copy of it;
- **rectification** of inaccurate data (for example a mistyped e-mail address);
- **erasure** — the quickest way is **Settings → Delete account**;
- **restriction** of processing;
- **data portability** — your account data in a machine-readable format (your notes are already plain files on your Mac);
- **object** to processing based on our legitimate interest;
- **withdraw consent** at any time, where processing relies on it, without affecting what happened before;
- **lodge a complaint** with the supervisory authority: in Poland, the President of the Personal Data Protection Office (Prezes Urzędu Ochrony Danych Osobowych), ul. Stawki 2, 00-193 Warszawa, [uodo.gov.pl](https://uodo.gov.pl/), or the authority in the EU country where you live or work.

Write to [contact@sumizai.com](mailto:contact@sumizai.com) from the e-mail address of your account, so we can confirm it is yours. We answer within one month. We do not make decisions about you based solely on automated processing.

## How we protect data

- All traffic between the app and `api.sumizai.com` is encrypted (HTTPS).
- Passwords are stored only as BCrypt hashes; refresh tokens only as SHA-256 hashes.
- The database is not reachable from the internet; only the web server is.
- Secrets on your Mac (provider keys, session tokens) are kept in the macOS keychain.

## Children

SumizAI is not directed at children and we do not knowingly create accounts for children under 16. If you believe a child has given us data, write to [contact@sumizai.com](mailto:contact@sumizai.com) and we will delete it.

## Changes to this policy

When the application or this policy changes, we publish the new version here with a new date and version number. The date at the top of the page always shows which version is in force.

## Contact

10UP Jan Śliwa, Kminkowa 26, 72-003 Bezrzecze, Poland — [contact@sumizai.com](mailto:contact@sumizai.com). Help with the app: [Support](https://sumizai.com/support/). Terms: [Terms of Service](https://sumizai.com/legal/terms.html).

