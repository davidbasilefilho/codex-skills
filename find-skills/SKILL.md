---
name: find-skills
description: Discover and install agent skills when users ask how to do something, request a skill, seek specialized capability, or want to extend agent functionality.
---

# Find Skills

## Workflow

1. Identify domain, task, and whether reusable skill likely exists.
2. Check [skills.sh](https://skills.sh/) leaderboard for established options.
3. Search when needed:

```bash
npx skills find [query] [--owner <owner>]
```

Use specific keywords and synonyms. Scope by owner when useful.

4. Verify before recommending:
   - install count: prefer 1K+, treat under 100 cautiously;
   - source reputation;
   - GitHub activity and stars; treat under 100 stars cautiously;
   - skill contents and fit.
5. Present name, purpose, source, install count, exact install command, and skills.sh link.
6. Offer installation. With approval:

```bash
npx skills add <owner/repo@skill> -g -y
```

`-g` installs globally; `-y` skips prompts.

Useful commands:

```bash
npx skills add <package>
npx skills update
npx skills init <name>
```

If none fit, say so, offer direct help, and mention `npx skills init <name>` for repeated needs.
