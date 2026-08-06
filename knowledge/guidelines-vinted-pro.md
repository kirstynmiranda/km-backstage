# Vinted voice and tone - Vinted Pro content

This tone guide explains how to modulate Vinted's general tone of voice for content in the Vinted Pro experience. If any of the guidance here conflicts with the information outlined in Vinted voice and tone - general guidelines, defer to this document.

---

## Context

Vinted Pro is a dedicated account type and registration experience for professional resellers — typically small business owners or sole traders who sell second-hand goods at scale on Vinted's marketplace. Unlike casual sellers, Pro users operate with a commercial mindset: they think in terms of revenue, inventory, compliance, and business growth.

Adopt this tone when creating content for any of the following experiences:

* **Registration and onboarding:** Any content a user interacts with during the Vinted Pro sign-up process, including eligibility checks, business verification, and account setup.
* **Pro account management:** Any content related to managing Pro-specific settings, billing, subscriptions, or business details.
* **Selling tools and features:** Any content related to Pro-specific selling features, such as bulk listing, inventory management, analytics, or promotional tools.
* **Compliance and legal obligations:** Any content that informs Pro users of their legal responsibilities as business sellers, including VAT, consumer rights, and platform policies.
* **System notifications and updates:** Any automated or triggered communications informing Pro users of account changes, policy updates, or required actions.

> **Note on terminology:** Vinted Pro users are both "members" of the Vinted community and professional sellers. Use "member" when referring to their participation in the wider Vinted marketplace (e.g. buyer-facing interactions). Use "you/your" and business-oriented language (e.g. "your shop", "your listings", "your business") when addressing them in Pro-specific contexts. Never refer to them as "customers" or "users."

**Example**

General Vinted content:
```yaml
dialog:
  heading: Vinted is your platform for pre-owned pieces you'll love
  subheading: One community, thousands of brands, and a whole lot of second-hand style. Ready to get started? Here's how it works.
```

Vinted Pro content:
```yaml
dialog:
  heading: Grow your business on Vinted
  subheading: Vinted Pro gives you the tools to list more, sell faster, and reach millions of buyers across Europe. Let's get your account set up.
  button:
    label: Get started
    action: Navigate to Vinted Pro registration flow
```

---

## Tone modulation

Vinted Pro content uses all three of Vinted's brand voice pillars, but in a different balance and context to the general consumer product.

1. **Practical (Foundation):** Clarity is the priority. Pro users are busy professionals — respect their time. Be precise, outcome-oriented, and never pad copy with fluff.
2. **Familiar (Tone):** Vinted Pro should feel like a reliable business partner, not a faceless enterprise tool. Keep the human warmth that makes Vinted distinct, but dial back casual or playful register.
3. **Joyful (Selective accent):** Use sparingly, and only in moments of genuine business achievement — a completed registration, a first sale milestone, or a successful upgrade. Never use in friction, compliance, or legal contexts.

> **Key distinction from B2C:** In the general Vinted product, Joyful is used broadly across high-reward moments like buying and selling. In Vinted Pro, Joyful is a much narrower accent — reserved for business milestones only. The default register is warmer and more purposeful than the brand management portal, but more professional and restrained than the general consumer product.

### Additional tone principles

**Vinted Pro content should always:**
* Lead with business value. Frame features and actions in terms of what the Pro user gains — reach, efficiency, revenue, compliance confidence.
* Respect the user's expertise. Pro users know how selling works. Do not over-explain basic concepts or use a hand-holding tone.
* Be honest about obligations. Pro users have legal responsibilities as business sellers. State these clearly and without softening, but without being punitive.
* Use consistent, professional language. Terminology for key concepts (e.g. "shop", "listings", "Pro account", "business details") should be uniform across all surfaces.

**Vinted Pro content should never:**
* Use casual consumer-facing language that undercuts the professional register (e.g. "Woohoo!", "You're crushing it!", "Snag a bargain").
* Be vague about fees, obligations, or account requirements. Pro users are accountable to their businesses and need accurate, specific information.
* Overload with legal or compliance language in non-legal contexts. Flag obligations clearly, but keep the overall experience approachable.
* Use urgency or pressure tactics. If a deadline or requirement exists, state it factually.

**Writing voice — active vs. passive:**

Vinted Pro content should use the active voice as the default, especially for onboarding, instructions, and feature copy. Use the passive voice only in these situations:

* To describe actions completed by Vinted's systems or moderation team (e.g. "Your account has been verified.")
* To describe compliance or legal outcomes neutrally (e.g. "VAT details are required by law.")
* To avoid implying fault when communicating errors or restrictions

---

## Tone mapping by situation

| Context | Primary pillar | Secondary pillar | Joyful allowed? | Other characteristics |
| :--- | :--- | :--- | :--- | :--- |
| **Onboarding and registration** | Familiar | Practical | ✅ Yes — at completion only | Welcome the user as a business partner. Focus on what they're gaining. Save celebration for when registration is complete. |
| **Business milestone moments** | Joyful | Familiar | ✅ Yes | First sale, account upgrade, reaching a sales threshold. Keep it grounded — acknowledge the achievement without being over-the-top. |
| **Selling tools and features** | Practical | Familiar | ❌ No | Lead with the business benefit. Be specific about what the feature does and why it matters to a Pro seller. |
| **Compliance and legal obligations** | Practical | Practical | ❌ No | State obligations clearly and factually. Do not soften or bury legal requirements. No filler or personality. |
| **Errors and failed actions** | Practical | Familiar | ❌ No | Identify the problem specifically. Tell the user how to fix it. Do not blame or lecture. |
| **Account and billing** | Practical | Practical | ❌ No | Be precise about costs, dates, and actions. No ambiguity. |
| **Empty states** | Practical | Familiar | ❌ No | Explain what the space is for and what the user can do. Keep it brief and business-focused. |
| **System notifications** | Practical | Practical | ❌ No | State what changed, why it matters, and what (if anything) the user needs to do. |

### Tone "Volume" logic

* **Onboarding and registration (pre-completion):** Volume 40% Familiar, 0% Joyful.
* **Registration complete / business milestones:** Volume 40% Familiar, 30% Joyful.
* **Selling tools and features:** Volume 30% Familiar, 0% Joyful.
* **Compliance and legal obligations:** Volume 0% Familiar, 0% Joyful.
* **Errors and failed actions:** Volume 20% Familiar, 0% Joyful.
* **Account and billing:** Volume 0% Familiar, 0% Joyful.
* **Empty states:** Volume 20% Familiar, 0% Joyful.
* **System notifications:** Volume 10% Familiar, 0% Joyful.

---

## Handling the B2C–B2B seam

Pro users move between the general Vinted consumer product and the Vinted Pro experience. Tone shifts at these seams can feel jarring if not managed carefully.

**Guidelines for seam moments:**

* **Transitioning into Pro:** When a user enters a Pro-specific flow from the general app, copy should shift register gradually. Avoid an abrupt switch from casual consumer language to formal business language within the same screen or flow step.
* **Transitioning out of Pro:** When a Pro user returns to the general marketplace (e.g. browsing or buying), standard B2C voice and tone applies. Do not carry the Pro register into consumer-facing surfaces.
* **Shared components:** If a component (e.g. an error message, a tooltip) appears in both B2C and Pro contexts, default to the more restrained Pro register. A slightly more professional tone never breaks the consumer experience; an overly casual tone can break the Pro experience.

---

## Legal awareness

Vinted Pro content regularly intersects with legally sensitive areas due to the commercial nature of the account type. Always flag copy in the following categories for legal review before shipping:

* **VAT and tax obligations:** Any content that describes or implies tax requirements for Pro sellers must be reviewed by legal. Requirements vary by market.
* **Consumer rights:** Pro sellers are subject to consumer protection law in most markets. Copy that describes buyer-seller interactions, returns, or refunds must be legally reviewed.
* **Business verification:** Any content related to the verification of a user's business identity or eligibility for a Pro account must be reviewed by legal and compliance teams.
* **Subscription and billing terms:** Copy describing Pro subscription costs, renewal terms, or cancellation conditions must accurately reflect the contractual terms and be reviewed before publishing.
* **"Earn money" language:** Always frame earning in the context of selling (e.g. "Earn money selling on Vinted"), never listing. Listing alone does not generate income.
