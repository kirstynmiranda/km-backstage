# Vinted voice and tone - trust, security, and moderation content

This tone guide explains how to modulate Vinted's general tone of voice for platform safety, security, and moderation related content. If any of the guidance here conflicts with the information outlined in Vinted voice and tone - general guidelines, differ to this document.

## Context
The primary goal of this type of content is to inform Vinted members about platform security features and platform safety actioning. Adopt this tone when creating content related to any of the following topics:
* **Safety content:** Any content asset or piece of information related to keeping members safe from fraud, scams, and bad actors when transacting in Vinted's marketplace. 
* **Security content:** Any content asset or piece of information members interact with as part of a security check or product flow. This includes topics such as account registration and login, changes to account settings, and user data management.
* **Moderation content:** Any content asset or piece of information related to platform moderation decisions and disciplinary action. This includes inbox communications (called Notices) related to moderation decisions and actions. 

**Example** 

General Vinted content:
```YAML
dialog:
	Heading: Vinted is your platform for pre-owned pieces you’ll love
	Subheading: One community, thousands of brands, and a whole lot of second-hand style. Ready to get started? Here’s how it works.
```

Safety-related content:

```YAML
dialog:
	Heading: Don’t share personal info
	Body-copy: Watch out for scammers who may try to get your email or phone number, or ask you to chat outside of Vinted. Sharing your personal information could lead to scam emails and texts. 
```

Security-related content:

```YAML
dialog:
	Heading: Choose a different email to use with Vinted Pro
	Body-copy: You can’t use a business or company email to register a Vinted Pro account. Update your current email address to finish signing up.
	Button: 
		label: Update your email
		action: Proceed to account settings, change email screen
```

Moderation-related content:

```YAML
Title: Submit report
input-form:
	Report-reason: Non-genuine listing
		Report-reason-description: Item isn’t actually for sale or was listed in bad faith (such as for advertising or as a joke). 
	Text-input-box:
		Description: Tell us why you’re submitting this report. Be as specific as possible.
Button: 
	label: Submit
	action: Submit report
```

## Tone modulation
**Instruction:** Safety, security, and moderation content typically only uses two of Vinted's three brand voice principles:
1. **Practical (Foundation):** Clarity is the priority. Function is non-negotiable. 
2. **Familiar (Tone):** Keeps the brand human and approachable.

One exception: Content that is intended to **educate members** about security topics. This content can adopt the Joyful tone principle. This is the only exception. 

#### Additional tone principles
**Safety, security, and moderation content should always:**
* Focus on helping members understand and calculate risks as well as protect themself from harm
* Provide relevant information to help members understand the full context and options
* Be supportive and empathetic (when appropriate)

**Safety, security, and moderation content should never:**
* Include fluff or jargon 
* Be judgemental or condescending. Focus on helping them understand the situation, consequences, and how to overcome challenges. 
* Blame members or use overly-aggressive/punative language.

**Writing voice - active vs. passive:**
* Safety, security, and moderation content should typically use the active voice, especially when instructing on user actions. Only use the passive voice in these situations:
	* To describe actions that are completed by the system
	* To avoid blaming the member
	* To convey an inpersonal tone, such as when describing negative consequences or disciplinary outcomes

### Tone mapping by situation
| Context | Primary Pillar | Secondary Pillar | Other characteristics|
| :--- | :--- | :--- | :--- |
| **Bad or frustrating news** | Practical | Familiar | Focus on reassuring the member. Consider acknowledging their frustration. Clearly outline the situation, consequences, and next steps. |
| **Alerts and updates** | Practical | Practical | Focus on neutrally stating the facts in a polite, concise way. |
| **Warnings and violations**| Practical | Practical | Focus on neutrally stating the facts in a sober and resolute way. Avoid making accusations or scolding. |
| **Member education**| Practical | Familiar | These interactions can be more personable and moderately joyful, but the focus should remain on providing clear and helpful explanation of safety-related topics. |

#### Tone "Volume" Logic
* **Bad or frustrating news:** Volume 30% Familiar.
* **Alerts and updates:** Volume 10% Familiar.
* **Warnings and violations:** Volume 0% Familiar.
* **Member education:** Volume 60% Familiar, 20% Joyful.
