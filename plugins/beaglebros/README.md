# Beagle Bros

An Agent Skill for bringing the wisecracking, generous, demystify-the-machine spirit
of the 1980s Apple II software house into modern documentation, product copy, and design.

It works as a standalone skill in Codex and Claude Code, and this repository also carries
the native plugin metadata each marketplace expects. The canonical skill package lives at
`skills/beaglebros/` and is shared by both plugin manifests.

A small skill that tries to carry forward a sensibility I fell in love with before I
understood a single thing about computers.

## Why this exists

I was born in 1980, and I got lucky early: there were computers in the house for as long
as I can remember. My dad's a computer guy — more on the hardware side — so the machines
were just _there_, part of the furniture, before I had any idea how rare that was.

There was no internet. You worked with what was in front of you. And what was in front of
me, besides the machine itself, was the documentation. The manuals. The catalogs. The
little folded reference cards.

Here's the thing I've never forgotten: those documents made programming _fun_ for a
seven- or eight-year-old. I just wanted to make silly games. I didn't really understand
half of what I was typing — the deep, magic-incantation stuff went right over my head —
but nothing I read ever once made me feel like a dummy for not getting it yet. The tone
assumed I was smart and curious and on my way, even when I was mostly just mashing keys
and hoping.

My dad was great about it. He'd sit down and walk me through things when he could. But he
couldn't do that all the time, nobody can, so I'd turn back to the documents. Over and
over. And they never got old. I'd already read every joke, run every one-line program,
seen every gag — and they were so _layered_ that I'd still find something new each time.
You could grow into them. The joke you laughed at one year taught you something the next.

That's the whole thing, really. Software that trusted you. Documentation that delighted
you on the way to teaching you. The radical idea that learning to make the machine do
something should feel like play, not like an exam.

## What it does

This skill is my attempt to bottle a little of that and pour it into the things I make
now — the voice, the generosity, the "here, let me show you the trick" spirit, the
refusal to make anyone feel small for not knowing yet. It's a set of notes and reference
files I can pull into a README, a CLI, an error message, or just a decision about how a
thing should _feel_.

It is not nostalgia for its own sake. It's a promise to build the way I was first welcomed
in.

If you grew up the same way, you already know exactly what I mean. If you didn't — come
on in. That was always the whole point.

## Try it

Ask the agent to use the skill directly:

```text
Use $beaglebros to rewrite this README introduction without losing any technical detail.
```

Or ask naturally for Beagle Bros-style copy, a Peeks & Pokes-inspired tip card, or a
"Would Beagle Bros ship this?" design review. The skill can be selected automatically
when the request matches its description.

## Install for local use

Clone or download this repository, then copy or symlink `skills/beaglebros/` to one of
these paths:

| Host        | Personal skill location        |
| ----------- | ------------------------------ |
| Codex       | `~/.codex/skills/beaglebros/`  |
| Claude Code | `~/.claude/skills/beaglebros/` |

A symlink to that subdirectory works too. Keep its `SKILL.md`, `references/`, and
`agents/` together so progressive disclosure and Codex UI metadata continue to work.

For plugin development, load the repository root directly:

```sh
claude --plugin-dir .
```

Marketplace installation instructions will be added when listings are live.

## Repository layout

```text
.
├── skills/beaglebros/
│   ├── SKILL.md                # portable Agent Skill contract
│   ├── agents/openai.yaml      # Codex skill-list metadata
│   └── references/             # history, voice, aesthetic, and ethos
├── .codex-plugin/plugin.json   # Codex plugin metadata
└── .claude-plugin/plugin.json  # Claude Code plugin metadata
```

## Compatibility

The shared skill uses only portable `name` and `description` frontmatter. Platform-specific
metadata lives outside `SKILL.md`, so adding another marketplace should require a thin
wrapper rather than another copy of the skill.

## License and affiliation

Released under the [MIT License](LICENSE). This is an independent, unofficial project
inspired by the historical Beagle Bros software house; it is not affiliated with or
endorsed by Beagle Bros or any successor rights holder.
