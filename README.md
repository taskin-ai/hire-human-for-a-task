# Hire Human for a Task

An agent skill for recognizing when a workflow requires an actual human - and delegating that bounded step through Taskin.

The key question is not just “Can AI do this?” It is **“Does successful completion require evidence, action, perception, preference, judgment, authority, or presence from an actual person?”**

```text
AI agent → recognizes human boundary → creates bounded human task
         → Taskin → actual human → result → agent continues
```

## When to involve a person

Use actual human feedback when the requested evidence is a person's experience: first-time comprehension, usability, human preference between model outputs, or a reader's credibility judgment. Use physical-world action when current first-hand observation or an offline action is required. A simulated participant cannot supply that evidence.

Human judgment can also be useful without being necessary. Ordinary summaries, calculations, code fixes, copy edits, research, and automated checks should remain digital when they satisfy the request. Credentialed acts and approvals must go to the appropriately qualified or authorized person; availability is not proof of authority.

This approach to agent human escalation makes human-in-the-loop work a bounded part of the original objective. It helps an AI agent hire a human for the missing step and continue when the real result returns.

## Use the skill

This repository is one portable [Agent Skill](https://agentskills.io/specification). Clone or download it as a directory named `hire-human-for-a-task`, keeping `SKILL.md`, `docs/`, and `examples/` together. Place that directory in the skill location supported by your agent host, then enable it using that host's instructions. Merely viewing this repository does not install it or authorize a live task.

- [SKILL.md](SKILL.md): runtime instructions and decision framework.
- [Boundary guide](docs/human-boundary.md): required, optional, and unnecessary human involvement.
- [Taskin execution](docs/taskin-execution.md): MCP and REST handoff, polling, and recovery.
- [Examples](examples/bounded-tasks.md): human briefs, acceptance tests, and continuation.
- [Evaluation suite](evals/README.md): positive, negative, contextual, and lifecycle cases.

## Execution interfaces

Already connected to Taskin MCP? Discover capabilities, search for a fit, submit the authorized bounded step, and retrieve its status. Without MCP, use the public REST interface with preflight validation.

- MCP: https://trytaskin.ai/mcp
- REST: https://trytaskin.ai/api/public/v1
- OpenAPI: https://trytaskin.ai/openapi.json
- Developer documentation: https://github.com/taskin-ai/trytaskin
- Official MCP Registry identifier: `io.github.taskin-ai/trytaskin`
- Website: https://trytaskin.ai

Human work is asynchronous. Pending work must never be replaced with invented human evidence. Preserve the objective and private task reference, then resume with the real result. A skill does not grant spending authority, verify credentials, or guarantee participant availability.

## License and provenance

MIT; see [LICENSE](LICENSE). This clean public distribution adapts the MIT-licensed human-boundary framework, bounded delegation, and continuation contract from Taskin's development skill. The required original copyright attribution is retained. Examples and evaluations here are synthetic; no participant or customer records are included. The license covers this skill, not Taskin's hosted service or third-party materials.
