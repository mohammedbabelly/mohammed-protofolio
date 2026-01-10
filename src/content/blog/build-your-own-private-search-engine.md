---
title: "Build Your Own Private Search Engine with SearXNG – Ditch Google Tracking"
description: "How to set up SearXNG, a self-hosted metasearch engine that aggregates results from multiple engines without profiling you. Privacy first!"
pubDate: "Feb 10 2023"  # Original post timing ~3 years ago; content still relevant in 2026
heroImage: "/blog-searxng.jpeg"
---

Big tech knows too much about us. Every search on Google or Bing builds a profile that's sold to advertisers. Incognito mode? Doesn't help. Even "private" alternatives like DuckDuckGo have their quirks.

That's why I love **SearXNG** – a free, open-source metasearch engine that aggregates results from 70+ sources (Google, Bing, DuckDuckGo, and more) without tracking or profiling you.

### How SearXNG Protects Your Privacy
- Builds a random, temporary profile for each search – nothing tied to you
- If self-hosted on your server, search engines only see your server's IP (not yours)
- No ads, no tracking cookies, full control

It's lightweight, customizable, and super easy to run with Docker.

### Quick Setup with Docker
1. Clone the official Docker repo:  
   https://github.com/searxng/searxng-docker

2. Edit `docker-compose.yaml` (change ports if needed, e.g., map to 8080)

3. Run:  
   ```bash
   docker compose up -d
```

4. Access at http://localhost:8080 (or your server's IP/port)

That's it – your own private search engine! For production, add HTTPS via reverse proxy (Nginx/Caddy) and consider Tailscale for secure remote access.
Try a Public Instance (or Mine Back Then)
You can test public instances first, but self-hosting gives ultimate privacy.
Docs: https://docs.searxng.org/ (still active and updated in 2026!)
If privacy matters to you, give SearXNG a spin. It's eye-opening how much better search feels without the surveillance.
What privacy tools do you use daily?


#Privacy #SelfHosting #Docker #OpenSource #SearchEngine #SearXNG