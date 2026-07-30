# Best Practices

Short, practical lessons for building with LLMs. One line each, plain language. These are
starting rules of thumb — not laws. Adapt to your case.

## Prompting

- Be specific — state the format, length, and audience you want. Vague in, vague out.
- Show examples (few-shot) — one good example often beats a paragraph of instructions.
- Ask for step-by-step reasoning on hard tasks; skip it on simple ones (it's slower and costlier).
- Put long reference text first and the question last — models attend to that layout better.

## Agents

- Start with a plain workflow, not an agent. Add autonomy only when the task truly needs it.
- Give tools clear names and descriptions — the model picks tools from those, like a person reading docs.
- Keep tools few and distinct — overlapping tools cause wrong picks.
- Add guardrails: validate tool inputs, cap loops and steps, and handle tool errors gracefully.

## Retrieval (RAG)

- Chunk by meaning (sections, paragraphs), not fixed character counts.
- Retrieve, then re-rank — the first search gives recall; re-ranking gives precision.
- Always show sources — cite what the answer came from. Builds trust and catches hallucination.

## Evaluation & cost

- Build a small eval set early — even 20 examples catch regressions fast.
- Test with real failure cases, not just the happy path.
- Track token cost per request — cache stable context, and trim what you resend.

## Designing Claude plugins & MCP servers

- Design tools around the **actions your agent takes**, not around your existing REST endpoints. Auto-generating one MCP tool per API call forces many round-trips and multiplies errors, latency, and cost. ([why](https://kylestratis.com/posts/stop-generating-mcp-servers-from-rest-apis/))
- Make each tool do one whole, meaningful job — hide internal composition (fetch → filter → format) behind a single call.
- Name and describe tools for the model, not the developer — the description is the model's only manual for when to use it.
- Return clean, minimal results — give the model what it needs to act, not a raw API dump it has to parse.
- Make tools safe to retry (idempotent where possible) and return clear, actionable error messages.
- Keep the toolset small and focused — fewer, distinct tools beat many overlapping ones.
- For a Claude Code plugin, bundle only related tools per server, document each clearly, and test with real agent tasks — not just unit calls.
