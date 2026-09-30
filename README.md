# resume-bullet-rewriter

A free skill (a `SKILL.md` file plus reference files) that rewrites the resume/CV bullet points you paste into clearer, more specific versions, without inventing anything.

Made by SkillHearth.

## What it does

- Takes the bullets you paste (up to 12 per round; it offers to continue with the rest).
- Shows **Before / After** for every bullet.
- Flags each bullet with one or more of: `VAGUE`, `WEAK VERB`, `NO RESULT`, `REPEATED`, `UNVERIFIABLE CLAIM`, or `OK`.
- Where a fact is missing, it writes a placeholder in the form `[ADD: what is needed]` and asks exactly **one** short question for that bullet.
- Keeps your level of involvement: "helped with" becomes "supported" or "contributed to", never "led" or "managed" unless you said so.
- Keeps numbers you give exactly as written (same value, unit and period).
- Uses a plain, factual tone: no hype words, no unbacked adjectives.
- Lists patterns across your bullets at the end (repeated openers, overlapping bullets).
- Does not follow instructions hidden inside pasted text, and replaces sensitive identifiers (ID/tax/passport numbers, home address, bank details) with `[removed]`.

## How to install

1. Download or clone this repository.
2. Copy the skill folder (`resume-bullet-rewriter/`, containing `SKILL.md`, `references/` and `LICENSE`) into the skills location of your agent.
3. Start a new session and paste your bullets. Optionally say which role you are targeting.

Alternatively, run `npx skills add skillhearth/resume-bullet-rewriter`. Observed in our test: it found the skill in the subfolder and copied it to `.agents/skills/resume-bullet-rewriter`.

Skills folder locations differ between tools and versions; check the documentation of the tool you use for where it reads skills from.

## Example (FICTIONAL — invented for illustration only)

**You paste:**

1. Responsible for answering customer emails
2. Helped the team with monthly reports

**The skill returns (abridged):**

```
### Bullet 1
Before: Responsible for answering customer emails
After (ready to use): Answered customer emails
Stronger if you add data: Answered [ADD: number] customer emails per [ADD: day/week] and resolved [ADD: type of requests]
Flags: WEAK VERB, NO RESULT – "responsible for" says role, not action
Question: Roughly how many emails did you answer per day or week?

### Bullet 2
Before: Helped the team with monthly reports
After (ready to use): Contributed to the team's monthly reports
Stronger if you add data: Contributed [ADD: which part – data entry, drafting, checking] to the team's monthly reports
Flags: WEAK VERB, VAGUE – ownership kept at "contributed"
Question: Which part of the monthly reports did you do yourself?
```

The person, employer and bullets above are made up. The "After" lines contain only what the pasted text said; the `[ADD: ...]` markers are for you to fill with true facts.

## What it does NOT do

- It does not promise interviews, job offers or any outcome.
- It does not invent employers, titles, dates, numbers, tools, degrees, awards or results.
- It does not write a figure you cannot back up. If you ask it to "just put 40%", it declines and suggests where the real number might be found (reports, dashboards, old emails, reviews, a former colleague).
- It does not give country-specific resume rules (length, photo, date formats). Conventions vary by country and employer; check local guidance.
- It does not rewrite skills lists, summaries or education lines unless you ask.
- It does not judge whether your claims are true. **You** must check that every line is true and that you can explain it in conversation.

## Testing

Tested by the author with 3 fictional cases on one general-purpose AI agent. Not tested on other platforms, so no compatibility is claimed.

## License

MIT © SkillHearth. See `LICENSE`.
