# MyDevTools

<p align="center">
  <img src="https://mydevtools.tech/favicon.ico" width="72" alt="MyDevTools">
</p>

<h1 align="center">MyDevTools</h1>

<p align="center">
  <strong>The local-first developer workspace.</strong><br>
  80+ developer tools. API client. SQL. MongoDB. Redis.<br>
  Open source. Offline. Privacy-first.
</p>

<p align="center">
  <a href="https://mydevtools.tech">Website</a> ·
  <a href="https://github.com/mydevtools">GitHub</a> ·
  <a href="https://mydevtools.tech/tools">Tools</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open%20Source-AGPL--3.0-111827?style=for-the-badge" alt="Open Source">
  <img src="https://img.shields.io/badge/Offline-First-111827?style=for-the-badge" alt="Offline First">
  <img src="https://img.shields.io/badge/Privacy-Local%20Processing-111827?style=for-the-badge" alt="Privacy">
  <img src="https://img.shields.io/badge/Developer%20Tools-80%2B-111827?style=for-the-badge" alt="80+ Tools">
</p>

---

## ⚡ One workspace. Fewer tabs.

Developers shouldn't need a browser full of random utility websites, a separate API client, a database GUI, a JWT debugger, a JSON formatter, a regex tester, and a dozen other applications just to get through a normal engineering day.

**MyDevTools brings those workflows together.**

It is a developer-focused toolkit built around one principle:

> **If a developer can do it locally, MyDevTools should make it possible locally.**

From formatting JSON to debugging APIs, inspecting JWTs, working with SQL/MongoDB/Redis, generating developer artifacts, testing regular expressions, and handling security utilities — MyDevTools is designed to be the toolbox that stays with the developer.

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

MyDevTools is not intended to become another cloud-first developer SaaS.

We are building a **local-first developer environment** where privacy and speed are architectural properties.

### Local by default

If a transformation can happen on the user's machine, it should.

```text
┌───────────────────────┐
│      Developer        │
└───────────┬───────────┘
            │
            ▼
┌───────────────────────┐
│     MyDevTools        │
│                       │
│  Tools + Processing   │
│  + Local Workflows    │
└───────────┬───────────┘
            │
            ▼
┌───────────────────────┐
│     Local Result      │
└───────────────────────┘
```

### No mandatory cloud storage

MyDevTools does not require an online storage or synchronization service for its core workflows.

The product is designed so developers can work with sensitive:

- source code
- API payloads
- credentials
- tokens
- certificates
- database queries
- configuration
- generated data

without having to upload that data to a MyDevTools cloud backend.

### Privacy is a feature

For security-sensitive utilities, processing locally is preferable to sending data to a remote server.

Examples include:

- hashing
- JWT inspection
- encryption/decryption utilities
- Base64 operations
- JSON transformation
- regex testing
- formatting
- secret generation
- certificate inspection

### Open source

The project is built in the open so developers can inspect the implementation, contribute improvements, self-host where applicable, and understand how their developer tooling works.

---

# 🧱 Technology Stack

MyDevTools uses a modern full-stack engineering ecosystem with a strong emphasis on TypeScript, Python, local processing, containerization, and pragmatic infrastructure.

<table>
<tr>
<td width="50%" valign="top">

### Frontend

- **Next.js**
- **React**
- **TypeScript**
- Modern component-driven UI
- Responsive developer-focused interfaces

</td>
<td width="50%" valign="top">

### Backend

- **Python**
- **FastAPI**
- **Pydantic**
- Async API architecture
- REST-oriented services

</td>
</tr>

<tr>
<td width="50%" valign="top">

### Data

- **MongoDB**
- **Redis**
- Document-oriented application data
- High-performance caching
- Local-first data workflows

</td>
<td width="50%" valign="top">

### Infrastructure

- **Docker**
- **AWS**
- Containerized services
- GitHub Actions
- Automated CI/CD

</td>
</tr>
</table>

### Engineering stack at a glance

```text
                    MyDevTools
                        │
        ┌───────────────┼────────────────┐
        │               │                │
        ▼               ▼                ▼
     Frontend        Backend           Local Tools
        │               │                │
  Next.js/React     FastAPI/Python     TypeScript
  TypeScript        Pydantic            Local APIs
        │               │                │
        └───────────────┼────────────────┘
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
           MongoDB              Redis
              │                   │
              └─────────┬─────────┘
                        ▼
                  Docker / AWS
                        │
                        ▼
                  GitHub Actions
```

> The architecture intentionally separates developer-facing tools from backend services so that utilities that do not require a backend can remain local.

---

# 🖥️ Local-First Architecture

The most important architectural decision is knowing **when not to use a server**.

```text
                 ┌─────────────────────┐
                 │    MyDevTools UI    │
                 └──────────┬──────────┘
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
        Local Tools      API Tools      DB Tools
             │              │              │
             ▼              ▼              ▼
        Browser/OS       Network        Database
        Processing       Requests       Connection
             │
             ▼
       Local Developer
          Workflow
```

This distinction matters.

A JSON formatter doesn't need a backend.

A JWT decoder doesn't need a backend.

A regex tester doesn't need a backend.

A hash generator doesn't need a backend.

A developer should not have to upload sensitive data to a server simply because the tool they need happens to be hosted on the web.

---

# 🔐 Security Principles

Security-sensitive developer tooling deserves a different threat model.

We design around:

### Least data movement

Don't transmit data that doesn't need to leave the machine.

### Least privilege

Services and CI jobs should receive only the permissions they actually require.

### Secure defaults

The easiest workflow should also be a safe workflow.

### Transparent processing

Developers should be able to understand where their data goes and why.

### Auditable software

Open source makes security review possible.

### Dependency awareness

Third-party dependencies and build infrastructure are treated as part of the application's attack surface.

---

# 🚀 Operations & Engineering

We treat MyDevTools as an engineering platform, not just a collection of utilities.

## CI/CD

Our engineering workflow emphasizes:

```text
Commit
  │
  ▼
Pull Request
  │
  ├── Lint
  ├── Type checks
  ├── Tests
  ├── Security checks
  ├── Build
  │
  ▼
Review
  │
  ▼
Deploy
```

Security and dependency checks are designed to fail closed where possible rather than silently producing false-clean results.

## Containerization

Services are containerized with **Docker** to keep development, testing, and deployment environments reproducible.

## Infrastructure

Cloud infrastructure is used for services that actually require infrastructure. Local developer utilities should not depend on the cloud merely to perform a local transformation.

## Observability

Production services are designed around operational visibility, including:

- structured application logs
- service health checks
- failure visibility
- resource monitoring
- deployment verification

---

# 🧩 Repository Philosophy

Our repositories are organized around clear responsibilities rather than one giant application.

Typical boundaries include:

```text
mydevtools/
│
├── frontend/
│   ├── web application
│   ├── UI components
│   └── developer workflows
│
├── backend/
│   ├── APIs
│   ├── authentication
│   ├── application services
│   └── data access
│
├── tools/
│   ├── formatters
│   ├── generators
│   ├── security utilities
│   ├── API utilities
│   └── developer helpers
│
├── infrastructure/
│   ├── Docker
│   ├── deployment
│   └── CI/CD
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
3. Independent where possible
4. Reusable
5. Fast
6. Privacy-preserving
7. Consistent with the rest of the platform

We prefer composable primitives over tightly coupled features.

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
- 🐳 Infrastructure
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
# run the development environment
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
| Many browser tabs | One workspace |
| Separate utilities | Unified toolkit |
| Copy/paste between sites | Connected workflows |
| Cloud tool for every small task | Local processing where possible |
| Scattered developer utilities | One developer environment |
| Closed tooling | Open source |
| SaaS dependency | Offline-first |
| Tool switching | Workflow continuity |

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
  Built for developers who want fewer tabs, faster workflows, and more control.
</p>

<p align="center">
  <sub>Open source · Local-first · Offline · Developer-first</sub>
</p>

