# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Intent Gifter** is a preference-driven gifting platform where users express preferences, earn progress, and occasionally unlock surprises that accelerate fulfillment—without gambling mechanics.

**Tagline:** Preference-first. Boundary-aware. Progress-driven.

**Core Concept:** Users express what fits them through selections, earn progress credits that never expire, and system learns preferences over time—surprise is optional acceleration, not the core path.

## Primary Documentation

**Start here:** [docs/MASTER_PLAN.md](./docs/MASTER_PLAN.md) - Complete project plan with architecture, features, wireframes, and implementation roadmap.

## Technology Stack

| Component | Technology |
|-----------|------------|
| **Frontend** | React + TypeScript + Next.js 14 (App Router) |
| **UI** | Tailwind CSS + shadcn/ui |
| **State** | Zustand |
| **Forms** | React Hook Form + Zod |
| **Backend** | Node.js + Express |
| **Database** | PostgreSQL + Redis |
| **Auth** | JWT + bcrypt |
| **Payments** | Stripe (micro-conversions) |
| **AI/ML** | Recommendation engine for preference matching |

## MVP Philosophy

**Full feature set at launch.** No deferred features. Everything ships in MVP:
- Preference capture (explicit + comparative)
- Progress credit system with milestones
- Surprise mechanics with transparent odds
- Gift-safe public profiles
- Category priority system
- Optional micro-conversion ($1-$3)

## Documentation Structure

```
/docs/
├── MASTER_PLAN.md           ← Start here (comprehensive)
├── planning/
│   ├── MVP_SPEC.md
│   └── ROADMAP.md
├── architecture/
│   └── ARCHITECTURE.md
├── ux/
│   └── WIREFRAMES.md
└── research/
    ├── FEATURES.md
    ├── MARKET_ANALYSIS.md
    └── LEGAL_COMPLIANCE.md
```

## Route Structure

**Marketing:** `/`, `/how-it-works`, `/features`, `/pricing`, `/privacy`, `/terms`

**Auth:** `/login`, `/signup`, `/onboarding`

**App:** `/dashboard`, `/preferences`, `/profile/:userId`, `/settings`

**Core Flows:**
- Preference selection (explicit + comparative)
- Progress tracking and milestones
- Surprise reveal at milestones
- Gift-safe profile sharing

## Core Data Models

- **Users** - Account + preference profile
- **PreferenceSelections** - User choices with category tags
- **ProgressCredits** - Earned credits (never expire)
- **Milestones** - 100/200/500 credit thresholds
- **SurpriseOutcomes** - Transparent outcome probabilities
- **CategoryPriorities** - User-ranked gift categories (1-8)
- **WishList** - Explicit item selections

See [docs/MASTER_PLAN.md](./docs/MASTER_PLAN.md) for full schema.

## Key Components

| Component | Purpose |
|-----------|---------|
| `preference-selector` | Comparative choice UI ("Pick 1 of 4") |
| `progress-bar` | Visual credit accumulation display |
| `category-ranking` | Drag-drop category priority |
| `milestone-reveal` | Surprise reveal animation |
| `gift-profile-share` | Public shareable profile link |

## MVP Rules (Non-Negotiables)

- Progress credits NEVER expire or reset
- Surprises are OPTIONAL (not core path to items)
- Transparent odds always displayed
- No pay-to-win mechanics
- No loss outcomes (progress always increases)
- No infinite replay loops
- Category boundaries respected ("Never buy me...")
- NOT gambling, NOT raffle, NOT layaway

## Legal & Ethical Design

**Non-negotiable constraints:**
- No pay-to-win
- No losses
- No infinite replay loops
- No hidden odds
- No forced engagement

**Core principle:** Progress always carries forward. Surprise accelerates but never replaces progress.

See [docs/research/LEGAL_COMPLIANCE.md](./docs/research/LEGAL_COMPLIANCE.md) for full legal analysis.

## When Modifying Scope

Update these files on every scope change:
- `docs/MASTER_PLAN.md`
- `docs/ux/WIREFRAMES.md`
- `docs/architecture/ARCHITECTURE.md`
