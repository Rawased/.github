<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-dark-1600x500.png?v=k3-v2">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-light-1600x500.png?v=k3-v2">
    <img alt="Rawased | رواصد - Price feeds miss the footnotes. Rawased reads them." src="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-dark-1600x500.png?v=k3-v2" width="100%">
  </picture>

  <br/>

  <h2>Rawased (رواصد) · Price feeds miss the footnotes. Rawased reads them.</h2>
  <p><b>«شاشات الأسعار تغفل الإيضاحات. رواصد تقرأها من المصدر.»</b></p>

  <p>
    A quote screen can drop a line the filing still has. Rawased keeps the audited note next to the feed across Saudi Exchange (<code>TASI</code> &amp; <code>Nomu</code>) and US SEC filings, splits Murabaha, sukuk, leases, end-of-service benefits, and Zakat apart, and leaves missing figures blank rather than guessing.
  </p>

  <p>
    <a href="https://rawased.com"><img src="https://img.shields.io/badge/Company_Site-rawased.com-0B0F14?style=for-the-badge&logoColor=white" alt="Company Site"/></a>
    <a href="https://app.rawased.com"><img src="https://img.shields.io/badge/Terminal-app.rawased.com-10B981?style=for-the-badge&logoColor=white" alt="Terminal"/></a>
    <a href="https://rawased.com/pricing"><img src="https://img.shields.io/badge/Founding_Member-79_SAR_%2F_mo-111827?style=for-the-badge" alt="Pricing"/></a>
    <a href="https://rawased.com/bridges"><img src="https://img.shields.io/badge/The_5_Bridges-rawased.com%2Fbridges-1E293B?style=for-the-badge" alt="5 Bridges"/></a>
  </p>
</div>

---

### 1. Approved `K3` Brand Identity (Continuous Unbroken Ribbon + 45° Breakout Facet)

| `K3` Monochrome Dark (`1024px`) | `K3` Sovereign Slate + `#10B981` Facet | `K3` Frameless `4x4` Rotational Matrix | `K3` Midnight Indigo `4x4` Matrix |
| :---: | :---: | :---: | :---: |
| <img src="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-mark-bw-dark-1024.png?v=k3-v2" width="136" alt="K3 Monochrome Dark"/> | <img src="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-mark-sovereign-slate-1024.png?v=k3-v2" width="136" alt="K3 Sovereign Slate"/> | <img src="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-pattern-4x4-bw-dark-1200.png?v=k3-v2" width="136" alt="K3 4x4 B&W Dark"/> | <img src="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-pattern-4x4-midnight-indigo-1200.png?v=k3-v2" width="136" alt="K3 4x4 Midnight Indigo"/> |
| [`rawased-mark-bw-dark.svg`](https://github.com/Rawased/.github/blob/main/brand/rawased-mark-bw-dark.svg) | [`rawased-mark-sovereign-slate.svg`](https://github.com/Rawased/.github/blob/main/brand/rawased-mark-sovereign-slate.svg) | [`rawased-pattern-4x4-bw-dark.svg`](https://github.com/Rawased/.github/blob/main/brand/rawased-pattern-4x4-bw-dark.svg) | [`rawased-pattern-4x4-midnight-indigo.svg`](https://github.com/Rawased/.github/blob/main/brand/rawased-pattern-4x4-midnight-indigo.svg) |

---

### 2. How Rawased Works & The 5 Bridges (`https://rawased.com/bridges`)

1. **Open the filing (`افتح القوائم`):** Start with the Saudi Exchange document (Tadawul filings, footnotes, and disclosures) or SEC report.
2. **Set the note beside the feed (`ضع الإيضاح بجانب السعر`):** When the delayed quote and the audited note differ, the note stays on the screen. A missing figure stays blank.
3. **Split what the note splits (`افصل ما يفصله الإيضاح`):** Murabaha, sukuk, ordinary debt, leases, end-of-service benefits, and the Zakat base stay apart.

| Bridge | Title | What It Shows |
| :--- | :--- | :--- |
| **Bridge 01** | **The audited note, next to the feed** | Keeps the delayed Saudi price labelled delayed (`Delayed 15 min`), and shows the audited note whenever feed and note disagree. |
| **Bridge 02** | **Zakat, not a flat company tax** | Separates the Saudi Zakat base from foreign-owner income tax rather than applying a flat corporate tax rate. |
| **Bridge 03** | **Debt, leases, and end-of-service** | Lists floating-rate Murabaha, sukuk, ordinary debt, `IFRS 16` leases, and the end-of-service benefit apart. |
| **Bridge 04** | **From profit to cash** | Shows how profit becomes cash after Zakat, tax, working capital, capital spending, and Murabaha or sukuk payments. |
| **Bridge 05** | **Your questions stay with the tools you already use** | Connects a subscriber's account to their own computer or AI tool (`Connector`, `Connect CLI`, or `Plugin`) under strict read-only, non-advisory rules. |

---

### 3. Security Measures, Data Governance & Non-Advisory Response Architecture

- **Non-Advisory Response Guard (`advice_guard.py`):**
  - Every response, prompt pack, and connector tool enforces `"Information, not investment advice."` (`معلومات، وليست نصيحة استثمارية.`) and refuses buy, sell, hold, price-target, position-sizing, and portfolio recommendations in both English and Arabic.
- **Read-Only Connector & OAuth 2.1 with PKCE (`oauth_flow.py`, `mcp_http.py`, `mcp_tools.py`):**
  - Streamable HTTP JSON-RPC endpoint (`/mcp`) protected by per-member revocable OAuth 2.1 `S256` PKCE tokens and an explicit PDPL consent screen before watchlist access.
  - Exposes 6 read-only tools (`stock_brief`, `disclosures`, `watchlist`, `alerts`, `screen`, `explain_filing`). There is no order tool. Every payload carries `source_links`, `as_of`, and `Delayed 15 min`, and untrusted filing text stays isolated inside `quoted`.
- **Zero Key Exposure & Local Connect CLI (`rawased-connect.py`, `rawased-tools.py`, `us_price.py`):**
  - Members never paste third-party data or AI keys into `rawased.com`. Optional AI keys and optional US price keys stay on the member's own computer.
- **Strict Member Data & News Isolation (`data_sources.py`, `news_policy.py`):**
  - Member Saudi quotes use a shared 15-minute delayed cache (`Data provided by SAHMK.`). Owner-only feeds are never called on member routes. Member news permits only five verified wires (`BBC News`, `GDELT`, `Federal Reserve`, `ECB`, `EDGAR`) as headline + link.
- **OWASP Edge Gate, Auth & Founding Member Price Lock (`rawased_auth.py`, `payments.py`, `platform_db.py`):**
  - Blocks SQLi, XSS, command injection, path traversal, oversized URIs (`414`), and auth rate-limit floods (`429`). Uses `PBKDF2-HMAC-SHA256` (`200,000` iterations), `HttpOnly; SameSite=Strict; Secure` cookies, CSRF tokens, `frame-ancestors 'self'` CSP, and peppered SHA-256 single-use invite codes.
  - **Pricing (`/pricing`):** Free plan (`3 company lookups/day`, `5 AI questions/day`) and Founding Member plan (`79 SAR/month` or `790 SAR/year` locked while subscribed; standard price later `99 SAR/month` or `990 SAR/year`, 15% VAT included).

---

### 4. Official Repository Suite (`https://github.com/Rawased`)

| Repository | Visibility | Description |
| :--- | :--- | :--- |
| [**`Rawased/rawased`**](https://github.com/Rawased/rawased) | Private (Core Platform) | Full bilingual reading product & terminal (`rawased.com` / `app.rawased.com`), phone-first `Geist` + `IBM Plex Sans Arabic` UI, OAuth 2.1 PKCE read-only connector, `advice_guard` non-advisory engine, D1/SQLite migrations, and Playwright E2E CI suite. |
| [**`Rawased/rawased-python`**](https://github.com/Rawased/rawased-python) | **Public (SDK & CLI)** | Python client and CLI for reading Saudi Exchange (`TASI` / `Nomu`) and US SEC filing notes, Zakat splits, and debt/lease structures. |
| [**`Rawased/rawased-mcp`**](https://github.com/Rawased/rawased-mcp) | **Public (MCP & Connect)** | Read-only Model Context Protocol (MCP) connector & plugin definitions (`stock_brief`, `disclosures`, `watchlist`, `alerts`, `screen`, `explain_filing`) with non-advisory guardrails. |
| [**`Rawased/rawased-quant-specs`**](https://github.com/Rawased/rawased-quant-specs) | **Public (Open Specs)** | Open specifications and JSON schemas for filing-to-feed note comparison, ZATCA Zakat vs. foreign tax splits, Murabaha/sukuk/lease/EOSB separation, and cash-flow bridges. |
| [**`Rawased/.github`**](https://github.com/Rawased/.github) | **Public (Brand & Org)** | Official Rawased `K3` geometric vector brand system (`1024px` marks, frameless `1200x1200` `4x4` rotated tile matrices, and `1600x500` banners across 6 palettes). |

---

### 5. Platform Links & Contacts

- **Company Overview:** [https://rawased.com](https://rawased.com) (`/en` & `/ar`)
- **Terminal:** [https://app.rawased.com](https://app.rawased.com)
- **The 5 Bridges:** [https://rawased.com/bridges](https://rawased.com/bridges)
- **Pricing (Free & Founding 79 SAR/mo):** [https://rawased.com/pricing](https://rawased.com/pricing)
- **Terms, Privacy & Refund Policy:** [https://rawased.com/terms](https://rawased.com/terms) · [https://rawased.com/privacy](https://rawased.com/privacy) · [https://rawased.com/refund-policy](https://rawased.com/refund-policy)
- **Contact:** [support@rawased.com](mailto:support@rawased.com) (account support) · [hi@rawased.com](mailto:hi@rawased.com) (general inquiries)

---

<div align="center">
  <sub>© 2026 Rawased (رواصد) · Riyadh, Kingdom of Saudi Arabia · Information, not investment advice. · Support: <a href="mailto:support@rawased.com">support@rawased.com</a> · General: <a href="mailto:hi@rawased.com">hi@rawased.com</a></sub>
</div>
