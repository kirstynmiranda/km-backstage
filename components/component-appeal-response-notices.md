# Appeal-response-notices.md

Reference documentation for writing DSA-compliant moderation notices on Vinted.
For use by content designers, strategists, and copywriters.

---

## What is an appeal response notice?

- A notice is a message sent to Vinted members in their in-app messaging inbox. Notices inform members of information about their account, platform updates, promotions, and more. 
- The EU Digital Services Act (DSA) requires Vinted to send a specific type of notice called a **moderation notice** each time Vinted issues a moderation decision or action against a member's account
- An **appeal response notice** is a follow up message sent to members who submit an appeal request after receiving a moderation notice

### Types of appeals
Appeal response notices can be sent in response to any of the following appeal types:
- **Reporter appeal** - appealing a decision about a content or user behavior report that was intially rejected
- **Notice appeal** - appealing a decision about an account moderation decision
-  

---

## Notice tone guidance

Moderation notices should generally follow Vinted's safety, security, and moderation tone of voice. Notices only use two of Vinted's three brand voice principles:
1. **Practical (Foundation):** Clarity is the priority. Function is non-negotiable. 
2. **Familiar (Tone):** Keeps the brand human and approachable.


### Tone mapping by situation
| Context | Primary Pillar | Secondary Pillar | Other characteristics|
| :--- | :--- | :--- | :--- |
| **Bad or frustrating news** | Practical | Familiar | Focus on reassuring the member. Consider acknowledging their frustration. Clearly outline the situation, consequences, and next steps. |
| **Warning or violations**| Practical | Practical | Focus on neutrally stating the facts in a sober and resolute way. Avoid making accusations or scolding. |

---

## Notice structure

### 1. Title *(required)*

The tile of every appeal response notice should be: "About your recent appeal"

### 2. Body *(required)*

**Requirements:**

- Guide or educate the member
- Clearly state the appeal outcome
- Aim for conciseness without sacrificing clarity 
- Be no longer than 2-3 paragraphs (± 350 words)

**Content structure**

```YAML

sections:
  - id: 1
    name: Greeting
    purpose: Acknowledge the member
    requirements:
      - Use {{ user_name }} liquid tag
    structure: "Hello + {{ user_name }}"

  - id: 2
    name: Intro
    purpose: >
      Acknowledge and thank member for taking action.
    requirements:
      - 1-2 sentences max
      - Include context about the type of appeal
    examples: 
    	- "Thanks for your message"
    	- "Thanks for reporting this content"
    	- "Thanks for bringing this to our attention"

  - id: 3
    name: Explanation of decision
    purpose: >
     Explain appeal outcome and reasoning behind our decision.
    requirements:
      - Approx. 1-3 paragraphs
      - Use bullet points to organize information as needed
      - Aim for conciseness without sacrificing clarity
      - Give enough detail to help the member understand our rationale
      - Front load the heading with relevant keywords to promote scannability

  - id: 5
    name: Additional information
    purpose: >
      Elaborate on consequences, account impact, possible next steps, OR affirm member if appeal was successful. *(include only when applicable)*
    requirements:
      - Stay concise
      - Avoid blaming or scolding the member
      - Affirm member's action and encourage repeat reporting if appeal was accepted
      - Include links to supporting information, if relevant

  - id: 6
    name: Sign off
    purpose: Close letter
    structure: 
      - "Thanks for your understanding," 
      - "Best regards"

  - id: 7
    name: Signature
    purpose: Close letter
    structure:
      - "Vinted Support" 

```

### Relevant links, resources *(include if relevant)*

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


---

## Approved phrase kit

Use these approved phrases in appeal response notices

| Situation | Approved text | Notes |
| :--- | :--- | :--- |
| **Acknowledging a mistake — item removal** | "We've reviewed and determined that this was a mistake. Your [listing has / listings have] been restored and your account is now unblocked. We apologise for the inconvenience." | Only use when the action was Vinted's error. |
| **Acknowledging a mistake — account moderation** | "We've reviewed and determined that this was a mistake. Your account info has been restored and your account is now unblocked. We apologise for the inconvenience." | Only use when the action was Vinted's error. |
| **Out-of-court settlement** | "If you aren't satisfied with this resolution, you can consider alternative ways to resolve your dispute as indicated in our Terms and Conditions (see Section 7, "Our right to handle concerns")." | Always add this sentence for notices sent after someone appeals a decision. |


---

## Example notices

The following are annotated examples of appeal response structure.

### Appeal accepted

```
Hello {{user_name}},                           ←  Greet member 


Thanks for bringing this     	   			   ← Acknowledge and thank member for taking action
to our attention.

We reviewed the content you 			   	   ← Explain appeal decision and outcome
reported and found that it violates our 
rules. Our team has already taken action 
to address the issue. 

We appreciate your commmittment to keeping	   ← Follow up: Affirm member and encourage repeat behavior	
our community safe, and encourage you 
to continue reporting future 
concerns. 

Best regards,								   ← Sign off
Vinted Support
```

### Appeal rejected

```
Hello {{user_name}},                              ←  Greet member 


Thanks for your message.						  ← Acknowledge and thank member for taking action

After manually reviewing your appeal, our 		  ← Explain appeal decision and outcome
team has decided to uphold our original
decision.

As a reminder, we took action against 			 
your account or listings because we 
found evidence of commercial activity
that isn't aligned with our Catalogue Rules, 
Community Standards, and/or Terms & Conditions.

Since we've upheld our decision, we're unable 	 ← Follow up: Elaborate on consequences, impact to member account
to reverse any related impact to your account, 
including warnings, restrictions, listing 
removals or bans.

We also can't issue refunds for 
paid services (like item Bumps or Spotlights) 
when we remove a listing for 
going against our rules.

Thanks for your understanding,				     ← Sign off
Vinted Support
```