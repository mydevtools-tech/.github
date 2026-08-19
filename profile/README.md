<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mydevtools-tech/mydevtools/main/assets/logo-light.png" />
    <img src="https://raw.githubusercontent.com/mydevtools-tech/mydevtools/main/assets/logo-dark.png" alt="MyDevTools logo" width="80" height="80" />
  </picture>
</p>

<h1 align="center">MyDevTools</h1>

<p align="center">
  <strong>The Offline Developer Workstation</strong><br />
  80+ developer tools, an API client and SQL / MongoDB / Redis clients —<br />
  one desktop app that runs entirely on your machine.
</p>

<p align="center">
  <a href="https://github.com/mydevtools-tech/mydevtools/releases/latest"><strong>⬇️ Download</strong></a> ·
  <a href="https://github.com/mydevtools-tech/mydevtools"><strong>⭐ Source</strong></a> ·
  <a href="https://mydevtools.tech">Website</a> ·
  <a href="https://mydevtools.tech/tools">Tools</a> ·
  <a href="https://github.com/mydevtools-tech/mydevtools/discussions">Discussions</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Free%20%26%20Open%20Source-AGPL--3.0-111827?style=for-the-badge" alt="Free & Open Source, AGPL-3.0" />
  <img src="https://img.shields.io/badge/100%25-Offline-111827?style=for-the-badge" alt="100% offline" />
  <img src="https://img.shields.io/badge/Accounts-None-111827?style=for-the-badge" alt="No accounts" />
  <img src="https://img.shields.io/badge/Developer%20Tools-80%2B-111827?style=for-the-badge" alt="80+ developer tools" />
</p>

---

## One workspace. Fewer tabs.

Developers shouldn't need a browser full of random utility websites, a separate
API client, a database GUI, a JWT debugger, a JSON formatter, a regex tester and
a dozen other apps just to get through a normal engineering day.

**MyDevTools brings those workflows together in one application that runs on
your computer** — and only there.

> Your data never leaves your machine.

## What's in the box

| | |
|---|---|
| 📝 **Formatters & validators** | JSON (format, diff, visualize, schema, to-code), YAML, TOML, XML, SQL, GraphQL, Markdown, regex, diff |
| 🌐 **Network & API** | API client (collections, environments, auth, gRPC, mock server — no browser CORS limits), cURL to code, webhook & WebSocket testers, DNS / WHOIS, subnet calculator |
| 🗄️ **Database & storage** | SQL client (PostgreSQL, MySQL, MariaDB), MongoDB explorer, Redis commander, S3 drive — native Rust drivers, straight from your machine to your database |
| 🔐 **Security & crypto** | Password manager, AES-GCM playground, JWT decoder, hash / HMAC / bcrypt, TOTP, SSH & RSA keys, certificate decoder, encrypted `.env` manager |
| 🔄 **Converters & generators** | Base64, URL, string case, timestamps, units, CSV ↔ JSON, UUID / ULID, mock data, cron, Docker Compose, `.gitignore`, QR codes |
| 🎨 **Media & design** | Color & contrast, CSS gradients & generators, image compressor, SVG optimizer, EXIF remover, favicons, code screenshots |
| 📱 **Productivity** | Notes, code snippets, tasks, bookmarks, API keys, a break room |

Everything is one `⌘K` away, in dark or light mode, in 27 languages.

## How it's built

- **No backend, by design.** No MyDevTools server, no account system, no sync
  service. There is nothing to sign in to and nothing to breach.
- **Local, encrypted storage.** Notes, snippets, tasks and saved requests live in
  a SQLCipher database on your disk, keyed from the OS keychain. Credentials are
  additionally vault-encrypted with a master password only you know.
- **The only network traffic is yours.** API requests you write, databases you
  connect to, DNS lookups you run, and the updater checking GitHub Releases.
  Usage stats are opt-in, anonymous and limited to two events — no tool input,
  no paths, no stable ids.
- **Free and open source under AGPL-3.0.** No paid tier, no license keys, no
  ads. Read the code; the claims above are in it.
- **Stack:** Tauri v2 (Rust) · Next.js 16 / React 19 / TypeScript · SQLCipher ·
  native Rust drivers for PostgreSQL, MySQL, MongoDB and Redis.

## Repositories

| Repo | What |
|---|---|
| [mydevtools](https://github.com/mydevtools-tech/mydevtools) | The desktop app (`apps/desktop-ui` + `apps/desktop`) and the marketing site (`apps/web`) |
| [mydevtools-releases](https://github.com/mydevtools-tech/mydevtools-releases) | Mirror of release artifacts for older installs |

## Get involved

Bug reports, new tools, UI polish, translations and docs are all welcome —
start with [CONTRIBUTING.md](https://github.com/mydevtools-tech/mydevtools/blob/main/CONTRIBUTING.md)
or an issue labelled
[`good first issue`](https://github.com/mydevtools-tech/mydevtools/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22).
Testing the desktop build on Windows or Linux is the most useful thing a new
contributor can do right now.

If MyDevTools saves you time, star the repo or
[sponsor the project](https://github.com/sponsors/itsmeakhil).

<p align="center">
  Made with ❤️ by <a href="https://github.com/itsmeakhil">Akhil</a> and <a href="https://github.com/mydevtools-tech/mydevtools/graphs/contributors">contributors</a>
</p>
