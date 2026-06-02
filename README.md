# The Copywriter Agent

A world-class direct-response copywriter you install into Claude Code in one command. You brief it, it writes the copy. It's trained on the lineage of the greats (Schwartz, Ogilvy, Sugarman, Kennedy, Halbert, Caples) and it carries its whole knowledge base with it, so it works the same on your machine as it does on mine.

It writes headlines, ads, emails, landing pages, sales letters, VSL scripts, and social posts. It runs research before it writes, builds the hook properly, edits in passes, and scores its own draft against a checklist before handing it back.

It's read-only. It reads files and returns copy. It never writes, changes, or deletes anything on your machine.


## Install it (one command, in Claude Code)

This ships as a Claude Code plugin, so installing it is two slash commands. Run these **inside Claude Code**:

```
/plugin marketplace add reapzyau/tvml-agents
/plugin install tvml-agents@tvml-agents
```

That's it. Type `/agents` and you'll see **Copywriter** in the list. The reference library installs with it automatically — nothing else to set up.

When I ship improvements later, update with:

```
/plugin marketplace update tvml-agents
/plugin install tvml-agents@tvml-agents
```


## How to use it

Once it's installed, just ask for it by name:

> "Use the Copywriter agent to write me a launch email for [thing]."

The more you give it, the better it writes. The full briefing guide — and what makes the difference between a decent draft and a great one — is in `how-to-brief-it.md`. Start there.


## What's in here

- `agents/Copywriter.md` — the agent itself.
- `copywriter-references/` — its knowledge base (13 files). The agent reads these every time it writes. They install automatically with the plugin.
- `templates/` — starter files for your brand voice and your customer avatar. Optional, but the copy gets a lot better when you give the agent these.
- `how-to-brief-it.md` — how to actually drive the agent once it's installed.
- `.claude-plugin/` — the plugin + marketplace manifests (you don't need to touch these).


## Manual install (if you'd rather not use plugins)

Clone the repo and copy two things into your project's `.claude/` folder:

```
git clone https://github.com/reapzyau/tvml-agents.git
mkdir -p .claude/agents
cp tvml-agents/agents/Copywriter.md .claude/agents/
cp -r tvml-agents/copywriter-references .claude/
```

The agent looks for its references in the plugin directory first; on a manual install it automatically falls back to finding the `copywriter-references` folder, so this works too. Want it in every project, not just one? Put both in your home `~/.claude/` instead.


## A note on the voice

Out of the box the agent writes in a "practical teacher, not thought leader" voice and it's allergic to AI-slop (no "unlock," no "game-changing," no em-dash-every-sentence, no "Real systems. Real results. No theory." triads). If your brand sounds different, fill in the voice template in `templates/` and point the agent at it — your file wins over its defaults.

The agent is set to run on Opus (`model: opus` in `agents/Copywriter.md`). If you're on a plan where you'd rather it use Sonnet, change that one line.
