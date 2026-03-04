# Task 07: URL Anatomy & Robots.txt Compliance

## Overview
Before an Information Retrieval system can index the web, it must be able to navigate it. This task involves two critical pre-crawling steps: **URL Decomposition** and **Web Ethics Compliance**. The system analyzes the structure of various URLs and programmatically fetches their `robots.txt` files to determine which areas of a website are off-limits to automated agents.



## Features
### 1. Advanced URL Parsing
The implementation uses the `urllib.parse` library but adds custom logic to handle complex, multi-part Top-Level Domains (TLDs) like `.ac.uk` and `.ac.il`. It extracts:
* **Scheme & Network Location:** Protocols and hostnames.
* **Component Extraction:** Precise identification of Subdomains, Domains, and TLDs.
* **Path & Query Analysis:** Extracting specific file names and dynamic query parameters (e.g., `tenant_id`, `recs_exp`).

### 2. Robots.txt Analysis
To ensure "polite" crawling, the script:
* **Automated Discovery:** Automatically constructs the `robots.txt` path for any given domain.
* **Rule Parsing:** Identifies `Disallow` paths to prevent crawling private or heavy-load directories.
* **User-Agent Filtering:** Detects specific rules for different crawlers.
* **Crawl-Delay Detection:** Identifies wait-time requirements to avoid overwhelming servers.

## Technical Tools
* **Urllib:** For network requests and URL manipulation.
* **Pandas:** To represent the parsed URL components in a clean, tabular format for comparison.
* **Stochastic Headers:** Uses custom `User-Agent` strings to simulate real-world crawler behavior.

## Author
**Yousef Shihade**
Information Retrieval Course | University of Haifa
