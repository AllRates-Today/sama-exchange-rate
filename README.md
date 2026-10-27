# Saudi Central Bank (SAMA) Exchange Rates API — sama-exchange-rate

[![npm version](https://img.shields.io/npm/v/sama-exchange-rate.svg)](https://www.npmjs.com/package/sama-exchange-rate)
[![license](https://img.shields.io/npm/l/sama-exchange-rate.svg)](https://github.com/AllRates-Today/sama-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/sama-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![EUR/SAR today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fsama%3Fsource%3DEUR%26target%3DSAR&query=%24.rate&label=EUR%2FSAR%20published%20by%20Saudi%20Central%20Bank%20(SAMA)&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/sama/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fsama%3Fsource%3DEUR%26target%3DSAR&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/sama/)

**Official Saudi Central Bank (SAMA) (Saudi Arabia) daily exchange rates for Node.js and TypeScript. The published central bank rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers Saudi Central Bank (SAMA) itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official published rates** — Saudi Central Bank (SAMA)'s own table, with the publisher's own `rate_date` on every response
- 📅 **History back to 2009** — point-in-time tables and daily series for any past date
- 🔀 **Published vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number Saudi Central Bank (SAMA) itself published, fixed once printed and carrying the central bank's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## ⚡ Try it without a key

The latest Saudi Central Bank (SAMA) table is also served keyless, CORS-open and edge-cached, for evaluation, embeds and AI agents:

```bash
curl "https://allratestoday.com/api/open/central-bank/sama?source=EUR&target=SAR"
```

```js
const r = await fetch('https://allratestoday.com/api/open/central-bank/sama').then((x) => x.json());
console.log(r.rate_date, r.rates.length); // the central bank's latest published table, no key
```

The open endpoint serves the *latest* table only (JSON by default; add `?format=csv`, `xml` or `xlsx` for a file) and is free to use with a visible, followable link where the rates are shown: `<a href="https://allratestoday.com">Exchange rates by AllRatesToday</a>` (terms: <https://allratestoday.com/terms/#attribution>). The client below uses the keyed API, which adds point-in-time tables and history; with a key the link is appreciated, not required.

## 📈 Latest published table

[![Latest Saudi Central Bank (SAMA) table](https://allratestoday.com/api/open/central-bank/sama/table.svg)](https://allratestoday.com/central-bank-rates-api/sama/)

The image is rendered live from the keyless endpoint above, so it follows the central bank's publications on npm and on GitHub alike without a new release. The same table as text is folded below for search and copy-paste: on GitHub [a daily Action](.github/workflows/daily-table.yml) refreshes it whenever the central bank publishes a new table; on npm it is as of the package's publish date.

<!-- daily-table:start -->
<details>
<summary>Table as text: published 2026-10-27 by Saudi Central Bank (SAMA) — 66 rates, first 60 shown. Updated 2026-10-27.</summary>

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| AED | SAR | reference | 1.02094 |
| AFN | SAR | reference | 0.05776 |
| ALL | SAR | reference | 0.04628 |
| ARS | SAR | reference | 0.00245 |
| AUD | SAR | reference | 2.63662 |
| BAM | SAR | reference | 2.14819 |
| BDT | SAR | reference | 0.03031 |
| BGN | SAR | reference | 2.14819 |
| BHD | SAR | reference | 9.94167 |
| BND | SAR | reference | 2.934 |
| BRL | SAR | reference | 0.74353 |
| CAD | SAR | reference | 2.68211 |
| CHF | SAR | reference | 4.54876 |
| CLP | SAR | reference | 0.00378 |
| CNY | SAR | reference | 0.56213 |
| COP | SAR | reference | 0.00119 |
| CUP | SAR | reference | 0.15625 |
| CZK | SAR | reference | 0.17258 |
| DJF | SAR | reference | 0.02109 |
| DKK | SAR | reference | 0.56213 |
| DZD | SAR | reference | 0.02781 |
| EGP | SAR | reference | 0.06781 |
| ETB | SAR | reference | 0.02305 |
| EUR | SAR | reference | 4.2015 |
| GBP | SAR | reference | 5.01956 |
| HKD | SAR | reference | 0.47819 |
| HUF | SAR | reference | 0.01146 |
| INR | SAR | reference | 0.03949 |
| ISK | SAR | reference | 0.0308 |
| JOD | SAR | reference | 5.28913 |
| JPY | SAR | reference | 0.02392 |
| KES | SAR | reference | 0.02887 |
| KRW | SAR | reference | 0.00283 |
| KWD | SAR | reference | 12.06563 |
| LKR | SAR | reference | 0.01128 |
| LYD | SAR | reference | 0.58537 |
| MAD | SAR | reference | 0.38216 |
| MMK | SAR | reference | 0.00178 |
| MUR | SAR | reference | 0.07951 |
| MXN | SAR | reference | 0.20092 |
| MYR | SAR | reference | 0.91788 |
| NGN | SAR | reference | 0.00278 |
| NOK | SAR | reference | 0.40182 |
| NZD | SAR | reference | 2.13731 |
| OMR | SAR | reference | 9.74025 |
| PHP | SAR | reference | 0.05894 |
| PKR | SAR | reference | 0.01355 |
| PLN | SAR | reference | 0.95493 |
| QAR | SAR | reference | 1.02993 |
| RON | SAR | reference | 0.78551 |
| RUB | SAR | reference | 0.04649 |
| SEK | SAR | reference | 0.37783 |
| SGD | SAR | reference | 2.93381 |
| SOS | SAR | reference | 0.00659 |
| THB | SAR | reference | 0.11104 |
| TJS | SAR | reference | 0.40725 |
| TND | SAR | reference | 1.24945 |
| TRY | SAR | reference | 0.07539 |
| TWD | SAR | reference | 0.11498 |
| TZS | SAR | reference | 0.00141 |

</details>

[Full table on the Saudi Central Bank (SAMA) rates page](https://allratestoday.com/central-bank-rates-api/sama/) · Source: [Official rates published by SAMA, served by AllRatesToday](https://allratestoday.com/central-bank-rates-api/sama/). Rates are as printed by the central bank; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 📦 Installation

```bash
npm install sama-exchange-rate
```

```bash
yarn add sama-exchange-rate
```

```bash
pnpm add sama-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/sama-exchange-rate`](https://www.npmjs.com/package/@allratestoday/sama-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'sama-exchange-rate';

const pair = await getRate('EUR', 'SAR', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official Saudi Central Bank (SAMA) rate, on the central bank's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest published table
- [Full published table](#full-published-table) — everything the central bank printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the central bank does not print directly are resolved from its table and flagged (see *Published vs derived rates* below).

```js
const pair = await getRate('EUR', 'SAR', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'sama',
  name: 'Saudi Central Bank (SAMA)',
  rate_date: '2026-10-27',   // Saudi Central Bank (SAMA)'s own publication date
  source: 'EUR',
  target: 'SAR',
  rate: 4.2015,
  rate_type: 'reference',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full published table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'sama-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'sama',
  name: 'Saudi Central Bank (SAMA)',
  rate_date: '2026-10-27',
  rates: [
    { "base": "EUR", "quote": "SAR", "type": "reference", "value": 4.2015 },
    // … the rest of the published table (66 currencies vs SAR)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 2009 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'sama-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'EUR', target: 'SAR' });
```

**Response:**

```javascript
{
  bank: 'sama',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'sama-exchange-rate';

const series = await getHistory(
  { source: 'EUR', target: 'SAR', from: '2026-01-01', to: '2026-10-27' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'sama',
  source: 'EUR',
  target: 'SAR',
  from: '2026-01-01',
  to: '2026-10-27',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-10-27', rate: 4.2015, rate_type: 'reference', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'EUR' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

Saudi Central Bank (SAMA) currently publishes rates covering **66 currencies** against the SAR (as of the latest table):

🇦🇪 `AED` · 🇦🇫 `AFN` · 🇦🇱 `ALL` · 🇦🇷 `ARS` · 🇦🇺 `AUD` · 🇧🇦 `BAM` · 🇧🇩 `BDT` · 🇧🇬 `BGN` · 🇧🇭 `BHD` · 🇧🇳 `BND` · 🇧🇷 `BRL` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇱 `CLP` · 🇨🇳 `CNY` · 🇨🇴 `COP` · 🇨🇺 `CUP` · 🇨🇿 `CZK` · 🇩🇯 `DJF` · 🇩🇰 `DKK` · 🇩🇿 `DZD` · 🇪🇬 `EGP` · 🇪🇹 `ETB` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇭🇰 `HKD` · 🇭🇺 `HUF` · 🇮🇳 `INR` · 🇮🇸 `ISK` · 🇯🇴 `JOD` · 🇯🇵 `JPY` · 🇰🇪 `KES` · 🇰🇷 `KRW` · 🇰🇼 `KWD` · 🇱🇰 `LKR` · 🇱🇾 `LYD` · 🇲🇦 `MAD` · 🇲🇲 `MMK` · 🇲🇺 `MUR` · 🇲🇽 `MXN` · 🇲🇾 `MYR` · 🇳🇬 `NGN` · 🇳🇴 `NOK` · 🇳🇿 `NZD` · 🇴🇲 `OMR` · 🇵🇭 `PHP` · 🇵🇰 `PKR` · 🇵🇱 `PLN` · 🇶🇦 `QAR` · 🇷🇴 `RON` · 🇷🇺 `RUB` · 🇸🇪 `SEK` · 🇸🇬 `SGD` · 🇸🇴 `SOS` · 🇹🇭 `THB` · 🇹🇯 `TJS` · 🇹🇳 `TND` · 🇹🇷 `TRY` · 🇹🇼 `TWD` · 🇹🇿 `TZS` · 🇺🇸 `USD` · `XAF` · `XDR` · `XOF` · 🇾🇪 `YER` · 🇿🇦 `ZAR`

## 🏛️ Source

The Saudi Central Bank (SAMA) publishes a riyal exchange-rate table every day — 60+ currencies, seven days a week — with the riyal itself pegged to the US dollar at 3.75 since 1986. This series comes straight from SAMA’s own exchange-rate page, with daily history from April 2021 and SAMA’s monthly period averages for 12 currencies back to 2009.

- Publisher's own page: [Exchange rates — sama.gov.sa](https://www.sama.gov.sa/en-US/Currency/FinExc/Pages/Currency.aspx) · [www.sama.gov.sa](https://www.sama.gov.sa)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [Saudi Central Bank (SAMA) rates page](https://allratestoday.com/central-bank-rates-api/sama/)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- Saudi Central Bank (SAMA) quotes **SAR per 1 unit of foreign currency** (e.g. `base: "USD", quote: "SAR"` means SAR per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- `rate_type` tells you which of the central bank's series a row belongs to (`reference` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official Saudi Central Bank (SAMA) rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/sama/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('sama')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate sama ...` command
- Evaluating? Agents can self-issue a trial key with no signup: `POST https://allratestoday.com/api/agent/keys` (send `Content-Type: application/json`) returns a 100-call key valid 7 days that covers the free-plan methods (latest table, pairs); dated tables and history need a [paid plan](https://allratestoday.com/pricing/). The MCP servers expose it as `request_trial_key`
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Published vs derived rates

If Saudi Central Bank (SAMA) does not print a pair directly, the API resolves it from the central bank's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The central bank printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via SAR from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('EUR', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by Saudi Central Bank (SAMA) |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'sama-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('sama-exchange-rate');

getRate('EUR', 'SAR', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the published table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the published table |
| `getLatestRates({ apiKey })` | Free | The central bank's full latest published table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 2009 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same published tables are mirrored daily as open data:

- Hugging Face: [AllRatesToday/central-bank-exchange-rates](https://huggingface.co/datasets/AllRatesToday/central-bank-exchange-rates) — one CSV per institution (`rates/sama.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- Raw JSON on GitHub: `https://raw.githubusercontent.com/AllRates-Today/central-bank-exchange-rates/main/data/sama/latest.json`

## 🔗 Links

- [Saudi Central Bank (SAMA) rates page](https://allratestoday.com/central-bank-rates-api/sama/) — live table, publication cadence, FAQ
- [All central bank sources](https://allratestoday.com/central-bank-rates-api/)
- [Package docs on the site](https://allratestoday.com/docs/sdk/sama-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (Free)](https://allratestoday.com/register) · [Dashboard](https://allratestoday.com/profile) · [Pricing](https://allratestoday.com/pricing/)
- [Status](https://allratestoday.com/status)
- [Postman collection](https://allratestoday.com/postman/)
- [GitHub](https://github.com/AllRates-Today/sama-exchange-rate)

## 📜 License

MIT
