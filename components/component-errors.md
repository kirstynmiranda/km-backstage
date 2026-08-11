# Error messages — Component Rules

Purpose: Clear, actionable UI messages that help users recover when they encounter validation failures, system errors, connection problems, or any state where something went wrong.

## Structure
Type 1 - **Error dialog:** 
[Error Title]
[Body explaining cause or context - optional]
**Action:** [Button label or instruction]


Type 2 - **In-line error:** 1-2 sentences structured as follows [problem + why it happened (if known) + action]


## Core rules

* Use inline format for field validation; use modal/banner for system-level errors
* Adjust formality based on the severity of the issue

### Error dialog rules
Follow guidance from component-dialogs.md PLUS these error-dialog-specific rules: 
* Never blame the user
* Focus on describing how to recover from the error
* Never expose technical details (stack traces, error codes) in user-facing copy
* Omit body if the title + action make the situation and fix obvious


### In-line error rules
* Never expose technical details (stack traces, error codes) in user-facing copy
* Identify the field and the problem specifically
* Lead with the action, then explain the reason if needed
* Neutral tone — don't blame the user
* No "sorry" or "please". No "to continue" (redundant)
* Fragment: no end punctuation. Full sentences: use punctuation
* Always offer a solution or next step, even if it's "try again" or "contact support"
