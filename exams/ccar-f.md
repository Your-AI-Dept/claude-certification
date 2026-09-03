# CCAR-F: Claude Certified Architect – Foundations

[CCAR-F](ccar-f.md) · [CCDV-F](ccdv-f.md) · [CCAO-F](ccao-f.md) · [CCAR-P](ccar-p.md) · [Handbook home](../README.md)

CCAR-F (Claude Certified Architect – Foundations) is Anthropic's certification for engineers and solution architects who design Claude-powered systems. The exam is 60 questions in 120 minutes, proctored and closed-book, delivered by Pearson VUE, with a passing score of 720 on a 100–1,000 scale and a $125 fee per attempt.

Against the rest of the program: CCDV-F tests hands-on application code where CCAR-F tests system design, CCAO-F is for non-developers, and CCAR-P is the professional tier that builds on this exam. If you sell or lead Claude implementation work, CCAR-F is the one to sit first; it is also the credential the market shortens to CCA-F.

Facts checked August 28, 2026 against the Pearson VUE program listing and the published exam guide. Longer guide with sources: [youraidept.com/network/ccar-f](https://youraidept.com/network/ccar-f).

## Quick facts

| | |
|---|---|
| Questions | 60 items in 120 minutes |
| Passing score | 720 on a 100–1,000 scale |
| Exam fee | $125 per attempt, per the current exam guide |
| Format | Proctored and closed-book, no AI assistance |
| Delivery | Pearson VUE, online proctored or at a test center |
| Retakes | Up to 4 attempts per rolling 12 months (14, 30, then 90-day waits) |
| Validity | 12 months, with a free on-time renewal assessment |

Registration runs through the Anthropic Partner Academy, which requires affiliation with a Claude Partner Network organization. Independent engineers usually get access by joining a partner firm such as [YAID](https://youraidept.com/network?ref=github). Full path: [registration.md](../registration.md).

## Who it is for

Engineers and solution architects who design systems on Claude: agent architectures, tool integrations, and the context strategies that hold them together. If you sell or deliver Claude implementation work, this is the credential clients will recognize first.

## Exam domains

| Domain | Weight |
|---|---|
| Agentic architecture | 27% |
| Claude Code workflows | 20% |
| Prompt engineering | 20% |
| Tool design and MCP | 18% |
| Context management | 15% |

Five domains, per the published exam guide.

## What each domain covers

What to know before you sit, organized by the published blueprint. Nothing here describes an exam question.

### Agentic architecture

- The agent loop: the model reasons, calls a tool, receives the result, and decides whether to continue or stop. Know what ends the loop (a final answer, a stop condition, a max-turns limit, a human checkpoint).
- Workflows versus agents. Anthropic's own framing: prompt chaining, routing, parallelization, orchestrator-workers, and evaluator-optimizer are workflows with fixed control flow; an agent decides its own path. Be able to say which pattern fits a given scenario and why a simpler one is often the right answer.
- Orchestrator and subagent designs: what the coordinator keeps, what it delegates, and why subagents get a clean context and a complete brief rather than a pointer to the parent's memory.
- Failure handling: retries with backoff, idempotent tool calls, timeouts, and what the system does when a tool returns an error instead of a result.
- Guardrails and human-in-the-loop: where approval gates belong (spend, deletion, external sends), and how hooks or permission checks enforce them outside the model's judgment.
- Cost and latency trade-offs: model choice per step, parallel tool calls, caching, and when a deterministic function beats a model call.

### Claude Code workflows

- CLAUDE.md as project memory: what belongs in it (commands, conventions, gotchas) and what does not (long documents the model can read on demand).
- The explore, plan, code, commit rhythm from Anthropic's best-practices guide, and plan mode as a way to separate thinking from editing.
- Slash commands, skills, and subagents: reusable prompts versus delegated work with its own context.
- Hooks: deterministic shell steps that run before or after tool calls, used for formatting, linting, blocking dangerous commands, and notifications.
- Permission modes and allow lists, and why the default asks before writes and shell commands.
- MCP server configuration at project and user scope, and headless use in CI and scripts with the print flag.
- Context hygiene: clearing and compacting, and why long sessions degrade without it.

### Prompt engineering

- System prompts for role and standing instructions; the user turn for the task. Clear, specific instructions work better than clever ones.
- Examples: a small number of high-quality examples steer format and tone more reliably than description alone.
- Structure with XML tags to separate instructions, documents, and examples, and to make long prompts unambiguous.
- Reasoning: chain-of-thought instructions and extended thinking, and when each is worth the tokens.
- Controlling output: response prefilling, requested formats, JSON via tool definitions or structured outputs.
- Long-context habits: put documents at the top, ask for quotes before analysis, and keep the question at the end.

### Tool design and MCP

- A tool definition is a name, a description, and a JSON schema for inputs. The description is what the model reads to decide when to call it; write it for the model, with edge cases and examples.
- A few well scoped tools work better than many overlapping ones. Namespace related tools, return meaningful context rather than raw dumps, and keep responses within a sane token budget.
- The tool_choice parameter (auto, any, a specific tool, none), parallel tool use, and how a tool result with an error flag differs from a successful result.
- MCP primitives: tools, resources, and prompts. Servers expose them; clients (Claude Code, the Agent SDK, Claude.ai) connect to them.
- MCP transports: stdio for local processes, streamable HTTP for remote servers, and where authentication sits for remote ones.
- Idempotency and safety: which tools need confirmation, which are read-only, and how the schema and description communicate that.

### Context management

- The context window is a budget: system prompt, conversation, tool definitions, tool results, and the response all share it.
- Context rot: quality falls as the window fills with stale material. Compaction, summarization, and clearing exist to fight it.
- Load context when it is needed rather than up front. Give the agent lightweight identifiers (file paths, record ids, URLs) and let it fetch what it needs.
- Structured note-taking and memory files as persistence across sessions; subagents as a way to isolate context for a subtask and return only the conclusion.
- Prompt caching: what makes a prefix cacheable, why stable system prompts and tool definitions go first, and the cost effect.
- Retrieval versus stuffing: when to search and load a slice versus pasting a whole corpus, and how chunking and citations interact.

## Prep notes

- Study against the blueprint, not vibes. Agentic architecture alone is 27% of the exam, so weight your prep the way the guide weights the domains.
- The exam is closed-book with no AI assistance. Anything you normally look up needs to be working knowledge before you sit it.
- Candidates who pass tend to recommend a stretch of theory first, then hands-on building. The Partner Academy prep course follows the same blueprint.

## Common mistakes

- Reaching for an agent when a workflow with fixed control flow would be cheaper, faster, and easier to test. The exam rewards the simplest design that meets the requirement.
- Writing tool descriptions as if a person will read them. The model reads them to decide when to call the tool, so the description has to carry the edge cases and an example or two.
- Ignoring the closed-book format. People who build with Claude daily still lose marks on parameter names and policy details they normally look up.
- Spreading prep evenly across the five domains when agentic architecture carries 27% on its own.

## A study path

1. Week 1: read the exam guide end to end and the four Anthropic engineering posts linked below. Write a one-page summary of each domain in your own words.
2. Week 2: build a small agent with the Agent SDK or Claude Code that uses at least two tools and one MCP server. Add a hook and a permission rule.
3. Week 3: work through the Partner Academy prep course, then a community practice exam. Review every miss against the docs.
4. Week 4: closed-book review. Rewrite your domain summaries from memory and compare.

## Official reading

- [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)
- [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
- [Writing tools for agents](https://www.anthropic.com/engineering/writing-tools-for-agents)
- [Claude Code best practices](https://www.anthropic.com/engineering/claude-code-best-practices)
- [Claude Developer Platform docs](https://docs.claude.com/)
- [Claude Code docs](https://code.claude.com/docs)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [Pearson VUE: Claude Certification Program by Anthropic](https://www.pearsonvue.com/us/en/anthropic.html)
- The CCAR-F exam guide, distributed through the Anthropic Partner Academy

## FAQ

### What is the CCAR-F exam?

CCAR-F is Claude Certified Architect – Foundations, Anthropic's certification for engineers and architects who design Claude-powered systems. It is 60 questions in 120 minutes, proctored and closed-book, with a passing score of 720 on a 100–1,000 scale.

### How much does the CCAR-F exam cost?

$125 per attempt, per the current exam guide. The fee is paid to the certification program when you register. Program pricing changes, so check the current guide before scheduling.

### Is CCAR-F the same as CCA-F?

Yes. CCA-F is a common shorthand; the official Pearson VUE listing uses CCAR-F for Claude Certified Architect – Foundations.

### How do I register for the CCAR-F exam?

Registration runs through the Anthropic Partner Academy, which is open to people affiliated with a Claude Partner Network organization. Independent engineers typically get access by joining a partner firm such as YAID, then schedule through Pearson VUE.

### How hard is CCAR-F?

It assumes real working knowledge across five domains: agentic architecture, Claude Code, prompt engineering, tool design and MCP, and context management. Engineers who build with Claude regularly report the material is fair; the closed-book format is what catches people who rely on looking things up.

### How do I take the CCAR-F exam?

Get eligibility through a Claude Partner Network organization, register inside the Anthropic Partner Academy, then schedule with Pearson VUE, online proctored or at a test center. Independent engineers usually join a partner firm such as [YAID](https://youraidept.com/network/apply?ref=github) to get that eligibility. Step by step: [registration.md](../registration.md).

---

Part of the [Claude Certification Handbook](../README.md), maintained by [YAID](https://youraidept.com/network?ref=github), a registered Claude Partner Network firm. Not an official Anthropic resource. Licensed [CC BY 4.0](../LICENSE).
