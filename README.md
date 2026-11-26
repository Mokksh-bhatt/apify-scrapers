# 67-labs — Pay-Per-Result Web Scrapers on Apify Store

Small, tested scrapers built by **[Mokksh Bhatt (67-labs)](https://apify.com/67-labs)**. Plain HTTPS requests, no login walls, and no CAPTCHA bypassing. Every scraper exports clean, flat rows to CSV, JSON, Excel, Google Sheets, **n8n**, **Make**, and **AI Agents via MCP**.

You pay per result — Apify compute & proxy usage are included, and Apify's **$5/month free plan credit** covers a full test of every scraper below.

---

## Lead Generation, Creators & Market Intelligence

| Scraper | What You Extract | Starting Price |
|---|---|---|
| **[Podcast Search & Host Email Scraper](https://apify.com/67-labs/podcast-search-scraper)** | Search Apple Podcasts & read live RSS feeds for **real host emails** (filters Anchor/Spotify proxy emails), owner names, websites, social links, publishing cadence & episodes | `$1 / 1,000` results *(Dec 10: `$2/1k` + `$15/1k` emails)* |
| **[YouTube Channel Scraper & Snapshot](https://apify.com/67-labs/youtube-channel-snapshot)** | Channel title, `@handle`, subscribers, exact total views, video count, country, created date, About links, upload cadence & median views (no API key) | `$2 / 1,000` channels |
| **[Review Lead Qualifier](https://apify.com/67-labs/review-lead-qualifier)** | Turn Google Maps review datasets/CSVs into prioritized agency outreach leads with recent 1–2 star written reviews, review links, owner reply status & business contacts | Free preview / `$0.05` per qualified lead |
| **[Y Combinator Companies Scraper](https://apify.com/67-labs/yc-companies-scraper)** | Filter YC startup directory by batch, industry, hiring status & region | `$2 / 1,000` companies |
| **[Remote Jobs Scraper](https://apify.com/67-labs/remote-jobs-scraper)** | Structured remote tech, product, design & marketing job listings with tags and apply links | `$1 / 1,000` jobs |

## Ads & Competitor Intelligence

| Scraper | What You Extract | Starting Price |
|---|---|---|
| **[Google Ads Transparency Center Scraper](https://apify.com/67-labs/google-ads-transparency-center-scraper)** | Every ad an advertiser runs on Google Search, Display & YouTube: format, first/last shown dates, regions & preview links | `$2 / 1,000` ads |
| **[Competitor Ad Watch](https://apify.com/67-labs/competitor-ad-watch)** | Weekly competitor report combining new Google ads + worst Play Store reviews | `$1` / competitor report |

## App Stores, Gaming & Reviews

| Scraper | What You Extract | Starting Price |
|---|---|---|
| **[Google Play Reviews Scraper](https://apify.com/67-labs/google-play-reviews-scraper)** | Mobile app reviews: star rating, text, date, helpful thumbs up & developer replies across any language/country | `$0.50 / 1,000` reviews |
| **[Steam Reviews Scraper](https://apify.com/67-labs/steam-reviews-scraper)** | Steam game reviews via Valve's current `IUserReviewsService` API: recommended flag, text, hours played, votes & Early Access status | `$0.50 / 1,000` reviews |
| **[App Store Top Charts Scraper](https://apify.com/67-labs/app-store-top-charts-scraper)** | Apple App Store top free, paid & grossing rankings by country and category | `$1 / 1,000` apps |
| **[Chrome Web Store Scraper](https://apify.com/67-labs/chrome-web-store-scraper)** | Chrome extension install counts, ratings, review count, version, last update & newest reviews | `$3 / 1,000` extensions |

## E-Commerce & Developer Data

| Scraper | What You Extract | Starting Price |
|---|---|---|
| **[Shopify Store Products Scraper](https://apify.com/67-labs/shopify-store-products-scraper)** | Full Shopify catalog: title, vendor, price, compare-at sale flags, all variants with SKU & stock, images & optional free collection rows | `$1 / 1,000` products |
| **[GitHub Repository Stats Scraper](https://apify.com/67-labs/github-repo-stats-scraper)** | Stars, forks, open issues & PRs, contributors, latest releases & license | `$2 / 1,000` repos |
| **[Hacker News Search Scraper](https://apify.com/67-labs/hacker-news-search-scraper)** | HN stories & comments filtered by keyword, date window & points | `$1 / 1,000` items |
| **[npm & PyPI Package Stats Scraper](https://apify.com/67-labs/npm-pypi-package-stats-scraper)** | Latest version, license, weekly/monthly downloads & maintainers across npm & PyPI | `$1 / 1,000` packages |

---

## Free Ready-to-Import n8n Workflow Templates

Download and import either JSON workflow straight into **n8n** — just paste your Apify API token:

- **[Podcast Guest & Sponsor Outreach Automation](workflows/n8n-podcast-guest-outreach.json)** — Searches active shows (`activeWithinDays: 60`, `onlyWithEmail: true`, 1 row per podcast) and outputs clean host emails + social links ready for Google Sheets or cold email.
- **[Local Agency Low-Star Review Lead Pipeline](workflows/n8n-review-lead-qualifier.json)** — Filters Google Maps review exports for recent unanswered 1–2 star reviews and deduplicates previously contacted businesses automatically.

---

## Quick Start (UI, API, or AI Agents via MCP)

1. Open any scraper link above and click **Try for free** (uses your free Apify credits).
2. Enter your search term, store URL, advertiser, or channel `@handle` and click **Start**.
3. Download results as CSV, JSON, or Excel — or connect straight into **Google Sheets**, **n8n**, **Make**, **Clay**, or **Claude / ChatGPT / Cursor via the Apify MCP Server**.

```bash
curl -X POST "https://api.apify.com/v2/acts/67-labs~podcast-search-scraper/run-sync-get-dataset-items?token=YOUR_APIFY_TOKEN&maxTotalChargeUsd=1" \
  -H "Content-Type: application/json" \
  -d '{
    "queries": ["startup founders"],
    "country": "US",
    "maxPodcasts": 25,
    "episodesPerPodcast": 0,
    "activeWithinDays": 60,
    "onlyWithEmail": true
  }'
```

---

## Need a Custom Automated Data Pipeline?

Want weekly verified podcast host leads, local low-star review outreach lists, or custom competitor monitoring delivered automatically to your Google Sheet, Airtable, or CRM?

- Email: **`mokkshbhatt@gmail.com`**
- Apify Profile: **[apify.com/67-labs](https://apify.com/67-labs)**
- Bug reports or new scraper requests: Open a GitHub Issue in this repo.
