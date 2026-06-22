> **This is a menu, not a commitment.** This page explains *what each piece of software does* and
> *what you'd be able to do with it*, in plain language, so you can decide what's actually worth
> running. Approximate yearly SaaS prices are shown only to give a sense of value — treat them as
> ballpark.

---

## The big picture — what "self-hosting this suite" gives you

You run a small set of open-source apps on your own machine (a PC now, a little always-on box later).
The capabilities you gain:

- **You stop renting software.** The apps are free and open-source. You pay in a bit of setup +
  electricity, not monthly fees.
- **Your data is yours.** Photos, documents, notes, finances, passwords — all on hardware you control,
  not someone else's cloud.
- **Private access from anywhere.** Via Tailscale (a private mesh network), you reach everything from
  your phone or laptop wherever you are, with **nothing exposed to the public internet**.
- **It feels like one product.** One dashboard as the front door, one login across apps, automatic
  encrypted backups, and health monitoring — instead of 30 disconnected tools.

---

## The platform — the foundation that ties everything together

Before the apps, there's a thin layer that turns a pile of separate programs into a coherent suite.
In plain terms, it gives you:

| Capability | What it means for you |
|---|---|
| **One dashboard (front door)** | A single homepage listing every app, each with a live status tile. You go to one place. |
| **One login (single sign-on)** | Sign in once; it carries you across apps. No 30 separate passwords to manage. |
| **Private remote access** | Reach everything securely from any of your devices, anywhere, nothing public. |
| **Real HTTPS everywhere** | Every app gets a clean `https://app.home.arpa` address with no scary browser warnings. |
| **Automatic encrypted backups** | Everything backed up on a schedule, encrypted, with a *tested* restore. |
| **Health & logs at a glance** | See what's up/down and read any app's logs without digging. |
| **Easy add/update/move** | Add an app, update one safely, or move the whole suite to a new machine with little fuss. |

This layer is the real engineering work; the apps below are mostly off-the-shelf.

---

## The software, by domain

Each entry: **what it is → what you can do with it → what it replaces.**

### Dev & productivity

- **Forgejo** — your own GitHub. → Host private git repos, track issues, run CI/CD pipelines, store
  container images. *Replaces:* GitHub/GitLab paid plans (~$50+/yr).
- **code-server** — VS Code in a browser tab. → Open your editor on any device, with the heavy work
  running on the server. *Replaces:* GitHub Codespaces (~$100+/yr).
- **Hoppscotch** — an API testing workbench. → Build, send, and save HTTP/API requests to test
  services. *Replaces:* Postman/Insomnia paid (~$100+/yr).
- **Opengist** — a private pastebin/gist. → Save and share code snippets with syntax highlighting.
  *Replaces:* GitHub Gist private.
- **Outline** — a polished wiki / knowledge base. → Write structured docs and notes in a Notion-like
  editor, organized and searchable. *Replaces:* Notion/Confluence (~$96+/yr).
- **Excalidraw + drawio** — whiteboard + diagramming. → Sketch ideas, draw architecture/flowcharts.
  *Replaces:* Lucidchart/Miro (~$100+/yr).
- **Kimai** — time tracking. → Track hours per project/client and export to invoices. *Replaces:*
  Toggl/Harvest (~$120/yr).
- **n8n** — visual automation (the glue). → Connect apps with "when X happens, do Y" workflows — e.g.
  "new document scanned → notify me." *Replaces:* Zapier/Make (~$240+/yr).
- **Umami** — privacy-respecting web analytics. → See traffic to any site you run, without spying on
  visitors. *Replaces:* Google Analytics / Plausible cloud (~$100/yr).

### Knowledge & notes

- **Vaultwarden** — a password manager (Bitwarden-compatible). → Store passwords/2FA, autofill in
  browser & phone, share securely. **Easiest high-value win.** *Replaces:* 1Password/Bitwarden/LastPass
  (~$36–96/yr).
- **Nextcloud** — your own Dropbox + Google Drive + Calendar/Contacts. → Sync and share files across
  devices, edit documents in the browser, run your calendar and contacts. *Replaces:* Dropbox/Drive/
  iCloud (~$100+/yr).
- **Syncthing** — direct device-to-device file sync. → Keep folders identical across machines with no
  server in the middle (great for note vaults). *Replaces:* paid sync tiers.
- **Obsidian + self-hosted sync** — local-first notes. → Write linked notes/PKM stored as plain files,
  synced across devices without paying for sync. *Replaces:* Notion / Obsidian Sync (~$96/yr).
- **Paperless-ngx** — a document brain. → Scan/drop in any PDF/receipt/bill; it OCRs, tags, and makes
  everything full-text searchable. **Huge quality-of-life.** *Replaces:* paid document managers /
  Evernote (~$130/yr).
- **FreshRSS** — an RSS reader. → Follow blogs/news/YouTube channels in one feed, no algorithm.
  *Replaces:* Feedly Pro (~$72/yr).
- **Karakeep** — smart bookmarks + read-later. → Save links/articles; it archives the full page and
  auto-tags with AI so you can actually find them later. *Replaces:* Raindrop/Pocket/Instapaper (~$45/yr).

### Media & files

- **Immich** — your own Google Photos. → Auto-backup phone photos, browse a timeline, and **search by
  what's in the picture** ("beach", a person's face) thanks to on-device ML. **Star app.** *Replaces:*
  Google Photos / iCloud Photos (~$24–100/yr).
- **Jellyfin** — your own Netflix/Plex. → Stream your movies, TV, and music to any device with a nice
  UI — fully free, no paid tier. *Replaces:* Plex Pass / a streaming sub (~$60/yr).
- **Navidrome** — your own Spotify (for music you own). → Stream your music library with great mobile
  apps and offline sync. *Replaces:* Spotify for owned music (~$120/yr).
- **Audiobookshelf** — audiobook + podcast server. → Stream your audiobooks/podcasts with progress sync
  across devices. *Replaces:* Audible-lite / paid podcast apps (~$90/yr).
- **Stirling-PDF** — a full PDF toolkit. → Merge/split/compress/sign/OCR/convert PDFs, all in the
  browser. **Huge quality-of-life.** *Replaces:* Adobe Acrobat / iLovePDF / SmallPDF (~$155/yr).
- **Calibre-Web / Kavita** — e-book & comics library. → Organize and read your books/comics from any
  device. *Replaces:* paid reader subs.
- **MeTube / Cobalt / ConvertX** — downloaders + file converters. → Save videos you have rights to and
  convert files between formats. *Replaces:* various small media/convert SaaS.
- **Filebrowser** — a simple web file manager. → Browse/upload/download your raw files from a browser.

> *Note: media-acquisition automation (the "\*arr" apps) exists but is intentionally left off this list
> — and only ever appropriate for legally obtained content.*

### Finance & home

- **Actual Budget** — envelope budgeting. → Plan every dollar a job, track spending, and stay on
  budget; local-first and fast. **Top finance win.** *Replaces:* YNAB (~$99/yr).
- **Firefly III** — deeper personal finance. → Full double-entry tracking of accounts, bills, and
  reports (heavier than Actual; complement or alternative). *Replaces:* paid finance trackers.
- **Invoice Ninja** — invoicing & light accounting. → Send invoices, track payments and expenses (if
  you freelance). *Replaces:* FreshBooks/QuickBooks-lite (~$180/yr).
- **Home Assistant** — smart-home hub. → Control and automate smart devices locally, without depending
  on vendor clouds (only useful if you have smart devices). *Replaces:* SmartThings / paid IoT clouds.
- **Grocy** — household/pantry manager. → Track groceries, stock, expiry, chores, and shopping lists.
  *Replaces:* assorted household apps.
- **Mealie** — recipe manager + meal planning. → Save recipes, plan meals, auto-build shopping lists.
  *Replaces:* paid recipe apps.

### Bonus — AI & search

- **Ollama + Open WebUI** — a private ChatGPT-style chat over local models. → Run AI chat fully
  offline/private for sensitive or no-internet work. *Replaces:* ChatGPT Plus-lite for private use
  (~$240/yr).
- **SearXNG** — a private meta-search engine. → Search the web without being tracked/profiled.
  *Replaces:* tracking search engines.

---

## What self-hosting asks of you (the honest tradeoffs)

- **A little upkeep.** Occasional updates and the odd fix. The platform layer (monitoring, backups,
  easy updates) is specifically designed to minimize this.
- **It needs to stay on.** On a regular PC, services stop when it sleeps/reboots — which is why the
  long-term plan is a cheap always-on box.
- **You are the IT department.** No vendor SLA. The mitigation is **tested backups** — the single most
  important habit; a backup you've never restored is just a wish.
- **Some electricity + (eventually) ~$100–200 one-time** for a small always-on machine, if you go that
  route. No recurring fees.

---

## Rough value tally

Adopting most of the catalog replaces well over **$1,500/yr** of subscriptions (passwords, photos,
drive, notes, budgeting, PDF tools, media, automation, AI, and more) with free software you own — at
the cost of some setup and modest upkeep.

---

## How to use this list

Treat each domain as independent. A good way in is to start with the **highest-value, lowest-effort
wins** — typically passwords (Vaultwarden), photos (Immich), documents (Paperless-ngx), budgeting
(Actual Budget), and a PDF toolkit (Stirling-PDF) — get the platform foundation solid, then add
domains over time as it proves itself. Skip anything that doesn't fit your life (e.g., Home Assistant
without smart devices, or media if you don't keep a library). Nothing here is all-or-nothing.
