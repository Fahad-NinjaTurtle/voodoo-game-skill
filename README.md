# Voodoo Puzzle Skills

Five portable Agent Skills for finding, validating, building, and improving mobile puzzle games. They turn Voodoo's ideation and execution guidance into short workflows with concrete design checks. Each workflow asks 1–3 questions and waits for your reply before starting. It loads the relevant references as needed.

## Download and install

Choose your app. The `npx` commands require Node.js and Git. Run the command for your app from your game project. Add `--global` to install the standalone skills for all your projects. To install one workflow, replace `"*"` with a name such as `voodoo-create`. [Skills CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md#skills-add)

### Codex

```sh
npx skills add Fahad-NinjaTurtle/voodoo-game-skill --skill "*" --agent codex --copy
```

To install the native plugin instead, use a Codex CLI version with `codex plugin add`. [Codex plugin packaging](https://developers.openai.com/plugins/build/plugins#add-a-marketplace-from-the-cli)

```sh
codex plugin marketplace add Fahad-NinjaTurtle/voodoo-game-skill
codex plugin add voodoo-puzzle-skills@voodoo-game-skill
```

Start a fresh session. In Codex desktop, type `/` and search for `voodoo`, or type `$voodoo-create` to select a workflow directly. In the Codex CLI, use `/skills` to browse. [Desktop slash commands](https://learn.chatgpt.com/docs/app/slash-commands) · [Codex skill invocation](https://learn.chatgpt.com/docs/build-skills)

### Cursor

```sh
npx skills add Fahad-NinjaTurtle/voodoo-game-skill --skill "*" --agent cursor --copy
```

For a native plugin install, open **Customize**, choose **From GitHub Repository**, enter `Fahad-NinjaTurtle/voodoo-game-skill`, and install **voodoo-puzzle-skills** from the imported marketplace. Type `/` in Agent chat to find the workflows. [Cursor repository install](https://cursor.com/docs/skills#installing-skills-from-a-repository)

### Claude Code

```sh
claude plugin marketplace add Fahad-NinjaTurtle/voodoo-game-skill
claude plugin install voodoo-puzzle-skills@voodoo-game-skill
```

In Claude Code, try `/voodoo-puzzle-skills:voodoo-create`. To use the standalone names such as `/voodoo-create`, install the skills with the command below instead. [Claude Code plugin install](https://code.claude.com/docs/en/discover-plugins)

```sh
npx skills add Fahad-NinjaTurtle/voodoo-game-skill --skill "*" --agent claude-code --copy
```

### Claude web and desktop

Upload the ZIP under **Customize → Skills → + → Create skill → Upload a skill** and enable `voodoo-puzzle`. In chat, say `Use my voodoo-puzzle skill, workflow voodoo-create.` Substitute the workflow you want. [Download the Claude upload ZIP](downloads/voodoo-puzzle-claude.zip?raw=true) · [Claude Help Center](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

### Other AI chats

Attach or paste the standalone prompt into a new chat and ask the app to follow the playbook for your chosen workflow. Apps that support Agent Skills can also use the five folders in their documented skill directory. [Download the standalone prompt](downloads/voodoo-puzzle-prompt.md?raw=true) · [Agent Skills specification](https://agentskills.io/specification)

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

You can also extract the standalone skills ZIP and copy the five folders to the same destination. Keep each `references/` folder beside its `SKILL.md`. [Download the standalone skills ZIP](downloads/voodoo-agent-skills.zip?raw=true)

### If the skills are missing from the menu

After cloning or downloading the repository, complete the installation for your app. A project install appears in sessions opened in that project. Use `--global` with your app's `npx` command to make the skills available across projects. If you added the native marketplace, finish installing and enabling **voodoo-puzzle-skills** in the app. Then open a fresh session and search for `voodoo`.

## Pick a workflow

- [`/voodoo-idea-generation`](skills/voodoo-idea-generation/SKILL.md) finds original ideas grounded in real games or toys. A starting example is optional.
- [`/voodoo-idea-validation`](skills/voodoo-idea-validation/SKILL.md) assesses a concept and recommends a test for its core mechanic.
- [`/voodoo-create`](skills/voodoo-create/SKILL.md) turns a chosen idea into a full game plan and one finished playable prototype.
- [`/voodoo-validate`](skills/voodoo-validate/SKILL.md) audits a build, clip, repository, or test data for the criteria you select.
- [`/voodoo-update`](skills/voodoo-update/SKILL.md) plans or implements focused changes to an existing game.

Try `Use voodoo-idea-generation. I want a one-finger mobile puzzle and I have no starting reference.` Expect a short intake before any ideas. For a game audit, try `Use voodoo-validate to review levels 1–5 of my Unity prototype for onboarding and visual readability.` Expect a request for the relevant evidence.

The skill folders contain Markdown and require no runtime dependencies. Playable prototypes, edits, browsing, and device checks depend on the tools available in your AI app and the scope you agree to.

The playable prototype stays in portrait and includes 20 levels, a Main Menu, and dedicated Win and Game Over panels. An animated hand guides restricted moves in levels 1–3. The first loss can occur at L4. Each action gets particles, screen shake, sound and phone vibration, with effects scaled to the action. A loss records how close the player got. Revive costs 900 coins. The prototype contains zero in-game ads.

## Repository layout

- `skills/` holds the five workflows and their references. All three native plugins load these same files.
- `.agents/plugins/marketplace.json` defines the Codex marketplace. `.codex-plugin/plugin.json` declares the plugin it offers.
- `.claude-plugin/` and `.cursor-plugin/` contain the manifests and marketplaces for those apps.
- `downloads/` holds the standalone skills ZIP, the Claude upload ZIP, and the chat prompt.

## Source guidance

The references draw on Voodoo's *Game Ideation Guidelines and Checklist*, the [Puzzle Prototype Playbook](https://claude.ai/artifact/YMNU5BTiJHZVDWS6fJ6dRS), and [Execution: Art, Gamefeel & Animations](https://app.notion.com/p/Execution-Art-Gamefeel-Animations-bc6fe94c74608317a6e001042f76d2bb). They cover decisions, forgiving controls, varied solutions, a 20-level core, late failure and readable game feedback.
