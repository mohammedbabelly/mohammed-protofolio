---
title: "Contributing to Litestar: Two Fix PRs Merged in v2.13.0"
description: "Excited to share my first contributions to Litestar – a fast, flexible Python web framework. Two bug fixes merged and released!"
pubDate: "Jan 15 2025"
heroImage: "/blog-contributing-to-litestar.jpeg"
---

Open source contributions always feel rewarding, and recently I hit a milestone: two of my pull requests to **Litestar** (a powerful, lightweight ASGI framework for building modern APIs) were merged and shipped in **v2.13.0** (released November 20, 2024) 🥳

### What is Litestar?
If you're building APIs in Python, Litestar is worth checking out. It's designed to be fast, flexible, and extensible while staying opinionated enough to get things done quickly. Think high-performance data validation, dependency injection, OpenAPI generation, and more – all with great developer experience.

### My Contributions
I opened and got merged two fixes:
- **Fix for Prometheus metrics**: Corrected the path template for routes without path parameters (PR #3784). This ensures accurate monitoring in production setups.
- **Duplicate RateLimit-* headers**: Fixed an issue where caching could cause duplicate rate-limit headers to appear (PR #3855). Cleaner responses, better compatibility.

Seeing these go live in the release was awesome – especially as my first contributions to the project!

### Why Contribute?
Litestar is growing fast in the Python community, and small fixes like these help make it more reliable for everyone. If you're using it (or thinking about it), dive into the repo, find an issue, and submit a PR. The maintainers are welcoming, and it's a great way to level up your skills.

Repo: https://github.com/litestar-org/litestar  
Release notes for v2.13.0: https://github.com/litestar-org/litestar/releases/tag/v2.13.0

I'm looking forward to more contributions – maybe some features next time! 😄

Have you contributed to a framework or library? What's your story?

#Python #Litestar #OpenSource #WebFrameworks #DevOps