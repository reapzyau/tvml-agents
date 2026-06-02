# How To Brief The Copywriter Agent

The agent owns the craft. You own the brief. The quality of what comes back tracks almost perfectly with how good your brief is, so this is the part worth getting right.

You don't need to fill in every field every time. For a quick social post, three lines is plenty. For a sales page, give it everything. The agent scales the depth to the job.


## The lazy version (works for quick stuff)

> "Use the Copywriter agent to write a [what] for [who], about [the one idea]. Keep it [length/tone]."

Example:

> "Use the Copywriter agent to write a short LinkedIn post for freelance marketers, about how I cut my client reporting from 3 hours to 15 minutes. Casual, no hashtags."

That'll get you a solid draft. Everything below makes it better.


## The full brief (use for anything that matters)

Hand the agent these, in plain language. Headers optional — it reads a paragraph fine.

- **Surface + format** — where it's going and what it is. "Skool community post, plain text, no markdown." "Cold email." "Landing page hero + 3 sections." The agent formats for the surface, so be specific (Skool and most community platforms don't render markdown — say so).

- **Audience** — who's reading, in one or two lines. Better: point it at your avatar file (see below).

- **The one idea** — the single thing this piece is about. If you can't say it in a sentence, the piece isn't ready. One reader, one idea, one action.

- **Voice** — how you sound. Point it at your voice file (see below), or give it a few rules ("casual, Australian, no hype, short sentences").

- **The hook structure** — if you want a specific opening. A strong default is **Proof → Promise → Plan**: lead with a real result (with a number), then what the reader will be able to do, then what's coming. If you don't specify, the agent picks.

- **Hard constraints** — the non-negotiables. Word count, banned phrases, emoji rules, "must include this number," "no CTA, end on the payoff." The agent treats these as law — they beat its own instincts.

- **Is it promotional?** — say so if it is. By default the agent ends on the payoff and does NOT bolt on a "comment below" CTA. Only when you tell it the piece is a launch / lead-magnet / product push will it close on a single call-to-action.


## Give it your voice and avatar (this is the real unlock)

In `templates/` there are two starter files:

- `voice.md` — how your brand sounds: tone, sentence rules, words you use, phrases you'd never use.
- `avatar.md` — who you're writing to: their situation, their pains in their own words, what they want.

Fill these in once (even roughly), save them somewhere in your project, and point the agent at them in the brief:

> "Read my voice file at `brand/voice.md` and my avatar at `brand/avatar.md`, then write..."

The single biggest jump in quality comes from the avatar — specifically, real customer language. If you have actual DMs, reviews, support tickets, or sales-call notes, drop a sample where the agent can read it and tell it to mine the exact phrases. Copy written in the reader's own words beats anything written about them.


## What you get back

Two blocks:

- `=== DRAFT ===` — the copy, ready to paste.
- `=== CRAFT NOTES ===` — how it made its calls: the reader/awareness stage, the one idea, the hook type, which frameworks it used, and its own checklist scores. Read the notes when a draft feels off — they usually tell you why.

If a draft misses, don't start over. Tell it the specific miss ("hook's too soft, lead with the number" / "cut the third paragraph" / "this broke my no-emoji rule") and it'll revise. Naming the exact problem beats "make it better" every time.
