# WIREFRAMES

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is PREFERENCE-FIRST.

1) Users EXPRESS preferences through comparative choice or explicit selection.
2) PROGRESS CREDITS are earned through meaningful preference selections.
3) CREDITS NEVER EXPIRE or reset.
4) SURPRISES are OPTIONAL ACCELERATORS triggered at milestones (100, 200, 500 credits).
5) GIFT-SAFE PROFILES show category priorities and boundaries to friends.
6) PROGRESS ALWAYS CARRIES FORWARD (no losses, no pay-to-win).

# EXECUTABLE STRUCTURAL WIREFRAMES (ESW)
Wireframe standard:
- Explicit, column-based ASCII schematics with vertical rails.
- Every wireframe includes: HEADER line, MODE indicator, 2-3 columns where relevant.
- Required symbols: [ ] pending, [x] confirmed, [>] active, [?] suggested.

## Route Catalog
| Route | Mode | Purpose | State transitions |
| --- | --- | --- | --- |
| /onboarding | PREFERENCE | Capture category ranking | Onboarding -> Dashboard |
| /dashboard | PROGRESS | View progress snapshot | Dashboard -> Preferences |
| /preferences | PREFERENCE | Comparative choice | Choice -> +10 credits |
| /wishlist | WISHLIST | Explicit item list | Item -> +5 credits |
| /surprises | SURPRISE | Milestone reveal | Milestone -> Outcome |
| /u/[username] | PROFILE | Gift-safe public view | Share link |

--------------------------------------------------------------------------------
ONBOARDING (STEP 2: CATEGORY RANKING) | MODE: PREFERENCE
--------------------------------------------------------------------------------
/onboarding
+------------------------------------------------------------------------------+
| HEADER: Onboarding | Step 2 of 3 | Category Ranking                          |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: CATEGORY PRIORITIES                                    |
|                                                                              |
| What kinds of gifts feel safest? Drag to reorder:                           |
|                                                                              |
| [≡] Cash / Flexible Credit                                                   |
| [≡] Experiences / Travel                                                     |
| [≡] Food & Drink                                                             |
| [≡] Home / Lifestyle                                                         |
| [≡] Tech & Gadgets                                                           |
| [≡] Clothing & Wearables                                                     |
| [≡] Toys / Games                                                             |
| [≡] Surprise Me                                                              |
|                                                                              |
| ACTION: [Continue] -> First choice                                           |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
ONBOARDING (STEP 3: FIRST CHOICE) | MODE: PREFERENCE
--------------------------------------------------------------------------------
/onboarding
+------------------------------------------------------------------------------+
| HEADER: Onboarding | Step 3 of 3 | First Choice                              |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: COMPARATIVE CHOICE                                     |
|                                                                              |
| Which feels more like you?                                                   |
|                                                                              |
| +-------+  +-------+  +-------+  +-------+                                   |
| | IMG   |  | IMG   |  | IMG   |  | IMG   |                                   |
| |  A    |  |  B    |  |  C    |  |  D    |                                   |
| | $199  |  | $249  |  | $179  |  | $299  |                                   |
| +-------+  +-------+  +-------+  +-------+                                   |
|                                                                              |
| Category: Home Decor                                                         |
|                                                                              |
| ACTION: [Select] -> Earn +10 credits                                         |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
DASHBOARD | MODE: PROGRESS
--------------------------------------------------------------------------------
/dashboard
+------------------------------------------------------------------------------+
| HEADER: Dashboard | 145 Credits | Next Milestone: 200                        |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: PROGRESS DISPLAY                                       |
|                                                                              |
| YOUR PROGRESS:                                                               |
| 145 Credits ████████████░░░░░░░░░░░░ 200                                    |
| Progress never expires                                                       |
|                                                                              |
| RECENT ACTIVITY:                                                             |
| [x] Comparative Choice (+10) - 2h ago                                        |
| [x] Added Desk to wishlist (+5) - 1d ago                                     |
| [x] Milestone 100 reached - 3d ago                                           |
|                                                                              |
| QUICK ACTIONS:                                                               |
| [Make Choice] -> /preferences                                                |
| [Add to Wishlist] -> /wishlist                                               |
| [View Profile] -> /u/username                                                |
|                                                                              |
| WISHLIST PREVIEW:                                                            |
| Desk $749  |  Chair $450  |  Monitor $350                                    |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
PREFERENCES (COMPARATIVE CHOICE) | MODE: PREFERENCE
--------------------------------------------------------------------------------
/preferences
+------------------------------------------------------------------------------+
| HEADER: Make a Choice | 145 Credits | 55 to next milestone                  |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: COMPARATIVE CHOICE                                     |
|                                                                              |
| Which feels more like you?                                                   |
| Category: Clothing & Wearables | Subcategory: Jackets                       |
|                                                                              |
| +-------+  +-------+  +-------+  +-------+                                   |
| | IMG   |  | IMG   |  | IMG   |  | IMG   |                                   |
| |  A    |  |  B    |  |  C    |  |  D    |                                   |
| | $199  |  | $249  |  | $179  |  | $299  |                                   |
| +-------+  +-------+  +-------+  +-------+                                   |
|                                                                              |
| [Tap any to select]                                                          |
|                                                                              |
| LEARNING OVER TIME:                                                          |
| 14 choices in this category                                                  |
| We're learning: Minimalist, neutral colors, mid-range budget                 |
|                                                                              |
| ACTION: [Select] -> +10 credits                                              |
|        [Skip This Round] [None Feel Right]                                   |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
WISHLIST | MODE: WISHLIST
--------------------------------------------------------------------------------
/wishlist
+------------------------------------------------------------------------------+
| HEADER: Wishlist | 8 Items | $2,447 Total | [Share Link]                   |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: WISHLIST                                               |
|                                                                              |
| +---------+  +---------+  +---------+  +---------+                           |
| |  IMG    |  |  IMG    |  |  IMG    |  |  IMG    |                           |
| | Desk    |  | Chair   |  | Monitor |  | Headph. |                           |
| | $749    |  | $450    |  | $350    |  | $299    |                           |
| | Amazon  |  | Wayfair |  | BestBuy |  | Amazon  |                           |
| | [Edit]  |  | [Edit]  |  | [Edit]  |  | [Edit]  |                           |
| | [Del]   |  | [Del]   |  | [Del]   |  | [Del]   |                           |
| +---------+  +---------+  +---------+  +---------+                           |
|                                                                              |
| +---------+  +---------+  +---------+  +---------+                           |
| |  IMG    |  |  IMG    |  |  IMG    |  |  IMG    |                           |
| | Lamp    |  | Plant   |  | Rug     |  | Art     |                           |
| | $89     |  | $45     |  | $199    |  | $120    |                           |
| | [Edit]  |  | [Edit]  |  | [Edit]  |  | [Edit]  |                           |
| | [Del]   |  | [Del]   |  | [Del]   |  | [Del]   |                           |
| +---------+  +---------+  +---------+  +---------+                           |
|                                                                              |
| ADD ITEM: [+ Add Item] -> [Search or paste link] -> +5 credits              |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SURPRISES (MILESTONE REVEAL) | MODE: SURPRISE
--------------------------------------------------------------------------------
/surprises
+------------------------------------------------------------------------------+
| HEADER: Surprises | Milestone Reached: 200 Credits                          |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: MILESTONE TRIGGER                                      |
|                                                                              |
| MILESTONE REACHED:                                                           |
| You've reached 200 credits                                                   |
|                                                                              |
| [Reveal Surprise]                                                            |
|                                                                              |
| Your progress is safe. Credits never expire.                                 |
|                                                                              |
| TRANSPARENT ODDS:                                                            |
| - Progress Boost (+50): 40%                                                  |
| - Discount (10% off): 30%                                                    |
| - Wish List Item: 15%                                                        |
| - Brand Item: 10%                                                            |
| - No Physical Item: 5%                                                       |
+------------------------------------------------------------------------------+

AFTER REVEAL:
+------------------------------------------------------------------------------+
| SURPRISE REVEALED                                                            |
|                                                                              |
|                          [ITEM IMAGE]                                        |
|                     Standing Desk - $749                                     |
|              From your wishlist! Ships in 3 days.                            |
|                                                                              |
| Outcome: Wish List Item (15% probability)                                    |
| New balance: 200 credits (carried forward)                                   |
| Next milestone: 500 credits                                                  |
|                                                                              |
| HISTORY:                                                                     |
| [x] 200 credits - Wish List Item                                             |
| [x] 100 credits - Progress Boost                                             |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
PUBLIC PROFILE (/u/[username]) | MODE: PUBLIC
--------------------------------------------------------------------------------
/u/[username]
+------------------------------------------------------------------------------+
| HEADER: Alex's Gift Profile | Public View | [Share Link]                   |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: CATEGORY PRIORITIES                                    |
|                                                                              |
| WHAT ALEX PREFERS:                                                           |
|                                                                              |
| ✓ SAFEST BETS:                                                               |
| 1. Cash / Flexible Credit                                                    |
| 2. Experiences / Travel                                                      |
| 3. Food & Drink                                                              |
|                                                                              |
| ⚠ PROCEED WITH CAUTION:                                                      |
| 4. Home / Lifestyle                                                          |
| 5. Tech & Gadgets                                                            |
|                                                                              |
| ❌ AVOID:                                                                     |
| 6. Clothing & Wearables (risky!)                                             |
| 7. Toys / Games                                                              |
|                                                                              |
| WISHLIST (PUBLIC VIEW):                                                      |
| +---------+  +---------+  +---------+                                        |
| |  IMG    |  |  IMG    |  |  IMG    |                                        |
| | Desk    |  | Chair   |  | Monitor |                                        |
| | $749    |  | $450    |  | $350    |                                        |
| | 85%     |  | 60%     |  | 45%     |                                        |
| | funded  |  | funded  |  | funded  |                                        |
| +---------+  +---------+  +---------+                                        |
|                                                                              |
| LEARNED PREFERENCES:                                                         |
| Style: Minimalist, modern                                                    |
| Colors: Neutral, white, black                                                |
| Budget: Mid-range ($200-$500)                                                |
+------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SETTINGS | MODE: SETTINGS
--------------------------------------------------------------------------------
/settings
+------------------------------------------------------------------------------+
| HEADER: Settings | Account | Preferences | Privacy | Notifications         |
+------------------------------------------------------------------------------+
| PREFERENCE LOCATION: USER SETTINGS                                          |
|                                                                              |
| ACCOUNT:                                                                     |
| Name:  [Alex Johnson______________]                                          |
| Email: [alex@example.com__________]                                          |
| Password: [••••••••] [Change]                                                |
|                                                                              |
| CATEGORY PRIORITIES (EDIT):                                                  |
| [≡] Cash / Flexible Credit                                                   |
| [≡] Experiences / Travel                                                     |
| [≡] Food & Drink                                                             |
| [≡] Home / Lifestyle                                                         |
| [≡] Tech & Gadgets                                                           |
| [≡] Clothing & Wearables                                                     |
| [≡] Toys / Games                                                             |
| [≡] Surprise Me                                                              |
|                                                                              |
| PRIVACY:                                                                     |
| Profile Visibility: ○ Public  ● Friends Only  ○ Private                      |
| Show Wishlist Progress: [x] Yes  [ ] No                                      |
| Show Learned Preferences: [x] Yes  [ ] No                                    |
|                                                                              |
| NOTIFICATIONS:                                                               |
| [x] Milestone reached                                                        |
| [x] Surprise available                                                       |
| [ ] Weekly progress summary                                                  |
|                                                                              |
| ACTION: [Save Settings]                                                      |
|                                                                              |
| DANGER ZONE: [Delete Account] (All progress will be lost)                    |
+------------------------------------------------------------------------------+
