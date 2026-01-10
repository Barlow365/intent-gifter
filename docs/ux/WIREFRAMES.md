# WIREFRAMES

# CANONICAL PRODUCT TRUTH (NO-DRIFT)
The system is PREFERENCE-FIRST.

1) Users EXPRESS preferences through comparative choice or explicit selection.
2) PROGRESS CREDITS are earned through meaningful preference selections.
3) CREDITS NEVER EXPIRE or reset.
4) SURPRISES are OPTIONAL ACCELERATORS triggered at milestones (100, 200, 500 credits).
5) GIFT-SAFE PROFILES show category priorities and boundaries to friends.
6) PROGRESS ALWAYS CARRIES FORWARD (no losses, no pay-to-win).

If any document or wireframe conflicts with this model, it is WRONG and must be rewritten to match.

# EXECUTABLE STRUCTURAL WIREFRAMES (ESW)
Wireframe standard:
- Explicit, column-based ASCII schematics with vertical rails.
- Every wireframe includes: HEADER line, MODE indicator, 2-3 columns where relevant.
- Required symbols: [ ] pending, [x] confirmed, [>] active, [?] suggested.
- Every wireframe answers: Where does preference live? What moves progress forward?

## Route Catalog
| Route | Mode | Purpose | Key actions | State transitions |
| --- | --- | --- | --- | --- |
| /onboarding | PREFERENCE | Capture category ranking | Drag categories, pick first | Onboarding -> Dashboard |
| /dashboard | PROGRESS | View progress snapshot | View credits, start choice | Dashboard -> Preferences |
| /preferences | PREFERENCE | Comparative choice | Pick 1 of 4 | Choice -> +10 credits |
| /wishlist | WISHLIST | Explicit item list | Add/edit items | Item -> +5 credits |
| /surprises | SURPRISE | Milestone reveal | Click reveal | Milestone -> Outcome |
| /u/[username] | PROFILE | Gift-safe public view | View priorities, wishlist | Share link |

--------------------------------------------------------------------------------
ONBOARDING (CATEGORY RANKING) | MODE: PREFERENCE PROFILE
--------------------------------------------------------------------------------
/onboarding
+--------------------------------------------------------------------------------------+
| HEADER: Onboarding | Step 2 of 3 | Category Ranking                                  |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: CATEGORY PRIORITIES   ||| ACTION: Rank categories                     |
| What kinds of gifts feel safest?           |||                                         |
| Drag to reorder (top = safest):            ||| PREVIEW:                                    |
| [≡] Cash / Flexible Credit                 ||| Your Preferences:                           |
| [≡] Experiences / Travel                   ||| 1. Cash (safest)                            |
| [≡] Food & Drink                           ||| 2. Experiences                              |
| [≡] Home / Lifestyle                       ||| 3. Food                                     |
| [≡] Tech & Gadgets                         ||| ...                                         |
| [≡] Clothing & Wearables                   |||                                         |
| [≡] Toys / Games                           ||| Surprises will only come                    |
| [≡] Surprise Me                            ||| from top-ranked categories                  |
| ACTION: [Continue] -> First choice         |||                                         |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
ONBOARDING (FIRST CHOICE) | MODE: PREFERENCE PROFILE
--------------------------------------------------------------------------------
/onboarding (Step 3)
+--------------------------------------------------------------------------------------+
| HEADER: Onboarding | Step 3 of 3 | First Choice                                      |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: COMPARATIVE CHOICE    ||| ACTION: Pick 1 of 4 (+10 credits)          |
| Which feels more like you?                 |||                                         |
| +-----+ +-----+ +-----+ +-----+            ||| Progress starts here:                       |
| |IMG | |IMG | |IMG | |IMG |            ||| [ ] 0 credits                               |
| | A  | | B  | | C  | | D  |            ||| [>] Pick one                                |
| |$199| |$249| |$179| |$299|            ||| Next: 100 credits (first milestone)        |
| +-----+ +-----+ +-----+ +-----+            |||                                         |
| Category: Home Decor                       |||                                         |
| ACTION: [Select] -> Earn +10 credits       |||                                         |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
DASHBOARD (MAIN VIEW) | MODE: PROGRESS CREDITS
--------------------------------------------------------------------------------
/dashboard
+--------------------------------------------------------------------------------------+
| HEADER: Dashboard | 145 Credits | Next Milestone: 200                               |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: PROGRESS DISPLAY       ||| ACTION: Quick actions                      |
| YOUR PROGRESS:                              |||                                        |
| 145 Credits ████████████░░░░░░░░░░░░ 200   ||| [Make Choice] -> /preferences              |
| Progress never expires                      ||| [Add to Wishlist] -> /wishlist             |
|                                             ||| [View Profile] -> /u/username              |
| RECENT ACTIVITY:                            |||                                        |
| [x] Comparative Choice (+10) - 2h ago       ||| WISHLIST PREVIEW:                          |
| [x] Added Desk to wishlist (+5) - 1d ago    ||| Desk $749  Chair $450  Monitor $350        |
| [x] Milestone 100 reached - 3d ago          ||| [View Full Wishlist]                       |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
PREFERENCES (COMPARATIVE CHOICE) | MODE: PREFERENCE PROFILE
--------------------------------------------------------------------------------
/preferences
+--------------------------------------------------------------------------------------+
| HEADER: Make a Choice | 145 Credits | 55 to next milestone                          |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: COMPARATIVE CHOICE     ||| ACTION: Pick 1 (+10 credits)               |
| Which feels more like you?                  |||                                        |
| Category: Clothing & Wearables              ||| Progress updates instantly:                |
| Subcategory: Jackets                        ||| 145 -> 155 credits                         |
|                                             |||                                        |
| +-----+ +-----+ +-----+ +-----+             ||| Learning over time:                        |
| |IMG | |IMG | |IMG | |IMG |             ||| 14 choices in this category                |
| | A  | | B  | | C  | | D  |             ||| We're learning: Minimalist,                |
| |$199| |$249| |$179| |$299|             ||| neutral colors, mid-range budget           |
| +-----+ +-----+ +-----+ +-----+             |||                                        |
| [Tap any to select]                         |||                                        |
| ACTION: [Select] -> +10 credits             ||| [Skip This Round] [None Feel Right]        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
WISHLIST (EXPLICIT ITEMS) | MODE: WISHLIST
--------------------------------------------------------------------------------
/wishlist
+--------------------------------------------------------------------------------------+
| HEADER: Wishlist | 8 Items | $2,447 Total | [Share Link]                            |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: WISHLIST               ||| ACTION: Add/edit items (+5 credits)        |
| +---------+ +---------+ +---------+ +---------+                                     |
| |  IMG   | |  IMG   | |  IMG   | |  IMG   |                                     |
| | Desk   | | Chair  | | Monitor| | Headph.|                                     |
| | $749   | | $450   | | $350   | | $299   |                                     |
| | Amazon | | Wayfair| | BestBuy| | Amazon |                                     |
| | [Edit] | | [Edit] | | [Edit] | | [Edit] |                                     |
| | [Del]  | | [Del]  | | [Del]  | | [Del]  |                                     |
| +---------+ +---------+ +---------+ +---------+                                     |
| +---------+ +---------+ +---------+ +---------+                                     |
| |  IMG   | |  IMG   | |  IMG   | |  IMG   |                                     |
| | Lamp   | | Plant  | | Rug    | | Art    |                                     |
| | $89    | | $45    | | $199   | | $120   |                                     |
| | [Edit] | | [Edit] | | [Edit] | | [Edit] |                                     |
| | [Del]  | | [Del]  | | [Del]  | | [Del]  |                                     |
| +---------+ +---------+ +---------+ +---------+                                     |
| ADD ITEM: [+ Add Item] -> [Search or paste link] -> +5 credits                     |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SURPRISES (MILESTONE REVEAL) | MODE: SURPRISE
--------------------------------------------------------------------------------
/surprises
+--------------------------------------------------------------------------------------+
| HEADER: Surprises | Milestone Reached: 200 Credits                                 |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: MILESTONE TRIGGER      ||| ACTION: Reveal surprise                    |
| MILESTONE REACHED:                          |||                                        |
| You've reached 200 credits                  ||| TRANSPARENT ODDS:                          |
| [Reveal Surprise]                           ||| - Progress Boost (+50): 40%                |
|                                             ||| - Discount (10% off): 30%                  |
| Your progress is safe.                      ||| - Wish List Item: 15%                      |
| Credits never expire.                       ||| - Brand Item: 10%                          |
|                                             ||| - No Physical Item: 5%                     |
| AFTER REVEAL: ---->                         |||                                        |
| +-------------------------------------------------------------------------------+   |
| |                       SURPRISE REVEALED                                       |   |
| |                          [ITEM IMAGE]                                         |   |
| |                      Standing Desk - $749                                     |   |
| |               From your wishlist! Ships in 3 days.                            |   |
| |                                                                               |   |
| | Outcome: Wish List Item (15% probability)                                    |   |
| | New balance: 200 credits (carried forward)                                   |   |
| | Next milestone: 500 credits                                                  |   |
| +-------------------------------------------------------------------------------+   |
| HISTORY: [x] 200 credits - Wish List Item | [x] 100 credits - Progress Boost         |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
PUBLIC PROFILE (GIFT-SAFE) | MODE: PUBLIC PROFILE
--------------------------------------------------------------------------------
/u/[username]
+--------------------------------------------------------------------------------------+
| HEADER: Alex's Gift Profile | Public View | [Share Link]                            |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: CATEGORY PRIORITIES    ||| ACTION: Friends view gift guidance         |
| WHAT ALEX PREFERS:                          |||                                        |
|                                             ||| WISHLIST (PUBLIC VIEW):                    |
| ✓ SAFEST BETS:                              ||| +---------+ +---------+ +---------+        |
| 1. Cash / Flexible Credit                   ||| |  IMG   | |  IMG   | |  IMG   |        |
| 2. Experiences / Travel                     ||| | Desk   | | Chair  | | Monitor|        |
| 3. Food & Drink                             ||| | $749   | | $450   | | $350   |        |
|                                             ||| | 85%    | | 60%    | | 45%    |        |
| ⚠ PROCEED WITH CAUTION:                    ||| | funded | | funded | | funded |        |
| 4. Home / Lifestyle                         ||| +---------+ +---------+ +---------+        |
| 5. Tech & Gadgets                           ||| [View Full Wishlist]                       |
|                                             |||                                        |
| ❌ AVOID:                                   ||| LEARNED PREFERENCES:                       |
| 6. Clothing & Wearables (risky!)            ||| Style: Minimalist, modern                  |
| 7. Toys / Games                             ||| Colors: Neutral, white, black              |
|                                             ||| Budget: Mid-range ($200-$500)              |
| ACTION: Friends use this to choose gifts    |||                                        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
SETTINGS | MODE: SETTINGS
--------------------------------------------------------------------------------
/settings
+--------------------------------------------------------------------------------------+
| HEADER: Settings | Account | Preferences | Privacy | Notifications                  |
+--------------------------------------------------------------------------------------+
| PREFERENCE LOCATION: USER SETTINGS          ||| ACTION: Update preferences                 |
| ACCOUNT:                                    |||                                        |
| Name:  [Alex Johnson______________]         ||| CATEGORY PRIORITIES (EDIT):                |
| Email: [alex@example.com__________]         ||| [≡] Cash / Flexible Credit                 |
| Password: [••••••••] [Change]               ||| [≡] Experiences / Travel                   |
|                                             ||| [≡] Food & Drink                           |
| PRIVACY:                                    ||| [≡] Home / Lifestyle                       |
| Profile Visibility:                         ||| [≡] Tech & Gadgets                         |
| ○ Public  ● Friends Only  ○ Private         ||| [≡] Clothing & Wearables                   |
|                                             ||| [≡] Toys / Games                           |
| Show Wishlist Progress: [x] Yes  [ ] No     ||| [≡] Surprise Me                            |
| Show Learned Preferences: [x] Yes  [ ] No   ||| [Save Changes]                             |
|                                             |||                                        |
| NOTIFICATIONS:                              ||| DANGER ZONE:                               |
| [x] Milestone reached                       ||| [Delete Account]                           |
| [x] Surprise available                      ||| (All progress will be lost)                |
| [ ] Weekly progress summary                 |||                                        |
| ACTION: [Save Settings]                     |||                                        |
+--------------------------------------------------------------------------------------+

--------------------------------------------------------------------------------
MOBILE RESPONSIVE NOTES
--------------------------------------------------------------------------------
All layouts stack vertically on mobile:
- Single column (|||  separators become stacked sections)
- Bottom navigation: Dashboard | Preferences | Wishlist | Profile
- Swipe gestures for comparative choice
- Touch-friendly tap targets (44x44px min)

--------------------------------------------------------------------------------
ANIMATION SPECIFICATIONS
--------------------------------------------------------------------------------
SURPRISE REVEAL:
1. Button expands to full-screen card (0.5s)
2. Card flips 3D rotation -> reveals outcome
3. Confetti effect for positive outcomes
4. Progress bar updates with smooth easing
5. "Continue" fades in after 2s

COMPARATIVE CHOICE:
1. Selected card scales 1.1x
2. Others fade to 50% opacity
3. Checkmark animates in
4. +10 credits floats up -> merges with progress bar
5. Next set slides in from right

--------------------------------------------------------------------------------
ACCESSIBILITY NOTES
--------------------------------------------------------------------------------
- All images have alt text
- Color contrast 4.5:1 min (WCAG AA)
- Keyboard nav (Tab, Enter, Arrow keys)
- Screen reader announcements for progress updates, surprise reveals, choice selections
- Focus indicators on all interactive elements
- ARIA labels on all icon buttons
