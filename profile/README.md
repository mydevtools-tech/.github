# MyDevTools

<p align="center">
  <img src="https://mydevtools.tech/favicon.ico" width="72" alt="MyDevTools">
</p>

<h1 align="center">MyDevTools</h1>

<p align="center">
  <strong>The local-first developer workspace.</strong><br>
  80+ developer tools. API client. SQL. MongoDB. Redis.<br>
  Runs on your machine. No account. No server.
</p>

<p align="center">
  <a href="https://mydevtools.tech">Website</a> ·
  <a href="https://github.com/mydevtools">GitHub</a> ·
  <a href="https://mydevtools.tech/tools">Tools</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open%20Source-AGPL--3.0-111827?style=for-the-badge" alt="Open Source">
  <img src="https://img.shields.io/badge/Offline-First-111827?style=for-the-badge" alt="Offline First">
  <img src="https://img.shields.io/badge/Backend-None-111827?style=for-the-badge" alt="No Backend">
  <img src="https://img.shields.io/badge/Developer%20Tools-80%2B-111827?style=for-the-badge" alt="80+ Tools">
</p>

---

## ⚡ One workspace. Fewer tabs.

Developers shouldn't need a browser full of random utility websites, a separate API client, a database GUI, a JWT debugger, a JSON formatter, a regex tester, and a dozen other applications just to get through a normal engineering day.

**MyDevTools brings those workflows together — as an application that runs on your computer.**

It is a developer-focused toolkit built around one principle:

> **Your data never leaves your machine.**

From formatting JSON to debugging APIs, inspecting JWTs, working with SQL/MongoDB/Redis, generating developer artifacts, testing regular expressions, and handling security utilities — MyDevTools is the toolbox that stays with the developer, and only with the developer.

🌐 **[mydevtools.tech](https://mydevtools.tech)**

---

## 🧰 What we build

### Data & Code

`JSON` `YAML` `SQL` `GraphQL` `Markdown` `CSV` `Regex` `Diff`

- JSON Formatter & Visualizer
- JSON Schema Generator
- JSON to Code
- SQL Formatter
- GraphQL Formatter
- YAML Formatter
- Markdown Preview
- JSON / CSV / Excel conversion
- Diff & JSON Diff
- JSONPath Playground
- Regex Tester

### API & Networking

`REST` `HTTP` `WebSocket` `DNS` `cURL`

- API Client
- cURL to Code
- Webhook Tester
- WebSocket Tester
- HTTP Status Codes
- DNS Lookup
- URL Parser
- IP / Subnet Calculator
- User-Agent Parser
- MIME Type Lookup

### Security & Cryptography

`AES` `JWT` `HMAC` `Hashing` `TOTP` `PEM`

- JWT Decoder
- Hash Generator
- HMAC Generator
- Encryption Playground
- Password Manager
- Bcrypt Generator & Checker
- TOTP / 2FA Generator
- Certificate / PEM Decoder
- SSH / RSA Key Generator
- Secret / API Key Generator

### Database & Infrastructure

`SQL` `MongoDB` `Redis` `S3` `Docker`

- SQL Client
- MongoDB / NoSQL Client
- Redis Client
- Database Explorer
- S3 / object-storage workflows
- Docker Compose Generator

> These connect **directly** from your machine to **your** databases and buckets. Connection strings, credentials, and query results are never proxied through a MyDevTools server — because there isn't one.

### Developer Productivity

`UUID` `Base64` `Cron` `Mock Data` `Images` `CSS`

- UUID / ULID Generator
- Base64 Encoder / Decoder
- Timestamp Converter
- Unit Converter
- Mock Data Generator
- Cron Builder
- `.gitignore` Generator
- Markdown Table Generator
- Image Compressor
- SVG Optimizer
- Favicon Generator
- Code Screenshot
- CSS Generators

And more.

---

# 🏗️ Engineering Philosophy

MyDevTools is not a cloud developer SaaS, and it is not trying to become one.

We removed the backend on purpose. **There is no application server, no hosted database, and no account system.** Privacy and speed stop being policies you have to trust and become properties of the architecture.

### Local by default — and by design

Every transformation happens on your machine. Not "usually." Not "for most tools."

```text
┌───────────────────────┐
│      Developer        │
└───────────┬───────────┘
            │
            ▼
┌───────────────────────┐
│  MyDevTools (desktop) │
│                       │
│  Tools + Processing   │
│  + Local Storage      │
└───────────┬───────────┘
            │
            ▼
┌───────────────────────┐
│     Local Result      │
└───────────────────────┘
```

No round trip. No upload. No "we don't log your data" promise you have to take on faith.

### No cloud storage

Your workspace — tabs, snippets, saved requests, connection profiles, history, preferences — lives in a local data directory on your own filesystem.

That means you can work with sensitive:

- source code
- API payloads
- credentials
- tokens
- certificates
- database queries
- configuration
- generated data

without any of it touching infrastructure we control.

### The only network traffic is yours

MyDevTools makes network requests in exactly three cases:

1. **You told it to** — an API call in the API client, a DNS lookup, a database connection.
2. **Update checks** — a version check against our release feed. Disableable.
3. **License validation** — a one-time activation call. Disableable after activation.

No analytics. No telemetry. No crash reporting that ships your payloads somewhere.

### Optional sync, off by default

Cloud sync exists as an **opt-in add-on** for developers who want their workspace on multiple machines. It is off unless you turn it on, it is not required for any tool to function, and the app is fully usable having never seen a network.

### Open source

The project is built in the open so developers can inspect the implementation, verify the privacy claims above rather than believe them, contribute improvements, and build from source.

---

# 🧱 Technology Stack

MyDevTools is a desktop application built with a web frontend and a native shell. The stack is deliberately small — fewer moving parts means fewer places for your data to go.

<table>
<tr>
<td width="50%" valign="top">

### Application

- **TypeScript**
- **React**
- **Next.js** (static export)
- Component-driven UI
- Developer-focused interfaces

</td>
<td width="50%" valign="top">

### Desktop Shell

- **Tauri**
- Native OS integration
- Filesystem access
- Direct TCP for DB clients
- Small binaries, low memory

</td>
</tr>

<tr>
<td width="50%" valign="top">

### Local Storage

- **SQLite** (local file)
- OS keychain for secrets
- Plain files for exports
- Fully user-owned
- Portable and inspectable

</td>
<td width="50%" valign="top">

### Build & Release

- **GitHub Actions**
- Cross-platform builds
- Signed releases
- Reproducible pipelines
- Static site for docs/marketing

</td>
</tr>
</table>

### Stack at a glance

```text
                    MyDevTools
                         │
              ┌──────────┴──────────┐
              │                     │
              ▼                     ▼
         Application            Desktop Shell
              │                     │
        TypeScript              Tauri / Rust
        React / Next.js         Native APIs
              │                     │
              └──────────┬──────────┘
                         │
                         ▼
                 Local Data Directory
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
           SQLite              OS Keychain
        (workspace)            (secrets)

              ── no server involved ──
```

> There is no `backend/` service to deploy, scale, monitor, or breach. That is the point.

---

# 🖥️ Local-First Architecture

The most important architectural decision was **deleting the server**.

```text
                 ┌─────────────────────┐
                 │    MyDevTools UI    │
                 └──────────┬──────────┘
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
        Local Tools     API Tools       DB Tools
             │              │              │
             ▼              ▼              ▼
         In-process    Your target     Your database
         computation     endpoint        (direct)
             │              │              │
             └──────────────┼──────────────┘
                            │
                            ▼
                   Local Data Directory
```

A JSON formatter doesn't need a backend.

A JWT decoder doesn't need a backend.

A regex tester doesn't need a backend.

A hash generator doesn't need a backend.

A developer should never have to upload sensitive data to a stranger's server simply because the tool they need happened to be hosted on the web.

### What this buys you

| | |
|---|---|
| **Speed** | No network latency on any transformation. Operations are instant. |
| **Offline** | Works on a plane, in a SCIF, on an air-gapped machine. |
| **Privacy** | Nothing to intercept, log, subpoena, or leak. |
| **Longevity** | No shutdown risk. If we vanish tomorrow, your copy keeps working. |
| **Compliance** | Easier to clear with security teams — there's no data processor to review. |

---

# 🔐 Security Principles

Security-sensitive developer tooling deserves a different threat model.

We design around:

### Zero data movement

The strongest guarantee isn't encrypting data in transit. It's not transmitting it at all.

### Minimal attack surface

No server means no API to exploit, no database to dump, no session store to hijack, and no shared multi-tenant blast radius.

### Secrets stay in the OS

Credentials and connection strings go to the platform keychain (Keychain / Credential Manager / Secret Service), not to a config file in plaintext and never to us.

### Secure defaults

The easiest workflow should also be the safe workflow. Sync off, telemetry absent, local-only unless you say otherwise.

### Transparent processing

Developers should be able to understand where their data goes and why. Here the answer is short: nowhere.

### Auditable software

Open source makes security review possible. Every claim in this README is checkable against the source.

### Supply chain awareness

Dependencies, build infrastructure, and release signing are treated as part of the application's attack surface — for a distributed binary, the pipeline *is* the threat model.

---

# 🚀 Build & Release

We treat MyDevTools as an engineering product, not a collection of utilities.

## CI/CD

```text
Commit
  │
  ▼
Pull Request
  │
  ├── Lint
  ├── Type checks
  ├── Tests
  ├── Dependency audit
  ├── Cross-platform build
  │
  ▼
Review
  │
  ▼
Tagged Release
  │
  ├── macOS  (signed + notarized)
  ├── Windows (Coming Soon)
  └── Linux  (Coming Soon)
```

Security and dependency checks fail closed rather than silently producing false-clean results.

## Distribution

Releases are published as signed, versioned artifacts on GitHub Releases. Builds are reproducible from source, so you can verify what you're running.

## Reliability

Because there is no production service, "operations" means shipping a binary that doesn't break:

- crash-safe local storage with migrations
- graceful degradation when offline
- opt-in diagnostics that stay on disk
- no forced auto-updates

---

# 🧩 Repository Philosophy

Repositories are organized around clear responsibilities rather than one giant application.

```text
mydevtools/
│
├── app/
│   ├── UI + tool surfaces
│   ├── workspace state
│   └── local persistence
│
├── shell/
│   ├── native integration
│   ├── filesystem + keychain
│   └── network + DB drivers
│
├── tools/
│   ├── formatters
│   ├── generators
│   ├── security utilities
│   ├── API utilities
│   └── developer helpers
│
├── build/
│   ├── packaging
│   ├── signing
│   └── CI/CD
│
├── web/
│   └── static marketing + docs site
│
└── docs/
    ├── architecture
    ├── development
    └── security
```

The exact repository boundaries may evolve as the platform grows.

---

# 🛠️ Developer Experience

We optimize for a short path from **idea → implementation → useful tool**.

A new utility should ideally be:

1. Easy to understand
2. Easy to test
3. Runnable without a network
4. Independent where possible
5. Reusable
6. Fast
7. Consistent with the rest of the platform

We prefer composable primitives over tightly coupled features. If a tool needs a server to work, it probably doesn't belong here.

---

# 🌍 Open Source

MyDevTools is released under **AGPL-3.0**.

We believe developer infrastructure should be inspectable and extensible.

Contributions are welcome across:

- 🧰 New developer tools
- ⚡ Performance
- 🎨 UI/UX
- 🔐 Security
- 🧪 Testing
- 🏗️ Architecture
- 📦 Packaging & distribution
- 📚 Documentation
- ♿ Accessibility
- 🛠️ Developer experience

---

# 🤝 Contributing

A good contribution doesn't just add code — it improves the developer experience.

Before opening a PR:

```bash
git clone <repository>
cd <repository>

# install dependencies
# run the desktop app in development mode
# run tests
# verify lint/type checks
```

Please check the individual repository's `README.md`, contribution guidelines, and development scripts for the exact commands.

---

# 🗺️ Direction

MyDevTools is evolving toward a broader **developer operating workspace**.

The long-term idea is not:

> "Put 100 random tools on one website."

It is:

> **Build the local toolbox developers wish their operating system shipped with.**

That means deeper workflows around:

```text
Developer
    │
    ├── Code
    ├── APIs
    ├── Databases
    ├── Security
    ├── Infrastructure
    ├── Data
    └── Productivity
            │
            ▼
      MyDevTools
            │
            ▼
     One local workspace
```

The number of tools matters less than how much **context switching** we eliminate.

---

# 📈 Why MyDevTools?

| Traditional workflow | MyDevTools |
|---|---|
| Many browser tabs | One application |
| Separate utilities | Unified toolkit |
| Copy/paste between sites | Connected workflows |
| Paste secrets into a stranger's website | Everything stays local |
| Data uploaded to process | Data never leaves the machine |
| Account required | No account, no login |
| Breaks without internet | Fully offline |
| Vendor shutdown risk | Your copy keeps working |
| Closed tooling | Open source |
| Subscription treadmill | Own it |

---

# ⭐ Help Build the Developer Toolbox

If MyDevTools saves you time:

⭐ Star the repositories  
🐛 Report bugs  
💡 Propose tools  
🔐 Report security issues responsibly  
🔧 Submit pull requests  
📖 Improve documentation  
📣 Share the project

Every contribution helps turn MyDevTools into a better open-source developer platform.

---

## 🔗 Links

🌐 **Website:** https://mydevtools.tech

🧰 **Developer Toolkit:** https://mydevtools.tech/tools

📚 **Documentation:** https://mydevtools.tech/help

🔐 **Security:** https://mydevtools.tech/security

---

<p align="center">
  <strong>MyDevTools</strong><br>
  Built for developers who want fewer tabs, faster workflows, and full control of their data.
</p>

<p align="center">
  <sub>Open source · Local-first · Offline · No backend</sub>
</p>
