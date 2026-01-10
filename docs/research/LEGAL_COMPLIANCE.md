# Intent Gifter - Legal Compliance & Safeguards

**Version:** 1.0
**Last Updated:** January 2026
**Status:** Legal Design Specification

---

## Executive Summary

Intent Gifter uses progress and surprise mechanics that could be misconstrued as gambling. This document outlines legal safeguards to ensure compliance with gambling laws while maintaining user engagement.

**Key Principle:** This is a preference platform with optional surprises, NOT a game of chance requiring payment for uncertain outcomes.

---

## Legal Classification Analysis

### What Makes Something "Gambling"?

Under US law, gambling typically requires three elements:

| Element | Definition | Intent Gifter Status |
|---------|------------|----------------------|
| **Consideration** | Payment or value given | ❌ No payment required |
| **Chance** | Random outcome | ⚠️ Surprises have randomness |
| **Prize** | Something of value received | ⚠️ Items have value |

**Conclusion:** If no payment is required (no consideration), it's NOT gambling under most US jurisdictions.

### Legal Precedents

| Case | Outcome | Relevance |
|------|---------|-----------|
| **Free-to-play loot boxes** | Legal if no purchase required | Intent Gifter requires no purchase |
| **Sweepstakes** | Legal if "no purchase necessary" | Similar framing applies |
| **Loyalty programs** | Legal with progress-based rewards | Intent Gifter uses progress, not chance alone |

---

## Non-Gambling Design Principles

### 1. No Payment Required

**Rule:** Users NEVER have to pay to:
- Create an account
- Express preferences
- Earn progress credits
- Trigger surprises
- Receive gifts

**Optional Micro-Conversion:**
- Framed as "accelerate progress" not "buy a chance"
- $1 → +50 credits (fixed, not random)
- Does NOT unlock additional surprise chances
- Limited to 3 per month to prevent abuse

**Legal Framing:**
```
✓ "Speed up your progress toward your goals"
✗ "Buy more chances to win"

✓ "Get credits faster"
✗ "Increase your odds"
```

### 2. Progress Always Carries Forward

**Rule:** Progress never expires, resets, or is lost.

| Scenario | Outcome |
|----------|---------|
| User stops using app | Credits remain |
| Surprise has "no item" outcome | Credits kept + new credits added |
| User doesn't pay | Progress continues |
| Account inactive | Progress preserved |

**Legal Significance:** This is a **progress system**, not a game of chance. Users always move forward.

### 3. Transparent Odds

**Rule:** All surprise outcome probabilities are disclosed upfront.

**Example Display:**
```
Surprise Outcomes:
  • Progress Boost (+50 credits): 40%
  • Discount (10% off): 30%
  • Wish List Item: 15%
  • Brand Item: 10%
  • No Physical Item: 5%

All outcomes shown before you trigger the surprise.
Your progress is never lost, regardless of outcome.
```

**Legal Significance:** Transparency + no loss = not gambling.

### 4. No "Spin" or "Roll" Framing

**Prohibited Framing:**
- ❌ "Spin the wheel"
- ❌ "Roll the dice"
- ❌ "Try your luck"
- ❌ "Gamble your credits"

**Approved Framing:**
- ✅ "See your surprise"
- ✅ "Unlock your reward"
- ✅ "Reveal what you earned"
- ✅ "Open your progress milestone"

**Legal Significance:** Language matters. Avoiding gambling terminology reduces legal risk.

### 5. No Infinite Replay

**Rule:** Surprises are tied to progress milestones, not on-demand.

| Model | Intent Gifter |
|-------|---------------|
| **Gambling (illegal)** | Pay $1 → trigger surprise → repeat infinitely |
| **Intent Gifter (legal)** | Earn 100 credits → trigger surprise once → earn next 100 for next surprise |

**Legal Significance:** Milestones prevent the "pay to replay" loop that defines gambling.

---

## Comparison to Legal Precedents

### vs. Loot Boxes (Legal with Safeguards)

| Feature | Loot Boxes | Intent Gifter |
|---------|------------|---------------|
| **Payment required?** | No (free option) | No |
| **Random outcomes?** | Yes | Yes (but transparent) |
| **Can be earned free?** | Yes | Yes |
| **Progress system?** | Sometimes | Always |

**Verdict:** Intent Gifter is MORE conservative (progress > chance).

### vs. Sweepstakes (Legal)

| Feature | Sweepstakes | Intent Gifter |
|---------|-------------|---------------|
| **No purchase necessary** | ✓ Yes | ✓ Yes |
| **Transparent odds** | ✓ Yes | ✓ Yes |
| **Free entry method** | ✓ Yes | ✓ Yes (preference choices) |

**Verdict:** Intent Gifter follows sweepstakes model.

### vs. Loyalty Programs (Legal)

| Feature | Loyalty Programs | Intent Gifter |
|---------|------------------|---------------|
| **Earn points** | ✓ Yes | ✓ Yes (progress credits) |
| **Redeem for rewards** | ✓ Yes | ✓ Yes (surprises) |
| **Random bonuses** | ✓ Sometimes | ✓ Yes |

**Verdict:** Intent Gifter is essentially a preference-based loyalty program.

---

## State-by-State Considerations

### High-Risk States (Stricter Gambling Laws)

| State | Risk Level | Mitigation |
|-------|------------|------------|
| **Washington** | High | Ensure "no purchase necessary" is prominent |
| **Tennessee** | Medium | Avoid gambling terminology |
| **Montana** | Medium | Transparent odds required |

**Action:** Consult state-specific counsel before launch.

### Federal Regulations

| Law | Relevance | Compliance |
|-----|-----------|------------|
| **Unlawful Internet Gambling Enforcement Act (UIGEA)** | Prohibits online gambling | Not gambling (no consideration) |
| **Wire Act** | Bans interstate gambling | Not applicable (no wagers) |
| **FTC Guidelines** | Consumer protection | Transparent terms, no deception |

---

## Terms of Service Requirements

### Must Include:

1. **No Purchase Necessary Statement**
   ```
   "You never have to pay to participate. Progress credits can be earned
   for free by making preference selections."
   ```

2. **Odds Disclosure**
   ```
   "Surprise outcomes have the following probabilities: [list odds].
   All outcomes are disclosed before you trigger a surprise."
   ```

3. **Not Gambling Statement**
   ```
   "This is a preference platform with progress-based rewards,
   not a game of chance. Your progress always carries forward."
   ```

4. **Age Restriction**
   ```
   "Users must be 18+ or have parental consent."
   ```

5. **No Sale or Transfer**
   ```
   "Progress credits have no cash value and cannot be sold, traded,
   or transferred."
   ```

---

## User Protection Measures

### 1. Spending Limits (Micro-Conversions)

- Max 3 purchases per month ($1 each = $3/month max)
- Clear warning: "You've reached your monthly limit"
- Cooldown period enforced

### 2. Transparency Dashboard

Users can view:
- Total credits earned (free vs paid)
- Surprise history (all outcomes)
- Probability of each outcome
- Total spent (if any)

### 3. No Dark Patterns

**Prohibited:**
- ❌ Hiding odds
- ❌ Fake scarcity ("Only 2 surprises left!")
- ❌ Pressure to pay ("Friends who pay get more!")
- ❌ Confusing refund policies

**Required:**
- ✅ Clear odds
- ✅ Honest timelines
- ✅ Easy opt-out
- ✅ Simple language

### 4. Parental Controls

For users under 18 (with parental consent):
- Spending disabled
- Surprise triggers require parental approval
- Parent dashboard for monitoring

---

## International Considerations

### European Union (GDPR + Consumer Protection)

| Requirement | Compliance |
|-------------|------------|
| **Data protection** | Full GDPR compliance (consent, right to deletion) |
| **Consumer rights** | 14-day cooling-off period for purchases |
| **Gambling regulations** | Varies by country; legal review per jurisdiction |

### United Kingdom (Gambling Act 2005)

- **Classification:** Likely NOT gambling (no stake, transparent odds)
- **Action:** UK Gambling Commission consultation recommended

### Other Markets

- **Australia:** Strict loot box laws; legal review required
- **Japan:** Gacha laws apply; may need adjustments
- **Canada:** Provincial regulations vary; comply with each

---

## Legal Review Checklist

Before launch:

- [ ] Consult gambling law attorney in key states (CA, NY, WA, TX)
- [ ] Review Terms of Service with legal counsel
- [ ] Confirm "no purchase necessary" is prominent
- [ ] Test all user flows for dark patterns
- [ ] Ensure odds disclosure is clear
- [ ] Verify age verification works
- [ ] Check spending limits are enforced
- [ ] Prepare response plan for regulatory inquiries
- [ ] Set up compliance monitoring

---

## Red Flags to Avoid

| Red Flag | Why It's Bad | How to Avoid |
|----------|--------------|--------------|
| **Pay to unlock surprises** | Creates gambling mechanic | Surprises earned via progress only |
| **Hidden odds** | Deceptive practice | Always disclose probabilities |
| **Infinite replay** | Slot machine behavior | Tie to milestones, not on-demand |
| **"Spin" language** | Gambling framing | Use "reveal" or "unlock" |
| **Credits expire** | Predatory | Credits never expire |
| **No free path** | Requires purchase | Always free to earn progress |

---

## Regulatory Response Plan

### If Contacted by Regulators:

1. **Respond quickly** (within 48 hours)
2. **Provide documentation** (odds, terms, user flows)
3. **Show no-purchase path** (screenshots of free earning)
4. **Demonstrate progress system** (credits persist)
5. **Offer to modify** (if concerns raised)

### Potential Modifications:

If regulators express concern:
- Remove surprise mechanic entirely → keep progress
- Make all outcomes "positive" (remove "no item")
- Disable micro-conversions
- Add more transparency

---

## Insurance & Liability

### Recommended Coverage:

| Type | Coverage |
|------|----------|
| **General Liability** | $1M-$2M |
| **Cyber Liability** | $1M (data breach protection) |
| **D&O Insurance** | $1M (if incorporated) |

---

## Conclusion

**Legal Position:** Intent Gifter is designed to be **NOT gambling** because:

1. ✅ No payment required to participate
2. ✅ Progress never lost or reset
3. ✅ Transparent odds
4. ✅ No gambling framing
5. ✅ Milestone-based, not on-demand

**Risk Level:** Low to medium (if safeguards followed)

**Recommendation:** Proceed with MVP + legal review before scaling.

---

**Preference-first. Progress-driven. Legally sound.**
