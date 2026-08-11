# Buttons — Component Rules

## Structure
- Just the verb: `Publish`, `Save`
- Verb + outcome: `Pay now`, `Finish setup`
- Verb + object: `Delete listing`, `Add photos`, `Update address`

## Core rules
- Starts with a verb. Sentence case. No exclamation mark. No full stop.
- 10–20 characters; 2–3 words maximum.
- Leave 20–30% headroom for localisation (short labels can expand up to 200%).
- Button text and screen header must be in conversation with each other — same messaging hierarchy.
- In dialogs: primary button verb should match the title verb.
- Be device-agnostic: prefer "Select" over "Click", "Tap", "Touch", "Press".
- Make consequences obvious: use verbs that describe the outcome (Delete, Remove, Report).
- Prefer specific over generic: "Choose pickup point" not "Continue".
- Replace "Cancel" with a safer alternative when user work is at risk: "Keep editing", "Go back".

## Edge cases

| Scenario | Rule | Examples |
|----------|------|---------|
| Explicit consent required | "Agree and continue" or "I agree." Do not shorten to "Continue." | Agree and continue; I agree |
| Third-party / payment buttons | Follow brand guidelines. Do not localise protected brand words. | Continue with Google; Sign in with Apple |
| Price CTAs | Amount after the verb; follow locale formatting. | Pay €15.00 |
| System permissions | Match platform expectations, be explicit. | Allow notifications; Enable location |
| Space-constrained | Shorter specific verb; rely on nearby context. | Save; Send |
| Icon-only buttons | Provide accessible label + tooltip on web. | aria-label "Delete message" |
| Reversible actions | Simpler label acceptable. | Remove; Archive |
| Irreversible actions | Be explicit. | Permanently delete |
| Undo patterns | "Undo" as a separate action (toast/snackbar). Don't overload the button label. | "Item deleted" [Undo] |

## ❌ Banned terms

| Don't use | Use instead |
|-----------|-------------|
| OK | Got it (toasts), or a specific action |
| Yes / No | Explicit outcomes: Save changes / Keep editing |
| Confirm | Specific verb: Publish, Delete listing (except legal contexts) |
| Proceed / Continue (alone) | Continue to payment; Choose pickup point |
| Submit | Send message; Save changes; Place order (except legal contexts) |
| Done | Save; Finish setup |
| Click here / Tap here | The action itself: Learn more, Open settings |
| More | View details; See offers |
| Next (alone) | Continue to shipping |
| Cancel (when risky) | Keep editing; Go back |
