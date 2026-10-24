<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-dark-1600x500.png">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-light-1600x500.png">
    <img alt="Rawased | رواصد - Saudi & US Financial Filing & Quant Terminal" src="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-dark-1600x500.png" width="100%">
  </picture>

  <br/>

  <h2>Rawased (رواصد) · Price feeds miss the footnotes. Rawased reads them.</h2>

  <p>
    Pull up Luberef (<code>2223.SR</code>) on a standard market feed and Q3 net income reads SAR 212.00M. Open Note 14 of the audited Tadawul filing and the real figure is SAR 238.45M, because the feed dropped a quarterly restatement. Rawased checks every Saudi and US line item against the audited filing first, splits Murabaha and Sukuk from leases and End-of-Service Benefits, and calculates Zakat and cash flow from the actual notes.
  </p>

  <p>
    <a href="https://rawased.com"><img src="https://img.shields.io/badge/Company_%26_Docs-rawased.com-09090B?style=for-the-badge&logoColor=white" alt="Company Site"/></a>
    <a href="https://app.rawased.com"><img src="https://img.shields.io/badge/Live_Terminal-app.rawased.com-10B981?style=for-the-badge&logoColor=white" alt="Live Terminal"/></a>
    <a href="https://rawased.com/bridges"><img src="https://img.shields.io/badge/The_5_Bridges-rawased.com%2Fbridges-111827?style=for-the-badge" alt="5 Bridges"/></a>
    <a href="https://rawased.com/brand-lab"><img src="https://img.shields.io/badge/Brand_&_Logo_Lab-rawased.com%2Fbrand--lab-1E293B?style=for-the-badge" alt="Brand Lab"/></a>
  </p>
</div>

---

### 1. How Rawased Goes Deeper Than Standard Saudi Market APIs

While basic Saudi market-data feeds stop at single-market quotes and unverified quarterly ratios, **Rawased** (رواصد) builds the full institutional underwriting and reconciliation stack across **Saudi Exchange (`TASI` & `Nomu`)**, **US Equities (`NYSE` / `Nasdaq` / `SEC EDGAR`)**, and **Sovereign Yield Curves (`SAIBOR`, `SOFR`, `US Treasury`)**:

| Architectural Layer | Standard Saudi Feed Alone | Rawased (رواصد) Platform + Open SDKs |
| :--- | :--- | :--- |
| **1. Cross-Border Market Scope** | Saudi Equities (`TASI` & `Nomu`) only | **Saudi (`TASI`/`Nomu`) + US (`NYSE`/`Nasdaq`/`SEC EDGAR` 10-K/10-Q) + `SAIBOR`/`SOFR` Curves** |
| **2. Financial Statement Audit (`DISAGREES` Guard)** | Single-source scraped/vendor tables (prone to Q2/Q3 YTD vs. discrete quarter errors) | **Dual-Source Reconciliation against Audited Tadawul PDF & SEC XBRL Notes (`DISAGREES` Flag)** |
| **3. Islamic & Conventional Debt Stack (`CAST`)** | Aggregate Total Debt line only | **Full Seniority Stack: Murabaha, Sukuk, Wakala, Senior Term Loans & IFRS 16 / ASC 842 Leases** |
| **4. Maturity Wall & Dividend Durability (`DDIS`)** | Historical dividend list | **10-Year Principal Repayment Wall + WAM + 24M Refinancing Cliff % + FCFE Dividend Coverage** |
| **5. Saudi Corporate Zakat vs. Income Tax** | Not modeled | **ZATCA Zakat Base (`2.5%` Hijri / `2.577%` Greg.) + Mixed Foreign Tax & Zakat-Adjusted ROIC/EVA** |
| **6. Interactive Valuation Sandbox** | Static opaque fair-value number | **Auditable 3-Statement FCFF/FCFE DCF + Analytical Reverse DCF Implied Growth + Residual Income** |
| **7. Developer & AI Agent Ecosystem** | Basic quote REST/MCP | **`rawased-python` SDK/CLI + 18-Tool `rawased-mcp` (Claude/Cursor/Gemini) + Local AI CLI Bridge** |

---

### 2. Official Repository Suite (`https://github.com/Rawased`)

| Repository | Visibility | Description |
| :--- | :--- | :--- |
| [**`Rawased/rawased`**](https://github.com/Rawased/rawased) | Private (Core Platform) | Full 53-file commercial terminal (`app.rawased.com`), multi-page bilingual company & developer platform (`rawased.com`), OWASP/PDPL security gate, and billing/promo engine. |
| [**`Rawased/rawased-python`**](https://github.com/Rawased/rawased-python) | **Public (SDK & CLI)** | Official Python SDK (`RawasedClient`) and CLI (`rawased quote / cast / ddis / zakat / dcf`) for Saudi & US filings and deterministic quantitative models. |
| [**`Rawased/rawased-mcp`**](https://github.com/Rawased/rawased-mcp) | **Public (MCP & Gemini)** | Official **18-Tool Model Context Protocol (MCP) Server** & **Gemini CLI Extension** for Claude Code, Claude Desktop, Cursor, ChatGPT, and Gemini CLI. |
| [**`Rawased/rawased-quant-specs`**](https://github.com/Rawased/rawased-quant-specs) | **Public (Open Specs)** | Open mathematical specifications and JSON schemas for Primary Filing Reconciliation (`DISAGREES`), `CAST`, `DDIS`, ZATCA Zakat Bridges, and Reverse DCF. |
| [**`Rawased/.github`**](https://github.com/Rawased/.github) | **Public (Brand & Org)** | Official Rawased geometric vector brand system (`1x1`, `2x2`, `4x4` rotated tile matrices across 6 monochrome and institutional palettes). |

---

### 3. Quick Start for Developers & AI Agents

```bash
# 1. Install Official Python SDK & CLI + 18-Tool MCP Server
pip install git+https://github.com/Rawased/rawased-python.git
pip install git+https://github.com/Rawased/rawased-mcp.git

# 2. Run Deterministic DCF & Reverse DCF from the Terminal
rawased dcf 2223.SR --wacc 0.089 --growth 0.055 --tg 0.025
rawased cast 2222.SR
rawased zakat 2223.SR --wacc 0.089

# 3. Connect Claude Code, Cursor, or Gemini CLI
claude mcp add rawased -- rawased-mcp
gemini extensions install https://github.com/Rawased/rawased-mcp
```

---

### 4. Platform Navigation (`rawased.com` & `app.rawased.com`)

- **Company & Product Overview:** `https://rawased.com` (`/en` & `/ar`)
- **Live Interactive Terminal:** `https://app.rawased.com`
- **Developer Portal & SDKs:** `https://rawased.com/developers`
- **API & Quant Documentation:** `https://rawased.com/developers/docs` (Machine-readable: `https://rawased.com/api-docs.md`)
- **Mathematical Methodology (`CAST` / `DDIS` / `Zakat`):** `https://rawased.com/methodology`
- **Enterprise & University Finance Labs:** `https://rawased.com/enterprise`
- **Quantitative Research Insights:** `https://rawased.com/insights`
- **Legal, CMA Art. 31 Safe Harbor & PDPL Policy:** `https://rawased.com/legal`

---

<div align="center">
  <sub>© 2026 Rawased (رواصد) · Riyadh, Kingdom of Saudi Arabia · Founders: Waleed Alogayel (<a href="mailto:waleed@rawased.com">waleed@rawased.com</a>) &amp; Abdulmohsen Alhassan (<a href="mailto:abdulmohsen@rawased.com">abdulmohsen@rawased.com</a>) · Support: <a href="mailto:help@rawased.com">help@rawased.com</a></sub>
</div>
