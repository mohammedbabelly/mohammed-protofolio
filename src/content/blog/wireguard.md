---
title: "Set Up Your Own Secure WireGuard VPN on AWS with Terraform – Under $4/Month"
description: "A simple, secure Terraform script to deploy a personal WireGuard VPN server on AWS, perfect for bypassing restrictions or secure remote access."
pubDate: "Sep 10 2025"  # Approx. 4 months before Jan 10, 2026
heroImage: "/blog-wireguard-vpn.jpeg"
---

Need a reliable, private VPN? Especially useful when traveling or in regions where services like GitHub are restricted (looking at you, Syria 🇸🇾).

I created a straightforward **Terraform script** that deploys a secure **WireGuard** VPN server on AWS in minutes. Here's the gist:

### Why WireGuard + Terraform?
- WireGuard is modern, fast, and super simple compared to OpenVPN
- Terraform makes it fully reproducible and easy to manage
- Runs on a tiny `t3.nano` EC2 instance → costs ~$4/month or less

### Key Features
- Secure WireGuard setup with automatic key generation
- Clean web UI (via a simple dashboard) to manage connected devices
- Easy configuration – just tweak variables and `terraform apply`
- SSH access locked down, firewall rules tightened

### How to Get Started
1. Clone the repo: https://github.com/mohammedbabelly/terraform-wireguard (my personal fork/setup)
2. Set your AWS credentials and preferred region
3. Run `terraform init && terraform apply`
4. Grab the generated config file → import into WireGuard client (mobile/desktop)
5. Connect and enjoy secure, private internet!

I've been using this setup regularly — it's reliable, cheap, and gives full control.

If you're into DevOps, homelabbing, or just need a personal VPN, give it a try. Contributions/PRs welcome!

Check it out here: https://github.com/mohammedbabelly/terraform-wireguard

#Terraform #WireGuard #AWS #VPN #DevOps #Automation