# Score

Open format specification for portable AI skill files.

Score is an open-source format specification for encoding organisational
knowledge as portable, human-readable skill files. A Score skill file is a
markdown file with YAML frontmatter. It defines what an AI assistant should
know, when it should know it, and how it should behave — written in plain
text so any human can read and edit it, and any LLM can consume it.

---

## Specifications

- **[Score format v0.1](score_spec.md)** — skill file format and validation rules
- **[Context API](score_context_api_spec.md)** — runtime integration contract for fetching skills
- **[Recording](score_recording_spec.md)** — immutable, hash-chained audit log format
- **[Governance metadata](score_governance_metadata_spec.md)** — optional fields for approval workflow and classification

## Guides

- **[Writing skills](WRITING_SKILLS.md)** — practical guide for skill authors
- **[Example skill](examples/brand.md)** — annotated reference implementation

## Reference implementations

- **[score-core](https://github.com/markusgoodie/score-core)** — Python library: parser, validator, CLI. Available on PyPI.
- **[maestro-runtime](https://github.com/multipleworks/maestro-runtime)** — Score protocol execution layer for governed enterprise AI.

## Status

- Format: **v0.1** — stable for use, actively developed
- Licence: MIT

## Licence

MIT. See [LICENCE](LICENCE).

Built by [MultipleWorks](https://multipleworks.com.hk).
