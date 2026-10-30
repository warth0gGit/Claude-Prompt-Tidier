# Prompt Tidier

Turns a messy prompt into a clear, tight one that gets better results from Claude (or any other AI).

- **`/tidy <your prompt>`**: light cleanup. Keeps your style, cuts the clutter and fixes the structure.
- **`/tidy deep <your prompt>`**: full rebuild with task, context, constraints, output format and success criteria, shaped for wherever you'll use the prompt.

If the prompt is vague, it first asks up to 3 quick questions, each with a suggested answer. Reply "go" to accept them all. You get back:

1. the tidied prompt in a copy-ready box
2. **What changed**: the key edits and why they help
3. **Fill in**: any `{placeholders}` for details it couldn't guess
4. **Ideas**: optional additions or removals that could make the prompt better

It never runs the prompt for you. If you want it run as well, say "tidy and run".

---

## Install on claude.ai and Claude Desktop

Installing it once on claude.ai makes it available in Claude Desktop and the mobile apps too, because skills follow your account.

1. Download **`dist/tidy.zip`** from this repo. On GitHub, click the file and then the download button (↓).
2. Go to **claude.ai → Settings → Capabilities**.
3. Make sure **Code execution and file creation** is turned on, since Skills need it.
4. Under **Skills**, click **Upload skill** and choose `tidy.zip`.
5. Check that the **tidy** toggle is on.

Then, in any chat, type:

```
/tidy write me sometihng for my blog about dogs, make it good and not too long
```

> On claude.ai and Desktop, `/tidy` is a trigger word that the skill recognises, not a built-in command, so it may not appear in a pop-up menu. Type it at the start of your message and it works the same way.
>
> On Team or Enterprise plans, an admin may need to allow Skills first.

## Install in Claude Code (terminal or the Code tab)

Here `/tidy` is a real slash command. In Claude Code, run:

```
/plugin marketplace add warth0gGit/Claude-Prompt-Tidier
```

```
/plugin install prompt-tidier@prompt-tidier
```

Before the repo exists on GitHub, you can instead copy the `skills/tidy` folder to `~/.claude/skills/tidy`.

## Updating

When the skill changes, download the new `dist/tidy.zip` and upload it again on claude.ai (remove the old one first). In Claude Code, run `/plugin marketplace update prompt-tidier`.

## What's in this repo

| Path | What it is |
|---|---|
| `skills/tidy/SKILL.md` | The instructions Claude follows. Edit this to change how it behaves. |
| `dist/tidy.zip` | The same skill, packaged for uploading to claude.ai |
| `.claude-plugin/` | The files that make this repo installable as a Claude Code plugin |
