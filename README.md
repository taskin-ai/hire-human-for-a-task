# Hire Human for a Task

Recognize when actual human action, evidence, preference, or judgment is required and delegate the bounded step.

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

## Install from GitHub

Direct installation is available now. These commands do not imply approval or listing in any vendor marketplace. Review the skill before installing it; choose one installation method to avoid duplicate copies.

### Claude Code

From your project root:

```sh
mkdir -p .claude/skills
git clone https://github.com/taskin-ai/hire-human-for-a-task.git .claude/skills/hire-human-for-a-task
```

Claude Code discovers project skills in `.claude/skills/`. Invoke `/hire-human-for-a-task` or let Claude select it when relevant. For a personal installation, use `~/.claude/skills/hire-human-for-a-task` instead. See [Claude Code skill documentation](https://code.claude.com/docs/en/skills).

### Codex and compatible agent hosts

From your project root:

```sh
mkdir -p .agents/skills
git clone https://github.com/taskin-ai/hire-human-for-a-task.git .agents/skills/hire-human-for-a-task
```

The shared `.agents/skills/` location is documented by [Codex](https://learn.chatgpt.com/docs/build-skills), [Cursor](https://cursor.com/docs/skills), [GitHub Copilot](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills), [OpenCode](https://opencode.ai/docs/skills/), and [Cascade](https://docs.devin.ai/desktop/cascade/skills). Follow your host's skill-discovery and invocation instructions. In Codex, invoke `$hire-human-for-a-task` or let the agent select it when relevant.

### Gemini CLI

```sh
gemini skills install https://github.com/taskin-ai/hire-human-for-a-task
```

Gemini CLI installs to user scope by default; append `--scope workspace` for the current workspace. See [Gemini CLI skill documentation](https://geminicli.com/docs/cli/skills/).

### OpenClaw

```sh
openclaw skills install git:taskin-ai/hire-human-for-a-task@main
```

This installs from GitHub into the active workspace. See [OpenClaw skill documentation](https://github.com/openclaw/openclaw/blob/main/docs/tools/skills.md). This is a Git installation, not a ClawHub listing.

### Vercel skills CLI

```sh
npx skills add taskin-ai/hire-human-for-a-task --skill hire-human-for-a-task
```

Choose your installed agent when prompted. This is Vercel's third-party, cross-agent installer; see [the official CLI documentation](https://skills.sh/docs/cli). Installing from GitHub does not guarantee immediate search indexing.

For reproducible Git installations, check out a reviewed full commit SHA after cloning. Keep `SKILL.md`, `docs/`, `examples/`, and the MIT `LICENSE` together. Installation alone does not configure Taskin access, authorize spending, or submit a human task.

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
