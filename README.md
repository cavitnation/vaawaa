<p align="center"><img src="./banner.png" alt="VaaWaa" width="100%"></p>

<h1 align="center">VaaWaa</h1>
<p align="center"><i>Ad-free world, tech, crypto, business, sports, science & health news.</i></p>

<p align="center">
  <a href="https://vaawaa.com/"><img src="https://img.shields.io/badge/Live%20site-vaawaa-12b76a?style=for-the-badge&logo=googlechrome&logoColor=white"></a>
  <a href="https://jeemmo.com/"><img src="https://img.shields.io/badge/Built%20by-Jeemmo-111111?style=for-the-badge"></a>
</p>

## About

VaaWaa is an ad-free world-news aggregator I built on a custom PHP stack. It pulls from 200+ trusted sources through an hourly RSS pipeline and organises everything into per-country and per-category feeds, with a clean, fast, distraction-free reading experience.

## Key features

- **200+ trusted sources** — aggregated and de-duplicated into clean feeds
- **Hourly refresh** — a scheduled pipeline keeps the front page current
- **Per-country & per-category pages** — world, tech, crypto, business, sports, science, health
- **Ad-free reading** — fast pages, no clutter
- **Custom RSS engine** — resilient parsing across inconsistent publisher feeds

## Built with

![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white) ![RSS](https://img.shields.io/badge/RSS-FFA500?style=flat&logo=rssfeed=rss&logoColor=white) ![Cron](https://img.shields.io/badge/Cron-333333?style=flat) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)

## Pipeline and evidence boundary

The documented flow is publisher RSS → scheduled ingestion → normalization/deduplication → country/category feeds → reading pages. RSS items are external data: attribution, timestamp interpretation, malformed feeds and repeated headlines are the main boundaries to explain.

Useful acceptance checks are: identical stories do not multiply on repeated imports; failed feeds retain prior usable data; one broken publisher does not block the entire refresh; and displayed freshness reflects the last successful import. These checks describe the intended quality bar, not a test result from private source.

This repository contains documentation and artwork only. The feed parser, scheduler and deduplication implementation are private, and no measured ingestion success rate or latency is published here.

## About this repository

This is a **case study** of a production project I designed, built and maintain. The application is live at **[vaawaa.com](https://vaawaa.com/)**. The source code is proprietary and kept private — this page documents the work and the engineering behind it.

---

<sub>Built by <b><a href="https://jeemmo.com/">Azeem Javed (Jeemmo)</a></b> · <a href="https://www.linkedin.com/in/azeem-javed-7666861a/">LinkedIn</a> · Jeemmo is the trading name of Verivello Ltd, a UK-registered company.</sub>
