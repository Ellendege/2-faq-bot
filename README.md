# Project 2 — FAQ Bot with XML Context

## Overview
This project builds a **FAQ Bot prompt** that separates:
- **Context (FAQ data)** → questions and answers in `<CONTEXT>`
- **Instructions** → guidance for how the bot should respond in `<INSTRUCTIONS>`
- **User query** → placed in `<USER_QUESTION>`

This reduces hallucinations and ensures concise, reliable answers.

## How It Works
1. Start with a base XML structure (`faq_prompt.xml`).
2. Insert FAQ data inside `<FAQS>`.
3. Add user questions inside `<USER_QUESTION>`.
4. Run in an LLM to generate answers limited to the context.

## FAQ Versions
- **faqs-v1**: Sample (password reset, refund policy, support channels)
- **faqs-v2**: M-Gas example (topping up via M-Pesa, cylinder troubleshooting, relocation, fraud reporting)

## Sample Outputs

### Example Q1: How do I top up my account?
You can top up via M-Pesa by selecting Paybill 332211, then entering your account number.


### Example Q2: What if I move to a new house?
Yes, but please notify M-Gas support so a technician can reinstall the cylinder safely at your new location.


### Example Q3: How do I report gas leaks?
I don’t have information on reporting gas leaks in the FAQs provided.
The best next step is to call M-Gas support immediately for safety assistance.
If you suspect danger, also contact your local emergency services right away.
Would you like me to share the support hotline number listed for other issues



## Reflections
- XML separation clearly improved accuracy and conciseness.
- Versioning FAQs (`faqs-v1`, `faqs-v2`) helps track changes over time.
- The bot gracefully handles missing info by suggesting next steps.
- Next iteration: enrich answers with support links and escalation paths.

---

📌 See prompt file: [`faq_prompt.xml`](./faq_prompt.xml)  
📒 Iteration notes: logged in Notion (`Intermediate Project 2 — FAQ Bot`)  
