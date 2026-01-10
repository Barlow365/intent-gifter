# Intent Gifter - PRODUCT MAP (CANONICAL)

**Version:** 1.0
**Last Updated:** 2026-01-09
**Status:** Ready for Development

---

## Purpose

This is the **single source of truth** for WHAT Intent Gifter is.

All features—past, present, and future—are documented here. Every other document in this repository is either:
- A **ZOOM** expansion of a section below
- A **REFERENCE** (market data, legal, etc.)
- A **NAVIGATION** (README, SITEMAP)

**If a feature isn't here, it doesn't exist.**

---

## Navigation

- **README.md** - Project overview and navigation hub
- **docs/EXECUTION_PLAN.md** - Technical implementation phases (HOW)
- **docs/ux/WIREFRAMES.md** - 🔍 ZOOM: Visual expansions of UI nodes
- **docs/ux/SITEMAP.md** - 🔍 ZOOM: Complete route structure
- **docs/architecture/ARCHITECTURE.md** - 🔍 ZOOM: Data models mapped to entities
- **docs/planning/MVP_SPEC.md** - 🔍 ZOOM: MVP rules and constraints
- **docs/research/LEGAL_COMPLIANCE.md** - Legal safeguards

---

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is PREFERENCE-FIRST.

1) Users EXPRESS preferences through comparative choice or explicit selection.
2) PROGRESS CREDITS are earned through meaningful preference selections.
3) CREDITS NEVER EXPIRE or reset.
4) SURPRISES are OPTIONAL ACCELERATORS triggered at milestones (100, 200, 500 credits).
5) GIFT-SAFE PROFILES show category priorities and boundaries to friends.
6) PROGRESS ALWAYS CARRIES FORWARD (no losses, no pay-to-win).

Terminology rules:
- Credits are NOT money. They're earned through selections, never purchased (except optional $1 boost).
- Surprises are NOT gambling. They're optional accelerators with transparent odds.
- Category boundaries are respected: "Never buy me clothing" means NEVER.

---

## Status Indicators

- ✓ Built and deployed
- ● In progress / current phase
- ○ Planned / next phase
- ⊘ Deferred / not applicable

---

## Product System Map

```
+==============================================================================+
| INTENT GIFTER | PRODUCT MAP (CANONICAL)                                      |
| Express → Earn → Refine → Accelerate                                        |
+==============================================================================+

Status Indicators:
✓ = Built  ● = In Progress  ○ = Planned  ⊘ = Deferred

+==============================================================================+
| CORE PRINCIPLE                                                               |
+==============================================================================+
| This is NOT gambling, NOT a raffle, NOT layaway.                            |
| Progress always carries forward. Surprise accelerates, doesn't replace.     |
+==============================================================================+

+==============================================================================+
| NAVIGATION & ENTRY                                                           |
+==============================================================================+
| Public Routes                   | Auth Routes              | App Entry     |
| /                          ○    | /login            ○      | /dashboard ○  |
| /how-it-works              ○    | /signup           ○      |               |
| /features                  ○    | /onboarding       ○      |               |
| /pricing                   ○    |                          |               |
| /privacy                   ○    |                          |               |
| /terms                     ○    |                          |               |
+------------------------------------------------------------------------------+

+==============================================================================+
| CORE ENTITIES                                                                |
+==============================================================================+
| User / Preference Profile        | Progress Credits    | Surprise Outcomes |
| - Category priorities       ○    | - Earned credits ○  | - Wish list item ○|
| - Risk boundaries           ○    | - Never expire   ✓  | - Discount       ○|
| - Wish list                 ○    | - Milestones     ○  | - Progress boost ○|
| - Bio, photo (optional)     ○    | - Not cash       ✓  | - Brand item     ○|
+------------------------------------------------------------------------------+
| Status: ○ All entities planned for MVP                                      |
+==============================================================================+

+==============================================================================+
| EXPRESS PREFERENCES (Layer 1: Capture)                                      |
+==============================================================================+
| /preferences - Preference Capture Interface                   | Status: ○   |
+------------------------------------------------------------------------------+
| EXPLICIT SELECTION                                                           |
| - Browse catalog                              ○                              |
| - Add to wish list                            ○                              |
| - Save specific items                         ○                              |
+------------------------------------------------------------------------------+
| COMPARATIVE CHOICE ("Pick 1 of 4")                                           |
| - System shows 4 similar items                ○                              |
| - User picks one                              ○                              |
| - Earns +10 progress credits                  ○                              |
| - System learns preferences                   ○                              |
+------------------------------------------------------------------------------+
| CATEGORY PRIORITY SYSTEM                                                     |
| 8 Gift Categories (drag-drop ranking):                         | Status: ○   |
| 1. Cash / Flexible Credit                                                    |
| 2. Experiences / Travel                                                      |
| 3. Food & Drink                                                              |
| 4. Clothing & Wearables                                                      |
| 5. Home / Lifestyle                                                          |
| 6. Tech / Gadgets                                                            |
| 7. Toys / Games / Fun                                                        |
| 8. Surprise Me                                                               |
+------------------------------------------------------------------------------+
| BOUNDARY SETTING                                                             |
| - Mark categories as "Never buy me this"     ○                              |
| - System respects boundaries                  ✓                              |
| - Surprises only from top-ranked categories   ✓                              |
+==============================================================================+

+==============================================================================+
| EARN PROGRESS (Layer 2: Accumulation)                                        |
+==============================================================================+
| /dashboard - Progress Display                                 | Status: ○   |
+------------------------------------------------------------------------------+
| PROGRESS CREDITS                                                             |
| - Earned per choice: +10 credits              ○                              |
| - Never expire or reset                       ✓                              |
| - Not cash, can't be withdrawn                ✓                              |
| - Visible progress bar                        ○                              |
| - Running total display                       ○                              |
+------------------------------------------------------------------------------+
| MILESTONES                                                                   |
| Milestone | Credits | Reward                                  | Status       |
| 1st       | 100     | Surprise chance                        | ○            |
| 2nd       | 200     | Surprise chance                        | ○            |
| Bonus     | 500     | Bonus reward                           | ○            |
+------------------------------------------------------------------------------+
| PROGRESS TRACKING                                                            |
| - Progress bar toward next milestone          ○                              |
| - "X credits away" messaging                  ○                              |
| - Milestone unlock notifications              ○                              |
+==============================================================================+

+==============================================================================+
| REFINE OVER TIME (Layer 3: Learning)                                         |
+==============================================================================+
| Preference Model (Background System)                          | Status: ○   |
+------------------------------------------------------------------------------+
| PREFERENCE LEARNING                                                          |
| - Taste patterns (style, brands, aesthetics)  ○                              |
| - Fit patterns (sizes, cuts, materials)       ○                              |
| - Risk tolerance (willing to try new?)        ○                              |
| - Identity alignment ("feels like you")       ○                              |
+------------------------------------------------------------------------------+
| ALGORITHM                                                                    |
| Input:                                                                       |
| - Past comparative choices                    ○                              |
| - Category rankings                           ○                              |
| - Explicit wish list items                    ○                              |
| - Boundaries                                  ○                              |
|                                                                              |
| Output:                                                                      |
| - Next "Pick 1 of 4" set                      ○                              |
| - Predicted items user will like             ○                              |
| - Improved surprise outcomes                  ○                              |
+==============================================================================+

+==============================================================================+
| ACCELERATE FULFILLMENT (Layer 4: Surprise)                                   |
+==============================================================================+
| /surprises - Surprise Reveal Interface                        | Status: ○   |
+------------------------------------------------------------------------------+
| SURPRISE MECHANICS                                                           |
| Trigger: Milestone reached (100, 200, 500)    ○                              |
| User Action: Click "See Your Surprise"        ○                              |
| No payment required                           ✓                              |
+------------------------------------------------------------------------------+
| SURPRISE OUTCOMES (Transparent Odds)                                         |
| Outcome              | Probability | Description              | Status      |
| Progress Boost       | 40%         | +50 bonus credits        | ○           |
| Discount             | 30%         | 10% off wish list item   | ○           |
| Wish List Item       | 15%         | Previously selected item | ○           |
| Brand Item           | 10%         | Sponsor-provided gift    | ○           |
| No Physical Item     | 5%          | Keep going! + retained   | ○           |
+------------------------------------------------------------------------------+
| REVEAL ANIMATION                                                             |
| - Smooth animation (Framer Motion)            ○                              |
| - Transparent odds always displayed           ✓                              |
| - Progress retained regardless                ✓                              |
| - No "spin" or "roll" framing                 ✓                              |
+------------------------------------------------------------------------------+
| RULES (Non-Negotiable)                                                       |
| ✓ No payment required to trigger                                            |
| ✓ No "spin" or "roll" framing                                               |
| ✓ No loss outcomes (progress always retained)                               |
| ✓ Transparent odds always displayed                                         |
| ✓ Milestone-based, not on-demand                                            |
+==============================================================================+

+==============================================================================+
| GIFT-SAFE PROFILE (Public Layer)                                             |
+==============================================================================+
| /u/[username] - Public Profile View                           | Status: ○   |
+------------------------------------------------------------------------------+
| PUBLIC PROFILE                                                               |
| - Shareable URL: /u/username                  ○                              |
| - Category priorities (safe → risky)          ○                              |
| - Wish list items                             ○                              |
| - Boundaries ("Never buy me...")              ○                              |
| - Progress state (optional)                   ○                              |
+------------------------------------------------------------------------------+
| FRIEND VIEW                                                                  |
| Display:                                                                     |
| - Safest categories (top 3)                   ○                              |
| - Risky categories (marked)                   ○                              |
| - Never buy list                              ○                              |
| - Current wish list items                     ○                              |
| - Progress toward items (optional)            ○                              |
+------------------------------------------------------------------------------+
| PRIVACY CONTROLS                                                             |
| - Public visibility toggle                    ○                              |
| - Share link copy button                      ○                              |
| - Privacy settings                            ○                              |
+==============================================================================+

+==============================================================================+
| MICRO-CONVERSION (Optional Accelerator)                                      |
+==============================================================================+
| /dashboard - Progress Boost Option                            | Status: ○   |
+------------------------------------------------------------------------------+
| ACCELERATE PROGRESS                                                          |
| - Pay $1 → +50 credits                        ○                              |
| - Framed as "speed up" not "buy chances"     ✓                              |
| - Limited to 3/month                          ○                              |
| - Never required                              ✓                              |
| - Stripe payment integration                  ○                              |
+------------------------------------------------------------------------------+
| PAYMENT FLOW                                                                 |
| Current Progress: X credits                   ○                              |
| Next Milestone: Y credits (Z away)            ○                              |
| "Want to reach it faster?"                    ○                              |
| [Pay $1 → +50 credits]                        ○                              |
| Optional messaging clear                      ✓                              |
+==============================================================================+

+==============================================================================+
| ADVANCED FEATURES (Phase 2+)                                                 |
+==============================================================================+
| BRAND DASHBOARD                                               | Status: ⊘   |
| - Upload product catalog                      ⊘                              |
| - Target demographics                         ⊘                              |
| - Engagement metrics                          ⊘                              |
| - Demand insights                             ⊘                              |
+------------------------------------------------------------------------------+
| FRIEND CO-FUNDING                                             | Status: ⊘   |
| - Create gift fund                            ⊘                              |
| - Invite friends to contribute                ⊘                              |
| - Vote on items                               ⊘                              |
| - Auto-purchase when funded                   ⊘                              |
+------------------------------------------------------------------------------+
| AI RECOMMENDATIONS                                            | Status: ⊘   |
| - Predict next items user will like          ⊘                              |
| - Auto-generate "Pick 1 of 4" sets           ⊘                              |
| - Optimize surprise outcomes                  ⊘                              |
| - Detect preference drift                     ⊘                              |
+==============================================================================+

+==============================================================================+
| SETTINGS & CONTROLS                                                          |
+==============================================================================+
| /settings - User Settings                                     | Status: ○   |
+------------------------------------------------------------------------------+
| ACCOUNT SETTINGS                                                             |
| - Email, password                             ○                              |
| - Profile (name, photo, bio)                  ○                              |
| - Delete account                              ○                              |
+------------------------------------------------------------------------------+
| PREFERENCE SETTINGS                                                          |
| - Edit category rankings                      ○                              |
| - Update boundaries                           ○                              |
| - Privacy controls                            ○                              |
+------------------------------------------------------------------------------+
| NOTIFICATIONS                                                                |
| - Email preferences                           ○                              |
| - Milestone alerts                            ○                              |
| - Friend gift notifications                   ○                              |
+==============================================================================+

+==============================================================================+
| SYSTEM HEALTH & STATES                                                       |
+==============================================================================+
| EMPTY STATES                                                  | Status: ○   |
| - Empty wish list                             ○                              |
| - No comparative choices yet                  ○                              |
| - No milestones reached                       ○                              |
+------------------------------------------------------------------------------+
| ERROR STATES                                                                 |
| - Failed API calls                            ○                              |
| - Payment failures                            ○                              |
| - Invalid form inputs                         ○                              |
+------------------------------------------------------------------------------+
| LOADING STATES                                                               |
| - Page transitions                            ○                              |
| - Surprise reveal loading                     ○                              |
| - Preference submission                       ○                              |
+==============================================================================+

+==============================================================================+
| LEGAL & ETHICAL DESIGN                                                       |
+==============================================================================+
| Non-Negotiable Constraints                    | Status: ✓                    |
| ❌ No pay-to-win                              | ✓ Enforced                   |
| ❌ No losses                                  | ✓ Enforced                   |
| ❌ No infinite replay loops                   | ✓ Milestone-gated            |
| ❌ No hidden odds                             | ✓ Transparent display        |
| ❌ No forced engagement                       | ✓ Optional only              |
+------------------------------------------------------------------------------+
| CORE PRINCIPLE: Progress always carries forward. Surprise accelerates but   |
| never replaces the path to what you want.                                   |
+==============================================================================+
```

---

## Route Map Summary

| Route | Purpose | Phase | Status |
|-------|---------|-------|--------|
| `/` | Marketing home | MVP | ○ |
| `/how-it-works` | Explainer | MVP | ○ |
| `/features` | Feature overview | MVP | ○ |
| `/pricing` | Pricing page | MVP | ○ |
| `/privacy` | Privacy policy | MVP | ○ |
| `/terms` | Terms of service | MVP | ○ |
| `/login` | Sign in | MVP | ○ |
| `/signup` | Create account | MVP | ○ |
| `/onboarding` | Category setup | MVP | ○ |
| `/dashboard` | Progress dashboard | MVP | ○ |
| `/preferences` | Comparative choice | MVP | ○ |
| `/wishlist` | Wish list view | MVP | ○ |
| `/surprises` | Surprise history | MVP | ○ |
| `/u/[username]` | Public profile | MVP | ○ |
| `/settings` | User settings | MVP | ○ |
| `/help` | Help/support | MVP | ○ |

See **docs/ux/SITEMAP.md** for complete route specifications.

---

## Feature Count by Status

| Status | Count | Percentage |
|--------|-------|------------|
| ✓ Built | 0 | 0% |
| ● In Progress | 0 | 0% |
| ○ Planned (MVP) | 45+ | 95% |
| ⊘ Deferred (Phase 2+) | 8 | 5% |

---

## MVP Rules (Non-Negotiables)

- **Full feature set at launch** - No deferred core features
- Progress credits NEVER expire or reset
- Surprises are OPTIONAL (not core path)
- Transparent odds always displayed
- No pay-to-win mechanics
- No loss outcomes
- Category boundaries respected
- NOT gambling, NOT raffle, NOT layaway

---

## When to Update This Document

Update PRODUCT_MAP.md when:
- Adding a new feature
- Changing feature status (○ → ● → ✓)
- Modifying core mechanics
- Adjusting user flows
- Changing route structure

**Rule:** All features must exist here FIRST before being implemented or documented elsewhere.

---

**Preference-first. Boundary-aware. Progress-driven.**
