# The Copywriter Agent

A world-class direct-response copywriter you install into Claude Code in about two minutes. You brief it, it writes the copy. It's trained on the lineage of the greats (Schwartz, Ogilvy, Sugarman, Kennedy, Halbert, Caples) and it carries its whole knowledge base with it, so it works the same on your machine as it does on mine.

It writes headlines, ads, emails, landing pages, sales letters, VSL scripts, and social posts. It runs research before it writes, builds the hook properly, edits in passes, and scores its own draft against a checklist before handing it back.

It's read-only. It reads files and returns copy. It never writes, changes, or deletes anything on your machine.


## What's in this folder

- `Copywriter.md` — the agent itself.
- `copywriter-references/` — its knowledge base (13 files). The agent reads these every time it writes. Without them it's just a shell, so they have to be installed too.
- `templates/` — starter files for your brand voice and your customer avatar. Optional, but the copy gets a lot better when you give the agent these.
- `how-to-brief-it.md` — how to actually use the agent once it's installed. Read this second.


## Install it (2 minutes)

Everything lives in a hidden folder called `.claude` inside whatever project you're working in. You're putting two things in there.

1. Put `Copywriter.md` into `.claude/agents/`
   (if the `agents` folder isn't there yet, make it)

2. Put the whole `copywriter-references` folder into `.claude/`
   (so you end up with `.claude/copywriter-references/` sitting next to `.claude/agents/`)

That's it. When you're done it should look like this:

```
your-project/
└── .claude/
    ├── agents/
    │   └── Copywriter.md
    └── copywriter-references/
        ├── copy-that-modern-playbook.md
        ├── prose-craft-rules.md
        └── ... (the rest)
```

If you'd rather do it from the terminal, from inside your project:

```
mkdir -p .claude/agents
cp /path/to/tvml-agents/Copywriter.md .claude/agents/
cp -r /path/to/tvml-agents/copywriter-references .claude/
```

Prefer it available in every project, not just one? Put both in your home `.claude` instead (`~/.claude/agents/` and `~/.claude/copywriter-references/`). The agent looks in the project first and falls back to searching for the folder, so either works.


## Use it

Once it's installed, just ask for it by name:

> "Use the Copywriter agent to write me a launch email for [thing]."

The more you give it, the better it writes. The full briefing guide (and what makes the difference between a decent draft and a great one) is in `how-to-brief-it.md`. Start there.


## A note on the voice

Out of the box the agent writes in a "practical teacher, not thought leader" voice and it's allergic to AI-slop (no "unlock," no "game-changing," no em-dash-every-sentence, no "Real systems. Real results. No theory." triads). If your brand sounds different, fill in the voice template in `templates/` and point the agent at it — your file wins over its defaults.
