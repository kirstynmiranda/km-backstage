# Vinted voice and tone - Brand Portal

This tone guide explains how to modulate Vinted's general tone of voice for content in the brand management portal. If any of the guidance here conflicts with the information outlined in Vinted voice and tone - general guidelines, defer to this document.

---

## Context

The brand management portal is a B2B tool used by corporate brand representatives — typically legal, compliance, or brand protection teams at established companies — to report suspected copyright infringement and counterfeit listings in Vinted's marketplace to Vinted's moderation team.

Adopt this tone when creating content for any of the following experiences:

* **Reporting flows:** Any content a brand representative interacts with when submitting, editing, or withdrawing an infringement or counterfeit report.
* **Case management:** Any content related to tracking the status of submitted reports, reviewing moderation outcomes, or managing open and closed cases.
* **Account and access management:** Any content related to portal registration, login, user permissions, and account settings.
* **System notifications and updates:** Any automated or triggered communications informing brand representatives of case status changes, required actions, or system-level updates.

> **Note on terminology:** In the brand management portal, do not refer to users as "members." Brand representatives are professionals acting on behalf of a corporate entity, not individual Vinted community members. Users are typically called "reporters" or "users", although there are other variations. Use "you/your" for second-person address. When referring to the brand collectively, use "your organisation" as appropriate.

**Example**

General Vinted content:
```yaml
dialog:
  heading: Vinted is your platform for pre-owned pieces you'll love
  subheading: One community, thousands of brands, and a whole lot of second-hand style. Ready to get started? Here's how it works.
```

Brand management portal content:
```yaml
dialog:
  heading: Report submitted
  body-copy: Your report has been received and assigned to our moderation team. We'll review it and update the case status within 5 business days. You can track progress in your case dashboard.
  button:
    label: Go to dashboard
    action: Navigate to case management dashboard
```

---

## Tone modulation

Brand management portal content uses only one of Vinted's three brand voice pillars as its foundation, with a significantly reduced secondary register:

1. **Practical (Foundation):** Clarity and precision are non-negotiable. Every string must orient the user, communicate status, or drive a specific action. Remove anything that does not serve one of these functions.
2. **Familiar (Minimal accent):** Retain enough human warmth to avoid feeling cold or robotic, but do not prioritise it. This is a professional tool, not a consumer product.

> **Joyful is never used** in the brand management portal. This includes success states. A successfully submitted report is a professional milestone, not a celebratory moment.

### Additional tone principles

**Brand management portal content should always:**
* Be precise and outcome-oriented. Lead with what happened, what it means, and what comes next.
* Respect the user's professional expertise. Do not over-explain standard business or legal concepts.
* Use consistent, predictable language. Terminology for key actions and statuses (e.g. "submit", "case", "under review", "resolved") should be used uniformly across all surfaces.
* Be status-driven. At every point in a flow, the user should be able to answer: *What did I submit? What is happening with it? What do I need to do next?*

**Brand management portal content should never:**
* Use celebratory or consumer-facing language (e.g. "Great job!", "You're all set!", "Nice one!").
* Use casual contractions or colloquial phrasing that would feel out of place in a professional SaaS tool.
* Be vague about case status or moderation outcomes. Users are accountable to their organisations and need accurate, unambiguous information.
* Use urgency language or pressure tactics (e.g. "Act now", "Don't miss this"). If a deadline exists, state it factually.

**Writing voice — active vs. passive:**

Brand management portal content should use the active voice as the default, particularly for instructions and user-facing actions. Use the passive voice only in these situations:

* To describe actions completed by Vinted's moderation team or automated systems (e.g. "Your report has been reviewed.")
* To describe case outcomes neutrally, without implying fault or judgement (e.g. "The listing was removed.")
* To communicate legal or compliance-adjacent decisions where an impersonal register is more appropriate

---

## Tone mapping by situation

| Context | Primary pillar | Secondary pillar | Other characteristics |
| :--- | :--- | :--- | :--- |
| **Case status updates** | Practical | Practical | State the outcome clearly and factually. Include what changed and any required next steps. No filler. |
| **Successful submissions** | Practical | Practical | Confirm what was submitted and what happens next. Do not celebrate. |
| **Errors and failed actions** | Practical | Familiar | Identify the problem specifically. Tell the user how to fix it. Do not blame. |
| **Required actions / deadlines** | Practical | Practical | State the action, the reason if relevant, and the deadline factually. Avoid urgency language. |
| **Empty states** | Practical | Familiar | Explain what the space is for and how to get started. Keep it brief. No filler copy. |
| **Account and access issues** | Practical | Familiar | Focus on resolution. Be direct about what went wrong and how to fix it. |

### Tone "Volume" logic

* **Case status updates:** Volume 0% Familiar.
* **Successful submissions:** Volume 0% Familiar.
* **Errors and failed actions:** Volume 20% Familiar.
* **Required actions / deadlines:** Volume 0% Familiar.
* **Empty states:** Volume 20% Familiar.
* **Account and access issues:** Volume 20% Familiar.

---

## Legal awareness

Brand management portal content frequently intersects with legally sensitive areas. Always flag copy in the following categories for legal review before shipping:

* **Infringement and counterfeit claims:** Avoid language that pre-judges the outcome of a report (e.g. "counterfeit item removed" before moderation has confirmed the outcome). Use neutral language such as "reported listing" until a decision has been made.
* **Moderation outcomes:** Do not imply that Vinted guarantees a specific outcome for any report. Vinted reviews reports and makes independent moderation decisions.
* **Timelines and SLAs:** Only include review timelines if they have been agreed with the relevant internal teams. Do not invent or estimate timelines in copy.
* **Data and evidence handling:** Any content that describes how submitted evidence (images, documents, URLs) is stored or used must be reviewed by legal and privacy teams.
