# component-moderation-notices.md

Reference documentation for writing DSA-compliant moderation notices on Vinted.
For use by content designers, strategists, and copywriters.

---

## What is a moderation notice?

- A notice is a message sent to Vinted members in their in-app messaging inbox. Notices inform members of information about their account, platform updates, promotions, and more. 
- The EU Digital Services Act (DSA) requires Vinted to send a specific type of notice called a **moderation notice** each time Vinted issues a moderation decision or action against a member's account
- The purpose of moderation notices is to clearly explain the rationale behind each moderation decision and the impact to the affected member
- All moderation notices must follow this structure to remain legally compliant

---

## Notice tone guidance

Moderation notices should follow Vinted's safety, security, and moderation tone of voice. This means using only two of Vinted's three brand voice principles:
1. **Practical (Foundation):** Clarity is the priority. Function is non-negotiable. 
2. **Familiar (Tone):** Keeps the brand human and approachable.


### Tone mapping by situation
| Context | Primary Pillar | Secondary Pillar | Other characteristics|
| :--- | :--- | :--- | :--- |
| **Bad or frustrating news** | Practical | Familiar | Focus on reassuring the member. Consider acknowledging their frustration. Clearly outline the situation, consequences, and next steps. |
| **Warning or violations**| Practical | Practical | Focus on neutrally stating the facts in a sober and resolute way. Avoid making accusations or scolding. |

---

## Notice structure

Every moderation notice is made up of the following parts. Required parts must always be included. Optional parts should be included only when they apply to the specific moderation situation.

### 1. Notice code
A code used internally to identify the notice type. Follow this convention:

| Situation | Code format |
| :--- | :--- |
| First notice sent | No numbered code needed |
| Removing or hiding content | No numbered code needed |
| Permanent block | Include `_BLOCK` |
| Proof-related notice | Include `_PROOF` |

Check with your team for situation-specific code information.

---

### 2. Title *(required)*

State what action was taken and why. This gives moderators context so they can select the correct notice to send.

**Format:** `[Action taken]: [reason]`

**Example:** `Listing deleted: copyright violation`

---

### 3. Body *(required)*

The body must follow this sequence. Each paragraph serves a specific legal and communicative purpose. 

**Body formatting**

```YAML
sections:
  - id: 1
    name: Greeting
    purpose: Acknowledge the member
    requirements:
      - Use {{ user_name }} liquid tag
      - No greeting words (e.g. hi, hello)

  - id: 2
    name: Intro
    purpose: >
      Brief summary of the reason the member is receiving this notice
      and the impact to them/their account. *(required)*
    requirements:
      - 1-2 sentences max
      - Outline key moderation/actioning decisions and the reason we took this action
      - Use passive voice when describing the outcome of moderation actions to distance us from liability or blame
    structure: "[impact to member] + [reason for decision]"

  - id: 3
    name: Detailed explanation of decision
    purpose: >
      Supporting details outlining the reason for the moderation/actioning
      decision introduced in section 2. *(required)*
    requirements:
      - Approx. 2-3 paragraphs
      - Use bullet points to organize information as needed
      - Aim for conciseness without sacrificing clarity
      - Give enough detail to help the member understand our rationale
      - Start with a section heading introducing the topic
      - Front load the heading with relevant keywords to promote scannability
    structure: "[Section heading] + [details]"

  - id: 4
    name: Next steps
    purpose: Help the member understand expected next steps or recovery actions. *(required when relevant)*
    requirements:
      - Guide or educate the member
      - Be concise and actionable
      - Can be a short paragraph (2-3 sentences) or an ordered list of steps
      - Start with a section heading titled "Next steps"
    structure: "[Section heading] + [details]"

  - id: 5
    name: Additional information
    purpose: >
      Follow up information about consequences, future actioning,
      or related resources. *(include only when applicable)*
    requirements:
      - Stay concise
      - Avoid blaming or scolding the member

  - id: 6
    name: Sign off
    purpose: Close letter
    structure:
      - "Thanks for your cooperation,"
      - "Thanks for your understanding,"

  - id: 7
    name: Signature
    purpose: Close letter
    structure:
      - "Vinted Support" 
```

#### a. Intro *(required)*
 Give the member a brief summary of the reason the member is receiving this notice and the impact to them/their account.

> *"Some of your recent activity appears to go against our Terms and Conditions."*

Refer to the specific contractual grounds for the decision. Choose the most accurate combination:
- Terms and Conditions
- Community Standards
- Catalogue Rules
- Terms and Conditions and Community Standards
- Terms and Conditions and Catalogue Rules
- Community Standards and Catalogue Rules
- Terms and Conditions, Community Standards, and Catalogue Rules

Note: write "Terms and Conditions" in full — no ampersand. Use "Catalogue" (not "Catalog").

---

#### b. Detailed explanation of decision *(required)*

##### b-1. Explain how the violation was detected 
Reassure the member that this was a considered decision, not a snap judgement.

> *"We use various methods, including internal practices and third-party reports, to help identify issues like this. Using these methods, we carefully evaluate and take action against misuse of Vinted's platform."*

If the notice was triggered via the notice and action form (NTD tool), use this instead:

> *"We're sending this message because we received a report from our notice and action form."*

##### b-2. Explain impact to the content or member's account
Explain what happened to the member's content as a direct consequence of the breach.

> *"As a result, we've hidden the following listings."*
> *"As a result, we've removed the following listings."*
> *"As a result, we've deleted your feedback."*
> *"As a result, we've deleted your profile description."*

**When two sanctioning actions are taken:** do not separate them into different paragraphs. Lead with the decision on the content (deleted or hidden item), then immediately state the account action.

> *"As a result, we've removed the post and blocked your account."*


##### b-3. Explain how the decision affects the member *(required when relevant)*
If the moderation action restricts what the member can do on the platform, explain the impact clearly.

> *"While your account is restricted, you won't be able to do things like buy items or add new payment methods."*

For banned accounts, include what the member **can** still do:

> *"Even though your account is banned, you can still access your messages on Vinted's website or app. You can also finish any ongoing transactions."*

> *"Even though your account is banned, you can still withdraw any remaining funds from your Vinted Balance"*

Use the same pattern for locked or blocked accounts, substituting the relevant account state.

---

#### c. Next steps *(required when resolvable)*
If the member can take action to resolve the situation, explain clearly what they need to do.

> *"Make sure to upload proof of authenticity, including any packaging or proof of purchase."*

Examples of resolvable situations include: uploading proof of authenticity, updating an item's brand, or providing photos of proof of purchase.

---

#### d. Additional information *(include only when applicable)*

**Reference a previous warning:**
> *"This is your second warning regarding your insulting, rude messages or comments to other members."*

**Warn about the consequences of further violations:**
> *"If your behaviour continues to go against our Catalogue Rules, we may have to ban your account."*

Use "we may" when the next notice won't include a ban. Use "we'll" when the next notice will.

**State the outcome for the member's account:**
> *"Because of this, we've temporarily banned your account for [NUMBER] days."*
> *"Because of this, we've permanently banned your account."*

**Warn that subsequent accounts aren't allowed:**
> *"Creating multiple accounts goes against our Terms and Conditions, so any further accounts you create will be removed."*

**Explain that paid services can't be refunded:**
> *"Unfortunately we can't issue refunds for paid services (like item Bumps or Spotlights) when we have to remove a listing for going against our rules."*

**Privacy Policy rider** *(ban and blocking notices only):*
> *"To learn more about your rights on Vinted, read our Privacy Policy."*

##### d-2. Relevant links, resources *(required)*

Always include country-specific links using liquid tags so they localise correctly for each member (e.g. `https://{{domain_name}}/help/articlenumber`).

**Standard links to include:**
- Terms and Conditions
- Community Standards
- Catalogue Rules
- Relevant Help Centre article(s)

**Situation-specific links:**

| Situation | Link to include |
| :--- | :--- |
| Account blocking | Why was my account blocked? |
| Profile description or photo removed | How to manage account details |
| Username changed by moderation | How to change username |
| Inappropriate behaviour | Community Standards |
| Listing hidden or deleted | Why your listing was hidden or deleted; What you can sell on Vinted |
| Photo quality or replica proof issues | What photos you should upload |
| Brand name or wrong description | Describing an item |
| Incorrect condition description | Choosing item condition |
| Auction notices | How to set a correct price? |
| Multiple items or duplicates | Selling multiple items |
| Pet care items | Pet care category: what you can sell |
| Entertainment items | Entertainment: what you can sell |
| Removed feedback | Review policy |

Note: only add a link to the Privacy Policy for account ban or blocking notices.

Note: do not mention appealing or include an appeal link. A separate automated message will be sent to the member informing them of that option.

---

## Approved phrase kit

These phrases have been reviewed and approved for tone of voice and legal compliance. Use them as your starting point — they are not exhaustive or one-size-fits-all.

| Type | Approved text | Notes |
| :--- | :--- | :--- |
| **Notifying of a violation** | "We've been notified that your behaviour on Vinted goes against our [contractual grounds]." | Choose the correct combination of grounds from the list above. |
| | "Another member has reported your Vinted account for behaviour that goes against our Terms and Conditions." | |
| | "Your behaviour may have been reported for any of the following reasons:" | |
| **Hiding content** | "As a result, we've hidden the following listings." | Use only when listings are included in the notice. |
| | "As a result, we've hidden one or more of your listings." | Use when the notice header contains affected listings. |
| **Removing content** | "As a result, we've removed the following listings." | Use only when listings are included in the notice. |
| | "As a result, we've removed one or more of your listings." | Use when the notice header contains affected listings. |
| | "As a result, we've deleted your feedback." | |
| | "As a result, we've deleted your profile description." | |
| **Further steps for members** | "Please review your wardrobe and remove any items that aren't allowed on Vinted. (If you need a refresher on what's allowed on Vinted, read our Catalogue Rules: [INSERT LINK])" | Note the closed parenthesis after the link. |
| **Grounds for decision** | "Our Catalogue Rules state that items which [INSERT REASON] aren't allowed on Vinted." | |
| | "Our Terms and Conditions forbid [INSERT SITUATION]." | |
| **Account decision — warning** | "If your behaviour continues to go against our Catalogue Rules, we may have to ban your account." | Use "may" when the next notice won't include an account ban. |
| | "If your behaviour continues to go against our Catalogue Rules, we'll have to temporarily ban your account." | Use "we'll" when the next notice will include an account ban. |
| **Account decision — temporary ban** | "Because of this, your account is temporarily banned for [NUMBER] days." | |
| **Account decision — block** | "Because of this, your account is permanently blocked." | |
| **Initiating a temporay ban** | "Your account is temporarily banned. The ban will expire in [NUMBER] days." | |
| **Maintaining a temporary ban** | "Your account will stay banned. The ban period lasts for [NUMBER] days, starting on the day you first received notice of temporary account ban." | |
| **Multiple accounts** | "Creating multiple accounts goes against our Terms and Conditions, so any further accounts you create will be removed." | |
| **Continued violations** | "If you continue to [send messages that go against our Terms and Conditions / list prohibited items / post comments or images that go against our Terms and Conditions] on Vinted, we'll have to remove them and block your account." | Choose the most relevant option. |
| **Information source** | "We use various methods, including internal practices and third-party reports, to help identify issues like this. Using these methods, we carefully evaluate and take action against misuse of Vinted's platform." | |
| | "We're sending this message because we received a report from our notice and action form." | Only for notices triggered via the NTD tool. |
| **Refunds** | "If we remove a listing for going against our rules, we can't issue refunds for paid services like Bumps or item verification." | |
| **Privacy Policy rider** | "To learn more about your rights on Vinted's platform, read our Privacy Policy." | ban and blocking notices only. |


---

## Example notice

The following is an annotated example of a compliant notice structure.

```
{{user_name}},                               	   ←  Acknowledge member 

It seems like you've been using Vinted in a        ← Summarize legal reason for decision and impact to member
way that goes against our Terms and               
Conditions, so we've temporarily restricted
your account while we review.

Our team regularly reviews and removes content     ← Explain how we detected the violation
that isn't aligned with our Terms and Conditions.


While your account is restricted, you won't        ← Explain how this affects the member
be able to do things like buy items or add
new payment methods.

We'll let you know as soon as we've                ← Include next steps (if any)
finished our review. This could take up
to 24 hours.

Thank you for understanding,
Vinted Support
```
