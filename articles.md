# Articles

Curated, high-signal reads on AI, Claude, and LLMs. Each entry says why it's worth your
time. Newer additions go at the top of their group.

## Getting started / big picture

- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — Jay Alammar. **Why read:** the clearest visual explanation of how transformers (the engine behind LLMs) actually work.
- [Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI) — Andrej Karpathy. **Why read:** a friendly, thorough walkthrough of how LLMs are trained and behave, from someone who builds them.
- [What We Learned from a Year of Building with LLMs](https://applied-llms.org/) — Eugene Yan et al. **Why read:** hard-won, practical lessons on shipping real LLM products, not toy demos.
- [Building LLM Applications for Production](https://huyenchip.com/2023/04/11/llm-engineering.html) — Chip Huyen. **Why read:** honest look at the gap between a cool prototype and a reliable product.

## Prompting

- [Prompt Engineering overview](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) — Anthropic docs. **Why read:** the canonical, practical techniques for getting good output from Claude.
- [Prompt Engineering](https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/) — Lilian Weng. **Why read:** a well-organized survey of prompting methods with the research behind them.
- [Prompt Engineering Guide](https://www.promptingguide.ai/) — DAIR.AI. **Why read:** a free, constantly-updated reference covering techniques from basics to advanced.

## Agents

- [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) — Anthropic. **Why read:** the best short guide on when to use simple workflows vs full agents, with clear patterns.
- [A Practical Guide to Building Agents](https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf) — OpenAI (PDF). **Why read:** vendor-neutral fundamentals of agent design, tools, and guardrails.
- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — Lilian Weng. **Why read:** the reference map of agent architecture — planning, memory, tool use.
- [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) — Yao et al. **Why read:** the paper behind the "reason then act" loop most agents still use.

## Retrieval (RAG)

- [Retrieval-Augmented Generation](https://arxiv.org/abs/2005.11401) — Lewis et al. **Why read:** the original RAG paper — grounding LLMs in your own data.
- [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) — Wei et al. **Why read:** shows how asking a model to "think step by step" boosts reasoning — foundational to RAG and agents.

## Claude & tooling

- [Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices) — Anthropic. **Why read:** concrete workflow tips for agentic coding with Claude.
- [Introducing the Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) — Anthropic. **Why read:** the open standard for connecting LLMs to tools and data — worth understanding early.
- [Stop Generating MCP Servers from REST APIs!](https://kylestratis.com/posts/stop-generating-mcp-servers-from-rest-apis/) — Kyle Stratis. **Why read:** shows why auto-converting REST APIs into MCP tools backfires, and to design tools around the actions an agent takes instead.
- [Simon Willison's blog](https://simonwillison.net/tags/llms/) — Simon Willison. **Why read:** the best running commentary on what's actually new and useful in LLMs, tested hands-on.
