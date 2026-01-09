# Intent Gifter - MVP Specification

**Version:** 1.0
**Last Updated:** January 2026

---

## MVP Goal

Validate that people will engage with a preference-resolution system and that progress mechanics drive continued use—without gambling stigma.

**Core Hypothesis:**
1. People will express preferences through comparative choices
2. Progress credits create motivation to continue
3. Occasional surprises increase delight without feeling like gambling
4. Friends will use gift-safe profiles to give better gifts

---

## MVP Features (Must-Have)

### 1. User Onboarding & Profile

| Feature | Specification |
|---------|---------------|
| **Create Account** | Email + password auth |
| **Category Ranking** | Drag-drop 8 categories into priority order |
| **Risk Boundaries** | Mark categories as "Never buy me this" |
| **Basic Profile** | Name, photo, bio (optional) |

**Categories:**
1. Cash / Flexible Credit
2. Experiences / Travel
3. Food & Drink
4. Clothing & Wearables
5. Home / Lifestyle
6. Tech / Gadgets
7. Toys / Games / Fun
8. Surprise Me

### 2. Preference Capture

| Feature | Specification |
|---------|---------------|
| **Explicit Selection** | Browse items → add to wish list |
| **Comparative Choice** | "Pick 1 of 4" interface |
| **Progress Earned** | +10 credits per meaningful choice |
| **Wish List** | View all selected items |

**Comparative Choice Logic:**
- Show 1 previously favored item + 3 close alternatives
- Items from top-ranked categories only
- User picks one
- System updates preference model
- +10 progress credits awarded

### 3. Progress System

| Feature | Specification |
|---------|---------------|
| **Progress Display** | "You have 250 credits" |
| **Never Expire** | Credits persist forever |
| **Progress Bar** | Visual bar toward next milestone |
| **Milestone Rewards** | Every 100 credits → unlock surprise chance |

**Milestones:**
- 100 credits → 1st surprise chance
- 200 credits → 2nd surprise chance
- 500 credits → bonus reward

### 4. Surprise Mechanics (Simplified MVP)

| Feature | Specification |
|---------|---------------|
| **Trigger** | Milestone reached (100, 200, 500 credits) |
| **User Action** | Click "See Your Surprise" |
| **Outcomes** | 5 possible outcomes with transparent odds |
| **No Payment** | Free to trigger |

**Outcome Distribution (MVP):**
| Outcome | Probability | Description |
|---------|-------------|-------------|
| Progress Boost | 40% | +50 bonus credits |
| Discount | 30% | 10% off wish list item |
| Wish List Item | 15% | Previously selected item |
| Brand Item | 10% | Sponsor-provided gift |
| No Physical Item | 5% | "Keep going!" message + credits retained |

**Display:**
```
Congratulations!
You unlocked: 10% Discount
on your wish list item: "Nike Jacket"

[Claim Discount]
```

### 5. Gift-Safe Profile (Public View)

| Feature | Specification |
|---------|---------------|
| **Public Profile URL** | `/u/username` shareable link |
| **Category Priorities** | Shows ranked categories (safe → risky) |
| **Wish List** | Shows items user wants |
| **Boundaries** | "Never buy me: Clothing, Perfume" |
| **Progress State** | "70% toward Nike Jacket" |

**Friend View:**
```
Sarah's Gift Profile
─────────────────────
Safest Categories:
  1. Food & Drink ✓
  2. Experiences ✓
  3. Home / Lifestyle ✓

Risky Categories:
  5. Clothing ⚠️
  6. Tech ⚠️

Never Buy:
  ✗ Perfume
  ✗ Jewelry

Current Wish List:
  • Nike Jacket ($80) - 70% progress
  • Coffee subscription ($40) - 30% progress
```

### 6. Micro-Conversion (Optional)

| Feature | Specification |
|---------|---------------|
| **Accelerate Progress** | Pay $1 → gain +50 credits |
| **Framing** | "Speed up your progress" not "buy a chance" |
| **Optional** | Never required, always opt-in |
| **Limit** | Max 3 purchases per month |

**Payment Flow:**
```
Current Progress: 180 credits
Next Milestone: 200 credits (20 away)

Want to reach it faster?
[Pay $1 → +50 credits]

This speeds up your progress toward your goals.
It's not required and you can always earn credits for free.
```

---

## Out of Scope for MVP

Explicitly deferred to Phase 2+:

- ❌ Mobile app (web-first)
- ❌ Brand partnerships (manual fulfillment for MVP)
- ❌ Friend co-funding (group gifting)
- ❌ Advanced AI recommendations
- ❌ Multiple wish lists
- ❌ Social features (likes, comments)
- ❌ Gift tracking/history
- ❌ Recurring subscriptions

---

## User Flows

### Flow 1: New User Onboarding

```
1. User signs up with email/password
2. "Let's set up your gift preferences"
3. Drag-drop categories into priority order
4. "Mark any categories you never want gifts from"
5. "Great! Your profile is ready"
6. Shown 4 items: "Which one feels most like you?"
7. User picks one → +10 credits earned
8. "You earned 10 credits! Keep going to unlock surprises."
```

### Flow 2: Earning Progress

```
1. User logs in
2. Dashboard shows: "170 credits - 30 away from next surprise!"
3. User clicks "Refine My Preferences"
4. Shown "Pick 1 of 4" interface
5. User selects item A
6. +10 credits awarded → now at 180
7. "Great choice! 20 more to your next surprise."
8. User continues or exits
```

### Flow 3: Unlocking Surprise

```
1. User reaches 200 credits
2. Banner: "You unlocked a surprise! 🎁"
3. User clicks "See Your Surprise"
4. Animation reveals outcome
5. "You got: 10% Discount on Nike Jacket!"
6. [Claim Discount] → discount code generated
7. User can now buy at reduced price
```

### Flow 4: Friend Gifting

```
1. Friend receives link: intent-gifter.com/u/sarah
2. Views Sarah's gift-safe profile
3. Sees: "Food & Drink is Sarah's top category"
4. Sees wish list: "Coffee subscription ($40)"
5. Friend decides to buy it
6. Clicks "Buy This For Sarah"
7. Checkout flow → friend pays
8. Sarah notified: "Your friend got you a gift!"
```

---

## Technical Requirements

### Platform
- **Web app** (responsive mobile design)
- **Authentication** (email/password, JWT)
- **Database** (PostgreSQL for structured data)
- **Payments** (Stripe for micro-conversions)

### Performance
| Metric | Target |
|--------|--------|
| Page load time | <2 seconds |
| Preference save | <500ms |
| Surprise animation | Smooth (60fps) |
| Mobile responsive | Works on iOS + Android browsers |

---

## Success Metrics

### Leading Indicators (30 days)

| Metric | Target |
|--------|--------|
| User signups | 200+ |
| Preference choices made | 2,000+ (10 per user avg) |
| Progress milestones reached | 100+ users reach 100 credits |
| Surprise trigger rate | 50%+ of eligible users trigger |
| Micro-conversion rate | 5-10% of users pay $1 |
| Friend profile views | 500+ views |

### Lagging Indicators (60 days)

| Metric | Target |
|--------|--------|
| 7-day retention | 40%+ |
| 30-day retention | 20%+ |
| Average credits per user | 150+ |
| Wish list item adds | 5+ per user |
| Gift purchases via platform | 50+ gifts bought |

### Qualitative Metrics

- **User Feedback:** "This doesn't feel like gambling"
- **Gifter Feedback:** "This helped me give a better gift"
- **Boundary Respect:** No complaints about unwanted gift suggestions

---

## MVP Timeline

| Phase | Duration | Tasks |
|-------|----------|-------|
| **Development** | 6-8 weeks | Auth, preferences, progress, surprise, profile |
| **Beta Testing** | 2 weeks | 20-30 testers, feedback iteration |
| **Launch** | 1 week | Polish, monitoring, public launch |

**Total:** 9-11 weeks from start to public launch

---

## MVP Exit Criteria

Before declaring MVP success:

- [ ] 200+ users signed up
- [ ] 40%+ 7-day retention
- [ ] 50%+ of eligible users trigger surprises
- [ ] 5%+ micro-conversion rate
- [ ] No legal/ethical complaints
- [ ] Positive user sentiment ("doesn't feel like gambling")
- [ ] Friend profiles used for gifting
- [ ] Clear data showing preference learning works

**If criteria met:** Proceed to Phase 2 (brand partnerships, advanced features)
**If not met:** Iterate on core mechanics, re-test

---

## Risk Mitigation

| Risk | Mitigation |
|------|------------|
| **Gambling perception** | Clear messaging, legal review, no "spin" framing |
| **Low engagement** | Gamify progress without gambling, show clear value |
| **Legal issues** | Consult lawyer, transparent odds, no pay-to-win |
| **Low conversions** | Iterate on surprise outcomes, test messaging |

---

**The MVP proves people trust the system and that progress drives engagement.**
