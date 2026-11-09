# Henry Agent Skills

I'm Henry. I run a small web design and marketing business by myself, mostly helping local companies with their websites and search visibility. I started leaning harder on AI because I needed help keeping up with the amount of work and context that comes with running everything solo.

The tools were useful, but I kept hitting the same problems. They would lose context, act before they should, or tell me something was finished without proving it. I started writing down the rules and workflows that actually worked for me. Those became the skills in this repo.

## What Hermes is

[Hermes Agent](https://github.com/NousResearch/hermes-agent) is an open-source agent framework from [Nous Research](https://nousresearch.com). I use it as the main agent layer around my work. It can run in a terminal or messaging apps, use tools, remember context between sessions, and load skills like these when a task calls for them.

What I like about Hermes is that I don't have to start with a blank chatbot every time. I can give it memory, tools, a working style, and repeatable instructions, then keep improving those instructions as I learn what works.

## Why I made these

Every skill here came from real work, repeated mistakes, or something I got tired of explaining twice.

An agent said a deployment was live without checking the actual site, so I wrote a skill for release verification. Work touched a real account and needed my approval first, so I wrote an approval gate. A task had to survive a long conversation or move between agents, so I wrote a better handoff process.

This is a small collection built from things that kept breaking and instructions I wanted to reuse. The goal is to make AI genuinely helpful without letting it get sloppy or overconfident.

## Skills

<!-- CATALOG:START -->
- [`approval-gated-external-actions`](skills/approval-gated-external-actions/SKILL.md): Use before sending, publishing, charging, or changing live records.
- [`durable-task-handoffs`](skills/durable-task-handoffs/SKILL.md): Use when work must survive a chat or agent boundary.
- [`evidence-first-operations`](skills/evidence-first-operations/SKILL.md): Use when reporting whether operational work is truly done.
- [`production-release-verification`](skills/production-release-verification/SKILL.md): Use when proving a release is live in production.
- [`public-skill-release-gate`](skills/public-skill-release-gate/SKILL.md): Use before publishing a private operating skill publicly.
- [`recurring-job-safety`](skills/recurring-job-safety/SKILL.md): Use when creating or operating scheduled agent jobs.
<!-- CATALOG:END -->

## Using a skill

Copy the skill directory into your agent's skill library, or use its `SKILL.md` as a portable instruction package. Hermes has its own [skills documentation](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills) if you want the setup details.

## License

Repository-authored skills are released under the MIT License unless a skill states otherwise.
