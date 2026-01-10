# WIREFRAMES

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is PREFERENCE-FIRST.

1) Users EXPRESS preferences through comparative choice or explicit selection.
2) PROGRESS CREDITS are earned through meaningful preference selections.
3) CREDITS NEVER EXPIRE or reset.
4) SURPRISES are OPTIONAL ACCELERATORS triggered at milestones (100, 200, 500 credits).
5) GIFT-SAFE PROFILES show category priorities and boundaries to friends.
6) PROGRESS ALWAYS CARRIES FORWARD (no losses, no pay-to-win).

Terminology rules:
- PREFERENCE PROFILE is the core object (internal).
- User-facing: "Your Preferences" / "What Fits You".
- Credits are NOT money. They're earned through selections, never purchased.
- Surprises are NOT gambling. They're optional accelerators with transparent odds.
- Wishlist is explicit intent. Public Profile is gift-safe sharing.

If any document or wireframe conflicts with this model, it is WRONG and must be rewritten to match.

# EXECUTABLE STRUCTURAL WIREFRAMES (ESW)
Wireframe standard:
- Explicit, column-based ASCII schematics with vertical rails.
- Every wireframe includes: HEADER line, MODE indicator (PREFERENCE / PROGRESS / WISHLIST / SURPRISE), 2-3 columns where relevant.
- Required symbols: [ ] pending, [x] confirmed, [>] active, [?] suggested.
- Every wireframe answers: Where does preference live? What moves progress forward?

All wireframes in this repo must follow ONE visual grammar:
- Use vertical rails, section blocks, and column layouts.
- Use the Inkwell-style planning layout.
- Do NOT introduce boxed UI mockups, new ASCII art styles, or different layout conventions.
- Every wireframe must be a zoom of the same canonical system:
  PREFERENCE PROFILE → PROGRESS CREDITS → COMPARATIVE CHOICE → WISHLIST → SURPRISES → PUBLIC PROFILE

Required conventions:
- Each wireframe must include:
  - HEADER line
  - Page/Mode name
  - 2-3 column layout where relevant
  - Clear section headings (ALL CAPS)
- Symbols:
  [ ] pending / not selected
  [x] confirmed / selected / completed
  [>] active / in-progress
  [?] suggested / stubbed
- Every screen must clearly indicate whether it operates on:
  (A) PREFERENCE PROFILE
  (B) PROGRESS CREDITS
  (C) COMPARATIVE CHOICE
  (D) WISHLIST
  (E) SURPRISE

If any wireframe is not traceable to this system, rewrite or delete it.


================================================================================
WIREFRAME LEGEND
================================================================================
| Symbols: [ ] pending | [x] confirmed | [>] active | [?] suggested

--------------------------------------------------------------------------------
HOME PAGE (PUBLIC MARKETING) | MODE: N/A
--------------------------------------------------------------------------------
/
+--------------------------------------------------------------------------------------+
| HEADER: Logo | How It Works | Features | Pricing | Login | Sign Up                  |
+--------------------------------------------------------------------------------------+
| HERO SECTION                                                                         |
| +-----------------------------------------------------------------------------------+|
| | Preference-first. Boundary-aware. Progress-driven.                               ||
| |                                                                                   ||
| | Help people express what fits them, refine those preferences over time,          ||
| | and move closer to receiving meaningful items—while occasionally unlocking       ||
| | surprises that accelerate fulfillment.                                           ||
| |                                                                                   ||
| | [Get Started Free] [See How It Works]                                            ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| HOW IT WORKS (3-STEP VISUAL)                                                         |
| +---------+ +---------+ +---------+                                                  |
| | EXPRESS | | EARN    | | RECEIVE |                                                  |
| | Choose  | | Credits | | Gifts   |                                                  |
| | between | | through | | that    |                                                  |
| | options | | choices | | fit you |                                                  |
| +---------+ +---------+ +---------+                                                  |
+--------------------------------------------------------------------------------------+
| FEATURES PREVIEW                                                                     |
| - No awkward wishlists                                                               |
| - Progress never expires                                                             |
| - Friends know what NOT to buy                                                       |
| - Optional surprises accelerate fulfillment                                          |
+--------------------------------------------------------------------------------------+
| FOOTER: Privacy | Terms | Help | Contact                                             |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SIGNUP / ONBOARDING | MODE: PREFERENCE PROFILE
--------------------------------------------------------------------------------
/signup → /onboarding
+--------------------------------------------------------------------------------------+
| HEADER: Intent Gifter | Onboarding | Step 1 of 3                                      |
+--------------------------------------------------------------------------------------+
| ONBOARDING FLOW (PROGRESSIVE DISCLOSURE)                                             |
+--------------------------------------------------------------------------------------+
| STEP 1: CREATE ACCOUNT                                                               |
| +-----------------------------------------------------------------------------------+|
| | Welcome to Intent Gifter                                                          ||
| |                                                                                   ||
| | Name:  [_____________________]                                                    ||
| | Email: [_____________________]                                                    ||
| | Password: [__________________]                                                    ||
| |                                                                                   ||
| | [Continue]                                                                        ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| STEP 2: CATEGORY RANKING (DRAG AND DROP)                                            |
| +-----------------------------------------------------------------------------------+|
| | What kinds of gifts feel safest?                                                  ||
| |                                                                                   ||
| | Drag these categories in order of comfort (top = safest):                        ||
| |                                                                                   ||
| | [≡] Cash / Flexible Credit                                                        ||
| | [≡] Experiences / Travel                                                          ||
| | [≡] Food & Drink                                                                  ||
| | [≡] Home / Lifestyle                                                              ||
| | [≡] Tech & Gadgets                                                                ||
| | [≡] Clothing & Wearables                                                          ||
| | [≡] Toys / Games                                                                  ||
| | [≡] Surprise Me                                                                   ||
| |                                                                                   ||
| | [Back] [Continue]                                                                 ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| STEP 3: FIRST PREFERENCES                                                            |
| +-----------------------------------------------------------------------------------+|
| | Let's learn your taste                                                            ||
| |                                                                                   ||
| | Which of these feels more like you? (Pick 1)                                     ||
| |                                                                                   ||
| | +-----+ +-----+ +-----+ +-----+                                                   ||
| | | IMG| | IMG| | IMG| | IMG|                                                   ||
| | | A  | | B  | | C  | | D  |                                                   ||
| | |    | |    | |    | |    |                                                   ||
| | +-----+ +-----+ +-----+ +-----+                                                   ||
| |                                                                                   ||
| | Category: Home Decor                                                              ||
| | (3 more rounds to complete setup)                                                ||
| |                                                                                   ||
| | [Skip for now] [Select]                                                           ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
DASHBOARD (MAIN VIEW) | MODE: PREFERENCE PROFILE + PROGRESS CREDITS
--------------------------------------------------------------------------------
/dashboard
+--------------------------------------------------------------------------------------+
| HEADER: Intent Gifter | Dashboard | Profile | Settings | Logout                      |
+--------------------------------------------------------------------------------------+
| PROGRESS OVERVIEW                                                                    |
| +-----------------------------------------------------------------------------------+|
| | YOUR PROGRESS                                                                     ||
| |                                                                                   ||
| | +-------------------------------------------------------------------------------+ ||
| | | 145 Credits ████████████░░░░░░░░░░░░ Next milestone: 200                     | ||
| | +-------------------------------------------------------------------------------+ ||
| |                                                                                   ||
| | Progress never expires • Earned through preferences • Unlocks surprises          ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| QUICK ACTIONS (3-CARD LAYOUT)                                                        |
| +--------+ +--------+ +--------+                                                     |
| | MAKE   | | ADD TO | | VIEW   |                                                     |
| | CHOICE | | WISH   | | PROFILE|                                                     |
| |        | | LIST   | |        |                                                     |
| | Pick 1 | | Add    | | Share  |                                                     |
| | of 4   | | items  | | with   |                                                     |
| | +10 cr | | +5 cr  | | friends|                                                     |
| |        | |        | |        |                                                     |
| | [Start]| | [Add]  | | [View] |                                                     |
| +--------+ +--------+ +--------+                                                     |
+--------------------------------------------------------------------------------------+
| RECENT ACTIVITY                                                                      |
| +-----------------------------------------------------------------------------------+|
| | [X] Comparative Choice - Home Decor (+10 credits) - 2 hours ago                  ||
| | [X] Added Standing Desk to wishlist (+5 credits) - Yesterday                     ||
| | [X] Milestone reached: 100 credits (Surprise revealed) - 3 days ago              ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| WISHLIST PREVIEW (TOP 3)                                                             |
| +---------+ +---------+ +---------+                                                  |
| |  IMG   | |  IMG   | |  IMG   |                                                  |
| | Desk   | | Chair  | | Headph.|                                                  |
| | $749   | | $450   | | $299   |                                                  |
| +---------+ +---------+ +---------+                                                  |
| [View Full Wishlist]                                                                 |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
PREFERENCES - COMPARATIVE CHOICE | MODE: PREFERENCE PROFILE + COMPARATIVE CHOICE
--------------------------------------------------------------------------------
/preferences
+--------------------------------------------------------------------------------------+
| HEADER: Intent Gifter | Make a Choice | Dashboard                                    |
+--------------------------------------------------------------------------------------+
| COMPARATIVE CHOICE INTERFACE                                                         |
| +-----------------------------------------------------------------------------------+|
| | Which of these feels more like you?                                               ||
| |                                                                                   ||
| | Category: Clothing & Wearables                                                    ||
| | Subcategory: Jackets                                                              ||
| |                                                                                   ||
| | +-----+ +-----+ +-----+ +-----+                                                   ||
| | | IMG| | IMG| | IMG| | IMG|                                                   ||
| | |    | |    | |    | |    |                                                   ||
| | | A  | | B  | | C  | | D  |                                                   ||
| | |    | |    | |    | |    |                                                   ||
| | |$199| |$249| |$179| |$299|                                                   ||
| | |    | |    | |    | |    |                                                   ||
| | +-----+ +-----+ +-----+ +-----+                                                   ||
| | [Tap any to select]                                                               ||
| |                                                                                   ||
| | Earns: +10 credits per choice                                                     ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| PROGRESS BAR                                                                         |
| +-----------------------------------------------------------------------------------+|
| | 145 Credits ████████████░░░░░░░░░░░░ Next milestone: 200 (55 to go)              ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| ACTIONS                                                                              |
| [Skip This Round] [None Feel Right] [Select]                                        |
+--------------------------------------------------------------------------------------+
| LEARNING OVER TIME                                                                   |
| You've made 14 choices in Clothing & Wearables                                      |
| We're learning: Minimalist style, neutral colors, mid-range budget                  |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
WISHLIST | MODE: WISHLIST
--------------------------------------------------------------------------------
/wishlist
+--------------------------------------------------------------------------------------+
| HEADER: Intent Gifter | Wishlist | Dashboard                                        |
+--------------------------------------------------------------------------------------+
| WISHLIST OVERVIEW                                                                    |
| Total Items: 8 | Total Value: $2,447 | Share: [Copy Link]                          |
+--------------------------------------------------------------------------------------+
| WISHLIST GRID (VISUAL CARDS)                                                         |
| +---------+ +---------+ +---------+ +---------+                                     |
| |  IMG   | |  IMG   | |  IMG   | |  IMG   |                                     |
| | Desk   | | Chair  | | Monitor| | Headph.|                                     |
| | $749   | | $450   | | $350   | | $299   |                                     |
| | Amazon | | Wayfair| | BestBuy| | Amazon |                                     |
| |        | |        | |        | |        |                                     |
| | [Edit] | | [Edit] | | [Edit] | | [Edit] |                                     |
| | [Del]  | | [Del]  | | [Del]  | | [Del]  |                                     |
| +---------+ +---------+ +---------+ +---------+                                     |
| +---------+ +---------+ +---------+ +---------+                                     |
| |  IMG   | |  IMG   | |  IMG   | |  IMG   |                                     |
| | Lamp   | | Plant  | | Rug    | | Art    |                                     |
| | $89    | | $45    | | $199   | | $120   |                                     |
| | Target | | Etsy   | | Wayfair| | Etsy   |                                     |
| |        | |        | |        | |        |                                     |
| | [Edit] | | [Edit] | | [Edit] | | [Edit] |                                     |
| | [Del]  | | [Del]  | | [Del]  | | [Del]  |                                     |
| +---------+ +---------+ +---------+ +---------+                                     |
+--------------------------------------------------------------------------------------+
| ADD ITEM                                                                             |
| +-----------------------------------------------------------------------------------+|
| | [+ Add Item]                                                                      ||
| |                                                                                   ||
| | Search or paste product link:                                                    ||
| | [_______________________________________]                                         ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SURPRISE REVEAL | MODE: SURPRISE
--------------------------------------------------------------------------------
/surprises
+--------------------------------------------------------------------------------------+
| HEADER: Intent Gifter | Surprises | Dashboard                                        |
+--------------------------------------------------------------------------------------+
| MILESTONE REACHED                                                                    |
| +-----------------------------------------------------------------------------------+|
| | Congratulations!                                                                  ||
| |                                                                                   ||
| | You've reached 200 credits                                                        ||
| |                                                                                   ||
| | Click to see your surprise                                                        ||
| |                                                                                   ||
| | [Reveal Surprise]                                                                 ||
| |                                                                                   ||
| | Your progress is safe. Credits never expire.                                     ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| AFTER REVEAL (ANIMATION)                                                             |
| +-----------------------------------------------------------------------------------+|
| | +-------------------------------------------------------------------------------+ ||
| | |                                                                               | ||
| | |                          SURPRISE REVEALED                                    | ||
| | |                                                                               | ||
| | |                              [ITEM IMAGE]                                     | ||
| | |                                                                               | ||
| | |                        Standing Desk - White Oak                              | ||
| | |                                $749                                           | ||
| | |                                                                               | ||
| | |                From your wishlist! Ships within 3 days.                       | ||
| | |                                                                               | ||
| | +-------------------------------------------------------------------------------+ ||
| |                                                                                   ||
| | Outcome: Wish List Item (15% probability)                                        ||
| |                                                                                   ||
| | Your new credit balance: 200 (carried forward)                                   ||
| | Next milestone: 500 credits                                                      ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| SURPRISE HISTORY                                                                     |
| +-----------------------------------------------------------------------------------+|
| | [X] 200 credits - Wish List Item (Standing Desk) - Today                         ||
| | [X] 100 credits - Progress Boost (+50 credits) - 2 weeks ago                     ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| TRANSPARENT ODDS                                                                     |
| +-----------------------------------------------------------------------------------+|
| | Surprise Outcome Probabilities:                                                   ||
| | - Progress Boost (+50 credits): 40%                                              ||
| | - Discount (10% off wish item): 30%                                              ||
| | - Wish List Item: 15%                                                            ||
| | - Brand-Funded Item: 10%                                                         ||
| | - No Physical Item: 5%                                                           ||
| |                                                                                   ||
| | All outcomes move you forward. No losses.                                        ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
PUBLIC PROFILE (GIFT-SAFE SHARING) | MODE: PUBLIC PROFILE
--------------------------------------------------------------------------------
/u/[username]
+--------------------------------------------------------------------------------------+
| HEADER: Intent Gifter | Profile: Alex's Gift Profile                                 |
+--------------------------------------------------------------------------------------+
| PROFILE HEADER                                                                       |
| +-----------------------------------------------------------------------------------+|
| | Alex Johnson                                                                      ||
| |                                                                                   ||
| | Gift-Safe Profile • Last updated: 2 days ago                                     ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| CATEGORY PRIORITIES (VISUAL)                                                         |
| +-----------------------------------------------------------------------------------+|
| | What Alex prefers:                                                                ||
| |                                                                                   ||
| | ✓ SAFEST BETS                                                                     ||
| | 1. Cash / Flexible Credit                                                         ||
| | 2. Experiences / Travel                                                           ||
| | 3. Food & Drink                                                                   ||
| |                                                                                   ||
| | ⚠ PROCEED WITH CAUTION                                                           ||
| | 4. Home / Lifestyle                                                               ||
| | 5. Tech & Gadgets                                                                 ||
| |                                                                                   ||
| | ❌ AVOID                                                                          ||
| | 6. Clothing & Wearables (risky!)                                                  ||
| | 7. Toys / Games                                                                   ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| WISHLIST (PUBLIC VIEW)                                                               |
| +---------+ +---------+ +---------+                                                  |
| |  IMG   | |  IMG   | |  IMG   |                                                  |
| | Desk   | | Chair  | | Monitor|                                                  |
| | $749   | | $450   | | $350   |                                                  |
| | 85%    | | 60%    | | 45%    |                                                  |
| | funded | | funded | | funded |                                                  |
| +---------+ +---------+ +---------+                                                  |
| [View Full Wishlist]                                                                 |
+--------------------------------------------------------------------------------------+
| LEARNED PREFERENCES                                                                  |
| +-----------------------------------------------------------------------------------+|
| | Alex's Taste:                                                                     ||
| | - Style: Minimalist, modern                                                       ||
| | - Colors: Neutral tones, white, black                                            ||
| | - Budget: Mid-range ($200-$500)                                                  ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| CONTRIBUTE TO WISHLIST                                                               |
| [Contribute to Desk] [Contribute to Chair] [Contribute to Monitor]                  |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SETTINGS | MODE: PREFERENCE PROFILE
--------------------------------------------------------------------------------
/settings
+--------------------------------------------------------------------------------------+
| HEADER: Intent Gifter | Settings | Dashboard                                        |
+--------------------------------------------------------------------------------------+
| ACCOUNT SETTINGS                                                                     |
| +-----------------------------------------------------------------------------------+|
| | Name:  [Alex Johnson______________]                                               ||
| | Email: [alex@example.com__________]                                               ||
| | Password: [••••••••] [Change Password]                                            ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| CATEGORY PRIORITIES (EDIT)                                                           |
| +-----------------------------------------------------------------------------------+|
| | Drag to reorder:                                                                  ||
| |                                                                                   ||
| | [≡] Cash / Flexible Credit                                                        ||
| | [≡] Experiences / Travel                                                          ||
| | [≡] Food & Drink                                                                  ||
| | [≡] Home / Lifestyle                                                              ||
| | [≡] Tech & Gadgets                                                                ||
| | [≡] Clothing & Wearables                                                          ||
| | [≡] Toys / Games                                                                  ||
| | [≡] Surprise Me                                                                   ||
| |                                                                                   ||
| | [Save Changes]                                                                    ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| PRIVACY SETTINGS                                                                     |
| +-----------------------------------------------------------------------------------+|
| | Profile Visibility: ○ Public  ● Friends Only  ○ Private                          ||
| |                                                                                   ||
| | Show Wishlist Progress: [X] Yes  [ ] No                                          ||
| | Show Learned Preferences: [X] Yes  [ ] No                                        ||
| |                                                                                   ||
| | [Save Privacy Settings]                                                           ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| NOTIFICATIONS                                                                        |
| +-----------------------------------------------------------------------------------+|
| | Email Notifications:                                                              ||
| | [X] Milestone reached                                                             ||
| | [X] Surprise available                                                            ||
| | [ ] Weekly progress summary                                                       ||
| | [ ] Friend contributed to wishlist                                                ||
| |                                                                                   ||
| | [Save Notification Preferences]                                                   ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+
| DANGER ZONE                                                                          |
| +-----------------------------------------------------------------------------------+|
| | [Delete Account] (All progress will be lost)                                     ||
| +-----------------------------------------------------------------------------------+|
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
MOBILE RESPONSIVE CONSIDERATIONS
--------------------------------------------------------------------------------

All layouts adapt to mobile with:
- Single column layout (no side-by-side cards)
- Touch-friendly tap targets (minimum 44x44px)
- Hamburger menu for navigation
- Bottom navigation bar for primary actions
- Swipe gestures for comparative choice
- Stack priority over side-by-side where needed

MOBILE DASHBOARD EXAMPLE:
+----------------------------------+
| ☰ Intent Gifter          Profile |
+----------------------------------+
| YOUR PROGRESS                    |
| 145 Credits                      |
| ████████░░░░░░░░ 200             |
+----------------------------------+
| MAKE CHOICE                      |
| Pick 1 of 4 (+10 cr)             |
| [Start]                          |
+----------------------------------+
| ADD TO WISHLIST                  |
| Add items (+5 cr)                |
| [Add]                            |
+----------------------------------+
| VIEW PROFILE                     |
| Share with friends               |
| [View]                           |
+----------------------------------+
| RECENT ACTIVITY                  |
| [X] Comparative Choice (+10)     |
| [X] Added Desk to wishlist (+5)  |
+----------------------------------+
| Dashboard | Preferences | Profile |
+----------------------------------+

--------------------------------------------------------------------------------
ANIMATION SPECIFICATIONS
--------------------------------------------------------------------------------

SURPRISE REVEAL ANIMATION:
1. Initial state: "Click to reveal" button centered
2. On click: Button expands to full-screen card
3. Card flips with 3D rotation (0.5s duration)
4. Back of card reveals outcome
5. Confetti/sparkle effect for positive outcomes
6. Progress bar updates with smooth animation
7. "Continue" button fades in after 2s

COMPARATIVE CHOICE SELECTION:
1. User taps option
2. Selected card scales up 1.1x
3. Other cards fade to 50% opacity
4. Checkmark animates in top-right corner
5. +10 credits floats up and merges with progress bar
6. Progress bar fills with smooth easing
7. Next set of options slides in from right

WISHLIST ADD:
1. Item card appears with slide-down animation
2. +5 credits badge pulses
3. Credits add to progress bar with number count-up
4. Success toast appears at bottom

--------------------------------------------------------------------------------
ACCESSIBILITY NOTES
--------------------------------------------------------------------------------

- All images have alt text
- Color contrast ratio minimum 4.5:1 (WCAG AA)
- Keyboard navigation supported (Tab, Enter, Arrow keys)
- Screen reader announcements for:
  - Progress updates ("145 credits earned, 55 to next milestone")
  - Surprise reveals ("Wish list item unlocked: Standing Desk")
  - Comparative choice selections ("Option A selected, 10 credits earned")
- Focus indicators visible on all interactive elements
- Skip to main content link
- ARIA labels on all icon buttons
- Form validation with clear error messages
