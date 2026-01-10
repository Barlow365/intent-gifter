# Intent Gifter - EXECUTION PLAN

**🔍 ZOOM: PRODUCT_MAP → Technical Implementation**

This document defines HOW to build `docs/PRODUCT_MAP.md`.

**Navigation**: [README](../README.md) → [PRODUCT_MAP](./PRODUCT_MAP.md) → This Document

---

## Phase Definitions

- **PHASE 1** = Foundation (Auth, database, routing)
- **PHASE 2** = Preference capture (Categories, comparative choice, wish list)
- **PHASE 3** = Progress tracking (Credits, milestones)
- **PHASE 4** = Surprise mechanics (Reveal animation, outcomes)
- **PHASE 5** = Public profiles (Gift-safe sharing)
- **PHASE 6** = Micro-conversion (Optional $1 boost)
- **PHASE 7** = Recommendation engine (Smart matching)
- **PHASE 8** = Polish & launch (Marketing, help)

---

## Implementation Matrix

| PRODUCT_MAP Node | Phase 1 | Phase 2 | Phase 3 | Phase 4 | Phase 5-8 |
|------------------|---------|---------|---------|---------|-----------|
| **Auth** | Full auth system | - | - | - | - |
| **Category Ranking** | - | Drag-drop UI | - | - | - |
| **Boundaries** | - | Selection UI | - | - | - |
| **Comparative Choice** | - | "Pick 1/4" UI | Credits +10 | - | AI sets |
| **Wish List** | - | CRUD operations | - | - | - |
| **Progress Display** | - | - | Bar + total | Milestones | - |
| **Surprise Trigger** | - | - | - | Full flow | - |
| **Public Profile** | - | - | - | - | Phase 5 |
| **Micro-Conversion** | - | - | - | - | Phase 6 |

---

## Technical Dependencies

**Foundation** (Must build first):
1. Auth system (JWT + bcrypt)
2. PostgreSQL schema
3. Next.js routing

**Feature Layer** (Can parallelize):
- Preferences → Progress (need credit tracking)
- Progress → Surprises (need milestones)

---

## Phase Exit Criteria

**Phase 1**: User can sign up, log in, complete onboarding
**Phase 2**: User can rank categories, make comparative choices, add to wish list
**Phase 3**: Progress displays correctly, milestones track
**Phase 4**: Surprise reveal works, all outcomes functional
**Phase 8**: Public launch ready, Lighthouse >90

---

**For complete implementation details, see MASTER_PLAN.md**
