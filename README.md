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

