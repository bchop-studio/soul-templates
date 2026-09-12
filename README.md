# Soul Templates

Eight ready-to-use personality templates for AI agents. Pick one, copy it into your agent's identity or instruction layer, then change anything that does not fit.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Hermes Agent](https://img.shields.io/badge/Hermes%20Agent-SOUL.md-00E5D9)](https://hermes-agent.nousresearch.com/docs/user-guide/features/personality)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-SOUL.md-blue)](https://docs.openclaw.ai/concepts/soul)

## What this changes

A personality file shapes how an agent talks, explains things, handles uncertainty, and works with you. It can make the same tool feel calm, blunt, patient, creative, structured, or more casual.

These templates do not give an agent new tools, memory, permissions, or security boundaries. They change behavior and tone. Your agent runtime still controls what the agent can access and do.

## Choose a personality

| Template | What it feels like | Best for |
| --- | --- | --- |
| [Chill Assistant](./templates/01-chill-assistant.md) | Calm, casual, and low on filler | Everyday help |
| [ADHD Brain](./templates/02-adhd-brain.md) | Small steps, less shame, fewer choices | Focus and task support |
| [Sarcastic Dev](./templates/03-sarcastic-dev.md) | Dry humor with a bias toward shipping | Development work |
| [Strict Executor](./templates/04-strict-executor.md) | Direct, literal, and low on opinions | Clear tasks and power users |
| [Creative Partner](./templates/05-creative-partner.md) | Curious, opinionated, and willing to push back | Writing and idea work |
| [Patient Teacher](./templates/06-patient-teacher.md) | Clear explanations without talking down | Learning something new |
| [Midnight Companion](./templates/07-midnight-companion.md) | Quiet, thoughtful, and unhurried | Late-night conversations |
| [Hype Person](./templates/08-hype-person.md) | Warm, energetic, and encouraging | Momentum and small wins |

Open any template to preview the full instructions before using it.

## Use with Hermes Agent

Hermes loads `SOUL.md` from its home folder and uses it as the agent's main identity. Review the template first, then copy it into place:

```bash
git clone https://github.com/bchop-studio/soul-templates.git
cd soul-templates
cp -i templates/02-adhd-brain.md "${HERMES_HOME:-$HOME/.hermes}/SOUL.md"
```

Start a new Hermes session after replacing the file.

Read the current [Hermes personality documentation](https://hermes-agent.nousresearch.com/docs/user-guide/features/personality) for location and loading details.

## Use with OpenClaw

OpenClaw loads `SOUL.md` from the active agent workspace. Its default workspace is `~/.openclaw/workspace`:

```bash
git clone https://github.com/bchop-studio/soul-templates.git
cd soul-templates
cp -i templates/01-chill-assistant.md ~/.openclaw/workspace/SOUL.md
```

If you changed the OpenClaw workspace location, copy the template there instead. See the current [OpenClaw SOUL.md guide](https://docs.openclaw.ai/concepts/soul).

## Use with Claude Code

Claude Code does not load a file named `SOUL.md` as a special identity file. Adapt the parts you want into `~/.claude/CLAUDE.md` for personal instructions, or into a project's `CLAUDE.md` for project-specific behavior.

See [How Claude remembers your project](https://code.claude.com/docs/en/memory) before changing an existing instructions file.

## Use with ChatGPT

ChatGPT does not load local `SOUL.md` files automatically. Copy the parts you want into **Settings → Personalization → Custom Instructions**.

See OpenAI's current [Custom Instructions guide](https://help.openai.com/en/articles/8096356-custom-instructions-for-chatgpt).

## Make it yours

These are starting points, not fixed personas. Change the tone, remove rules you dislike, combine useful sections, and add real boundaries for your workflow.

Keep the final file short enough to read yourself. If two instructions fight each other, the agent will have the same problem you would.

## Safety

Read a template before loading it. Do not put passwords, API keys, private memory, customer data, or machine credentials inside personality files.

Personality is not access control. Keep dangerous actions behind approval prompts and give the agent only the permissions it needs.

See [SECURITY.md](./SECURITY.md) for reporting and safety notes.

---

MIT. Do whatever you want with these.

Built by [@BChopLXXXII](https://x.com/BChopLXXXII)

Built for BUILDERS who just want their AI to feel less... corporate.

Ship it. 🚀

If this helped, ⭐ the repo — it helps others find it.
