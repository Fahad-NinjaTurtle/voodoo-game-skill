# Voodoo Puzzle Skills

Five portable Agent Skills for finding, validating, building, and improving mobile puzzle games. They turn Voodoo's ideation and execution guidance into short workflows with concrete design checks. Each workflow asks 1–3 questions and waits for your reply before starting. It loads the relevant references as needed.

## Download and install

### Install from GitHub

With Node.js and Git installed, run this from your game project to download and install all five skills for Codex, Cursor, and Claude Code. Keep only the agent names you use after `--agent`. [Skills CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md#skills-add)

```sh
npx skills add Fahad-NinjaTurtle/voodoo-game-skill --skill "*" --agent codex cursor claude-code --copy
```

To install for all your projects, append `--global`. To install one workflow, replace `"*"` with its name, such as `voodoo-create`. Run `npx skills list` from your project to check what was installed, or `npx skills list --global` for a global install. Start a fresh agent session to use the skills.

### Download without Node.js

From the directory that contains your game project, clone the skills beside it.

```sh
git clone https://github.com/Fahad-NinjaTurtle/voodoo-game-skill.git
```

Open a terminal in your game project. To install for Codex and Cursor, use the commands for your shell. For Claude Code, use `.claude/skills/` as the destination instead.

```sh
mkdir -p .agents/skills
cp -R ../voodoo-game-skill/skills/voodoo-* .agents/skills/
```

```powershell
New-Item -ItemType Directory -Force -Path '.agents/skills' | Out-Null
Copy-Item -Path '../voodoo-game-skill/skills/voodoo-*' -Destination '.agents/skills/' -Recurse -Force
```

The checkout also contains the upload ZIPs in `voodoo-game-skill/downloads/`. You can download individual packages below.

- **Codex, Cursor, or Claude Code**. [Download the five Agent Skills](downloads/voodoo-agent-skills.zip?raw=true) and extract them, or use the folders under [`skills/`](skills/). Copy the five folders into your app's skill directory and keep the `references/` folders alongside each `SKILL.md`.
- **Claude web or desktop**. [Download the Claude upload ZIP](downloads/voodoo-puzzle-claude.zip?raw=true). Under **Customize → Skills → + → Create skill → Upload a skill**, upload the ZIP and enable `voodoo-puzzle`. In chat, say `Use my voodoo-puzzle skill, workflow voodoo-create.` Substitute the workflow you want. [Claude Help Center](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
- **Other AI chats**. [Download the standalone Markdown prompt](downloads/voodoo-puzzle-prompt.md?raw=true). Attach or paste it into a new chat and ask it to follow the playbook for your chosen workflow. Other apps that implement Agent Skills can use the five folders in their documented skill directory. [Agent Skills specification](https://agentskills.io/specification)

## Where to put the five folders

- **Codex**. Use `.agents/skills/` in a project or `~/.agents/skills/` for personal use. Type `$` and select the skill by name, for example `$voodoo-create`. [OpenAI installation](https://developers.openai.com/api/reference/cli), [OpenAI invocation](https://learn.chatgpt.com/docs/build-skills)
- **Cursor**. Use `.cursor/skills/` in a project or `~/.cursor/skills/` for personal use. Cursor also reads `.agents/skills/`. Type `/` in Agent chat and select the skill. [Cursor documentation](https://cursor.com/docs/skills)
- **Claude Code**. Use `.claude/skills/` in a project or `~/.claude/skills/` for personal use. Type the slash command. [Claude Code documentation](https://code.claude.com/docs/en/skills)

`~` means your user folder (`%USERPROFILE%` on Windows). A project install in Codex should contain `.agents/skills/voodoo-create/SKILL.md`. If a skill does not appear after copying it, open a fresh session.

## Pick a workflow

- [`/voodoo-idea-generation`](skills/voodoo-idea-generation/SKILL.md) finds original ideas grounded in real games or toys. A starting example is optional.
- [`/voodoo-idea-validation`](skills/voodoo-idea-validation/SKILL.md) assesses a concept and recommends a small prototype test.
- [`/voodoo-create`](skills/voodoo-create/SKILL.md) turns a chosen idea into a full game plan and can build the agreed playable scope.
- [`/voodoo-validate`](skills/voodoo-validate/SKILL.md) audits a build, clip, repository, or test data for the criteria you select.
- [`/voodoo-update`](skills/voodoo-update/SKILL.md) plans or implements focused changes to an existing game.

Try `Use voodoo-idea-generation. I want a one-finger mobile puzzle and I have no starting reference.` Expect a short intake before any ideas. For a game audit, try `Use voodoo-validate to review levels 1–5 of my Unity V1 for onboarding and visual readability.` Expect a request for the relevant evidence.

The skill folders contain Markdown and require no runtime dependencies. Playable prototypes, edits, browsing, and device checks depend on the tools available in your AI app and the scope you agree to.

## Source guidance

The references draw on Voodoo's *Game Ideation Guidelines and Checklist*, the [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS), and [Execution: Art, Gamefeel & Animations](https://app.notion.com/p/Execution-Art-Gamefeel-Animations-bc6fe94c74608317a6e001042f76d2bb). The skills cover decisions and forgiving controls, varied solutions, a 20-level core, late failure and fair revives, the 3–5 second ad hook, and readable art and motion.
