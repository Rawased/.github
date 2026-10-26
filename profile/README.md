<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-dark-1600x500.png?v=k3-v4">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-light-1600x500.png?v=k3-v4">
    <img alt="Rawased · رواصد | Price feeds miss the footnotes. Rawased reads them." src="https://raw.githubusercontent.com/Rawased/.github/main/brand/rawased-banner-v3-bw-dark-1600x500.png?v=k3-v4" width="100%">
  </picture>

  <br/>

  <h1>Rawased · رواصد</h1>
  <p><b>Price feeds miss the footnotes. Rawased reads them.</b><br/>
  <b>«شاشات الأسعار تغفل الإيضاحات. رواصد تقرأها من المصدر.»</b></p>

  <p>
    Saudi Exchange (<code>TASI</code> &amp; <code>Nomu</code>) and US <code>SEC EDGAR</code> filing intelligence.<br/>
    Audited footnotes set beside the price feed · Zakat &amp; Islamic debt unbundled · Read-only <code>MCP</code> connectors.
  </p>

  <p>
    <a href="https://rawased.com"><img src="https://img.shields.io/badge/Overview-rawased.com-0B0F14?style=flat-square&logoColor=white" alt="Overview"/></a>
    <a href="https://app.rawased.com"><img src="https://img.shields.io/badge/Open_Terminal-app.rawased.com-10B981?style=flat-square&logoColor=white" alt="Open Terminal"/></a>
    <a href="https://rawased.com/bridges"><img src="https://img.shields.io/badge/Methodology-The_5_Bridges-1E293B?style=flat-square" alt="The 5 Bridges"/></a>
    <a href="https://rawased.com/pricing"><img src="https://img.shields.io/badge/Founding_Member-79_SAR%2Fmo-111827?style=flat-square" alt="Pricing"/></a>
    <a href="https://rawased.com/developers"><img src="https://img.shields.io/badge/Rawased_Connect-OAuth_2.1_MCP-0F172A?style=flat-square" alt="Rawased Connect"/></a>
    <a href="mailto:support@rawased.com"><img src="https://img.shields.io/badge/Support-support%40rawased.com-1F2937?style=flat-square" alt="Support"/></a>
  </p>
</div>

---

## Why Rawased Exists

A quote screen can drop a line the filing still has. Standard market feeds compress restatements, merge floating-rate Islamic facilities with conventional debt, and apply flat tax assumptions to Saudi companies that pay Zakat.

Rawased starts with the primary filing: Saudi Exchange (`Tadawul` and `Nomu`) financial statements and notes, alongside US `SEC EDGAR` (`10-K`, `10-Q`, `20-F`) reports. When the quote feed and the audited note differ, the note stays on the screen. When a figure is not stated in the filing, it stays blank rather than guessed.

### Illustrative Filing vs. Feed Reconciliation (`2223.SR · Luberef`)

| Source Surface | Period & Line Item | Reported Figure | Reconciliation Note |
| :--- | :--- | :---: | :--- |
| **Standard Quote Screen** | Q3 Net Income (`Delayed 15 min`) | `212.00 SAR m` | Omits footnote restatement line |
| **Note 14, Audited Tadawul Filing** | Q3 Net Income (Audited PDF Note) | **`238.45 SAR m`** | **`26.45M SAR` (`1,109.2 bps`) sits in Note 14, not on the feed** |

> *Illustrative sample shown on [rawased.com](https://rawased.com). Saudi market quotes displayed in the product are delayed 15 minutes and labelled delayed (`Data provided by SAHMK`).*

---

## How It Works · The Five Accounting Bridges

Rawased structures every company view around five transparent bridges documented at **[rawased.com/bridges](https://rawased.com/bridges)**:

| Bridge | Name | What Rawased Keeps Separate |
| :---: | :--- | :--- |
| **01** | **The Audited Note Beside the Feed** | Sets the audited Tadawul PDF or SEC XBRL footnote next to the 15-minute delayed price feed so restatements and reclassifications stay visible. |
| **02** | **Zakat, Not a Flat Corporate Tax** | Separates the Saudi `ZATCA` Zakat base (`2.5%` lunar / `2.577%` Gregorian) from foreign-owner corporate income tax instead of applying a blended western tax rate. |
| **03** | **Debt, Leases & End-of-Service Apart** | Unbundles floating-rate **Murabaha**, **Sukuk**, conventional bank debt, **`IFRS 16` lease liabilities**, and Saudi Labor Law **`IAS 19` end-of-service benefits (`EOSB`)**. |
| **04** | **From Reported Profit to Cash** | Traces operating cash flow after Zakat paid, working-capital swings, capital expenditure, and Murabaha or Sukuk financing costs. |
| **05** | **Your AI, Your Key (`Rawased Connect`)** | Connects your own Claude, ChatGPT, Grok, or Cursor workspace to Rawased's read-only `OAuth 2.1 + PKCE` Model Context Protocol (`/mcp`) endpoint and CLI. |

---

## Security Posture, Data Governance & Non-Advisory Boundaries

Rawased is engineered from the ground up around strict regulatory, security, and data-attribution boundaries:

1. **Non-Advisory Safe-Harbor (CMA Boundary):**
   - Rawased provides financial information and filing arithmetic only, never investment advice. Rawased is not a Capital Market Authority (`CMA`) licensed adviser.
   - All product surfaces, terminal answers, and API/MCP outputs enforce non-advisory rules in English and Arabic and refuse buy, sell, hold, or target-price recommendations.
2. **Read-Only `OAuth 2.1 + S256 PKCE` MCP Architecture (`/mcp`):**
   - External AI assistants connect via short-lived authorization codes, `S256` PKCE verification, and scoped, revocable `rws_mcp_` bearer tokens.
   - Every MCP tool is strictly read-only (`readOnlyHint: true`, `destructiveHint: false`, `openWorldHint: false`).
   - Personal watchlist reads require explicit Saudi `PDPL` consent (`pdpl_consent_at`), and verbatim filing excerpts are isolated inside `quoted` blocks to defend against indirect prompt injection.
3. **Zero-Knowledge Key Isolation:**
   - Rawased never stores, logs, or proxies member AI API keys. Your LLM credentials remain on your own device.
4. **Exchange Attribution & 15-Minute Delay Discipline:**
   - Saudi Exchange (`TASI` and `Nomu`) price quotes are served from a shared 15-minute delayed cache (`Delayed 15 min · Data provided by SAHMK`).
   - Primary filing and macro series carry explicit `as_of` timestamps and source citations (`Saudi Exchange`, `SEC EDGAR`, `SAMA`, `GASTAT`, `FRED`).
5. **Application, Session & Payment Hardening:**
   - **Authentication:** `PBKDF2-HMAC-SHA256` (`200,000` iterations) password hashing, `HttpOnly; SameSite=Strict; Secure` session cookies, device/IP session audit trails, and one-click session revocation.
   - **Edge Controls:** Strict Content-Security-Policy (`CSP`), `X-Frame-Options`, `Strict-Transport-Security`, OWASP input validation, and per-route rate limiting.
   - **Billing Verification:** Moyasar payment callbacks verified via constant-time `HMAC-SHA256` signature checks (`SAR`, 15% VAT inclusive).

---

## Organization Repositories

| Repository | Role | Visibility | Surface |
| :--- | :--- | :---: | :--- |
| **[`Rawased/rawased`](https://github.com/Rawased/rawased)** | Core web application, bilingual paper terminal, filing reconciliation engine, and `OAuth 2.1` `/mcp` server | `Private` | [rawased.com](https://rawased.com) · [app.rawased.com](https://app.rawased.com) |
| **[`Rawased/rawased-python`](https://github.com/Rawased/rawased-python)** | Official Python client & CLI for Saudi Exchange (`TASI` & `Nomu`) and US SEC filing reconciliation | `Private` | [rawased.com/developers](https://rawased.com/developers) |
| **[`Rawased/rawased-mcp`](https://github.com/Rawased/rawased-mcp)** | Read-only Model Context Protocol (`MCP`) connector & tool definitions for Claude, ChatGPT, Grok, and Cursor | `Private` | [rawased.com/developers](https://rawased.com/developers) |
| **[`Rawased/rawased-quant-specs`](https://github.com/Rawased/rawased-quant-specs)** | Quantitative & accounting specifications: `ZATCA` Zakat (`2.577%`), Islamic debt unbundling, `IAS 19` EOSB, and cash bridges | `Private` | [rawased.com/bridges](https://rawased.com/bridges) |
| **[`Rawased/.github`](https://github.com/Rawased/.github)** | Organization profile, `K3` brand identity assets, and public documentation | `Public` | [github.com/Rawased](https://github.com/Rawased) |

---

## Membership, Legal & Contact

- **Free Tier:** Delayed prices labelled delayed (`Delayed 15 min`), three company lookups a day, and five filing questions a day.
- **Founding Member:** **`79 SAR` a month** or **`790 SAR` a year** (15% VAT included). Locked while your subscription stays active (standard rate later: `99 SAR/month` or `990 SAR/year`).
- **Product & Policies:**
  - [Overview (`rawased.com`)](https://rawased.com) · [Open Terminal (`app.rawased.com`)](https://app.rawased.com) · [Pricing (`rawased.com/pricing`)](https://rawased.com/pricing) · [The 5 Bridges (`rawased.com/bridges`)](https://rawased.com/bridges)
  - [Terms & Conditions (`rawased.com/terms`)](https://rawased.com/terms) · [Privacy Policy (`rawased.com/privacy`)](https://rawased.com/privacy) · [Refund Policy (`rawased.com/refund-policy`)](https://rawased.com/refund-policy)
- **Contact:**
  - Subscriber & Account Support: [support@rawased.com](mailto:support@rawased.com)
  - General & Institutional Inquiries: [hi@rawased.com](mailto:hi@rawased.com)
  - Location: Riyadh, Kingdom of Saudi Arabia

<div align="center">
  <sub>Information only. Rawased is not investment advice and is not a CMA-licensed adviser. Saudi quotes shown are delayed 15 minutes (Data provided by SAHMK).<br/>
  © 2026 Waleed Alogayel (Rawased · رواصد). All rights reserved.</sub>
</div>
