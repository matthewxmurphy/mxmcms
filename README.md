# MXMCMS: AI-Powered Multi-Tenant CMS for Web & Marketing Automation

![MXMCMS Logo](https://via.placeholder.com/728x90.png?text=MXMCMS+AI+CMS) <!-- Replace with actual logo URL -->

[![GitHub license](https://img.shields.io/github/license/yourusername/mxmcms)](https://github.com/yourusername/mxmcms/blob/main/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/yourusername/mxmcms?style=social)](https://github.com/yourusername/mxmcms/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/yourusername/mxmcms)](https://github.com/yourusername/mxmcms/issues)
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/yourusername/mxmcms/actions) <!-- Update with real CI if set up -->
[![Powered by Grav](https://img.shields.io/badge/Powered%20by-Grav-blueviolet)](https://getgrav.org)

**MXMCMS** (Multi-X Multi-CMS) is a forked and enhanced version of Grav CMS, transformed into an **API-first, AI-orchestrated multi-tenant platform** for launching web design firms, SEO/marketing agencies, and auxiliary online businesses. Built for scalability on Oracle Cloud's Always Free tier, it powers low-cost and high-dollar services with seamless AI automation – from site provisioning to content generation and social posting.

Target markets? We've got you: Cheapskates get $49.95 websites, while big spenders drop $999+ for premium vibes. All funnel to net30hosting.com for hosting upsells, with AI handling SEO, graphics, and cross-promotions. Client sites tie back to business credit services like Net30 Hosting, Net30 VoIP, and Net30 Websites for seamless affiliate loops. Think "OpenClaw" – a central AI rig clawing control over everything, bypassing costs internally and generating revenue externally.

🚀 **Why MXMCMS?** Automate your empire: Forkable themes, Brave-powered SEO, OpenAI graphics, social blasts (FB/X), and more – all under one roof.

## Key Features

- **Multi-Firm Structure**:
  - 2 Web Design Firms: Budget ($49.95) vs. Premium ($999) – unique frontends, shared backend.
  - 2 Marketing Firms: Low-cost vs. High-dollar SEO, handling Twitter cards, OG tags, Facebook posts.
  - Auxiliary Sites: Business credit portals (promoting Net30 services with affiliate ties), news sites with RSS feeds and auto-social posting (1¢/tweet budgeting via prepaid APIs).
  - Client Sites: All tie back to business credit and hosting (e.g., upsells to Net30 Hosting for credit-building).

- **AI-First Automation**:
  - Central AI Rig ("OpenClaw"-style): Equipped with CUDA for LLMs, tunnels in via SSH/WireGuard to provision sites, generate content, optimize SEO via Brave API calls (from the rig), create graphics with OpenAI (DALL-E proxy from the rig), and post to X/Facebook.
  - Daily SEO Updates: AI analyzes logs, implements changes on-the-fly.
  - Random Portfolio Building: AI launches sites, adds to portfolios, bypasses internal costs.

- **API-Centric Design**:
  - REST API for LLMs/AI Agents: CRUD sites, themes, SEO data, forms, graphics, social posts.
  - Integrations: Stripe/PayPal payments, Google Places/Analytics, Cloudflare Turnstile, Brave Search (via AI Rig), OpenAI (via AI Rig), Facebook Graph, Twitter API.

- **Security Fortress**:
  - SSH Keys Only (no passwords).
  - CrowdSec + Fail2Ban for intrusion detection.
  - OCI CLI for network-level firewalls.
  - JWT/API Keys for secure AI interactions.

- **Database & Deployment**:
  - Flat-file core (Grav) with optional Oracle Free Tier DBs: Autonomous (metadata/logs), NoSQL (key-value), HeatWave (analytics).
  - VHost/Certbot Automation: AI-managed SSL via Let's Encrypt.
  - Free-Tier Friendly: Runs on Oracle VM with tunneling for AI rig access.

- **Shared Resources**:
  - Unified Outbound Email: hello@ for all.
  - Form Approvals: Routed to AI/manager dashboard.
  - Hosting Upsells: All sites recommend net30hosting.com, with ties to business credit services.

## Architecture Overview

MXMCMS starts as a single-site Grav install, evolving into multi-tenant magic:

```mermaid
graph TD
    A[AI Rig: OpenClaw with CUDA/LLMs] -->|API Calls/Tunnel<br>Brave/OpenAI Proxies| B[MXMCMS Server on Oracle VM]
    B --> C[Shared Grav Backend: Plugins/API/DB]
    C --> D[Unique Themes: Cheap/Premium Firms]
    C --> E[SEO/Marketing: Brave/OpenAI Integrations<br>(Handled via AI Rig)]
    C --> F[Aux Sites: News/Business Credit<br>(Ties to Net30 Hosting)]
    D --> G[Client Sites: $49.95 or $999<br>(Upsell Net30/Business Credit)]
    E --> H[Social Posts: FB/X with Budgeting]
    B --> I[Security: CrowdSec/Fail2Ban/OCI Firewall]
    B --> J[DB Layer: Oracle Autonomous/NoSQL]
```

- **Backend**: Forked Grav with custom plugins for vhosts, Certbot, API endpoints.
- **Frontend**: Forkable themes per firm/site – customize without touching core.
- **AI Control**: Python scripts on rig call APIs for orchestration, with Brave/OpenAI handled directly from the rig's CUDA-powered setup.

## Getting Started

### Prerequisites
- PHP 8+, Composer.
- Oracle Cloud Account (Free Tier VM/DB).
- API Keys: Brave, OpenAI, Stripe, PayPal, Facebook, Twitter, Cloudflare, Google.

### Installation
1. Clone the repo:
   ```
   git clone https://github.com/yourusername/mxmcms.git
   cd mxmcms
   ```
2. Install Grav base:
   ```
   composer install
   bin/grav install
   ```
3. Configure multi-site (edit `setup.php` for subdomains).
4. Set up security:
   - Install CrowdSec/Fail2Ban via scripts in `/bin/security/`.
   - Configure OCI CLI: `oci setup config`.
5. Add DB: Edit `user/config/system.yaml` for Oracle PDO connection.
6. Deploy to Oracle VM: Rsync files, run Certbot hooks.

### Development in VS Code
- Open in VS Code: Use PHP extensions for IntelliSense.
- Local Server: `bin/gpm server`.
- API Testing: Use Postman to hit `/api/` endpoints.

## Usage
- **Provision a Site**: AI calls `/api/create-site?type=cheap&domain=example.com` – auto-vhost, theme, SSL, with business credit ties.
- **Generate Graphics**: `/api/generate-graphics?prompt="Cool logo"` – proxies to OpenAI via AI Rig.
- **SEO Update**: `/api/update-seo?site=example.com` – Uses Brave for data (from AI Rig), applies tags.
- **Social Post**: `/api/social-post?platform=x&content="News update"&budget=0.01` – Posts with limits.

Run AI rig scripts (Python) to automate: `python openclaw.py --provision random`.

## Contributing
Fork, PR, or open issues! We're building an AI empire – join the claw. 🦞

## License
MIT License – Fork Grav's open-source spirit. See [LICENSE](LICENSE) for details.

---

Built with ❤️ by [Bold Tee Hub](https://x.com/boldteehub) | Stockton, CA | SuperGrok User | Feb 2026
