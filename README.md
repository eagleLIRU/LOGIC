# LOGIC

A thinking, planning, reviewing, guiding and testing skill for AI assistants.

LOGIC helps an assistant understand the goal, check how something should work, test what can be verified, explain findings in simple English, and recommend only necessary changes.

## What it does

LOGIC gives an assistant one engine for five jobs: **think** (ideas, plans, decisions), **review** (check something that exists), **plan** (turn a goal into a build order), **guide** (brief a builder and keep the work on the goal) and **test** (apps, sites, AI agents, dashboards). Its rules: understand before judging, never fix blindly, explain in plain words, and label every claim as Known, Probably, Guessing, Don't know or Wrong.

## Install

Copy the `logic` folder into your assistant's skills directory, then restart or reload skills. For Claude Code that is `~/.claude/skills/logic` (Windows: `$HOME\.claude\skills\logic`).

```bash
git clone https://github.com/eagleLIRU/LOGIC.git
cp -r LOGIC/logic ~/.claude/skills/logic
```

## Contents

- `logic/SKILL.md` — main skill instructions
- `logic/references/product-testing.md` — checking digital products
- `logic/references/art-brief.md` — Act as / Request / Terms structure
- `logic/references/plain-words.md` — plain-language guidelines
- `logic/references/mapping-patterns.md` — mapping goals and workflows

## The Eight Guards

Every time LOGIC is used, these non-negotiable rules apply: never hallucinate; understand the bigger picture; understand the single prompt; connect the prompt to the bigger picture without widening scope; follow instructions 100%; never deviate from the approved scope; protect existing work; verify before claiming success. Where a guard cannot be guaranteed, LOGIC must say what is unknown or unverified instead of faking certainty. No instruction file can force any AI to behave perfectly, so treat the guards as strong instructions, not a guarantee.

## Strict rule: Instruction Compliance, Completeness & Accountability

A second mandatory rule applies whenever LOGIC is activated, including audits, builds, fixes and investigations: complete the whole authorised task, never declare completion early, account for every requirement with evidence, disclose anything unfinished (the task stays INCOMPLETE until then), and make no unauthorised decisions. See `logic/SKILL.md` for the full text.

## Usage examples

- “Apply LOGIC to this business idea.”
- “Test the logic of this user flow.”
- “Think this through before changing the app.”

## Status

The skill is instructions only (no code), so there is no automated test suite. It has been checked for valid frontmatter and for missing referenced files, but its real-world behaviour has not been formally evaluated.

## License

[MIT](LICENSE). Provided as is, without warranty.
