# What is this repository?

AI coding assistants and tool platforms (agents, hooks, MCP servers, plugins, skills) each define their own conventions, formats, and capabilities. This fragmentation makes it hard to build tools that work consistently across providers.

`ai-spec` is an attempt to define an open, opinionated specification for AI-assisted development — a common configuration that AI providers and environments can align to.

## Goals

- Provide a clear, community-driven specification covering how agents, hooks, MCP integrations, plugins, and skills should be defined and behave.
- Reduce inconsistencies between AI coding assistants and tooling platforms.
- Aim to become an open standard: if adopted, tools built against this spec would work across any compliant provider, instead of being tied to a single vendor.

## Non-goals

- This project does not aim to build a unified abstraction layer or wrapper across all existing platforms.

## Current status

This specification is under active discussion and is **not yet stable**. Expect breaking changes to proposals as the community refines scope and details.

See [discussions](https://github.com/opinionated-ts/ai-spec/discussions) for ongoing conversations and open questions.

## Scope

The specification aims to cover:

- **Agents**: how autonomous AI agents are defined, invoked, and scoped
- **Hooks**: integration points between AI and development workflows
- **MCP**: conventions on top of the Model Context Protocol
- **Plugins**: how IDE/tool extensions should expose capabilities to AI
- **Skills**: a common format for reusable AI agent capabilities
- **Environment**: recommended baseline configuration for AI-enhanced development

## Contributing

This spec is meant to be built by the community. Contributions, proposals, and critiques are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose changes or open a discussion.

## License

[MIT license](LICENSE)
