# Henry Agent Skills

A collection of reusable agent skills for reliable, verifiable work.

Each skill is self-contained and written to be portable across compatible agent setups.

## Skills

<!-- CATALOG:START -->
- [`approval-gated-external-actions`](skills/approval-gated-external-actions/SKILL.md): Use before sending, publishing, charging, or changing live records.
- [`durable-task-handoffs`](skills/durable-task-handoffs/SKILL.md): Use when work must survive a chat or agent boundary.
- [`evidence-first-operations`](skills/evidence-first-operations/SKILL.md): Use when reporting whether operational work is truly done.
- [`production-release-verification`](skills/production-release-verification/SKILL.md): Use when proving a release is live in production.
- [`public-skill-release-gate`](skills/public-skill-release-gate/SKILL.md): Use before publishing a private operating skill publicly.
- [`recurring-job-safety`](skills/recurring-job-safety/SKILL.md): Use when creating or operating scheduled agent jobs.
<!-- CATALOG:END -->

## Repository structure

- `skills/` contains the installable skills.
- `catalog.json` provides a machine-readable index.

## Install a skill

Copy the skill directory into your agent's skill library, or use its `SKILL.md` as a portable instruction package.

## License

Repository-authored skills are released under the MIT License unless a skill states otherwise.
