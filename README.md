# Awesome-Public-API-Marketplace-Directory

# Awesome Public API Marketplace & Directory

> A curated list of top Public API Marketplace and Directory platforms — both SaaS/Hosted commercial discovery hubs and open-source alternatives for finding, publishing, and consuming public APIs.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Postman API Network](#postman-api-network)
  - [RapidAPI Hub](#rapidapi-hub)
  - [APIs.guru](#apisguru)
  - [Zapier App Directory](#zapier-app-directory)
- [Open-Source Software](#-open-source-software)
  - [APIs.guru OpenAPI Directory](#apisguru-openapi-directory)
  - [Public APIs (public-apis)](#public-apis-public-apis)
  - [DopeForge](#dopeforge)
  - [Lorapok Atlas](#lorapok-atlas)
  - [API Hub](#api-hub)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Public API Marketplace and Directory platforms. These are not open-source but are included as reference points for feature comparison.

### Postman API Network
**Type:** API discovery integrated with Postman workspaces
Postman API Network is the public directory within the Postman platform, allowing developers to discover and explore APIs published by organizations. Publishing requires a public workspace with a reference collection imported from an OpenAPI file and an overview collection [citation:2][citation:8]. It is the natural discovery layer for teams already using Postman for API development, with no listing fee mentioned in publisher documentation [citation:2]. The network surfaces APIs within Postman's client and through organic search, making it a strong first channel for API distribution [citation:2].

### RapidAPI Hub
**Type:** Commercial API marketplace with billing and key management
RapidAPI Hub is the largest commercial API marketplace, connecting developers with thousands of APIs and providing a unified billing layer, API key management, and usage analytics. Listing is free, but RapidAPI takes a **flat 25% marketplace fee on all payments** made through the Hub [citation:2][citation:8]. Free plans are capped at **1,000 requests per hour and 500,000 per month** [citation:2][citation:8]. New APIs start private until explicitly made public, and payouts are processed exclusively via PayPal [citation:8]. It is the primary commercial reference for API monetization and discovery.

### APIs.guru
**Type:** Community-driven machine-readable API definition directory
APIs.guru provides a searchable directory of public API definitions in OpenAPI format, described as a "Wikipedia for Web APIs." It hosts **2,529 API descriptions** covering **108,837 endpoints**, with weekly updates and automatic conversion to OpenAPI 3.0. The key requirement for listing is a **stable URL to a machine-readable definition** (OpenAPI, RAML, or API Blueprint)—no definition means no listing [citation:2][citation:8]. All data is accessible via a REST API, making it a foundational resource for code generation and tooling.

### Zapier App Directory
**Type:** Integration marketplace for no-code automation
Zapier's App Directory lists integrations that connect 7,000+ apps with trigger-action workflows. It is a discovery surface for no-code automation rather than an API directory per se, but it is where many developers and business users search for connectivity between services. Integrately and Make offer similar catalogs with prebuilt automations [citation:5].

---

## 🟩 Open-Source Software

Self-hosted, community-driven Public API Marketplace and Directory tools. The open-source ecosystem spans **machine-readable definition repositories**, **curated public API lists**, **AI-agent-accessible registries**, and **self-hosted API portals**.

### APIs.guru OpenAPI Directory
**Stack:** JavaScript / YAML / JSON | **License:** CC0-1.0 (data)
The **openapi-directory** repository is the open-source data layer behind APIs.guru, containing a comprehensive collection of REST API definitions in OpenAPI 2.0/3.x format. It has **4,533 GitHub stars** and **739 forks**, making it the most-starred open-source API directory [citation:2]. The data is community-driven—anyone can add or change an API—with automated weekly updates from original sources and validation before commit. It is machine-readable and accessible through a REST API, and is used by HTTP Toolkit, Apideck, Microsoft Kiota, and others. It is a **data repository** rather than a web application.

**Best for:** Developers needing a comprehensive, machine-readable collection of OpenAPI definitions for code generation, testing, and API discovery.

### Public APIs (public-apis)
**Stack:** Markdown / GitHub | **License:** Open Source (MIT)
The **public-apis** repository is a collective list of free APIs, organized by category (Animals, Anime, Blockchain, Finance, Health, Music, News, Sports, Test Data, Text Analysis, and more). It has **474k GitHub stars**, making it one of the most popular open-source API directories [citation:14]. The format lists API name, description, authentication type (apiKey, OAuth, or none), HTTPS support, and CORS status. **Important:** It is a curated list with strict submission rules—marketing pull requests are rejected, and listings require free access or a free tier, HTTPS, and auth/CORS facts [citation:8]. It is not a machine-readable directory or interactive portal.

**Best for:** Developers wanting a curated, human-readable list of free APIs for side projects and prototyping, particularly for discovering APIs with no authentication requirements.

### DopeForge
**Stack:** Python / MCP | **License:** Open Source
DopeForge is an open-source registry built specifically for AI agents, merging the biggest developer catalogs on GitHub into one searchable database of **6,623 entries** [citation:14]. Key characteristics:
- **Multi-source aggregation**: combines public-apis (1,721 entries), awesome-mcp-servers (3,482), free-for-dev (1,304), and awesome-llm-apps (116) into one registry covering **838k+ combined stars** of curated markdown [citation:14]
- **Callable blueprints**: hand-verified specs (base URL, endpoints, params) that make APIs invocable right now, with `forge try` for terminal calls and `call_api` for agents [citation:14]
- **Alive verification**: `forge check` calls every blueprinted API for real, with a nightly CI run; dead APIs (expired TLS, no HTTPS, deprecation stubs) are excluded [citation:14]
- **MCP server**: three tools (`discover`, `inspect`, `call_api`) safe by construction—GET-only, no-auth-only, HTTPS-only, with bounded responses and no keys to leak [citation:14]

It ships a registry snapshot inside the package, so it works offline instantly [citation:14].

**Best for:** Developers using AI coding agents (Claude, Cursor) wanting a live, verified registry of public APIs that agents can discover and call directly without per-API setup.

### Lorapok Atlas
**Stack:** JavaScript / Browser Extension | **License:** MIT
Lorapok Atlas is a browser extension that lets you browse, search, and **live-test 2,100+ free open-source APIs** directly in Firefox (and similar browsers) [citation:3]. Key features:
- **2,100+ curated APIs** across 34 categories (AI & ML, Developer Tools, Weather, Crypto, Maps, Music, Health, Space, Movies, Food, Privacy & Anonymity, and more) [citation:3]
- **Live HTTP testing** with automatic CORS proxy fallback (corsproxy.io → allorigins.win) [citation:3]
- **Code snippets** in JavaScript, Python, and cURL with one-click copy [citation:3]
- **Filter by auth type**: Free / API Key / OAuth [citation:3]
- **No account required**, no data collected, 100% local [citation:3]

The data is bundled as a static Postman Collection v2.1 schema, and the source is plain, unminified JavaScript on GitHub [citation:3].

**Best for:** Developers wanting to discover and immediately test free APIs from within their browser, without switching to a separate web portal or signing up for an account.

### API Hub
**Stack:** TypeScript / Next.js / Docker | **License:** MIT
API Hub (dukex/api-hub) is a **simple OpenAPI discovery portal** for creating an elegant API portal from your OpenAPI specifications with minimal configuration. Features include a searchable and filterable list of APIs by name, team, and metadata; interactive Swagger UI documentation; **AI-powered summaries** using Google Gemini (requires `GEMINI_API_KEY`); and simple configuration via a `specs/apis.json` file listing OpenAPI URLs and names. Deploys via Docker with a single command.

**Best for:** Teams wanting a self-hosted, lightweight API portal for their internal or public OpenAPI specs, accepting a minimal configuration-driven approach.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Machine-Readable | Self-Hosted | Live Testing | AI/MCP | Best For |
|----------|---------|-------|------------------|-------------|--------------|--------|----------|
| **Postman API Network** | Proprietary | Cloud | (Postman format) | ❌ | (Via Postman) | ❌ | Postman ecosystem discovery |
| **RapidAPI Hub** | Proprietary | Cloud | (Proprietary) | ❌ | (Via Hub) | ❌ | Commercial API marketplace |
| **APIs.guru** | CC0 (data) | Cloud | ✅ OpenAPI | (Data) | ❌ | ❌ | Machine-readable directory |
| **APIs.guru OpenAPI Directory** | CC0-1.0 | YAML/JSON | ✅ OpenAPI | ✅ (Data) | ❌ | ❌ | 4,533-star OSS directory |
| **Public APIs** | MIT | Markdown | ❌ (Curated list) | ✅ | ❌ | ❌ | 474k-star free API discovery |
| **DopeForge** | Open Source | Python/MCP | ✅ Blueprints | ✅ (CLI/MCP) | ✅ `forge check` | ✅ MCP | AI-agent API discovery |
| **Lorapok Atlas** | MIT | JS Extension | (Postman Collection) | ✅ (Extension) | ✅ Live HTTP | ❌ | In-browser API testing |
| **API Hub** | MIT | TypeScript/Docker | ✅ OpenAPI | ✅ | ❌ | ✅ Gemini | Self-hosted OpenAPI portal |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Public API Marketplace or Directory tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for **API directories** is strongest for machine-readable OpenAPI collections and curated lists. **APIs.guru OpenAPI Directory** is the most established machine-readable directory with 4,533 stars and CC0 licensing , while **Public APIs** is the most accessible curated list with 474k stars for discovering free APIs . **DopeForge** is the most notable newer entrant, aggregating multiple catalogs into a live-verified registry specifically designed for AI agents via MCP . **Lorapok Atlas** uniquely enables in-browser live testing without account creation , and **API Hub** provides a self-hosted portal for your own OpenAPI specs.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
