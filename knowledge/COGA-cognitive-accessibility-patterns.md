# Cognitive Accessibility patterns

Derived from the W3C note **"Making Content Usable for People with Cognitive and Learning Disabilities"** (COGA), 2021. COGA is not normative — it's a set of **design patterns** that complement WCAG for users with cognitive, learning, and neurodivergent needs (memory limits, attention, literacy, executive function, anxiety).

A content-critique agent should treat COGA as `Practice`-level findings (see `critique-format.md`).

## The patterns, condensed for a content critic

### 1. Help users understand what things are and how to use them

**Check:**
- Use familiar words over technical ones.
- When technical terms are unavoidable, explain on first use (overlaps with SC 3.1.3 / 3.1.4).
- Name things by their function, not by brand metaphor.

**Typical failure at Vinted:**
- "Vinted Go" used as a noun with no explanation on first use in shipping flows.
- "Verified Pro" used in trust UI without saying what's been verified.

---

### 2. Help users find what they need

**Check:**
- Front-load the most important information in headings, labels, and notifications.
- Use consistent labels for the same action (overlaps with SC 3.2.4).
- Avoid burying critical info at the end of long sentences.

**Typical failure at Vinted:**
- Notification: "After review, we have decided to approve your listing" → critical word ("approve") is last. Put it first.

---

### 3. Use clear and understandable content

**Check:**
- Short sentences (≤ 20 words as a rule of thumb; see `plain-language.md`).
- One idea per sentence.
- Active voice.
- Avoid double negatives.
- Avoid metaphors and idioms when precise instructions are needed.

**Typical failure at Vinted:**
- "You wouldn't not want to verify your identity" — double negative.
- "Don't sleep on this deal" — idiom in a promotion; unclear to non-native speakers.

---

### 4. Help users avoid mistakes and know how to correct them

**Check:**
- Give clear instructions before the action (overlaps with SC 3.3.2).
- Confirm destructive actions.
- Error messages name the problem and the fix (overlaps with SC 3.3.1 / 3.3.3).
- Don't penalise users for trivial formatting differences (spaces in card numbers, dashes in phone numbers).

**Typical failure at Vinted:**
- "Invalid card number" when the user entered "4111 1111 1111 1111" with spaces — should auto-format.
- Delete listing without confirmation.

---

### 5. Help users focus

**Check:**
- One primary action per screen.
- Reduce cognitive load by chunking (e.g. address into: line 1, line 2, city, postcode, country — not one free-text field).
- Don't use copy that creates urgency when urgency isn't real ("Only 2 left!" when the system doesn't actually know — anxiety trigger).

**Typical failure at Vinted:**
- Multiple equally-weighted CTAs on checkout.
- Countdown timers on non-time-limited offers.

---

### 6. Ensure processes do not rely on memory

**Check:**
- Don't ask users to remember info from a previous step.
- Show entered data on review screens without requiring users to scroll back.
- Overlaps with SC 3.3.7 Redundant Entry — but COGA goes further: even if the system *could* ask again safely, don't make the user remember across steps.

**Typical failure at Vinted:**
- Multi-step listing flow where the photo uploader is on step 1 and the price is on step 4, and the review screen only shows price.

---

### 7. Provide help and support

**Check:**
- Inline help next to the decision (overlaps with SC 3.3.5).
- A way to contact a human when the user is stuck.
- Plain-language summaries at the top of long articles.

**Typical failure at Vinted:**
- Help Center articles with 2000 words and no TL;DR.
- Support links hidden three taps deep.

---

### 8. Support adaptation and personalisation

**Check:**
- Don't rely on colour alone to convey meaning.
- Don't rely on icons alone without text labels.
- Support user choice of reminder cadence, notification volume, etc.

This is more UX than copy, but the critic should flag copy that depends on visual context (e.g. "Click the red button" — if a colour-blind user can't identify it).

---

## Applying COGA findings

- Tag with `dimension: COGA`, `conformance: Practice`.
- Cite the pattern number (e.g. `COGA pattern 3`).
- Suggest a rewrite that addresses the specific pattern.

Example:

```json
{
  "severity": "Minor",
  "conformance": "Practice",
  "dimension": "COGA",
  "source": "COGA pattern 3 (clear content)",
  "quote": "After a thorough review of the materials you have submitted, we have come to the conclusion that your listing meets our requirements and has been approved for publication on the platform.",
  "finding": "Sentence is 32 words, buries the outcome at the end. COGA pattern 3 recommends one idea per sentence, active voice, critical info first.",
  "suggested rewrite": "Your listing is approved and now live on Vinted."
}
```


## Out of scope

This agent critiques **copy** against accessibility content requirements. It does not critique design, engineering, or policy. If a user asks about one of these, the agent should name the right owner and decline politely.

### Explicitly out of scope

| Topic | Why out of scope | Who owns it |
|-------|------------------|-------------|
| Colour contrast (WCAG 1.4.3, 1.4.6, 1.4.11) | Visual design; not a copy decision | Design team + design tokens (Bloom) |
| Focus order (SC 2.4.3) | Engineering / DOM structure | Engineering |
| Keyboard operability (SC 2.1.1, 2.1.2, 2.1.4) | Engineering | Engineering |
| Timing and motion (SC 2.2.x, 2.3.x) | Engineering / animation | Engineering + design |
| Touch targets (SC 2.5.5, 2.5.8) | Design | Design |
| Bypass blocks (SC 2.4.1) | Engineering | Engineering |
| Reflow, text resize (SC 1.4.4, 1.4.10) | Engineering / CSS | Engineering |
| Audio descriptions and captions (SC 1.2.x) | Video production | Marketing / video team |
| Forms validation timing (SC 3.3.4) | Engineering | Engineering |
| Character key shortcuts (SC 2.1.4) | Engineering | Engineering |
| Pointer gestures (SC 2.5.1) | Engineering | Engineering |

### What the agent does with out-of-scope asks

1. If the user asks directly ("Does this pass contrast?"), decline briefly and name the right owner.
2. If the user pastes copy that **hints** at an out-of-scope issue (e.g. "Click the red button"), add a **short flag** to the findings list, not a full finding. Format:

```json
{
  "severity": "Nit",
  "conformance": "Practice",
  "dimension": "Localization flag",
  "source": "out-of-scope.md § sensory cue",
  "quote": "Click the red button",
  "finding": "Copy relies on colour to identify the control. Accessibility of the control itself (contrast, focus, hit target) is out of scope for this critic — refer to design/engineering. The copy can avoid the sensory cue regardless.",
  "suggested rewrite": "Select 'Confirm'"
}
```

3. Never claim competence in the out-of-scope area. Prefer "refer to" over a half-answer.

### Brand, SEO, legal

These are adjacent critique dimensions the user's agent is likely already running in parallel.

- **Brand voice:** not this agent's job. When the agent's rewrite might conflict with brand voice, it says so (`uncertainty`).
- **SEO:** not this agent's job. Keyword density, meta titles, URL slugs — handed off to the SEO critic.
- **Legal:** not this agent's job. If copy claims something that might be regulated (medical, financial, safety), flag *that there's a claim* and refer to the Legal Advisor project.
