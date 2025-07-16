---
layout: post
title: "Tool Using Between LLM Providers"
date: 2025-07-16
categories: [llm, tools]
tags: [openai, anthropic, langgraph]
---

When implementing tool calling across different LLM providers, there's one critical distinction you need to know: **most providers follow OpenAI's format, except Anthropic**.

The majority of LLM providers have adopted OpenAI's client interface as their standard:

- Gemini (Google)
- Grok (xAI)
- DeepSeek

This standardization means you can swap providers with minimal code changes. 

Anthropic's Claude models stand alone with their own format. But the real gotcha isn't the client call -- it's how tool conversations are managed: Stateless vs Stateful

### OpenAI-Style: Stateless Freedom

With OpenAI-compatible providers, you can freely switch between tool and non-tool calls:

```python
# Start with tools
response1 = model.bind_tools(tools).invoke(messages)

# Later, call without tools - totally fine!
response2 = model.invoke(messages)  

# Switch back to tools whenever - no problem!
response3 = model.bind_tools(tools).invoke(messages)
```

### Anthropic-Style: Stateful Commitment

With Anthropic, **once you use tools, you're locked in**:

```python
# Start with tools
response1 = model.bind_tools(tools).invoke(messages)

# Try to call without tools...
response2 = model.invoke(messages)  # 💥 ERROR!
```

Remember this distinction and you'll save hours of debugging when working with different LLM providers!

