![Open Anime API Banner](open_anime_api_banner.png)

# Open Anime API

A lightweight, high-performance, self-configuring streaming API wrapper designed to compile, cache, and serve anime media resources dynamically. 
This project integrates metadata aggregation and on-demand Puppeteer scraping tools to provide a seamless interface for web applications.

Open Anime API is a next-generation, developer-focused, open-source anime streaming and metadata database engine. It acts as an intelligent middleware between anime frontends and public metadata indexes (like MyAnimeList via the Jikan API).

By deploying headless browsers in the background, it scrapes, extracts, and resolves compatible video player streams (Sub/Dub) and P2P torrent download links in real-time. With a plug-and-play setup, it automatically self-configures local databases or Supabase cloud caches to ensure sub-millisecond response times for cached links, creating the perfect foundation for custom anime applications.
---

## 📡 Live Preview
Here is a look at the modern web streaming dashboard powered entirely by the Open Anime API server:

![Website Preview](dashboard_preview.png)

---

## 🚀 Key Features

* **Zero-Configuration Setup:** Automatically installs missing npm packages on startup.
* **On-Demand Mining:** If a stream link is missing from the database, it deploys Puppeteer headless miners in real-time to find and save it.
* **Unified Database Layer:** Configures instantly to save cache results to a local JSON file database or to Supabase cloud.
* **Jikan API Proxy:** Proxies metadata directly from MyAnimeList/Jikan to populate web pages.
* **Bulk Database Loader (`fillDB.js`):** Deep-mines entire anime series in advance to skip on-demand wait times.

---

## 🛠️ Installation & Setup

1. Clone or copy the folder to your local system.
2. In your terminal, navigate to the directory and run:
   ```bash
   node start.js
   ```
3. Follow the wizard in the command terminal to configure your chosen database choice (Local JSON file or Supabase credentials).
4. Connect your web player frontend to the resolver endpoint:
   `http://localhost:3000/api/stream?title=one+piece&episode=1`

---

## 📑 Command Catalog

### Run Server Dashboard
```bash
node start.js
```

### Pre-fill Database (Deep-Dive Bulk Scraping)
```bash
node fillDB.js "Anime Title"
```

---

## ⚖️ Academic License & Exemption
* **Project Nature:** This repository represents an academic **Project of the Year** created solely for private, educational research and engineering studies.
* **Content Indexing:** All anime stream URLs and metadata resolved by this API represent index results compiled courtesy of public networks and search assistance. No copyright content is hosted, owned, or stored directly on this server.
* **Usage Restrictions:** The core API structure, custom controllers, and codebase are strictly proprietary. **This code cannot be modified, redistributed, or reproduced by any other parties.**
* **DMCA Notice:** Anti-piracy, copyright enforcement, and DMCA claims do not apply under global **Fair Use academic exemptions** for private student research. Any attempts to target this repository will be contested under legal academic protections.
