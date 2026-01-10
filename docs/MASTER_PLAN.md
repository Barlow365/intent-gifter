# Intent Gifter: Research & Implementation Plan

## Executive Summary

Build a **preference-driven gifting platform** that provides:
1. **Preference capture without feeling demanding** - Express what fits you through comparative choices
2. **Progress that never expires** - Credits persist forever, building trust
3. **Optional surprise mechanics** - Accelerate fulfillment without gambling
4. **Gift-safe profiles** - Help friends give meaningful gifts
5. **Boundary respect** - Never buy categories work effectively

**Measurable Win**: Preference learning accuracy - system correctly predicts user preferences
- Track: comparative choices made → preference model accuracy → gift match rate
- Target: 80%+ accuracy in predicting user's preferred items from choices

**Target**: Hard-to-shop-for people, gift recipients, thoughtful gifters who want to avoid bad gifts.

**Architecture**: React/Next.js frontend + Node.js/Express backend + PostgreSQL + Redis

**Platform**: Web-first (responsive PWA) with full feature set at launch

**MVP Includes Everything**: Preference capture (explicit + comparative), progress credits, milestone surprises, gift-safe profiles, category priority system, micro-conversion option - all in MVP. No deferred features.

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Competitive Landscape Research](#competitive-landscape-research)
3. [User Requirements](#user-requirements)
4. [Architecture Design](#architecture-design)
5. [Core Innovation: Preference Resolution System](#core-innovation-preference-resolution-system)
6. [Feature System](#feature-system-express--earn--refine--accelerate)
7. [Real-Value Innovations](#real-value-innovations)
8. [Feature Milestones](#feature-milestones-full-mvp---no-phasing)
9. [AI/ML Integration](#aiml-integration)
10. [Database Schema](#database-schema)
11. [Critical Files to Create](#critical-files-to-create)
12. [Differentiation Summary](#differentiation-summary)
13. [Implementation Roadmap](#implementation-roadmap-phased)
14. [Complete Application Sitemap](#complete-application-sitemap)
15. [Open Questions / Decisions](#open-questions--decisions)
16. [Sources](#sources)

---

## Competitive Landscape Research

### Feature Comparison Matrix

| Platform | Pricing | Strengths | Weaknesses | Preference Learning |
|----------|---------|-----------|------------|---------------------|
| **Wishlists (Amazon, etc.)** | Free | Simple, integrated | Static, goes stale | None |
| **Giftster** | $20/yr | Organized wishlists | No preference learning | None |
| **Elfster** | Free | Group gift exchange | Focus on exchange, not learning | None |
| **Prezzybox** | Free | Gift ideas | Not personalized | Basic categories |
| **StoryWorth** | $79 | Experience-based | Narrow focus (stories) | None |
| **Sweepstakes Apps** | Free | Surprise/delight | Gambling mechanics | None |

### Key Insight: Our Differentiator

**NOT** "another wishlist app" - Amazon, Giftster already do that.
**NOT** "surprise boxes" - Too random, no learning.

**Our claim**: The only platform that combines:
1. **Preference learning without demanding** - Comparative choices feel like a game
2. **Progress that never expires** - Build trust, not urgency
3. **Surprise without gambling** - Transparent odds, no losses
4. **Boundary respect** - Categories you never want work
5. **Gift-safe profiles** - Help friends give better gifts

### Market Position Analysis

```
               High Preference Learning
                       │
                       │
        INTENT GIFTER ★│  AI Recommendation
        (our position) │  Engines
                       │
                       │
───────────────────────┼───────────────────────
                       │
        Wishlists      │  Surprise Boxes
        (Amazon,       │  (Random, no learning)
         Giftster)     │
                       │
               Low Preference Learning
```

**Gap in market**: No platform learns preferences while respecting boundaries and avoiding gambling mechanics.

---

## User Requirements

### The Core Problem (What the market still fails at)

Most wishlists solve remembering what you want.
Some recommendation engines solve suggesting items.
A few surprise mechanics solve delight.

**None solve the real-life system people live in:**
- People have preferences but feel awkward demanding specific gifts
- Wishlists go stale (added 2 years ago, never updated)
- Surprises often miss badly ("Why would you buy me this?")
- Hard-to-shop-for people say "I don't want anything"
- Gift categories have varying comfort levels (cash OK, clothing risky)
- Friends want to give good gifts but lack information

**People don't need another wishlist. They need a preference resolution system.**

### Pain Points Identified

| Pain Point | Current Workaround | Impact |
|------------|-------------------|--------|
| **Can't express preferences without feeling demanding** | Stay silent, get bad gifts | Disappointment |
| **Wishlists go stale** | Never update, gifts miss | Waste |
| **Surprises feel random** | Hope for the best | Bad gifts |
| **Gift categories vary in comfort** | Verbal hints ("not clothing") | Misunderstandings |
| **Friends lack information** | Ask directly (awkward) | Stress |

### The Mental Model (How users think)

People think in **fit and boundaries**, not specific items:
- "I like practical things, not novelties."
- "Food and experiences are always safe bets."
- "Don't buy me clothing—it never fits."
- "I want to move closer to items I actually want."

**The app mirrors this reality.**

### Priority Features Requested

1. **Comparative preference capture** - "Pick 1 of 4" feels like a game
2. **Progress that persists** - Credits never expire, build trust
3. **Gift-safe profiles** - Friends see what's safe vs. risky
4. **Category boundaries** - "Never buy me..." actually works
5. **Optional surprises** - Accelerate without gambling
6. **Transparent odds** - Always know the probabilities

---

## Architecture Design

### Technology Stack

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Framework** | React + TypeScript | Type safety, component reusability |
| **Build Tool** | Next.js 14+ (App Router) | SSR, file-based routing |
| **UI Library** | Tailwind CSS + shadcn/ui | Rapid development, consistent design |
| **Animations** | Framer Motion | Smooth surprise reveals |
| **State Management** | Zustand | Simple, performant |
| **Forms** | React Hook Form + Zod | Type-safe validation |

### Backend

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Framework** | Node.js + Express | Fast, JavaScript full-stack |
| **Authentication** | JWT + bcrypt | Stateless auth, secure passwords |
| **Validation** | Zod (shared with frontend) | Single source of truth |
| **Payments** | Stripe | Micro-conversions ($1-$3) |

### Database

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Primary DB** | PostgreSQL | ACID compliance, JSON support |
| **Cache Layer** | Redis | Fast in-memory cache |

### Infrastructure

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Hosting** | Vercel (frontend) + Railway (backend) | Simple deployment |
| **CDN** | Cloudflare | Global edge caching |
| **File Storage** | AWS S3 | Product images |
| **Monitoring** | Sentry (errors) + PostHog (analytics) | Error tracking, user behavior |

### External Services

| Service | Purpose | Phase |
|---------|---------|-------|
| **Email** | Resend / SendGrid | Transactional emails | MVP |
| **Payments** | Stripe | Micro-conversions | MVP |
| **AI/ML** | Custom recommendation engine | Preference matching | MVP |

---

### High-Level Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                         CLIENT LAYER                            │
├─────────────────────────────────────────────────────────────────┤
│  Web App (React + TypeScript + Tailwind)                        │
│  - Desktop browsers                                             │
│  - Mobile browsers (responsive PWA)                             │
└──────────────────────┬──────────────────────────────────────────┘
                       │ HTTPS
                       ▼
┌─────────────────────────────────────────────────────────────────┐
│                        API GATEWAY LAYER                        │
├─────────────────────────────────────────────────────────────────┤
│  Cloudflare (CDN + DDoS protection)                             │
│  - Rate limiting                                                │
│  - SSL termination                                              │
└──────────────────────┬──────────────────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────────────────┐
│                      APPLICATION LAYER                          │
├─────────────────────────────────────────────────────────────────┤
│  Node.js API Server (Express)                                   │
│  ├── REST API (CRUD operations)                                 │
│  ├── Authentication (JWT)                                       │
│  ├── Recommendation Engine (preference matching)                │
│  └── Background Workers (email notifications)                   │
└──────────────────────┬──────────────────────────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────────────────────────┐
│                         DATA LAYER                              │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────────┐  ┌─────────────────┐  ┌─────────────────┐ │
│  │  PostgreSQL     │  │  Redis          │  │  S3             │ │
│  │  (Primary DB)   │  │  (Cache/Queue)  │  │  (File Storage) │ │
│  │  - Users        │  │  - Sessions     │  │  - Product imgs │ │
│  │  - Preferences  │  │  - Cache        │  │                 │ │
│  │  - Progress     │  │                 │  │                 │ │
│  │  - Surprises    │  │                 │  │                 │ │
│  └─────────────────┘  └─────────────────┘  └─────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
```

---

## Core Innovation: Preference Resolution System

### The Mental Model

**This is NOT a wishlist—it's a preference learning system.**

Users express preferences through:
- **Explicit Selection** - "I want this specific thing" (traditional wishlist)
- **Comparative Choice** - "Which of these 4 feels most like me?" (learning mechanism)
- **Category Ranking** - Drag-drop 8 categories from safe → risky
- **Boundary Setting** - "Never buy me..." works

### Core Objects (The System)

#### User Profile

Properties:
| Field | Description |
|-------|-------------|
| **Category Rankings** | Drag-drop priority order (1-8) |
| **Boundaries** | "Never buy me this" categories |
| **Wish List** | Explicit items added |
| **Progress Credits** | Earned credits (never expire) |

#### Preference Selection

Each comparative choice:
| Field | Description |
|-------|-------------|
| **Items Shown** | 4 items presented |
| **Selected Item** | Which one user picked |
| **Category** | Which category it's from |
| **Timestamp** | When choice was made |
| **Credits Earned** | +10 per meaningful choice |

#### The Progress Spine

Progress is not a feature—it's the spine that runs through everything:
- Always visible in the UI
- Updates as choices are made
- Drives milestone unlocks
- Never expires

---

## Feature System: Express → Earn → Refine → Accelerate

### EXPRESS PREFERENCES

#### 1. Explicit Selection (Traditional Wishlist)

**Input:**
```
Browse catalog → Add "Nike Jacket" to wish list
```

**Output:**
- Item saved to wish list
- No credits earned (this is explicit asking)

#### 2. Comparative Choice ("Pick 1 of 4")

**User sees:**
```
Which one feels most like you?

[A] Coffee Maker ($80)
[B] Coffee Subscription ($40)
[C] French Press ($25)
[D] Electric Kettle ($50)
```

**User picks B**

**System:**
- Records selection → preference model
- Earns +10 credits
- Updates algorithm
- Shows next set

| Feature | Behavior |
|---------|----------|
| **Items shown** | 1 previously favored + 3 close alternatives |
| **Categories** | Only from top-ranked categories |
| **Credits earned** | +10 per choice |
| **Learning** | Updates preference model |

#### 3. Category Priority System

**8 Gift Categories (drag-drop ranking):**
1. Cash / Flexible Credit
2. Experiences / Travel
3. Food & Drink
4. Clothing & Wearables
5. Home / Lifestyle
6. Tech / Gadgets
7. Toys / Games / Fun
8. Surprise Me

**Boundaries:**
- Mark categories as "Never buy me this"
- System respects boundaries (no items from blocked categories)
- Surprises only come from top-ranked categories

### EARN PROGRESS

#### Progress Credits

| Element | Description |
|---------|-------------|
| **Earned** | +10 per comparative choice |
| **Never Expire** | Credits persist forever |
| **Not Cash** | Can't withdraw, only unlock value |
| **Transparent** | Always show current state |

#### Milestones

| Credits | Milestone | Reward |
|---------|-----------|--------|
| 100 | 1st surprise | Unlock surprise chance |
| 200 | 2nd surprise | Unlock surprise chance |
| 500 | Bonus | Unlock bonus reward |

### REFINE OVER TIME

#### Preference Learning

System learns:
- **Taste patterns** - Style, brands, aesthetics
- **Fit patterns** - Sizes, cuts, materials
- **Risk tolerance** - Willing to try new categories?
- **Identity alignment** - What "feels like you"

#### Algorithm

**Input:**
- Past comparative choices
- Category rankings
- Explicit wish list items
- Boundaries

**Output:**
- Next "Pick 1 of 4" set optimized for learning
- Predicted items user will like
- Improved surprise outcomes

### ACCELERATE FULFILLMENT

#### Surprise Mechanics

**Trigger:** Milestone reached (100, 200, 500 credits)

**User Action:** Click "See Your Surprise"

**Outcomes (Transparent Odds):**

| Outcome | Probability | Description |
|---------|-------------|-------------|
| **Progress Boost** | 40% | +50 bonus credits |
| **Discount** | 30% | 10% off wish list item |
| **Wish List Item** | 15% | Previously selected item |
| **Brand Item** | 10% | Sponsor-provided gift |
| **No Physical Item** | 5% | "Keep going!" message + credits retained |

**Rules:**
- No payment required to trigger
- No "spin" or "roll" framing
- No loss outcomes (progress always retained)
- Transparent odds always displayed

#### Optional Micro-Conversion

**Accelerate Progress:**
- Pay $1 → gain +50 credits
- Framed as "speed up" not "buy chances"
- Limited to 3/month
- Never required

---

## Real-Value Innovations

### What We're NOT Building (Gimmicky)

| Feature | Why Skip |
|---------|----------|
| Gamification badges/streaks | Not about points, about preferences |
| Social feeds / influencer content | Not Instagram for gifts |
| Complex AI chatbots | Over-engineered |
| Achievement systems | Patronizing |
| Loot box mechanics | Gambling stigma |

### What We ARE Building (Real Value - All MVP)

| Innovation | Value |
|------------|-------|
| **Comparative Choice** | Preference capture without demanding |
| **Never-Expiring Progress** | Build trust, not urgency |
| **Transparent Surprise Odds** | Delight without gambling |
| **Category Boundaries** | Respect comfort zones |
| **Gift-Safe Profiles** | Help friends give better gifts |
| **Preference Learning** | System gets smarter over time |

**Principle:** Every innovation must answer: "Does this help people get gifts they actually want?" If no, don't build it.

---

## Feature Milestones (Full MVP - No Phasing)

**Everything ships in MVP. No deferred features. Full automation from day one.**

### Milestone 1 - Foundation Layer

**Goal:** Core infrastructure and routing

- Routes: implement full route map from SITEMAP
- Global layout: header, nav, progress bar
- All pages render (no stubs, full implementations)
- States: empty, error, loading
- Testing: route smoke tests + layout snapshot
- Auth: signup, login, onboarding flow

**Exit Criteria:**
- [ ] Every route renders with full UI
- [ ] Auth flow complete
- [ ] Progress bar visible on all pages

### Milestone 2 - Preference Capture

**Goal:** Complete preference capture system

- Category ranking: drag-drop 8 categories
- Boundary setting: mark "Never buy me..." categories
- Explicit selection: browse + add to wish list
- Comparative choice: "Pick 1 of 4" interface
- Progress credits: +10 per choice, display credits
- Preference model: record selections, update algorithm

**Exit Criteria:**
- [ ] Can rank categories and set boundaries
- [ ] Can add items to wish list
- [ ] Comparative choice works and earns credits
- [ ] Progress credits display correctly

### Milestone 3 - Progress & Milestones

**Goal:** Progress tracking and milestone system

- Progress display: "You have 250 credits"
- Progress bar: visual toward next milestone
- Milestone tracking: 100/200/500 thresholds
- Milestone unlock: banner when reached
- Never expire: credits persist forever

**Exit Criteria:**
- [ ] Progress displays correctly
- [ ] Milestones trigger at right thresholds
- [ ] Banner appears when milestone reached

### Milestone 4 - Surprise Mechanics

**Goal:** Surprise reveal system

- Surprise trigger: click "See Your Surprise"
- Outcome algorithm: transparent probability distribution
- Reveal animation: smooth animation (Framer Motion)
- Outcome types: progress boost, discount, item, brand item, no item
- Odds display: always show probabilities upfront

**Exit Criteria:**
- [ ] Surprise trigger works at milestones
- [ ] Reveal animation is smooth
- [ ] All outcome types work correctly
- [ ] Odds are transparent

### Milestone 5 - Gift-Safe Profiles

**Goal:** Public shareable profiles

- Public profile URL: `/u/username`
- Profile display: category rankings, wish list, boundaries, progress
- Friend view: see what's safe vs. risky
- Share link: copyable link for friends
- Privacy: only show what user allows

**Exit Criteria:**
- [ ] Profile URL works and is shareable
- [ ] Friend view displays correctly
- [ ] Privacy settings respected

### Milestone 6 - Micro-Conversion

**Goal:** Optional progress acceleration

- Payment integration: Stripe for $1 micro-conversions
- Progress boost: pay $1 → +50 credits
- Limit enforcement: max 3/month
- Framing: "speed up" not "buy chances"
- Optional: never required

**Exit Criteria:**
- [ ] Payment flow works via Stripe
- [ ] Progress boost applied correctly
- [ ] Monthly limit enforced
- [ ] Clear "optional" framing

### Milestone 7 - Recommendation Engine

**Goal:** Smart preference matching

- Algorithm: collaborative filtering + content-based
- Next set generation: optimized "Pick 1 of 4"
- Explore/exploit: 70% similar, 30% new
- Category filtering: respect boundaries
- Learning: improve over time

**Exit Criteria:**
- [ ] Recommendation engine generates good sets
- [ ] Respects category boundaries
- [ ] Improves with more data

### Milestone 8 - Polish & Marketing

**Goal:** Public launch readiness

- Marketing pages: home, how-it-works, features, pricing, privacy, terms
- Dashboard: progress snapshot, quick actions
- Settings: profile, preferences, notifications
- Help: FAQ, support contact
- Performance: optimize load times
- Accessibility: WCAG 2.1 AA compliance

**Exit Criteria:**
- [ ] All marketing pages complete
- [ ] Lighthouse score > 90
- [ ] Mobile experience polished
- [ ] Help content complete

---

## AI/ML Integration

### Preference Matching Algorithm

**Input:**
```python
{
  "user_id": "123",
  "past_choices": [
    {"item_id": "A", "category": "Food & Drink"},
    {"item_id": "B", "category": "Food & Drink"},
    {"item_id": "D", "category": "Experiences"}
  ],
  "category_rankings": [1, 2, 3, 4, 5, 6, 7, 8],
  "boundaries": ["Clothing", "Jewelry"]
}
```

**Output:**
```python
{
  "next_set": [
    {"item_id": "X", "score": 0.92, "category": "Food & Drink"},
    {"item_id": "Y", "score": 0.85, "category": "Food & Drink"},
    {"item_id": "Z", "score": 0.78, "category": "Experiences"},
    {"item_id": "W", "score": 0.65, "category": "Home"}
  ]
}
```

**Algorithm:**
1. Score all items based on past choices (collaborative filtering)
2. Filter out boundary categories
3. Prioritize top-ranked categories
4. Include 1 previously favored + 3 alternatives
5. Balance explore (30%) vs. exploit (70%)

### Surprise Outcome Generator

**Input:** User milestone (100, 200, 500 credits)

**Output:**
```python
def generate_surprise(user_id, milestone):
    # Get user's top categories
    top_categories = get_user_top_categories(user_id, limit=3)

    # Roll for outcome type
    outcome_roll = random.uniform(0, 1)

    if outcome_roll < 0.40:  # 40% Progress Boost
        return {"type": "progress_boost", "value": 50}
    elif outcome_roll < 0.70:  # 30% Discount
        wish_list_item = random.choice(get_wish_list(user_id))
        return {"type": "discount", "value": 0.10, "item": wish_list_item}
    elif outcome_roll < 0.85:  # 15% Wish List Item
        item = random.choice(get_wish_list(user_id))
        return {"type": "wish_list_item", "item": item}
    elif outcome_roll < 0.95:  # 10% Brand Item
        brand_item = get_brand_inventory(top_categories)
        return {"type": "brand_item", "item": brand_item}
    else:  # 5% No Item
        return {"type": "no_item", "message": "Keep going!"}
```

---

## Database Schema

### Users Table

```sql
CREATE TABLE users (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  email VARCHAR(255) UNIQUE NOT NULL,
  password_hash VARCHAR(255) NOT NULL,
  username VARCHAR(50) UNIQUE NOT NULL,
  name VARCHAR(255),
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_users_email ON users(email);
CREATE INDEX idx_users_username ON users(username);
```

### User Profiles Table

```sql
CREATE TABLE user_profiles (
  user_id UUID PRIMARY KEY REFERENCES users(id) ON DELETE CASCADE,
  category_rankings JSONB, -- [1,2,3,4,5,6,7,8]
  boundaries TEXT[], -- ["Clothing", "Jewelry"]
  bio TEXT,
  avatar_url VARCHAR(500),
  created_at TIMESTAMP DEFAULT NOW(),
  updated_at TIMESTAMP DEFAULT NOW()
);
```

### Preference Choices Table

```sql
CREATE TABLE preference_choices (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  items_shown JSONB, -- [item_id, item_id, item_id, item_id]
  selected_item_id UUID,
  category VARCHAR(50),
  credits_earned INTEGER DEFAULT 10,
  created_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_preference_choices_user_id ON preference_choices(user_id);
CREATE INDEX idx_preference_choices_created_at ON preference_choices(created_at);
```

### Progress Table

```sql
CREATE TABLE progress (
  user_id UUID PRIMARY KEY REFERENCES users(id) ON DELETE CASCADE,
  total_credits INTEGER DEFAULT 0,
  milestone_100_reached BOOLEAN DEFAULT FALSE,
  milestone_200_reached BOOLEAN DEFAULT FALSE,
  milestone_500_reached BOOLEAN DEFAULT FALSE,
  last_updated TIMESTAMP DEFAULT NOW()
);
```

### Wish List Items Table

```sql
CREATE TABLE wish_list_items (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  item_name VARCHAR(255) NOT NULL,
  item_url VARCHAR(500),
  item_image_url VARCHAR(500),
  price DECIMAL(10, 2),
  category VARCHAR(50),
  added_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_wish_list_items_user_id ON wish_list_items(user_id);
```

### Surprises Table

```sql
CREATE TABLE surprises (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  milestone INTEGER NOT NULL, -- 100, 200, 500
  outcome_type VARCHAR(50) NOT NULL, -- progress_boost, discount, wish_list_item, brand_item, no_item
  outcome_value JSONB, -- {"credits": 50} or {"discount": 0.10, "item_id": "..."}
  triggered_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_surprises_user_id ON surprises(user_id);
```

### Gifts Table

```sql
CREATE TABLE gifts (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  giver_id UUID REFERENCES users(id),
  recipient_id UUID REFERENCES users(id) ON DELETE CASCADE,
  item_id UUID REFERENCES wish_list_items(id),
  amount DECIMAL(10, 2),
  status VARCHAR(20) CHECK (status IN ('pending', 'purchased', 'delivered')),
  created_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_gifts_recipient_id ON gifts(recipient_id);
CREATE INDEX idx_gifts_giver_id ON gifts(giver_id);
```

### Micro-Conversions Table

```sql
CREATE TABLE micro_conversions (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  user_id UUID REFERENCES users(id) ON DELETE CASCADE,
  amount DECIMAL(10, 2) NOT NULL,
  credits_purchased INTEGER NOT NULL,
  stripe_payment_id VARCHAR(255),
  created_at TIMESTAMP DEFAULT NOW()
);

CREATE INDEX idx_micro_conversions_user_id ON micro_conversions(user_id);
CREATE INDEX idx_micro_conversions_created_at ON micro_conversions(created_at);
```

---

## Critical Files to Create

### Project Structure

```
/web/                          # Next.js Application
├── app/
│   ├── (marketing)/          # Public pages
│   │   ├── page.tsx          # Home
│   │   ├── how-it-works/
│   │   │   └── page.tsx
│   │   ├── features/
│   │   │   └── page.tsx
│   │   ├── pricing/
│   │   │   └── page.tsx
│   │   ├── privacy/
│   │   │   └── page.tsx
│   │   └── terms/
│   │       └── page.tsx
│   ├── (auth)/               # Auth routes
│   │   ├── login/
│   │   │   └── page.tsx
│   │   ├── signup/
│   │   │   └── page.tsx
│   │   └── onboarding/
│   │       └── page.tsx
│   ├── (app)/                # Main app (authenticated)
│   │   ├── layout.tsx        # App shell with nav
│   │   ├── dashboard/
│   │   │   └── page.tsx      # Dashboard
│   │   ├── preferences/
│   │   │   └── page.tsx      # Comparative choice UI
│   │   ├── wishlist/
│   │   │   └── page.tsx      # Wish list view
│   │   ├── surprises/
│   │   │   └── page.tsx      # Surprise history
│   │   ├── u/
│   │   │   └── [username]/
│   │   │       └── page.tsx  # Public profile
│   │   └── settings/
│   │       └── page.tsx
│   └── layout.tsx            # Root layout
├── components/
│   ├── preferences/
│   │   ├── comparative-choice.tsx
│   │   ├── category-ranking.tsx
│   │   └── boundary-selector.tsx
│   ├── progress/
│   │   ├── progress-bar.tsx
│   │   ├── milestone-banner.tsx
│   │   └── credits-display.tsx
│   ├── surprise/
│   │   ├── surprise-trigger.tsx
│   │   ├── reveal-animation.tsx
│   │   └── outcome-display.tsx
│   ├── profile/
│   │   ├── gift-safe-profile.tsx
│   │   └── share-link.tsx
│   └── ui/                   # shadcn/ui components
│       ├── button.tsx
│       ├── input.tsx
│       ├── dialog.tsx
│       └── ...
├── lib/
│   ├── api-client.ts         # API fetch wrapper
│   ├── utils.ts              # Utility functions
│   └── hooks/
│       ├── use-preferences.ts
│       ├── use-progress.ts
│       └── use-surprises.ts
├── stores/                   # Zustand stores
│   ├── user-store.ts
│   ├── preferences-store.ts
│   └── ui-store.ts
└── package.json

/api/                          # Node.js Backend
├── src/
│   ├── index.ts              # Entry point
│   ├── app.ts                # Express app setup
│   ├── routes/
│   │   ├── auth.ts
│   │   ├── preferences.ts
│   │   ├── progress.ts
│   │   ├── surprises.ts
│   │   ├── profile.ts
│   │   └── gifts.ts
│   ├── services/
│   │   ├── auth.ts
│   │   ├── recommendation.ts
│   │   ├── surprise-generator.ts
│   │   └── payment.ts
│   ├── middleware/
│   │   ├── auth.ts
│   │   ├── validate.ts
│   │   └── error-handler.ts
│   ├── db/
│   │   ├── schema.sql
│   │   ├── client.ts
│   │   └── migrations/
│   └── types/
│       └── index.ts
├── package.json
└── tsconfig.json
```

---

## Differentiation Summary

### What Makes Intent Gifter Unique

| Differentiator | Description | Competitors |
|----------------|-------------|-------------|
| **Preference capture without demanding** | Comparative choice feels like a game | None have this |
| **Progress that never expires** | Build trust, not urgency | None |
| **Surprise without gambling** | Transparent odds, no losses | None (sweepstakes are gambling) |
| **Category boundaries** | "Never buy me..." actually works | None |
| **Gift-safe profiles** | Help friends give better gifts | None |
| **Learning system** | Gets smarter over time | Wishlists are static |

### What We DON'T Claim (Competitors Already Do)

| Feature | Who Does It |
|---------|-------------|
| "Wishlists" | Amazon, Giftster |
| "Gift ideas" | Prezzybox |
| "Group gift exchange" | Elfster |

### Technical Moat

1. **Preference learning database** - More choices = better recommendations
2. **Boundary respect system** - Trust in the system increases engagement
3. **Transparent surprise mechanics** - Legal clarity (not gambling)

---

## Implementation Roadmap (Phased)

Each phase builds on the previous. Every phase includes: implementation, tests, and demo.

---

### Phase 1: Foundation

**Build:** Auth system, database, basic routing

| Create | Test | Demo |
|--------|------|------|
| User signup/login/logout | Auth flow e2e test | User can create account and log in |
| PostgreSQL schema (users, profiles, preferences) | Schema migrations run | Database populated |
| Basic routing structure | All routes render | Navigate between pages |
| Onboarding flow | Onboarding e2e test | New user ranks categories |

**Exit Criteria:**
- [ ] User can sign up, log in, create profile
- [ ] Database persists data correctly
- [ ] All routes accessible

---

### Phase 2: Preference Capture

**Build:** Category ranking, comparative choice, wish list

| Create | Test | Demo |
|--------|------|------|
| Category ranking UI (drag-drop) | Ranking save test | Drag categories to reorder |
| Boundary selector | Boundary save test | Mark "Never buy me..." |
| Wish list (explicit selection) | Wish list CRUD test | Add/remove items |
| Comparative choice UI ("Pick 1 of 4") | Choice recording test | Select item, earn credits |
| Progress credits display | Credit calculation test | Credits update on selection |

**Exit Criteria:**
- [ ] Can rank categories and set boundaries
- [ ] Can add items to wish list
- [ ] Comparative choice works and earns credits
- [ ] Progress displays correctly

---

### Phase 3: Progress & Milestones

**Build:** Progress tracking, milestone system

| Create | Test | Demo |
|--------|------|------|
| Progress bar component | Progress calculation test | Visual bar updates |
| Milestone tracking | Milestone trigger test | 100/200/500 thresholds |
| Milestone banner | Banner display test | Shows when milestone reached |
| Credit persistence | Never expire test | Credits persist across sessions |

**Exit Criteria:**
- [ ] Progress bar displays correctly
- [ ] Milestones trigger at right thresholds
- [ ] Credits never expire

---

### Phase 4: Surprise Mechanics

**Build:** Surprise reveal system

| Create | Test | Demo |
|--------|------|------|
| Surprise trigger button | Trigger test | Click "See Your Surprise" |
| Outcome algorithm | Probability test | Correct distribution |
| Reveal animation (Framer Motion) | Animation test | Smooth reveal |
| Outcome types | All types test | Progress, discount, item, brand, no item |
| Odds display | Transparency test | Show probabilities upfront |

**Exit Criteria:**
- [ ] Surprise trigger works at milestones
- [ ] Reveal animation is smooth
- [ ] All outcome types work
- [ ] Odds are transparent

---

### Phase 5: Gift-Safe Profiles

**Build:** Public shareable profiles

| Create | Test | Demo |
|--------|------|------|
| Public profile page | Profile render test | `/u/username` works |
| Profile display | Data display test | Show categories, wish list, boundaries |
| Share link | Link copy test | Copyable link for friends |
| Privacy settings | Privacy test | Respect user settings |

**Exit Criteria:**
- [ ] Profile URL works and is shareable
- [ ] Friend view displays correctly
- [ ] Privacy settings respected

---

### Phase 6: Micro-Conversion

**Build:** Optional progress acceleration

| Create | Test | Demo |
|--------|------|------|
| Stripe integration | Payment test | Pay $1 via Stripe |
| Progress boost | Credit addition test | +50 credits applied |
| Monthly limit | Limit enforcement test | Max 3/month enforced |
| Optional framing | Messaging test | "Speed up" not "buy chances" |

**Exit Criteria:**
- [ ] Payment flow works via Stripe
- [ ] Progress boost applied correctly
- [ ] Monthly limit enforced
- [ ] Clear "optional" framing

---

### Phase 7: Recommendation Engine

**Build:** Smart preference matching

| Create | Test | Demo |
|--------|------|------|
| Recommendation algorithm | Matching accuracy test | Good "Pick 1 of 4" sets |
| Collaborative filtering | Filter test | Similar users → similar items |
| Content-based filtering | Content test | Item attributes match |
| Explore/exploit balance | Balance test | 70% similar, 30% new |
| Boundary filtering | Boundary test | Respect "Never buy me..." |

**Exit Criteria:**
- [ ] Recommendation engine generates good sets
- [ ] Respects category boundaries
- [ ] Improves with more data

---

### Phase 8: Polish & Marketing

**Build:** Public launch readiness

| Create | Test | Demo |
|--------|------|------|
| Marketing home page | Page render test | Value prop clear |
| How it works page | Page render test | 4-step flow explained |
| Features page | Page render test | Feature grid |
| Pricing page | Page render test | Free + optional $1 explained |
| Privacy/Terms pages | Page render test | Legal content |
| Settings page | Settings test | Profile, preferences |
| Help page | Help render test | FAQ, support contact |
| Performance optimization | Lighthouse audit | Score > 90 |
| Accessibility audit | a11y test | WCAG 2.1 AA |

**Exit Criteria:**
- [ ] All marketing pages complete
- [ ] Lighthouse score > 90
- [ ] Accessibility compliant
- [ ] Mobile experience polished

---

### Phase Summary

| Phase | Focus | Key Pages |
|-------|-------|-----------|
| 1 | Foundation | login, signup, onboarding |
| 2 | Preferences | preferences, wishlist |
| 3 | Progress | dashboard, progress |
| 4 | Surprises | surprises, reveal |
| 5 | Profiles | profile, share |
| 6 | Payments | micro-conversion |
| 7 | AI | recommendation engine |
| 8 | Launch | marketing, settings, help |

**Total:** 8 phases

---

## Complete Application Sitemap

### Site Architecture Overview

**Route Pattern**: Authenticated app routes use `/dashboard`, `/preferences`, etc.

```
/                           → Marketing home (redirect to /dashboard if logged in)
├── /how-it-works           → Marketing: How it works
├── /features               → Marketing: Features overview
├── /pricing                → Marketing: Pricing (free + optional $1)
├── /privacy                → Marketing: Privacy policy
├── /terms                  → Marketing: Terms of service
│
├── /login                  → Auth: Sign in
├── /signup                 → Auth: Create account
├── /onboarding             → Auth: Category ranking setup
│
├── /dashboard              → Dashboard: Progress snapshot, quick actions
│
├── /preferences            → Comparative choice ("Pick 1 of 4")
│
├── /wishlist               → Explicit wish list items
│
├── /surprises              → Surprise history and trigger
│
├── /u/[username]           → Public gift-safe profile (shareable)
│
├── /settings               → User preferences, account, notifications
│
└── /help                   → FAQ, support contact
```

### Complete Page Index (12 Routes)

| # | Route | Purpose | Phase |
|---|-------|---------|-------|
| 1 | `/` | Marketing home | 8 |
| 2 | `/how-it-works` | How it works | 8 |
| 3 | `/features` | Features overview | 8 |
| 4 | `/pricing` | Pricing | 8 |
| 5 | `/privacy` | Privacy policy | 8 |
| 6 | `/terms` | Terms of service | 8 |
| 7 | `/login` | Sign in | 1 |
| 8 | `/signup` | Create account | 1 |
| 9 | `/onboarding` | Category ranking setup | 1 |
| 10 | `/dashboard` | Dashboard | 3 |
| 11 | `/preferences` | Comparative choice | 2 |
| 12 | `/wishlist` | Wish list | 2 |
| 13 | `/surprises` | Surprises | 4 |
| 14 | `/u/[username]` | Public profile | 5 |
| 15 | `/settings` | Settings | 8 |
| 16 | `/help` | Help/support | 8 |

---

## Open Questions / Decisions

| Question | Options | Recommendation | Decision |
|----------|---------|----------------|----------|
| **Auth method** | Email/password vs OAuth | Email/password for MVP | TBD |
| **Mobile** | PWA vs Native | PWA for v1 | TBD |
| **AI provider** | Custom vs third-party | Custom (scikit-learn) | TBD |
| **Brand partnerships** | Launch with vs without | Manual fulfillment MVP | TBD |

---

## Sources

### Market Research

- Gift retailing market: $93.2B (2024) → $111.4B (2030) at 3% CAGR
- Source: December 2025 market report

### Competitor Analysis

- Amazon Wishlists: https://www.amazon.com/registries
- Giftster: https://www.giftster.com
- Elfster: https://www.elfster.com

### Technology Documentation

- Next.js: https://nextjs.org/docs
- Framer Motion: https://www.framer.com/motion/
- Tailwind CSS: https://tailwindcss.com/docs
- shadcn/ui: https://ui.shadcn.com
- PostgreSQL: https://www.postgresql.org/docs
- Zustand: https://zustand-demo.pmnd.rs/

---

## MVP Rules (Non-Negotiables)

- **Full feature set at launch** - No deferred features, no Phase 2 for core
- Progress credits NEVER expire or reset
- Surprises are OPTIONAL (not core path)
- Transparent odds always displayed
- No pay-to-win mechanics
- No loss outcomes
- Category boundaries respected
- NOT gambling, NOT raffle, NOT layaway
- Update docs on every scope change

---

**Preference-first. Boundary-aware. Progress-driven.**
