# Inclusive language

Tag findings with `dimension: Inclusive language`, `conformance: Practice`.

Not a WCAG criterion. It sits in this project because the copy-critique agent is expected to flag language that excludes or misrepresents disabled users — that's part of the accessibility conversation even when no SC applies.

## Disability-first vs. person-first

There is no single correct form. Communities differ:

| Preferred | Where | Example |
|-----------|-------|---------|
| Identity-first | Deaf community, autistic community, many blind adults | "Deaf users", "autistic people", "blind users" |
| Person-first | Many intellectual-disability communities, clinical settings, US federal style | "Person with a disability", "people with Down syndrome" |

**Critic's rule:**
- Do not "correct" identity-first language to person-first (e.g. don't change "autistic users" to "users with autism").
- Avoid euphemisms: "differently abled", "special needs", "handi-capable", "person of determination".
- When unsure, use the community's preferred form — default to the plural ("Deaf users", "blind users", "autistic users").

## Ableist idioms to flag

The critic should flag these in any content and suggest a non-ableist alternative. The severity is usually `Minor` or `Nit`.

| Idiom | Issue | Alternative |
|-------|-------|-------------|
| Fall on deaf ears | Uses deafness as a synonym for ignoring | Go unheard / be ignored |
| Turn a blind eye | Uses blindness as a synonym for ignoring | Look the other way / ignore |
| Crazy / insane | Uses mental illness as intensifier | Wild / extreme / impressive |
| Lame | Uses disability as insult | Weak / boring / disappointing |
| Psycho / psychotic | Stigmatises mental illness | Erratic / reckless |
| Cripple / crippling | Uses mobility disability as metaphor | Weaken / severely limit |
| Dumb | Historically mute; now "stupid" | Silly / weak / unwise |
| OCD (used casually) | Trivialises a condition | Detailed / particular / precise |
| Tone deaf | Uses deafness for "unaware" | Out of touch / insensitive |
| Blind spot | Usually acceptable in driving; flag when used for "ignored area" | Gap / oversight |
| Schizophrenic (for "contradictory") | Stigmatises | Contradictory / inconsistent |
| Special needs | Euphemism | Disabled / with disabilities / specific needs |
| Wheelchair-bound | Implies restriction; many users describe chairs as freedom | Wheelchair user / uses a wheelchair |
| Suffers from | Frames disability as suffering | Has [condition] |
| Stricken with | Dramatic, pity-framing | Has [condition] / lives with [condition] |
| Retarded | Slur in most contexts | Delayed (for timing) / intellectually disabled (for people) |

## Implicit assumptions to flag

- **Assuming sight**: "See the image below", "Look at the chart" — instead use "The image shows…", "The chart shows…".
- **Assuming hearing**: "Listen to the audio" — ensure a transcript is mentioned.
- **Assuming standing / walking**: "Stand up and walk over to…" — often fine in metaphor, but flag in instructions.
- **Assuming typing / mouse use**: "Click" vs "Select" (select is input-agnostic and preferred); "Type your message" vs "Enter your message".

## Emoji and symbols

- Screen readers announce emoji by their Unicode name, which is often surprising (e.g. 💅 = "nail polish", 🌮 = "taco"). When emoji carry meaning, their announced name must match the message.
- Flag copy that relies on emoji to carry critical meaning without text. Example: "✅ Your order" without any text is announced as "check mark button Your order" — acceptable but unclear.
- Flag excessive emoji density in product copy (5+ emoji in a line): announcement becomes noise.
- Brand / flag emoji: 🇺🇸 is "flag: United States" — fine; but double flags for a language pair are announced as two flag names with no relationship.
- Skin-tone modifiers announce the tone; intent is usually fine.

## Gendered language

- Default to **gender-neutral** in UI and marketing: "they/them", "people", "folks".
- Where the user has shared a pronoun, use it.
- Fashion categories ("Men's / Women's / Kids") are a business constraint — flag only if the copy excludes non-binary users explicitly (e.g. "Gentlemen, this is for you!"). Otherwise leave to content-design team.

## Cultural and religious inclusion

- Not the direct focus of this agent, but the critic can flag obvious issues (holidays assumed, US-centric date formats in EU copy, etc.) and pass them to localization.
- Tag such findings as `dimension: Localization flag`, `conformance: Practice`.

## Handling uncertainty

- Inclusive-language findings can be contested. When an idiom is borderline, raise the finding with `uncertainty` set and suggest the alternative without insisting.
- Never rewrite a user's quoted words — if a user has said "I am autistic", don't change it.

## References

- Disability Language Style Guide (US National Center on Disability and Journalism).
- Autistic Self Advocacy Network — identity-first language explainer.
- RNIB guidance on language about sight loss (UK).
- UK Government Digital Service — style guide on accessibility and disability.
- Conscious Style Guide — broader inclusive-language resources.
