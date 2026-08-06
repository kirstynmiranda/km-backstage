# Localization readiness

Vinted operates across 20+ markets and languages. Localization has specialist critics of its own. **This agent does not diagnose localization issues.** It flags risks in the source-language copy that tend to break localization or hurt accessibility after translation.

Tag findings with `dimension: Localization flag`, `conformance: Practice`. Every such finding should end with "Refer to the localization team for diagnosis".

## What to flag

### 1. Text expansion risk

Target languages expand and contract relative to English:

| Language | Approx. expansion | Implication |
|----------|-------------------|-------------|
| German   | +30% to +40% | Buttons overflow; labels truncate |
| French   | +15% to +25% | Similar |
| Italian  | +20% | Similar |
| Spanish  | +20% to +25% | Similar |
| Russian  | +20% | Cyrillic; longer words |
| Polish   | +15% to +25% | Compound words, diacritics |
| Chinese / Japanese / Korean | –30% to –40% | UI can look sparse |
| Arabic / Hebrew | ≈ same length, but RTL | See RTL below |

**Flag when:**
- A button label is near the layout limit and cannot expand (e.g. tight card grid).
- A microcopy string relies on matching length across a row (e.g. aligned columns).

### 2. Idioms, metaphors, puns

Idioms rarely survive translation and usually translate literally. Flag and suggest a direct equivalent.

**Examples:**
- "Don't sleep on this deal" → literal: "Ne pas dormir sur cette offre" (incomprehensible in French).
- "Pro tip" — often fine, but consider the direct "Helpful tip".
- "Game changer", "slam dunk", "out of the park" — culturally specific idioms.

### 3. Culture-specific references

- Weather metaphors that assume seasons (a "spring clean" in a market where seasons are reversed or irrelevant).
- Holiday assumptions (4th July, Thanksgiving, Halloween copy shipped to markets that don't observe them).
- Sports metaphors (cricket / baseball / rugby).

### 4. Formats

- Date format: always write out the month ("15 March 2026", not "03/15/2026") to avoid ambiguity.
- Numbers: beware decimal separators (1,000.00 vs 1.000,00).
- Currency: use the ISO code + symbol ("EUR €12.50") in cross-market copy.
- Time: 24h is widely accepted in EU; 12h still used in UK and US.
- Units: metric vs imperial (fashion sizes differ by market — EU 38, UK 10, US 6 — call out the system).

Flag copy that uses ambiguous formats, but leave the fix to localization.

### 5. RTL (right-to-left) considerations

Arabic and Hebrew markets require RTL layouts. The critic should flag:

- Directional words in icon labels ("Next →", "Back ←") — the arrow direction flips in RTL; the word may need a different translation.
- Numbers embedded in RTL sentences — native digits vs. Arabic-Indic digits.
- UI metaphors that assume left-to-right progress (e.g. "swipe left to delete").

This is mostly engineering, but copy decisions (arrow in the string, positional language) trigger issues.

### 6. Concatenated strings

Flag strings built by concatenation in source code. Example:

- Bad: `"You have " + count + " messages"`
- Good: `"You have {count, plural, one {# message} other {# messages}}"` (ICU format)

Translators can't reorder concatenated pieces. In source-language review, flag placeholders that look positional and suggest ICU/named placeholders.

### 7. Placeholder content in variables

When a string has variables (`{name}`, `{count}`, `{date}`), flag:

- Variables that have grammatical dependencies (gendered nouns, plural forms) but no ICU handling.
- Variables that are hard-coded English names in non-English locales ("Thanks, {firstName}" — usually fine, but some locales use family name first).

## What the critic does NOT do

- Does not translate or propose translations.
- Does not diagnose locale-specific grammar or register.
- Does not rank translations for quality.

## Example finding

```json
{
  "severity": "Minor",
  "conformance": "Practice",
  "dimension": "Localization flag",
  "source": "localization-notes.md § idioms",
  "quote": "Don't sleep on this deal",
  "finding": "Idiomatic expression. Will likely translate literally and lose meaning in DE, FR, IT, PL, and other markets. May also be unclear to non-native English speakers in English-language markets.",
  "suggested rewrite": "Don't miss this deal",
  "uncertainty": "Refer to the localization team for market-specific diagnosis."
}
```