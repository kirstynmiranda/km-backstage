# Plain language guidelines

Practice-level critique (not a WCAG requirement, except WCAG 2.2 SC 3.1.5 Reading Level at AAA, which we treat as guidance).

Tag findings with `dimension: Plain language`, `conformance: Practice`.

## Targets

| Metric | Target | Why |
|--------|--------|-----|
| Reading level | Lower secondary education (≈ 13–15 years old) | Matches SC 3.1.5 (AAA) recommendation; matches GOV.UK and EU plain-language guidance. |
| Sentence length | Average ≤ 20 words; maximum ≤ 25 words | Above this, comprehension drops sharply, especially for non-native speakers. |
| Paragraph length | ≤ 4 sentences in UI; ≤ 6 sentences in long-form | Keeps scan-ability. |
| Syllables per word | Prefer ≤ 3 | "Utilise" → "use"; "purchase" → "buy". |
| Voice | Active, second person ("You") | Directness reduces cognitive load. |

## Rules the critic applies

### Rule 1 — Active voice

**Check:** is the subject doing the action?
**Flag:** passive constructions in instructions.
**Examples:**
- Bad: "Your listing will be reviewed by our team within 24 hours."
- Good: "We'll review your listing within 24 hours."
- Bad: "Payments are processed by our provider."
- Good: "Our provider processes your payment."

### Rule 2 — Second person

**Check:** does the copy address the user directly?
**Flag:** "the user", "the customer", "members" in UI copy.
**Examples:**
- Bad: "The user must complete identity verification before selling."
- Good: "You need to verify your identity before you can sell."

### Rule 3 — Short sentences

**Check:** word count per sentence.
**Flag:** sentences > 25 words.
**Example:**
- Bad: "After you have uploaded your photos and entered a description, and provided that you have selected a valid category and size, you can proceed to set your price and publish the listing." (33 words)
- Good: "Upload your photos. Add a description. Pick a category and size. Then set your price and publish." (4 short sentences)

### Rule 4 — Simple words

**Check:** is there a shorter word with the same meaning?
**Common swaps:**

| Instead of | Use |
|------------|-----|
| utilise | use |
| purchase | buy |
| commence | start |
| terminate | end |
| facilitate | help |
| endeavour | try |
| assist | help |
| ascertain | find out |
| prior to | before |
| subsequent to | after |
| in the event that | if |
| in order to | to |
| at this time | now |
| is able to | can |
| has the ability to | can |
| make a decision | decide |
| provide assistance | help |

### Rule 5 — No double negatives

**Check:** two negatives cancelling.
**Flag:** any sentence with more than one "no/not/don't/never/without" unless they are clearly in separate clauses.
**Examples:**
- Bad: "You wouldn't not want to miss this offer."
- Good: "You'll want this offer."
- Bad: "We won't reject your listing unless it doesn't meet our guidelines."
- Good: "We accept listings that meet our guidelines."

### Rule 6 — Specific over vague

**Check:** could a number or a concrete term replace a vague phrase?
**Examples:**
- Bad: "Your refund will arrive soon."
- Good: "Your refund will arrive within 3–5 business days."
- Bad: "Your listing may be reviewed."
- Good: "We review all listings with a price over €100."

### Rule 7 — Lead with the point

**Check:** what's the most important information? Is it in the first sentence?
**Examples:**
- Bad: "As a result of our ongoing commitment to platform safety, and in line with our updated Community Guidelines, which were published on 1 March, your listing 'Red leather jacket' has been removed."
- Good: "We removed your listing 'Red leather jacket' because it didn't meet our Community Guidelines (updated 1 March)."

### Rule 8 — Consistent terminology

**Check:** is the same concept named the same way across nearby copy?
**Overlaps with:** WCAG SC 3.2.4 (Consistent Identification).
**Example:**
- Bad: "Start a listing / Create an item / Sell now" — three labels for one action in the same onboarding flow.
- Good: Pick one. Use it everywhere.

### Rule 9 — No technical error messages in user-facing surfaces

**Check:** does the error contain stack traces, exception names, HTTP codes, or internal terms that only a developer understands?
**Flag:** strings that look copy-pasted from a log. Pair with SC 3.3.1 Error Identification — even a clearly-worded error fails this rule if the wording is engineering-language.
**Examples:**
- Bad: "Failed to instantiate object due to exception in constructor."
- Good: "We couldn't load your listing. Please try again or refresh the page."
- Bad: "Error 500: Internal Server Error"
- Good: "Something on our side went wrong. You haven't lost your draft — try saving again in a moment."
- Bad: "NullPointerException at line 412"
- Good: "We hit a problem saving your photo. Try uploading it again."

**Rule of thumb:** if a non-technical reader can't tell what went wrong from the message, rewrite it. Keep the technical detail in the logs, not the UI.

### Rule 10 — Successful actions must point to the next step

**Check:** when a confirmation or status message reports success, does it also tell the user what just happened in enough detail to know what to do next?
**Flag:** generic confirmations — "Action successful", "Done", "OK", "Success" — that leave the user unclear on state or next move. Pair with SC 4.1.3 Status Messages; this rule adds the *what-next* dimension.
**Examples:**
- Bad: "Success!"
- Good: "Listing published. It's now live on Vinted — view it in your Catalog."
- Bad: "Submitted."
- Good: "ID submitted. We'll verify it within 24 hours and email you when we're done."
- Bad: "Offer sent."
- Good: "Offer sent to Anna. You'll get a notification when she replies."

**When the next step is nothing:** it's fine to confirm and close, but the message must confirm *what* happened ("Payment confirmed") rather than *that something* happened ("Success").

### Rule 11 — Break up long passages

**Check:** does any block of copy exceed ~150 words with no paragraph break, bullet list, or heading?
**Flag:** walls of text in Help Center articles, T&Cs, onboarding explainers, and long email bodies. Pair with SC 2.4.10 Section Headings (AAA) for long-form; this rule also applies to in-app blocks where headings aren't appropriate.
**Fixes:**
- Split into short paragraphs of 2–3 sentences each.
- Use bullet lists when presenting three or more parallel items.
- Use sub-headings when the passage exceeds ~250 words, even mid-article.
- Lead with a one-sentence TL;DR for passages over 300 words.

**Example:**
- Bad: a 280-word paragraph in the "How returns work" article with no break.
- Good: the same content split into "When you can return" (2 paragraphs), "How to start a return" (3 bullets), "How refunds work" (2 paragraphs) — each section with its own sub-heading.

## Measuring reading level

Target: **Flesch Reading Ease ≥ 60** or **Flesch-Kincaid Grade Level ≤ 8** (roughly equivalent to UK Year 9 / EU lower-secondary).

The critique agent should estimate reading level for any passage ≥ 3 sentences. For short UI strings (button labels, error messages), skip the metric and apply the rules above directly.

## When brand voice and plain language conflict

Brand voice sometimes favours playful or poetic copy. The critic should:

- Raise the plain-language finding as `Minor` with `uncertainty` set ("may conflict with brand voice").
- Suggest a rewrite that preserves the intent in plain language.
- Defer the final call to the human — this project's agent is one voice, not the arbiter.