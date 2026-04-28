# Score

A specification format for AI skills, separate from the runtime that executes them.

Score files are plain markdown with YAML frontmatter. They describe what an AI system should know, what it is allowed to do, and what governance applies — written once, in a format independent of any particular vendor's tools, and compiled to whichever runtime target the deployment uses.

## Why a separate format

Most AI skill formats today — Anthropic Skills, MCP server configurations, OpenAI tools, Microsoft Copilot Studio plugins — are runtime formats. They describe how a capability gets executed against an LLM. They are good at what they do.

What they do not capture is the authoring and governance metadata that organisations need to keep over the long term: who wrote a skill, who approved it, what version is in production, what regulatory classification applies, what the audit trail looks like. That metadata lives somewhere or it does not exist. If it lives in the runtime configuration, it gets rewritten when the vendor changes their format. If it lives in a separate ticketing system, it goes out of sync with the runtime. If it does not exist, the system cannot be audited.

Score sits above the runtime formats. A skill is authored once in Score, version-controlled in Score, audited in Score. Adapters compile Score skills to whichever runtime target the deployment needs — MCP, Anthropic Skills, OpenAI tools, vendor-native APIs. The compilation is lossy by design and the loss is documented; what is preserved at the Score level is the source of truth.

This is the OpenAPI playbook applied to AI skills: author upstream, generate downstream artefacts, treat the runtime targets as compilation targets rather than as sources of truth.

## Status

- Format: **v0.1** — stable for use, actively developed
- Licence: MIT

## Specifications

- **[Score format v0.1](score_spec.md)** — skill file format and validation rules
- **[Context API](score_context_api_spec.md)** — runtime integration contract for fetching skills
- **[Recording](score_recording_spec.md)** — immutable, hash-chained audit log format
- **[Governance metadata](score_governance_metadata_spec.md)** — fields for approval workflow and classification

## Guides

- **[Writing skills](WRITING_SKILLS.md)** — practical guide for skill authors
- **[Example skill](examples/brand.md)** — annotated reference implementation

## Reference implementations

- **[score-core](https://github.com/multipleworks/score-core)** — Python library: parser, validator, CLI. Available on PyPI.
- **[maestro-runtime](https://github.com/multipleworks/maestro-runtime)** — Score protocol execution layer for governed enterprise AI.

## On the broader architecture

Score is the specification-layer reference implementation in a broader architecture for AI in the enterprise. The non-technical framing — what knowledge an AI system needs to handle, how the layers fit together, what governance properties have to hold — is in *AI That Knows Your Business: An Executive Briefing*, available at [multipleworks.com.hk/briefings](https://multipleworks.com.hk/briefings).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on contributing to Score.

## Licence

MIT. See [LICENCE](LICENCE).

---

Built by [MultipleWorks](https://multipleworks.com.hk).
