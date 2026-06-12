# System Architecture

## Overview

MY WEB APP CATALOG ecosystem consists of multiple interconnected layers:

```
┌─────────────────────────────────────────────────────────────┐
│                    INTERFACE LAYER                         │
│   Telegram Bots · Web Apps · TikTok · Instagram · YouTube  │
└───────────────────────┬────────────────────────────────┘
                         │
                         ▼
┌─────────────────────────────────────────────────────────────┐
│                    CONTROL LAYER                           │
│       API Gateway · Router · Auth · Job Manager            │
└───────────────────────┬────────────────────────────────┘
                         │
              ┌────────┴────────┐
              │                  │
              ▼                  ▼
┌────────────────┐  ┌────────────────┐
│  SONAR API          │  │  PERPLEXITY     │
│  (fast Q&A,         │  │  COMPUTER       │
│   research,         │  │  (long workflows │
│   citations)        │  │   multi-step     │
└────────────────┘  │   skills)       │
                         └────────────────┘
                                  │
                                  ▼
┌─────────────────────────────────────────────────────────────┐
│                    ACTION LAYER                            │
│  Telegram Post · TikTok Upload · Sheets · Notion · n8n    │
└─────────────────────────────────────────────────────────────┘
```

## Routing Logic

| Input type | Engine | Reason |
|---|---|---|
| Quick Q&A, fact check, brief | Sonar API | Fast, web-grounded, one-shot |
| Content plan, multi-step pipeline | Perplexity Computer | Multi-model, background, skills |
| Posting, publishing, notifications | Action Layer (own services) | Controlled write access |

## Data Flow

1. User sends command via Telegram or Web
2. API Gateway receives and authenticates request
3. Router classifies job type (fast vs long)
4. Fast jobs → Sonar API → return result
5. Long jobs → create Job record → Perplexity Computer
6. Computer executes skill + returns artifacts
7. Backend stores output, sends preview to user
8. User approves → Action Layer publishes

## Key Principles

- **Human-in-the-loop**: No publish without explicit approve
- **Idempotency**: Every job has unique ID, no duplicate actions
- **Observability**: All steps logged with timestamps
- **Modularity**: Each app is independent, catalog is the index
