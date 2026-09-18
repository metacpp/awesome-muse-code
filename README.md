<h1 align="center">Awesome Muse Code</h1>

<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="https://github.com/metacpp/awesome-muse-code/pulls"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs welcome"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT"></a>
</p>

> A hand-picked collection of tools, extensions, skills, integrations, and learning resources for [Muse Code](https://dev.meta.ai/docs/muse-code).

Muse Code is Meta's agentic coding companion. This list focuses on resources that make it easier to learn, extend, integrate, and operate Muse Code in real-world development workflows.

The ecosystem is young, so the list favors relevance and substance over raw size. If something is missing, [contributions are welcome](#contributing).

---

## Contents

- [Start Here](#start-here)
- [Official Resources](#official-resources)
- [Skills](#skills)
- [Hooks](#hooks)
- [Plugins](#plugins)
- [MCP Servers](#mcp-servers)
- [Agents & Workflows](#agents--workflows)
- [Clients & Editor Integrations](#clients--editor-integrations)
- [SDK & Muse Session Protocol](#sdk--muse-session-protocol)
- [Model Providers & Proxies](#model-providers--proxies)
- [Developer Tools](#developer-tools)
  - [Status Lines & Session UX](#status-lines--session-ux)
  - [Remote Access & Notifications](#remote-access--notifications)
  - [Sandboxing & Security](#sandboxing--security)
- [Guides, Tutorials & Examples](#guides-tutorials--examples)
- [Community](#community)
- [Contributing](#contributing)
- [License](#license)

---

## Start Here

The shortest path from installation to a useful Muse Code workflow. Beginner-friendly setup guides, practical introductions, and essential first-run references belong here.

- [Muse Code documentation](https://dev.meta.ai/docs/muse-code) - Install Muse Code and learn the core product workflow.
- [SDK quickstart](https://meta-models.github.io/muse-code-sdk/next/guides/quickstart/) - Build and run a minimal client that controls a Muse Code session.

## Official Resources

- [Muse Code Developer Docs](https://meta-models.github.io/muse-code-sdk/) - Guides and references for the SDK, Muse Session Protocol, extensions, and plugins.
- [Muse Code SDK](https://github.com/meta-models/muse-code-sdk) - Official TypeScript SDK and protocol definitions for building clients that drive Muse Code sessions. ![GitHub stars](https://img.shields.io/github/stars/meta-models/muse-code-sdk?style=flat-square)

## Skills

Reusable instructions and focused capabilities designed for Muse Code, including skill collections and tools for authoring, validating, or managing skills.

## Hooks

Hooks, automations, and event-driven extensions that customize Muse Code's behavior across a development session.

## Plugins

Installable Muse Code plugins and plugin collections. Prefer entries with clear setup instructions, a focused purpose, and an actively maintained source repository.

- [Agentic Control Plane for Muse Code](https://github.com/agentic-control-plane/muse-code-acp-plugin) - Native Muse plugin that policy-checks tool calls before execution, scans outputs afterward, and records decisions in an audit log. Currently tracks Muse's experimental plugin and hook interfaces; interactive sessions fail open with a warning when the control plane is unavailable, while unattended runs fail closed.<br>
  <img src="https://img.shields.io/github/last-commit/agentic-control-plane/muse-code-acp-plugin?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/agentic-control-plane/muse-code-acp-plugin?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/agentic-control-plane/muse-code-acp-plugin?style=flat-square" alt="GitHub stars">

## MCP Servers

Model Context Protocol servers with documented Muse Code setup or a particularly strong fit for coding workflows. General-purpose MCP servers should be included only when the Muse-specific integration is clear.

## Agents & Workflows

Agent configurations, orchestration patterns, reusable workflows, and task-specific setups that are tested with Muse Code.

## Clients & Editor Integrations

Desktop and web clients, editor extensions, ACP adapters, and other interfaces for working with Muse Code outside its default experience.

- [Helicon](https://helicon.sh/) by [Harjot Singh Rana](https://github.com/HarjjotSinghh) - Free, MIT-licensed desktop and web client for Muse Code. Brings projects, session history, inline diffs, approvals, API-rate cost estimates, and remote-daemon access into one UI; ships installers for Windows and macOS, with Linux available from [source](https://github.com/HarjjotSinghh/helicon).<br>
  <img src="https://img.shields.io/github/last-commit/HarjjotSinghh/helicon?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/HarjjotSinghh/helicon?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/HarjjotSinghh/helicon?style=flat-square" alt="GitHub stars">

- [mortiφ](https://github.com/Aeroknight786/mortiphi) - Focused local browser GUI for an existing Muse Code installation. Supports projects and sessions, queued or steered tasks, approvals, model and permission settings, file references, and working-tree changes while leaving Muse as the source of truth.<br>
  <img src="https://img.shields.io/github/last-commit/Aeroknight786/mortiphi?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/stars/Aeroknight786/mortiphi?style=flat-square" alt="GitHub stars">

- [Muse Code for VS Code](https://github.com/corona10/muse-code-vscode) by [corona10](https://github.com/corona10) - Unofficial native VS Code chat interface with editor context, file mentions, inline diffs, approvals, durable sessions, worktrees, subagents, and Muse model and reasoning controls. Connects to `muse serve` over MSP.<br>
  <img src="https://img.shields.io/github/last-commit/corona10/muse-code-vscode?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/corona10/muse-code-vscode?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/corona10/muse-code-vscode?style=flat-square" alt="GitHub stars">

- [muse-code-acp](https://github.com/bex-co/muse-code-acp) - Unofficial Agent Client Protocol adapter that makes Muse Code available in ACP clients such as Zed and VS Code. Uses the official Muse Code SDK and covers streaming, session resume, approvals, file changes, workflows, and client-provided MCP servers.<br>
  <img src="https://img.shields.io/github/last-commit/bex-co/muse-code-acp?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/bex-co/muse-code-acp?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/bex-co/muse-code-acp?style=flat-square" alt="GitHub stars">

## SDK & Muse Session Protocol

Libraries, protocol tooling, client examples, and integrations built on the [Muse Code SDK](https://github.com/meta-models/muse-code-sdk) or Muse Session Protocol (MSP).

## Model Providers & Proxies

Adapters and local proxies that connect the Muse Code harness to alternative model providers. These tools may rely on unofficial compatibility surfaces, so review their security model and current Muse version support before use.

- [muse-shim](https://github.com/luckeyfaraday/muse-shim) - Dependency-free Python loopback proxy that lets Muse Code use Codex OAuth, the Claude Code CLI, OpenRouter, and OpenAI-compatible Responses APIs. Alternative models appear in Muse's built-in `/model` menu without modifying Muse itself.<br>
  <img src="https://img.shields.io/github/last-commit/luckeyfaraday/muse-shim?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/luckeyfaraday/muse-shim?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/luckeyfaraday/muse-shim?style=flat-square" alt="GitHub stars">

## Developer Tools

Utilities that improve day-to-day operation, visibility, portability, or safety when using Muse Code.

### Status Lines & Session UX

Status lines, session browsers, context tools, usage views, and other small quality-of-life improvements.

### Remote Access & Notifications

Remote-control interfaces, relays, mobile access, and notification tools for long-running Muse Code sessions.

### Sandboxing & Security

Sandbox runners, permission and policy tools, audit utilities, and secure deployment patterns for agent-generated code and tool calls.

## Guides, Tutorials & Examples

High-quality walkthroughs, reference projects, videos, articles, and starter kits. Prefer material that teaches a durable technique rather than merely announcing Muse Code.

- [musecodes.io](https://musecodes.io/) - Unofficial multilingual reference site covering installation, core concepts, pricing, comparisons, cookbook recipes, articles, and release changes. Important details such as pricing and data policies should be checked against Meta's official documentation.

- [Meta Model API Cookbook: Muse Code](https://github.com/dadaccai/meta-model-cookbook/tree/main/04_muse_code) - Ten end-to-end recipes for auditable sessions, deterministic replay, staged approvals, contained execution, immutable guardrails, subagent fan-out, goal tracking, bundled skills, scheduled work, and side chats.<br>
  <img src="https://img.shields.io/github/last-commit/dadaccai/meta-model-cookbook?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/dadaccai/meta-model-cookbook?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/dadaccai/meta-model-cookbook?style=flat-square" alt="GitHub stars">

## Community

Community spaces, recurring events, and other places where Muse Code users and extension authors can exchange practical knowledge.

## Contributing

Pull requests are welcome. A good addition should be directly useful to Muse Code users, publicly accessible, clearly documented, and placed in the most specific category that fits.

Please use this format:

```markdown
- [Project Name](https://example.com) - A concise, factual description that explains what makes the resource useful for Muse Code.
```

For GitHub projects, compact stars, last-commit, or license badges may be added when they help readers judge maturity and maintenance. Avoid decorative badges and manually maintained counts.

Before submitting, check that the link works, the project is not already listed, and the description does not read like marketing copy.

## License

[MIT](LICENSE)
