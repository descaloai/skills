# Skills

Agent skills for go-to-market work by [Boaz Descalo](https://www.linkedin.com/in/descalo/). Each skill is a folder with a `SKILL.md` and supporting reference files, and works with Claude Code and other agents that support the skills format.

## GTM skills

| Skill | Category | What it does |
| --- | --- | --- |
| [Call follow-up sweep](gtm/call-followup-sweep/SKILL.md) | Deals | Reads a day or week of customer calls, pulls out the commitments (especially yours), and drafts one follow-up email per account that needs one. It also lists the promises still open from earlier sweeps. Drafts only; it never sends. |
| [Company domain resolver](gtm/company-domain-resolver/SKILL.md) | Prospecting | Takes a list of company names (CSV, CRM export, attendee list) and adds a website domain with a match-confidence label to each row, using the free, keyless Clearbit autocomplete endpoint. Run it before enrichment, dedupe, or CRM import. |
| [Event account plan](gtm/event-account-plan/SKILL.md) | Events | Turns a conference attendee or registration list into a deduplicated, signal-scored, tiered account plan. It includes the buying committee for each top account, a play per track, and a shared war-room page for the floor team. |

## Using the skills

Copy a skill folder into your skills directory, for example `~/.claude/skills/` for Claude Code:

```bash
git clone https://github.com/descaloai/skills.git
cp -r skills/gtm/company-domain-resolver ~/.claude/skills/
```

The agent picks up the skill and uses it when a request matches its description.

## About the author

**Boaz Descalo** is Founder & CEO of [Node8](https://node8.ai).

I build and scale AI systems for B2B companies. At Node8, we work with teams from early-stage startups to public companies, taking them from AI strategy to production and to adoption they can measure. My skills encode the data-plumbing side of GTM: the unglamorous resolution, dedupe, and hygiene steps that decide whether enrichment and outreach downstream actually work.

[LinkedIn](https://www.linkedin.com/in/descalo/) · [node8.ai](https://node8.ai)
