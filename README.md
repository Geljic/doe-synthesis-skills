# DoE Data Synthesis — Public Skill Prompts

Markdown skill prompts used by the [DoE Data Synthesis Tool](https://github.com/Geljic/ai-pilot/tree/main/tools/data-synthesis) (private repo).

The tool fetches these files at runtime, so editing a prompt here = an immediate change for every user once they refresh the tool. The HTML tool also bundles fallback copies, so it keeps working if this repo is unreachable.

## Skills

- [`skills/synthesise-transcript.md`](skills/synthesise-transcript.md) — Single-source synthesis (one transcript / memo / email / status report / artefact).
- [`skills/synthesise-themes.md`](skills/synthesise-themes.md) — Multi-source theme synthesis (e.g. 20 interviews → cross-cutting themes).

## How to point the tool at this repo

In the data synthesis tool's **Settings → Skills base URL**, enter:

```
https://raw.githubusercontent.com/Geljic/doe-synthesis-skills/main/skills
```

The tool appends `/{skill-name}.md`.

## Editing a prompt

Edit the file in a feature branch, open a PR, merge to `main`. Users see the change next time they synthesise (skills are cached per session — refresh the tool to bust the cache).

PII / privacy rules in the prompts are load-bearing. Don't relax them without team review.
