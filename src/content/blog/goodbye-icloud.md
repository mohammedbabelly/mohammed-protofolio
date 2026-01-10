---
title: "Goodbye iCloud, Hello Free 4TB Home Server"
description: "How I ditched paid cloud storage and built my own private, automated media + photo solution using an old laptop, Docker, and smart tools."
pubDate: "Dec 27 2025"  # Approx. two weeks before Jan 10, 2026
heroImage: "/blog-homelab.jpeg"
---

Tired of monthly cloud bills and lock-in? I was too. So I dusted off an old laptop, installed Debian, and turned it into a full-featured **4TB home server** — completely free (after the initial hardware, of course).

Here's the stack I used and why it works so well:

### 1. The Media Center (Plex + *arr Stack)
Migrated all my movies, TV shows, and music to **Plex**. To keep everything organized and fresh automatically, I added the famous *arr suite:
- Sonarr (TV)
- Radarr (Movies)
- Lidarr (Music)
- Prowlarr (Indexer manager)

Result: Zero manual downloads — everything finds itself and stays updated.

### 2. The Photo Cloud (Immich – Google Photos Killer)
**Immich** is the real game-changer here. It's a 100% self-hosted, open-source alternative to Google Photos with:
- Automatic backups from iOS and Android
- Face recognition
- Map view for location-based memories
- Stunning timeline UI
- Complete privacy (no one else sees your photos)

Setup was straightforward with Docker Compose — and it just works.

### 3. Secure Remote Access (Tailscale)
No port forwarding, no exposed services. **Tailscale** creates a secure mesh VPN that lets me access the server from anywhere (phone, laptop, even when traveling) as if I were at home. Zero-config magic.

### 4. Disaster-Proof Backup (Backblaze B2 + rclone)
Self-hosting is awesome, but data loss is a nightmare. I follow the **3-2-1 rule**:
- 3 copies of data
- 2 different media types
- 1 off-site

I use **rclone** to sync my entire library + Immich database dumps to **Backblaze B2** (S3-compatible, ~$6/TB/month — way cheaper than iCloud).

### The End Result
- Blazing-fast local access at home
- Off-site backup for peace of mind
- Full ownership of my media and memories
- Learned a ton about Docker, networking, and automation

If you're fed up with subscriptions and want more control, start small — an old PC + Docker is all you need. Those green containers in Portainer are incredibly satisfying! 🚀

Have you built a homelab yet? What's in your stack?

#SelfHosting #HomeLab #Docker #Immich #Tailscale #DataPrivacy