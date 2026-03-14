# Medical Product Strategist

Translate medical and clinical research into product strategy with evidence grading, clinical significance, product translation, regulatory considerations, and commercial value.

## What This Skill Does

- Extracts study facts (PICOS + key results)
- Grades evidence strength
- Interprets clinical significance
- Translates findings into product opportunities
- Assesses regulatory pathway and commercial value
- Outputs a report + structured JSON

## Workflow

Literature Identification  
Evidence Level  
Clinical Significance  
Product Translation  
Regulatory Pathway  
Commercial Value  
Strategic Recommendation

## Output

1. Strategic Analysis Report  
2. Structured JSON (schema defined in `SKILL.md`)

## Install

### Codex

Create a local skill folder and copy the files from this repo:

- `SKILL.md`
- `agents/openai.yaml`

Then restart Codex to load the skill.

### OpenClaw (manual)

Create a folder and place the two files above into:

- `~/.openclaw/skills/medical-product-strategist/`

Then refresh OpenClaw skills.

## Usage

```
$medical-product-strategist
Analyze the following study:
Title: ...
Design: ...
Sample size: ...
Comparator: ...
Outcomes: ...
Safety: ...
```

## Contributing

1. Open an issue with suggestions, use cases, or corrections.
2. Fork the repo and submit a PR with your changes.
3. For large changes, discuss in an issue before implementation.

## Notes

- Keep evidence separate from product speculation.
- Avoid overstating clinical claims.
- For real-time market or competitor data, do a live lookup.
