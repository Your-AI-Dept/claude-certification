# CCDV-F: Claude Certified Developer – Foundations

[CCAR-F](ccar-f.md) · [CCDV-F](ccdv-f.md) · [CCAO-F](ccao-f.md) · [CCAR-P](ccar-p.md) · [Handbook home](../README.md)

CCDV-F (Claude Certified Developer – Foundations) is Anthropic's certification for developers who build applications on Claude. The exam is 53 questions in 120 minutes, proctored and closed-book, delivered by Pearson VUE, with a passing score of 720 on a 100–1,000 scale and a $125 fee per attempt.

Against the rest of the program: CCAR-F tests system design where CCDV-F tests the code itself, CCAO-F is the non-developer track, and CCAR-P extends the architect side. Developers who spend their days shipping Claude features fit here; a third of the marks are applications and integration, which no other exam in the program weights so heavily.

Facts checked August 28, 2026 against the Pearson VUE program listing and the published exam guide. Longer guide with sources: [youraidept.com/network/ccdv-f](https://youraidept.com/network/ccdv-f). Free practice questions: [youraidept.com/network/ccdv-f-practice-questions](https://youraidept.com/network/ccdv-f-practice-questions).

## Quick facts

| | |
|---|---|
| Questions | 53 items in 120 minutes |
| Passing score | 720 on a 100–1,000 scale |
| Exam fee | $125 per attempt, per the current exam guide |
| Format | Proctored and closed-book, no AI assistance |
| Delivery | Pearson VUE, online proctored or at a test center |
| Retakes | Up to 4 attempts per rolling 12 months (14, 30, then 90-day waits) |
| Validity | 12 months, with a free on-time renewal assessment |

Registration runs through the Anthropic Partner Academy, which requires affiliation with a Claude Partner Network organization. Independent engineers usually get access by joining a partner firm such as [YAID](https://youraidept.com/network?ref=github). Full path: [registration.md](../registration.md).

## Who it is for

The exam guide describes the target candidate precisely: an engineer with one to five years of experience, at least six months hands-on with Claude or comparable LLM systems, proficient in Python or TypeScript, and fluent with REST APIs and CLI tools. A third of the exam is applications and integration, so it rewards people who have shipped.

## Exam domains

| Domain | Weight |
|---|---|
| Applications and integration | 33.1% |
| Model selection and optimization | 16.8% |
| Agents and workflows | 14.7% |
| Prompt and context engineering | 11% |
| Tools and MCPs | 10.6% |
| Security and safety | 8.1% |
| Claude Code | 3.1% |
| Eval, testing, and debugging | 2.6% |

Eight domains, per exam guide v1.0 (July 2026).

## What each domain covers

What to know before you sit, organized by the published blueprint. Nothing here describes an exam question.

### Applications and integration

- The Messages API: request shape, message roles, system prompt placement, max_tokens, and what each stop_reason means (end_turn, max_tokens, tool_use, stop_sequence).
- Streaming responses and how to handle partial content and tool-use blocks as they arrive.
- Multimodal inputs: images and PDFs as content blocks, and the Files API for reusing uploads.
- Structured output: JSON via tool definitions or structured outputs, and validating what comes back.
- The Batch API for high-volume, non-urgent work at lower cost.
- Errors, rate limits, and retries: status codes, exponential backoff, and idempotent design for anything that writes.
- Prompt caching mechanics: cache breakpoints, minimum lengths, and ordering stable content first.

### Model selection and optimization

- The model family trade-off: the most capable model for hard reasoning, the mid-tier for most production work, the smallest for high-volume classification and routing.
- Cost is tokens in plus tokens out; latency is dominated by output tokens. Optimize both by trimming prompts, capping max_tokens, and caching.
- Extended thinking budgets: when deeper reasoning pays for itself and when it is wasted.
- Temperature and sampling settings, and why deterministic tasks want low temperature.
- Routing patterns: a small model classifies, a larger model handles the hard cases.

### Agents and workflows

- Implementing the agent loop in code: send messages, detect tool_use blocks, execute, append tool_result blocks, repeat until end_turn.
- Workflow patterns from Anthropic's guidance (chaining, routing, parallelization, orchestrator-workers, evaluator-optimizer) and how to pick one.
- The Claude Agent SDK: what it handles for you (the loop, tools, permissions, hooks, subagents) versus a hand-rolled loop.
- Stop conditions, max turns, and human approval steps.

### Prompt and context engineering

- System prompt versus user turn, examples, XML structure, prefilling, and long-context ordering.
- Managing conversation history: truncation, summarization, and what to keep verbatim.

### Tools and MCPs

- Tool definitions with JSON schema, descriptions written for the model, tool_choice, parallel tool calls, and error results.
- Connecting to MCP servers from an application and the difference between tools, resources, and prompts.

### Security and safety

- Prompt injection through tool results and documents: treat retrieved content as data, and keep instructions in the system prompt.
- Least privilege for tools: read-only by default, confirmation for writes, no secrets in prompts.
- Handling personal data, logging, and retention; Anthropic's usage policies as constraints on what you build.
- Output validation before anything is executed, sent, or stored.

### Claude Code

- What Claude Code is, where it runs, CLAUDE.md, and the basics of hooks, MCP configuration, and headless use. A small domain, so keep the prep proportionate.

### Eval, testing, and debugging

- Golden test sets, LLM-as-judge grading, regression tests on prompt changes, and logging enough to reproduce a bad response. This is the smallest domain on the exam.

## Prep notes

- Applications and integration is a third of the exam. If your Claude experience is mostly prompting, build and deploy something real against the API before you sit it.
- Claude Code and eval tooling together are under 6% of the marks. Do not over-prepare the small domains at the expense of integration and model selection.
- The guide's experience profile is honest: six months of hands-on Claude work is the real prerequisite, even though no formal one is enforced.

## Common mistakes

- Preparing as if this were the architect exam, when a third of the marks are integration code and Claude Code plus evals together are under 6%.
- Not knowing the stop_reason values and what to do with each one.
- Skipping the Batch API, Files API, and prompt caching because they were not needed in your own project.
- Sitting the exam with mostly prompting experience. The guide asks for six months of hands-on API work and the question mix is built around it.

## A study path

1. Week 1: read the exam guide and the Messages API reference. Build a script that streams a response, calls a tool, and handles every stop_reason.
2. Week 2: add prompt caching, a batch job, and a PDF input to that script. Measure cost before and after caching.
3. Week 3: build a small agent loop by hand, then rebuild it with the Agent SDK. Add an eval with a golden set.
4. Week 4: Partner Academy prep course and a practice exam; closed-book review of the API reference.

## Official reading

- [Claude Developer Platform docs](https://docs.claude.com/)
- [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
- [Writing tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents)
- [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [Claude Code docs](https://code.claude.com/docs)
- [Pearson VUE: Claude Certification Program by Anthropic](https://www.pearsonvue.com/us/en/anthropic.html)
- The CCDV-F exam guide, distributed through the Anthropic Partner Academy

## FAQ

### What is the CCDV-F exam?

CCDV-F is Claude Certified Developer – Foundations, Anthropic's certification for developers building applications on Claude. It is 53 questions in 120 minutes, proctored and closed-book, with a passing score of 720 on a 100–1,000 scale.

### What is the difference between CCDV-F and CCAR-F?

CCDV-F tests hands-on application development: integration, model selection, and agents in code. CCAR-F tests system design: agentic architecture, tool design, and context strategy. Developers deep in the code usually fit CCDV-F; engineers who design and sell systems usually fit CCAR-F.

### How much does the CCDV-F exam cost?

$125 per attempt, per exam guide v1.0. The credential is valid for 12 months, with a free on-time renewal via a non-proctored assessment on the Anthropic Partner Academy.

### What experience do I need for CCDV-F?

No prerequisite is enforced, but the exam guide targets engineers with one to five years of experience, six months of hands-on Claude or LLM work, Python or TypeScript proficiency, and fluency with REST APIs and CLI tools.

### How do I register for the CCDV-F exam?

Through the Anthropic Partner Academy, which requires affiliation with a Claude Partner Network organization. Independent developers usually get access by joining a partner firm such as YAID, then schedule through Pearson VUE.

### How do I take the CCDV-F exam?

Get eligibility through a Claude Partner Network organization, register inside the Anthropic Partner Academy, then schedule with Pearson VUE, online proctored or at a test center. Independent engineers usually join a partner firm such as [YAID](https://youraidept.com/network/apply?ref=github) to get that eligibility. Step by step: [registration.md](../registration.md).

---

Part of the [Claude Certification Handbook](../README.md), maintained by [YAID](https://youraidept.com/network?ref=github), a registered Claude Partner Network firm. Not an official Anthropic resource. Licensed [CC BY 4.0](../LICENSE).
