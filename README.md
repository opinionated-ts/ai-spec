# What is this repository?

AI coding assistants and tool platforms define their own conventions, formats, and capabilities for concepts such as agents, hooks, MCP, plugins, and skills. This fragmentation makes it difficult to build tools and workflows that work consistently across different providers and environments.

`ai-spec` is an attempt to define an open, opinionated specification for AI-assisted development — a common set of conventions that providers, tools, and environments can align to.

## Goals

* Provide a clear, community-driven specification for common concepts and behaviors in AI-assisted development.
* Reduce unnecessary inconsistencies between AI coding assistants and tooling platforms.
* Establish conventions that can be implemented across different providers and environments.
* Aim to become an open standard: tools built against the specification should be usable across any compliant ecosystem rather than being tied to a single vendor.

## Non-goals

* Build a unified abstraction layer or wrapper across existing AI platforms.
* Replace existing providers, tools, or development environments.
* Require providers to adopt a specific implementation.

## Current status

This specification is under active discussion and is **not yet stable**. Proposals and definitions may change significantly as the community refines the specification.

See [Discussions](https://github.com/opinionated-ts/ai-spec/discussions) for ongoing conversations, proposals, and open questions.

## Specification

The specification is organized into independent scopes covering different areas of AI-assisted development.

Scopes are intentionally open-ended and may evolve as new areas emerge.

Each scope can contain:

* An overview and navigation document.
* RFCs proposing or defining changes to the specification.
* Decisions documenting broader decisions relevant to the scope.

```text
spec/
└── <scope>/
    ├── <scope>.md
    ├── rfcs/
    └── decisions/
```

Potential areas include agents, hooks, MCP, plugins, skills, system prompts, configuration, and other concepts that emerge through the specification process.

## Contributing

This specification is built by the community through discussion, proposals, review, and iteration.

See [CONTRIBUTING.md](CONTRIBUTING.md) to learn how to participate and propose changes.

## License

[CC BY 4.0](LICENSE)
