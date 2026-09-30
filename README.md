# Storyworld Agent Skills

Agent skills for making films with [Storyworld](https://storyworld.ai): the studio that turns stories into video, with consistent characters and shots from one episode to the next.

You can [read SKILL.md on GitHub](https://github.com/storyworld-ai/storyworld-skills/blob/main/skills/storyworld/SKILL.md) or fetch its [raw Markdown](https://raw.githubusercontent.com/storyworld-ai/storyworld-skills/main/skills/storyworld/SKILL.md).

## Install

The skill works through the Storyworld MCP server, so connect that first, then install the skill with one of the methods below.

### Connect Storyworld

In Claude Code, run:

```bash
claude mcp add --transport http storyworld https://api.storyworld.ai/mcp --scope user
```

In any other agent, add a remote MCP server named `storyworld` with the URL `https://api.storyworld.ai/mcp` (Streamable HTTP). No API key is needed: the first time your agent calls Storyworld, approve the sign-in in the browser window that opens.

### Claude Code plugin

Run in your terminal:

```bash
claude plugin marketplace add storyworld-ai/storyworld-skills
claude plugin install storyworld@storyworld-ai
```

### Other agents via skills.sh

```bash
npx skills add storyworld-ai/storyworld-skills --skill storyworld
```

Select your agent when prompted. Installation is project-local by default; add `-g` to install globally.

See the [setup guide](https://docs.storyworld.ai/docs/setup/agent-skill) for a prompt to copy to your agent that does all of this in one paste.

## Use

Ask your agent, for example:

> Using Storyworld, plan the opening sequence of my short film: a lighthouse keeper finds a message in a bottle.

In Claude Code, you can explicitly invoke the plugin skill with `/storyworld:storyworld`.

| Skill | Purpose |
|---|---|
| [storyworld](skills/storyworld/SKILL.md) | Find the right project, direct shots with Storyworld's shot method, write screenplays, quote credits before generating, and recover from refusals |

## Source

Published from Storyworld's platform repository, where the tests that check the Storyworld MCP server also check that every tool this skill names still exists. Changes made here directly are overwritten on the next publish.

## License

[MIT](LICENSE)
