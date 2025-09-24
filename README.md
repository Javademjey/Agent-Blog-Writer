# Agent-Blog-Writer
Generate polished Markdown blog posts from a topic and a template using a simple LangGraph workflow.

## Project Overview
A lightweight, two-step blog generator powered by *LangGraph*, *Tavily Search*, and an *OpenAI* chat model.

- Input: a topic (`query`) and a blog template (`specific_format`).
- Step 1 — Search: Uses Tavily to fetch relevant web content and aggregates results.
- Step 2 — Write: Prompts an OpenAI model to produce a blog post that follows your template, grounded in the search results.
- Orchestration: A simple LangGraph state machine routes from search → generate → done.
- Output: A polished Markdown blog post you can publish immediately.

**Key features:**

- Pluggable template: define tone, structure, and SEO fields.
- Deterministic flow with max simplicity (two nodes, one conditional).
- Notebook-friendly: renders the graph and displays the final post.

**Notes:**

- Replace hard-coded API keys with environment variables.
- You can extend the graph with steps like summarization, outlining, or SEO refinement.
