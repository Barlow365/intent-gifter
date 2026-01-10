# Intent Gifter - SITEMAP

**🔍 ZOOM: PRODUCT_MAP → Navigation & Entry**

This document expands on `docs/PRODUCT_MAP.md`:
- **Parent Section**: Navigation & Entry + All Routes
- **Purpose**: Complete route structure with authentication, layouts, and feature flags
- **Binding**: All routes described here MUST exist in PRODUCT_MAP first

**Navigation**: [README](../../README.md) → [PRODUCT_MAP](../PRODUCT_MAP.md) → This Document

---

## Site Architecture Overview

**Route Pattern**: Public routes at root level, authenticated app routes under `/dashboard`, `/preferences`, etc.

**Total Routes**: 16 pages

---

## Complete Route Map

```
intent-gifter.com/
│
├── PUBLIC ROUTES (Marketing)
│   ├── /                           → Home / Landing Page
│   ├── /how-it-works               → How It Works (4-step flow)
│   ├── /features                   → Features Overview
│   ├── /pricing                    → Pricing (Free + Optional $1)
│   ├── /privacy                    → Privacy Policy
│   └── /terms                      → Terms of Service
│
├── AUTH ROUTES (Unauthenticated)
│   ├── /login                      → Sign In
│   ├── /signup                     → Create Account
│   └── /onboarding                 → Category Ranking Setup
│
├── APP ROUTES (Authenticated)
│   ├── /dashboard                  → Dashboard (Progress Snapshot)
│   ├── /preferences                → Comparative Choice ("Pick 1 of 4")
│   ├── /wishlist                   → Explicit Wish List
│   ├── /surprises                  → Surprise History & Trigger
│   ├── /settings                   → User Settings
│   └── /help                       → Help / FAQ / Support
│
└── PUBLIC PROFILE (Shareable)
    └── /u/[username]               → Gift-Safe Profile (Public View)
```

---

## Route Specifications

### 1. PUBLIC ROUTES (Marketing)

#### `/` - Home / Landing Page

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: First impression, value proposition, CTA to sign up

**Layout**: Marketing layout (header, hero, features, footer)

**Key Elements**:
- Hero: "Help people give you gifts you actually want"
- Tagline: "Preference-first. Boundary-aware. Progress-driven."
- 3-step explanation: Express → Earn → Accelerate
- Social proof (when available)
- CTA: [Sign Up Free]

**Auth State**:
- If logged in → redirect to `/dashboard`
- If not logged in → show landing page

---

#### `/how-it-works` - How It Works

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Explain the system in detail

**Layout**: Marketing layout

**Key Sections**:
1. **Express Preferences** - Comparative choice + categories
2. **Earn Progress** - Credits, milestones, never expire
3. **Refine Over Time** - System learns your taste
4. **Accelerate Fulfillment** - Surprises (optional)

**Visuals**: Step-by-step flow diagrams

---

#### `/features` - Features Overview

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Feature grid highlighting key innovations

**Key Features Displayed**:
- Preference capture without demanding
- Progress that never expires
- Surprise without gambling
- Category boundaries
- Gift-safe profiles

**CTA**: [Sign Up Free]

---

#### `/pricing` - Pricing

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Explain pricing model (free + optional micro-conversion)

**Pricing Tiers**:
- **Free Forever** - All core features
  - Preference capture
  - Progress credits
  - Milestones & surprises
  - Gift-safe profile

- **Accelerate (Optional)** - $1 per boost
  - +50 credits instantly
  - Max 3/month
  - Speeds up progress
  - NOT required

**Messaging**: "Free to use. Optional to accelerate."

---

#### `/privacy` - Privacy Policy

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Legal compliance, user data handling

**Key Points**:
- What data we collect
- How we use it
- Who we share it with (none)
- User rights (GDPR, CCPA)

---

#### `/terms` - Terms of Service

**PRODUCT_MAP Reference**: Navigation & Entry → Public Routes

**Purpose**: Legal terms, user agreement

**Key Points**:
- NOT gambling (explicit statement)
- User responsibilities
- Account termination
- Liability limits

---

### 2. AUTH ROUTES (Unauthenticated)

#### `/login` - Sign In

**PRODUCT_MAP Reference**: Navigation & Entry → Auth Routes

**Purpose**: Existing user login

**Layout**: Centered auth form

**Form Fields**:
- Email (required)
- Password (required)
- "Remember me" checkbox
- "Forgot password?" link

**Actions**:
- [Sign In] → POST `/api/auth/login` → redirect to `/dashboard`
- "Don't have an account?" → `/signup`

**Validation**:
- Email format
- Password minimum 8 chars

---

#### `/signup` - Create Account

**PRODUCT_MAP Reference**: Navigation & Entry → Auth Routes

**Purpose**: New user registration

**Layout**: Centered auth form

**Form Fields**:
- Email (required)
- Password (required, min 8 chars)
- Confirm Password (required, must match)
- Name (optional)
- Username (required, unique)

**Actions**:
- [Create Account] → POST `/api/auth/register` → redirect to `/onboarding`
- "Already have an account?" → `/login`

**Validation**:
- Email unique
- Username unique, alphanumeric
- Password strength

---

#### `/onboarding` - Category Ranking Setup

**PRODUCT_MAP Reference**: EXPRESS PREFERENCES → Category Priority System

**Purpose**: First-time user setup (rank categories, set boundaries)

**Layout**: Full-screen onboarding flow

**Steps**:
1. **Welcome** - "Let's set up your gift preferences"
2. **Category Ranking** - Drag-drop 8 categories into priority order
3. **Boundaries** - Mark categories as "Never buy me this"
4. **First Choice** - Shown 4 items: "Which one feels most like you?"
5. **Complete** - "You earned 10 credits! Keep going to unlock surprises."

**Progression**:
- Step 1/4 → Step 2/4 → Step 3/4 → Step 4/4
- Can't skip steps
- On complete → redirect to `/dashboard`

---

### 3. APP ROUTES (Authenticated)

#### `/dashboard` - Dashboard

**PRODUCT_MAP Reference**: EARN PROGRESS → Progress Display

**Purpose**: Central hub, progress snapshot, quick actions

**Layout**: App layout (sidebar nav, main content, header)

**Key Sections**:

**Progress Section**:
- Progress bar showing credits toward next milestone
- "You have 250 credits"
- "50 away from your next surprise!"

**Quick Actions**:
- [Refine Preferences] → `/preferences`
- [View Wish List] → `/wishlist`
- [See Surprises] → `/surprises` (if milestone reached)

**Recent Activity**:
- Latest preference choices
- Milestones reached
- Surprises unlocked

**Stats**:
- Total credits earned
- Preferences expressed
- Milestones reached

---

#### `/preferences` - Comparative Choice

**PRODUCT_MAP Reference**: EXPRESS PREFERENCES → Comparative Choice

**Purpose**: "Pick 1 of 4" interface for preference learning

**Layout**: App layout

**Interface**:

**Header**:
- "Which one feels most like you?"
- Current progress: "170 credits (30 away from next surprise)"

**Grid** (2x2 on desktop, stack on mobile):
```
┌─────────────┬─────────────┐
│  Option A   │  Option B   │
│  [Image]    │  [Image]    │
│  $80        │  $40        │
└─────────────┴─────────────┘
┌─────────────┬─────────────┐
│  Option C   │  Option D   │
│  [Image]    │  [Image]    │
│  $25        │  $50        │
└─────────────┴─────────────┘
```

**On Selection**:
- Highlight selected item
- "+10 credits" animation
- Update progress bar
- Show next set (or "Great! Keep going")

**Empty State**:
- "We're generating your next set..."
- Show loading spinner

---

#### `/wishlist` - Wish List View

**PRODUCT_MAP Reference**: EXPRESS PREFERENCES → Explicit Selection

**Purpose**: View and manage explicit wish list items

**Layout**: App layout

**Display**:

**Header**:
- "Your Wish List"
- [+ Add Item] button

**Item Cards** (grid view):
```
┌───────────────────────────┐
│ [Product Image]           │
│ Nike Jacket               │
│ $80                       │
│ Progress: 70%             │
│ [Remove]                  │
└───────────────────────────┘
```

**Add Item Flow**:
- Modal: "Add Item to Wish List"
- Fields: Item name, URL (optional), Price estimate, Category
- [Add to Wish List] → adds to list

**Empty State**:
- "You haven't added any items yet"
- "Add items explicitly, or let us learn your preferences through choices"
- [Refine Preferences] CTA

---

#### `/surprises` - Surprise History & Trigger

**PRODUCT_MAP Reference**: ACCELERATE FULFILLMENT → Surprise Mechanics

**Purpose**: View surprise history, trigger new surprises at milestones

**Layout**: App layout

**Trigger Section** (if milestone reached):
```
┌───────────────────────────────────────┐
│  🎁 You unlocked a surprise!          │
│                                       │
│  You reached 200 credits              │
│                                       │
│  [See Your Surprise]                  │
└───────────────────────────────────────┘
```

**Transparent Odds** (always visible):
```
Outcome Probabilities:
- Progress Boost (+50 credits): 40%
- Discount (10% off): 30%
- Wish List Item: 15%
- Brand Item: 10%
- No Physical Item: 5%
```

**Surprise History**:
- List of past surprises
- Date unlocked
- Outcome received
- Status (claimed/unclaimed)

**Empty State**:
- "No surprises yet!"
- "Keep refining your preferences to reach your first milestone (100 credits)"

---

#### `/u/[username]` - Public Gift-Safe Profile

**PRODUCT_MAP Reference**: GIFT-SAFE PROFILE → Public Profile View

**Purpose**: Shareable profile for friends to view gift preferences

**Layout**: Public profile layout (no sidebar, simple header)

**Display**:

**Header**:
- User's name & photo
- "Gift Profile"
- [Share Link] button (copy to clipboard)

**Safest Categories**:
```
Safest to Buy:
  ✓ Food & Drink
  ✓ Experiences / Travel
  ✓ Home / Lifestyle
```

**Risky Categories**:
```
Approach with Caution:
  ⚠️ Clothing & Wearables
  ⚠️ Tech / Gadgets
```

**Never Buy**:
```
Never Buy:
  ✗ Perfume
  ✗ Jewelry
```

**Wish List**:
```
Current Wish List:
  • Nike Jacket ($80) - 70% progress
  • Coffee subscription ($40) - 30% progress
```

**Privacy**:
- User can toggle public/private
- If private → shows "This profile is private"

---

#### `/settings` - User Settings

**PRODUCT_MAP Reference**: SETTINGS & CONTROLS → Settings

**Purpose**: Account, preferences, privacy, notifications

**Layout**: App layout with sidebar tabs

**Tabs**:

**1. Account**:
- Email (change email)
- Password (change password)
- Delete account (danger zone)

**2. Profile**:
- Name
- Username
- Photo upload
- Bio (optional)

**3. Preferences**:
- Edit category rankings
- Update boundaries
- Profile visibility (public/private)

**4. Notifications**:
- Email preferences (marketing, milestones, friend gifts)
- Push notifications (when available)

**5. Privacy**:
- Profile visibility toggle
- Data export
- Data deletion

---

#### `/help` - Help / FAQ / Support

**PRODUCT_MAP Reference**: System → Help

**Purpose**: User support, FAQs, contact

**Layout**: App layout

**Sections**:
- **FAQs** - Common questions
- **Contact Support** - Email form
- **System Status** - Uptime, incidents

**Common FAQs**:
- "Is this gambling?" → NO (detailed explanation)
- "Do credits expire?" → NO (never)
- "How do I delete my account?" → Settings
- "How do surprises work?" → Milestones + transparent odds

---

## Route Access Control

| Route | Authentication | Redirect If Logged In | Redirect If Not Logged In |
|-------|----------------|----------------------|---------------------------|
| `/` | Public | → `/dashboard` | - |
| `/how-it-works` | Public | - | - |
| `/login` | Public | → `/dashboard` | - |
| `/signup` | Public | → `/dashboard` | - |
| `/onboarding` | Required | - | → `/login` |
| `/dashboard` | Required | - | → `/login` |
| `/preferences` | Required | - | → `/login` |
| `/wishlist` | Required | - | → `/login` |
| `/surprises` | Required | - | → `/login` |
| `/settings` | Required | - | → `/login` |
| `/help` | Public | - | - |
| `/u/[username]` | Public | - | - |

---

## Mobile Navigation

**Bottom Tab Bar** (authenticated app):
```
┌─────────┬─────────┬─────────┬─────────┐
│ Home    │ Prefs   │ Wish    │ Profile │
│ 🏠      │ 🎯      │ ❤️      │ 👤      │
└─────────┴─────────┴─────────┴─────────┘
```

Maps to:
- Home → `/dashboard`
- Prefs → `/preferences`
- Wish → `/wishlist`
- Profile → `/settings`

---

## URL Parameters & Query Strings

**Onboarding**:
- `/onboarding?step=2` - Jump to specific step (if already started)

**Surprise Reveal**:
- `/surprises?reveal=true` - Auto-trigger reveal animation

**Profile Sharing**:
- `/u/sarah` - Dynamic username route

---

## Feature Flags (All Routes)

**Phase-Based Routing** (controlled via environment variables):

```javascript
FEATURE_SURPRISE_MECHANICS=true    // Enable/disable surprise features
FEATURE_MICRO_CONVERSION=true      // Enable/disable $1 boost option
FEATURE_PUBLIC_PROFILES=true       // Enable/disable profile sharing
FEATURE_BRAND_DASHBOARD=false      // Phase 2 feature (disabled in MVP)
```

---

## Route Summary Table

| # | Route | PRODUCT_MAP Section | Auth | Phase |
|---|-------|---------------------|------|-------|
| 1 | `/` | Navigation & Entry | Public | MVP |
| 2 | `/how-it-works` | Navigation & Entry | Public | MVP |
| 3 | `/features` | Navigation & Entry | Public | MVP |
| 4 | `/pricing` | Navigation & Entry | Public | MVP |
| 5 | `/privacy` | Navigation & Entry | Public | MVP |
| 6 | `/terms` | Navigation & Entry | Public | MVP |
| 7 | `/login` | Navigation & Entry | Public | MVP |
| 8 | `/signup` | Navigation & Entry | Public | MVP |
| 9 | `/onboarding` | Express Preferences | Required | MVP |
| 10 | `/dashboard` | Earn Progress | Required | MVP |
| 11 | `/preferences` | Express Preferences | Required | MVP |
| 12 | `/wishlist` | Express Preferences | Required | MVP |
| 13 | `/surprises` | Accelerate Fulfillment | Required | MVP |
| 14 | `/u/[username]` | Gift-Safe Profile | Public | MVP |
| 15 | `/settings` | Settings & Controls | Required | MVP |
| 16 | `/help` | System | Public | MVP |

**Total MVP Routes**: 16

---

## API Endpoints (Route Support)

See `docs/architecture/ARCHITECTURE.md` for full API specifications.

**Quick Reference**:
- `/api/auth/*` - Authentication
- `/api/preferences/*` - Preference capture
- `/api/progress/*` - Progress tracking
- `/api/surprises/*` - Surprise mechanics
- `/api/profile/*` - Public profiles
- `/api/gifts/*` - Gifting

---

**For wireframes of each route, see [WIREFRAMES.md](./WIREFRAMES.md)**
