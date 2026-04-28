# Contributing to Score

Score is the specification format for AI skills. This repository is the canonical home of the specification documents and the writing guides for skill authors.

If you are looking to contribute to a Score-compatible implementation, see [score-core](https://github.com/multipleworks/score-core) (the Python reference implementation) or your specific runtime's repository.

## What belongs in this repository

- Specification documents (`score_spec.md`, `score_context_api_spec.md`, `score_recording_spec.md`, `score_governance_metadata_spec.md`)
- Writing guides for skill authors (`WRITING_SKILLS.md`)
- Example skill files demonstrating the format
- Discussion of format-level questions, validation rules, and version management

## What does not belong in this repository

- Implementation code. Code lives in `score-core` (Python) or in other implementations as they are built.
- API documentation for a specific implementation. That belongs in the implementation's repository.
- Vendor-specific runtime adapters. Those belong with the runtime they adapt to.
- Maestro-specific behaviour. Maestro is a product built on Score; its documentation lives in its own repository.

## The single-source-of-truth rule

The specification documents in this repository are canonical. Any other repository that needs to reference the specification should link to the file here, not duplicate it.

This rule exists because duplicated documentation drifts. When a specification is updated, only the canonical version is changed. Anyone reading a duplicate will eventually see something the canonical version no longer says.

If you find a copy of any specification document outside this repository, that copy is wrong. The fix is to delete the copy and replace it with a link to the canonical version, not to update the copy.

## Versioning

The specification follows the versioning scheme described in `score_spec.md`. The protocol version (currently `0.1`) tracks the format itself. The spec revision number tracks changes to specification documents within the same protocol version.

A change that adds an optional field is a spec revision increment. A change that adds a required field, removes a field, or alters validation behaviour is a protocol version increment. Protocol version increments require a documented migration path.

## Making changes

For corrections to existing documentation (typos, broken links, ambiguous wording where the intent is clear), open a pull request directly. The change should not alter the substance of the specification.

For substantive changes (new fields, new validation rules, new event types, new behaviour), open an issue first. Substantive changes require discussion and a clear statement of which spec revision or protocol version they target.

For framing or positioning changes (how Score is described, the relationship to MCP or other formats, the architecture this specification sits within), open an issue. The framing of the specification is part of its substance.

## Style

Documentation is written in British English. Specifications use hyphens (-) rather than em-dashes for any inline separator. Code examples use the conventions of the language being shown. The voice is direct and rule-stating; specifications are reference documents and should read as such.

## Licence

By contributing, you agree that your contributions are licensed under the same MIT licence that covers the rest of this repository.
