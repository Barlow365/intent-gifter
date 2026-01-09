# Intent Gifter - Technical Architecture

**Version:** 1.0
**Last Updated:** January 2026

---

## Technology Stack

### Frontend
- **Framework:** React + TypeScript
- **UI:** Tailwind CSS + Framer Motion (animations)
- **State:** Zustand or Redux Toolkit
- **Build:** Vite

### Backend
- **Framework:** Node.js + Express or Python + FastAPI
- **Database:** PostgreSQL (structured data)
- **Cache:** Redis (sessions, real-time data)
- **AI/ML:** Recommendation engine (scikit-learn or custom)
- **Payments:** Stripe

### Infrastructure
- **Hosting:** Vercel (frontend) + Railway (backend)
- **Storage:** AWS S3 (images)
- **Monitoring:** Sentry + PostHog
- **Email:** Resend

---

## Data Models

### Core Tables

**users**
- id, email, password_hash, name, created_at

**user_profiles**
- user_id, category_rankings (JSON), boundaries (array)

**preference_choices**
- id, user_id, items_shown (array), selected_item_id, created_at

**progress**
- user_id, total_credits, milestone_reached, last_updated

**wish_list_items**
- id, user_id, item_name, item_url, price, added_at

**surprises**
- id, user_id, milestone, outcome_type, outcome_value, triggered_at

**gifts**
- id, giver_id, recipient_id, item_id, amount, status, created_at

---

## API Design

### Authentication
- POST `/api/auth/register`
- POST `/api/auth/login`
- GET `/api/auth/me`

### Preferences
- POST `/api/preferences/choice` (record choice → earn credits)
- GET `/api/preferences/next` (get next 4-choice set)
- PUT `/api/preferences/categories` (update rankings)

### Progress
- GET `/api/progress` (get current credits + milestones)
- POST `/api/progress/boost` (pay $1 → +50 credits)

### Surprises
- POST `/api/surprises/trigger` (unlock surprise at milestone)
- GET `/api/surprises/history` (past outcomes)

### Gifting
- GET `/api/profile/:username` (public gift-safe profile)
- POST `/api/gifts/create` (friend purchases gift)
- GET `/api/gifts/received` (gifts received)

---

## Surprise Algorithm

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

## Recommendation Engine (Phase 2)

**Input:**
- User's past choices
- Category rankings
- Demographic data

**Output:**
- Next "Pick 1 of 4" set optimized for learning

**Algorithm:**
- Collaborative filtering (users with similar choices)
- Content-based (item attributes)
- Explore/exploit balance (70% similar, 30% new)

---

## Performance Targets

| Metric | Target |
|--------|--------|
| Page load | <2s |
| API response | <200ms |
| Surprise animation | 60fps |
| Mobile responsive | iOS + Android |

---

## Security

- HTTPS only
- JWT authentication
- bcrypt password hashing
- Input validation (Zod)
- Rate limiting (100 req/min)
- CSRF protection

---

**Simple, scalable, secure.**
