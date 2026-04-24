# Card Alerter

  Personal command-line tool that monitors a small watchlist of MLB and NBA players for performance breakouts and
  surfaces relevant trading card listings via Telegram alerts.

  ## What it does

  - Polls MLB Stats API and NBA CDN feeds for live and daily player performance.
  - When a watched player triggers a configured threshold (e.g., breakout K%/ISO trend, multi-HR game, 30+ point game),
  composes a Telegram alert.
  - Enriches each alert with up to 3 active eBay listings for that player's trading cards (Browse API, category 213).

  ## eBay API usage

  - **Browse API** — `item_summary/search` to fetch active listings filtered to category 213 (Sports Trading Cards).
  Triggered only at alert time.
  - **Marketplace Insights API** *(pending approval)* — `item_sales/search` to fetch recent sold-comparable prices so
  alerts can flag listings priced below recent sold medians.

  ## Scope

  - Single user (the developer/owner).
  - Local CLI tool, no public-facing web interface.
  - No long-term storage of eBay data — fetched at alert time, included in the Telegram message, discarded.
  - No redistribution, no resale, not commercial.

  ## Compliance

  - eBay Marketplace Account Deletion notification exemption granted.
