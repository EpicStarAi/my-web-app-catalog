# MY WEB APP CATALOG

> Centralized registry of all web applications, SaaS products, bots and automation projects by EpicStarAI.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-active-brightgreen)](#)
[![Projects](https://img.shields.io/badge/projects-10+-blue)](#catalog)

---

## Table of Contents

- [Overview](#overview)
- [Catalog](#catalog)
  - [AI & Automation](#ai--automation)
  - [Content & Media](#content--media)
  - [E-Commerce](#e-commerce)
  - [Telegram Bots](#telegram-bots)
  - [Web & SaaS](#web--saas)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [How to Add a Project](#how-to-add-a-project)
- [Roadmap](#roadmap)

---

## Overview

This repository serves as the **single source of truth** for all web apps, bots, automation tools and digital products developed and maintained under EpicStarAI umbrella.

Each entry includes:
- Short description
- Tech stack
- Current status
- Links (repo, live, docs)
- Category tags

---

## Catalog

### AI & Automation

| Project | Description | Stack | Status | Links |
|---|---|---|---|---|
| **AI App Control Center** | Orchestration hub for Perplexity Computer + Sonar API + Telegram bots | Python, FastAPI, Redis, Postgres | `in-dev` | [repo](#) |
| **n8n Automation Hub** | Central n8n instance with 50+ workflows for content, posting, scraping | n8n, Node.js, Webhooks | `active` | [repo](#) |
| **EpicStarAI Agent** | Multi-agent AI system with skills, memory and web actions | Python, Perplexity, Claude | `in-dev` | [repo](#) |

### Content & Media

| Project | Description | Stack | Status | Links |
|---|---|---|---|---|
| **NOVIKOVA MEDIA** | Multi-platform content generation pipeline with AI avatars | Python, ElevenLabs, Grok, FFmpeg | `active` | [repo](#) |
| **DEEP INSIDE** | Story-driven serial/media project with AI-generated content | Claude, Grok, Midjourney | `active` | [repo](#) |
| **BAMBINO LAND** | Virtual avatar and children content automation project | Python, HuggingFace, TTS | `in-dev` | [repo](#) |
| **novikova-3d-avatar** | 3D avatar generation and animation pipeline | Three.js, Python, AI models | `active` | [repo](https://github.com/EpicStarAi/novikova-3d-avatar) |

### E-Commerce

| Project | Description | Stack | Status | Links |
|---|---|---|---|---|
| **SHOP TOK** | AI-driven dropshipping content automation for TikTok Shop | Python, n8n, Grok, TikTok API | `active` | [repo](#) |
| **pro100fem.com** | Service/marketplace website with automated catalog | Next.js, Vercel, Stripe | `live` | [repo](#) [site](https://pro100fem.com) |

### Telegram Bots

| Project | Description | Stack | Status | Links |
|---|---|---|---|---|
| **Bot Farm Manager** | Centralized management for Telegram bot network | Python, Telethon, Redis | `active` | [repo](#) |
| **AI Content Bot** | Telegram bot for on-demand AI content generation | Python, aiogram, Sonar API | `active` | [repo](#) |
| **Posting Scheduler Bot** | Automated cross-channel posting and scheduling | Python, aiogram, Postgres | `active` | [repo](#) |

### Web & SaaS

| Project | Description | Stack | Status | Links |
|---|---|---|---|---|
| **ROCKY BUILDER** | Construction/services website with CMS | Next.js, Tailwind, Vercel | `live` | [repo](#) |
| **Telegram Mini App** | Web app embedded in Telegram for user flows | React, Vite, Railway | `in-dev` | [repo](#) |

---

## Tech Stack

```
Languages:    Python · JavaScript · TypeScript
Frameworks:   FastAPI · Next.js · React · aiogram
Databases:    PostgreSQL · Redis · Supabase
AI/ML:        Perplexity (Computer + Sonar) · Claude · Grok · ElevenLabs · HuggingFace
Automation:   n8n · Telegram Bot API · TikTok API
Deployment:   Vercel · Railway · Replit · Azure VPS
Tools:        GitHub · GoDaddy · Google Workspace · Cloudflare
```

---

## Project Structure

```
my-web-app-catalog/
├── README.md                  # This file — main catalog
├── LICENSE
├── apps/
│   ├── ai-automation/         # AI & automation project docs
│   ├── content-media/         # Content & media project docs
│   ├── ecommerce/             # E-commerce project docs
│   ├── telegram-bots/         # Telegram bot project docs
│   └── web-saas/              # Web & SaaS project docs
├── templates/
│   └── app-entry-template.md  # Template for new entries
├── docs/
│   ├── architecture.md        # Overall system architecture
│   ├── tech-stack.md          # Full tech stack reference
│   └── deployment.md          # Deployment guides
└── scripts/
    └── validate-catalog.py    # Script to check entry completeness
```

---

## How to Add a Project

1. Copy `templates/app-entry-template.md`
2. Fill in all fields: name, description, stack, status, links
3. Add entry to the correct table in this README
4. Place the full file under `apps/<category>/your-project.md`
5. Commit with message: `feat: add [project-name] to catalog`

Status values:
- `active` — live and in use
- `in-dev` — under active development
- `paused` — temporarily on hold
- `archived` — no longer maintained
- `live` — publicly deployed and serving users

---

## Roadmap

- [ ] Add GitHub Actions to auto-validate catalog entries
- [ ] Build web UI for catalog (Next.js + GitHub API)
- [ ] Add deployment status badges via shields.io
- [ ] Integrate with Notion database for project management
- [ ] Auto-sync with n8n workflow registry
- [ ] Domain: mywebappcatalog.com or epicstarai.com/catalog

---

> Maintained by [@EpicStarAi](https://github.com/EpicStarAi) · Updated: June 2026
