# Intent Gifter

| Repo Map | Purpose | Authority |
| --- | --- | --- |
| docs/PRODUCT_MAP.md | Canonical product model (preference-first, progress-driven) | Source of truth |
| docs/MASTER_PLAN.md | End-to-end behavior and execution | Source of truth |
| docs/ux/WIREFRAMES.md | ESW wireframes for all routes | Derived |
| docs/ux/SITEMAP.md | Route map tied to PRODUCT_MAP | Derived |
| docs/planning/MVP_SPEC.md | MVP definition and success criteria | Derived |
| docs/architecture/ARCHITECTURE.md | Data model + API contracts | Architecture-only |

| System Entities | Description | Persisted? | User-facing label |
| --- | --- | --- | --- |
| User | Account with preference profile | Yes | Your Profile |
| PreferenceSelection | Comparative choice ("Pick 1 of 4") | Yes | Choice |
| ProgressCredit | Earned credits (never expire) | Yes | Progress Credits |
| Milestone | 100/200/500 credit thresholds | No (calculated) | Milestone |
| SurpriseOutcome | Triggered at milestones | Yes (history) | Surprise |
| CategoryPriority | User-ranked gift categories (1-8) | Yes | Category Order |
| WishList | Explicit item selections | Yes | Wish List |
| GiftProfile | Public shareable profile | No (generated) | Gift-Safe Profile |

| Routes Index | Mode | Writes | Reads | Wireframe location |
| --- | --- | --- | --- | --- |
| / | PUBLIC | None | None | docs/ux/WIREFRAMES.md (Home) |
| /onboarding | PREFERENCE | Category rankings, first choices | None | docs/ux/WIREFRAMES.md (Onboarding) |
| /dashboard | PROGRESS | None | Progress, activity | docs/ux/WIREFRAMES.md (Dashboard) |
| /preferences | PREFERENCE | Preference selections | Progress | docs/ux/WIREFRAMES.md (Comparative Choice) |
| /wishlist | WISHLIST | Wishlist items | Wishlist | docs/ux/WIREFRAMES.md (Wishlist) |
| /surprises | SURPRISE | Surprise claims | Milestone status, history | docs/ux/WIREFRAMES.md (Surprise Reveal) |
| /u/[username] | PROFILE | None | Category priorities, wishlist | docs/ux/WIREFRAMES.md (Public Profile) |
| /settings | SETTINGS | Account, preferences, privacy | User profile | docs/ux/WIREFRAMES.md (Settings) |

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is PREFERENCE-FIRST.

1) Users EXPRESS preferences through comparative choice or explicit selection.
2) PROGRESS CREDITS are earned through meaningful preference selections.
3) CREDITS NEVER EXPIRE or reset.
4) SURPRISES are OPTIONAL ACCELERATORS triggered at milestones (100, 200, 500 credits).
5) GIFT-SAFE PROFILES show category priorities and boundaries to friends.
6) PROGRESS ALWAYS CARRIES FORWARD (no losses, no pay-to-win).

Terminology rules:
- Internal system term: Preference Profile (architecture only).
- User-facing term: Your Preferences / What Fits You.
- Credits are NOT money. They're earned through selections, never purchased.
- Surprises are NOT gambling. They're optional accelerators with transparent odds.
- Category boundaries are respected: "Never buy me clothing" means NEVER.

## Gut Check (Yes/No)
- Can progress expire? NO
- Can you lose credits? NO
- Is surprise required to get items? NO
- Are odds transparent? YES
- Can you pay to skip ahead? NO (optional $1 boost max 3/month for acceleration)
- Is this gambling? NO

## Core Innovation
Two ways to express desire:
- **Explicit Selection**: "I want this specific thing"
- **Comparative Choice**: "Which of these feels more like me?" (system learns patterns)

## Key Principle
**This is NOT gambling, NOT a raffle, NOT layaway.**

It's a preference platform where:
- No payment required to participate
- Progress never expires or resets
- Surprises are optional accelerators, not the main path
- All outcomes are transparent
- You always move closer to what you want

---

**Tagline:** Preference-first. Boundary-aware. Progress-driven.

**Documentation:** See [docs/PRODUCT_MAP.md](./docs/PRODUCT_MAP.md) for complete feature specifications.

**Technology Stack:** React + TypeScript + Next.js 14 | Node.js + Express | PostgreSQL + Redis | Stripe

**Status:** Ready for Development
