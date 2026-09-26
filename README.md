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
- [Plugins](#plugins)
- [MCP Servers](#mcp-servers)
- [Agents & Workflows](#agents--workflows)
- [Clients & Editor Integrations](#clients--editor-integrations)
- [SDK & Muse Session Protocol](#sdk--muse-session-protocol)
- [Model Providers & Proxies](#model-providers--proxies)
- [Developer Tools](#developer-tools)
  - [Status & Observability](#status--observability)
  - [Session Management & Migration](#session-management--migration)
  - [Sandboxing & Security](#sandboxing--security)
  - [Packaging & Distribution](#packaging--distribution)
- [Guides, Tutorials & Examples](#guides-tutorials--examples)
- [Contributing](#contributing)
- [License](#license)

---

## Start Here

The shortest path from installation to a useful Muse Code workflow. Beginner-friendly setup guides, practical introductions, and essential first-run references belong here.

- [Muse Code documentation](https://dev.meta.ai/docs/muse-code) - Install Muse Code and learn the core product workflow.
- [SDK quickstart](https://meta-models.github.io/muse-code-sdk/next/guides/quickstart/) - Build and run a minimal client that controls a Muse Code session.

## Official Resources

- [Authentication](https://dev.meta.ai/docs/muse-code/auth) - Browser login and API-key authentication for local and headless sessions.
- [Changelog](https://dev.meta.ai/docs/muse-code/changelog) - Product releases, new features, and behavior changes.
- [Configuration](https://dev.meta.ai/docs/muse-code/configuration) - User and project settings, providers, models, and environment configuration.
- [Extending Muse Code](https://dev.meta.ai/docs/muse-code/extending) - Official overview of skills, hooks, plugins, MCP servers, and headless use.
- [Interactive Mode](https://dev.meta.ai/docs/muse-code/interactive) - Interactive commands, input modes, and voice features.
- [Permissions & Sandboxing](https://dev.meta.ai/docs/muse-code/permissions) - Approval policies, trust scopes, and sandbox behavior.
- [Rewind](https://dev.meta.ai/docs/muse-code/rewind) - Restore a session to a safe point in its event log.
- [Session Messaging](https://dev.meta.ai/docs/muse-code/session-messaging) - Communication between concurrent Muse Code sessions.
- [Subscriptions](https://dev.meta.ai/docs/muse-code/subscriptions) - Usage plans, account setup, and billing options.
- [Workflows](https://dev.meta.ai/docs/muse-code/workflows) - Orchestrate and manage teams of specialized subagents.
- [Muse Code Developer Docs](https://meta-models.github.io/muse-code-sdk/) - Guides and references for the SDK, Muse Session Protocol, extensions, and plugins.
- [Muse Code SDK](https://github.com/meta-models/muse-code-sdk) - Official TypeScript SDK and protocol definitions for building clients that drive Muse Code sessions. ![GitHub stars](https://img.shields.io/github/stars/meta-models/muse-code-sdk?style=flat-square)

## Plugins

Installable Muse Code plugins and plugin collections. Prefer entries with clear setup instructions, a focused purpose, and an actively maintained source repository.

- [Agentic Control Plane for Muse Code](https://github.com/agentic-control-plane/muse-code-acp-plugin) - Native Muse plugin that policy-checks tool calls before execution, scans outputs afterward, and records decisions in an audit log. Currently tracks Muse's experimental plugin and hook interfaces; interactive sessions fail open with a warning when the control plane is unavailable, while unattended runs fail closed.<br>
  <img src="https://img.shields.io/github/last-commit/agentic-control-plane/muse-code-acp-plugin?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/agentic-control-plane/muse-code-acp-plugin?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/agentic-control-plane/muse-code-acp-plugin?style=flat-square" alt="GitHub stars">

- [oh-my-musecode](https://github.com/hypery11/oh-my-musecode) - Curated content bundle and thin CLI for Meta Muse Code: 35 skills, 3 slash commands, 8 hooks, an in-binary MCP server, themes, and settings profiles, installed through Muse's own plugin and config surface. Every write into Muse's directories is recorded in an ownership ledger, so `omm uninstall` removes it cleanly.<br>
  <img src="https://img.shields.io/github/last-commit/hypery11/oh-my-musecode?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/hypery11/oh-my-musecode?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/hypery11/oh-my-musecode?style=flat-square" alt="GitHub stars">

## MCP Servers

Model Context Protocol servers with documented Muse Code setup or a particularly strong fit for coding workflows. General-purpose MCP servers should be included only when the Muse-specific integration is clear.

- [Muse Code Bridge](https://github.com/danny-hines/muse-code-bridge) - Local MCP bridge and skill collection for consulting, reviewing with, or delegating implementation to Muse Code from Codex and ChatGPT desktop. Supports continued Muse sessions through either a Muse subscription or an explicit API key.<br>
  <img src="https://img.shields.io/github/last-commit/danny-hines/muse-code-bridge?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/danny-hines/muse-code-bridge?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/danny-hines/muse-code-bridge?style=flat-square" alt="GitHub stars">

- [Muse-Code-Bridge-plugin](https://github.com/stts0919/Muse-Code-Bridge-plugin) - Independent community skill and local MCP plugin that runs an account-authenticated Muse Code session (via `muse serve`) from a Codex conversation: retained workspace sessions, explicit approval handling, and a subscription usage monitor. Strips key-bearing env vars from the Muse child process and refuses model turns until Muse reports an account login.<br>
  <img src="https://img.shields.io/github/last-commit/stts0919/Muse-Code-Bridge-plugin?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/stts0919/Muse-Code-Bridge-plugin?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/stts0919/Muse-Code-Bridge-plugin?style=flat-square" alt="GitHub stars">

## Agents & Workflows

Agent configurations, orchestration patterns, reusable workflows, and task-specific setups that are tested with Muse Code.

- [Mjolnir](https://github.com/BrokkAi/mjolnir) - Open-source meta-harness for managing Muse Code and other coding agents with durable sessions, isolated environments, account and quota controls, and remote access from a terminal or web interface.<br>
  <img src="https://img.shields.io/github/last-commit/BrokkAi/mjolnir?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/BrokkAi/mjolnir?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/BrokkAi/mjolnir?style=flat-square" alt="GitHub stars">

- [muse](https://github.com/jellologic/claude-code-muse) - Claude Code plugin that offloads bulk coding work to Muse Code workers in isolated git worktrees. Each worker is supervised by a Claude agent that reads the patch, runs the acceptance check itself, and sends the worker back with defects until the patch passes.<br>
  <img src="https://img.shields.io/github/last-commit/jellologic/claude-code-muse?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/jellologic/claude-code-muse?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/jellologic/claude-code-muse?style=flat-square" alt="GitHub stars">

- [dsh-muse-subagent](https://github.com/Pascapone/dsh-muse-subagent) - DeepSeek Harness bundle that exposes an authenticated Muse Code CLI as a one-shot `subagent_muse` tool. Runs `muse exec --json` in the parent session's workspace with native or WSL execution, approval-mode-never sandbox defaults, and Windows path translation.<br>
  <img src="https://img.shields.io/github/last-commit/Pascapone/dsh-muse-subagent?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/stars/Pascapone/dsh-muse-subagent?style=flat-square" alt="GitHub stars">

## Clients & Editor Integrations

Desktop and web clients, editor extensions, ACP adapters, and other interfaces for working with Muse Code outside its default experience.

- [Helicon](https://helicon.sh/) by [Harjot Singh Rana](https://github.com/HarjjotSinghh) - Free, MIT-licensed desktop and web client for Muse Code. Brings projects, session history, inline diffs, approvals, API-rate cost estimates, and remote-daemon access into one UI; ships installers for Windows and macOS, with Linux available from [source](https://github.com/HarjjotSinghh/helicon).<br>
  <img src="https://img.shields.io/github/last-commit/HarjjotSinghh/helicon?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/HarjjotSinghh/helicon?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/HarjjotSinghh/helicon?style=flat-square" alt="GitHub stars">

- [Ancilla](https://github.com/aleff-ferreira/ancilla) - Open-source desktop and web companion for Meta's Muse Code CLI: groups agent threads by project folder and lets you read, resume, steer, and approve them without the terminal UI, talking to the local `muse` CLI over the Muse Session Protocol with state in a local SQLite file. MIT-licensed fork of Helicon, unaffiliated with Meta.<br>
  <img src="https://img.shields.io/github/last-commit/aleff-ferreira/ancilla?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/aleff-ferreira/ancilla?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/aleff-ferreira/ancilla?style=flat-square" alt="GitHub stars">

- [mortiφ](https://github.com/Aeroknight786/mortiphi) - Focused local browser GUI for an existing Muse Code installation. Supports projects and sessions, queued or steered tasks, approvals, model and permission settings, file references, and working-tree changes while leaving Muse as the source of truth.<br>
  <img src="https://img.shields.io/github/last-commit/Aeroknight786/mortiphi?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/stars/Aeroknight786/mortiphi?style=flat-square" alt="GitHub stars">

- [Muse Code for VS Code](https://github.com/corona10/muse-code-vscode) by [corona10](https://github.com/corona10) - Unofficial native VS Code chat interface with editor context, file mentions, inline diffs, approvals, durable sessions, worktrees, subagents, and Muse model and reasoning controls. Connects to `muse serve` over MSP.<br>
  <img src="https://img.shields.io/github/last-commit/corona10/muse-code-vscode?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/corona10/muse-code-vscode?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/corona10/muse-code-vscode?style=flat-square" alt="GitHub stars">

- [muse-code-acp](https://github.com/bex-co/muse-code-acp) - Unofficial Agent Client Protocol adapter that makes Muse Code available in ACP clients such as Zed and VS Code. Uses the official Muse Code SDK and covers streaming, session resume, approvals, file changes, workflows, and client-provided MCP servers.<br>
  <img src="https://img.shields.io/github/last-commit/bex-co/muse-code-acp?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/bex-co/muse-code-acp?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/bex-co/muse-code-acp?style=flat-square" alt="GitHub stars">

- [muse-acp](https://github.com/BrokkAi/muse-acp) - Dependency-free Rust adapter that connects Muse Code's native session protocol to ACP clients, with documented setup for Zed, IntelliJ IDEA, and other JetBrains IDEs. Preserves Muse sessions, streaming, cancellation, configuration, and approval flows.<br>
  <img src="https://img.shields.io/github/last-commit/BrokkAi/muse-acp?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/BrokkAi/muse-acp?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/BrokkAi/muse-acp?style=flat-square" alt="GitHub stars">

- [Muse Code plugin for Claude Code](https://github.com/rtravellin/muse-code-plugin-cc) - Claude Code marketplace plugin that drives Meta's Muse Code 1.3 from a Claude session: read-only reviews, structured critiques, task delegation to Muse subagents, background runs, and one-way session transfer, all documented with a captured real-session demo.<br>
  <img src="https://img.shields.io/github/last-commit/rtravellin/muse-code-plugin-cc?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/rtravellin/muse-code-plugin-cc?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/rtravellin/muse-code-plugin-cc?style=flat-square" alt="GitHub stars">

- [baaz](https://github.com/latekaapi/baaz) - Native macOS client for Muse Code built with gpui (Rust): approvals, questions, plans, and tool output drawn as interface elements rather than printed as terminal text.<br>
  <img src="https://img.shields.io/github/last-commit/latekaapi/baaz?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/latekaapi/baaz?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/latekaapi/baaz?style=flat-square" alt="GitHub stars">

- [muse-for-opencode](https://github.com/CBannink/muse-for-opencode) - Routes OpenCode coder/reviewer agents through a Muse coding subscription. No server component; requires an authenticated Muse Code installation.<br>
  <img src="https://img.shields.io/github/last-commit/CBannink/muse-for-opencode?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/CBannink/muse-for-opencode?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/CBannink/muse-for-opencode?style=flat-square" alt="GitHub stars">

- [opencode-muse-code](https://github.com/swalker326/opencode-muse-code) - OpenCode plugin that registers a `muse-code` provider so OpenCode runs on a Meta Muse Code subscription. Discovers Muse Spark models from the account catalog with reasoning-effort variants, resolves credentials from the Muse OAuth login, macOS keychain, or config, and refreshes models and login state every 30 minutes.<br>
  <img src="https://img.shields.io/github/last-commit/swalker326/opencode-muse-code?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/swalker326/opencode-muse-code?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/swalker326/opencode-muse-code?style=flat-square" alt="GitHub stars">

- [muse-openclaw](https://github.com/stricker67-ai/muse-openclaw) - Setup script and provider config to use Meta's Muse Spark models in OpenClaw authenticated by Muse Code's browser OAuth login, without a separate API key or plugin. Documents how the credential minted by `muse login` works as a Bearer <redacted> the OpenAI-compatible Model API endpoint.<br>
  <img src="https://img.shields.io/github/last-commit/stricker67-ai/muse-openclaw?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/stricker67-ai/muse-openclaw?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/stricker67-ai/muse-openclaw?style=flat-square" alt="GitHub stars">

- [Muse Code Desktop](https://github.com/srikantmehra57/muse-code) by [srikantmehra57](https://github.com/srikantmehra57) - Native desktop command center (Tauri 2) for the Muse Code CLI: organizes workspaces and sessions, streams agent activity with approvals and reasoning controls, and reviews changed files and diffs. Independent open-source project, not affiliated with Meta; requires the official `muse` CLI plus a Muse Code subscription or API key.<br>
  <img src="https://img.shields.io/github/last-commit/srikantmehra57/muse-code?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/srikantmehra57/muse-code?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/srikantmehra57/muse-code?style=flat-square" alt="GitHub stars">

- [muse-desktop](https://github.com/EtienneLescot/muse-desktop) by [EtienneLescot](https://github.com/EtienneLescot) - Desktop app for Meta's Muse Code coding agent with opt-in computer use: lets it see the screen and drive Windows apps. Works with the installed `muse` CLI.<br>
  <img src="https://img.shields.io/github/last-commit/EtienneLescot/muse-desktop?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/EtienneLescot/muse-desktop?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/EtienneLescot/muse-desktop?style=flat-square" alt="GitHub stars">

- [ai-code-interface.el](https://github.com/tninja/ai-code-interface.el) - Unified Emacs interface (MELPA package) for coding-agent CLIs with documented Muse Code support: customizable executable, session resume via `muse resume`, and per-CLI configuration.<br>
  <img src="https://img.shields.io/github/last-commit/tninja/ai-code-interface.el?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/tninja/ai-code-interface.el?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/tninja/ai-code-interface.el?style=flat-square" alt="GitHub stars">

## SDK & Muse Session Protocol

Libraries, protocol tooling, client examples, and integrations built on the [Muse Code SDK](https://github.com/meta-models/muse-code-sdk) or Muse Session Protocol (MSP).

- [MSP Concepts](https://meta-models.github.io/muse-code-sdk/next/guides/msp-concepts/) - Sessions, turns, items, approvals, and other core protocol concepts.
- [MSP Wire Guide](https://meta-models.github.io/muse-code-sdk/next/guides/msp-wire/) - Transport, framing, lifecycle, and wire-level behavior.
- [MSP Method Reference](https://meta-models.github.io/muse-code-sdk/next/generated/msp/methods/) - Generated reference for protocol methods and notifications.
- [TypeScript SDK Reference](https://meta-models.github.io/muse-code-sdk/next/generated/sdk/) - Generated API reference for `@muse-code/sdk`.
- [SDK Cookbook](https://meta-models.github.io/muse-code-sdk/next/cookbook/) - Executable recipes for common client and session workflows.

## Model Providers & Proxies

Adapters and local proxies that connect the Muse Code harness to alternative model providers. These tools may rely on unofficial compatibility surfaces, so review their security model and current Muse version support before use.

- [muse-shim](https://github.com/luckeyfaraday/muse-shim) - Dependency-free Python loopback proxy that lets Muse Code use Codex OAuth, the Claude Code CLI, OpenRouter, and OpenAI-compatible Responses APIs. Alternative models appear in Muse's built-in `/model` menu without modifying Muse itself.<br>
  <img src="https://img.shields.io/github/last-commit/luckeyfaraday/muse-shim?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/luckeyfaraday/muse-shim?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/luckeyfaraday/muse-shim?style=flat-square" alt="GitHub stars">

## Developer Tools

Utilities that improve day-to-day operation, visibility, portability, or safety when using Muse Code.

### Status & Observability

Status lines, session activity indicators, usage views, and other tools that make Muse Code's work visible.

- [herdr-muse](https://github.com/akshat12/herdr-muse) - Herdr integration that maps Muse lifecycle hooks to idle, working, blocked, and completed terminal-pane states. Includes crash recovery safeguards and does not let subagent events overwrite the lead session's status.<br>
  <img src="https://img.shields.io/github/last-commit/akshat12/herdr-muse?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/akshat12/herdr-muse?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/akshat12/herdr-muse?style=flat-square" alt="GitHub stars">

### Session Management & Migration

Tools for finding, inspecting, organizing, and moving coding-agent sessions.

- [agent-cli-session](https://github.com/POSTTTT/agent-cli-session) - Local-only web app for browsing, searching, and analyzing Muse Code, Claude Code, Codex, Gemini CLI, OpenCode, Cursor, and Grok session logs across macOS, Linux, and Windows.<br>
  <img src="https://img.shields.io/github/last-commit/POSTTTT/agent-cli-session?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/POSTTTT/agent-cli-session?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/POSTTTT/agent-cli-session?style=flat-square" alt="GitHub stars">

- [session-migrate](https://github.com/xhluca/session-migrate) - CLI for inspecting and transferring native session transcripts across Muse Code and 17 other coding-agent formats while preserving resumability where the target supports it.<br>
  <img src="https://img.shields.io/github/last-commit/xhluca/session-migrate?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/xhluca/session-migrate?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/xhluca/session-migrate?style=flat-square" alt="GitHub stars">

- [aonia](https://github.com/HarjjotSinghh/aonia) - Named profiles for the Muse Code CLI: keep multiple logins on one machine, run two of them at once, and let a project pick which profile it uses.<br>
  <img src="https://img.shields.io/github/last-commit/HarjjotSinghh/aonia?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/HarjjotSinghh/aonia?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/HarjjotSinghh/aonia?style=flat-square" alt="GitHub stars">

### Sandboxing & Security

Sandbox runners, permission and policy tools, audit utilities, and secure deployment patterns for agent-generated code and tool calls.

- [Muse Code Sandbox Kit](https://github.com/shelajev/muse-code-sbx-kit) - Docker Sandbox kit for running the official Muse binary in an isolated environment with a restricted network policy and persistent credentials and sessions.<br>
  <img src="https://img.shields.io/github/last-commit/shelajev/muse-code-sbx-kit?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/shelajev/muse-code-sbx-kit?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/shelajev/muse-code-sbx-kit?style=flat-square" alt="GitHub stars">

### Packaging & Distribution

Distribution packages and installers that make Muse Code available on more platforms.

- [muse-code](https://github.com/Twilight0/muse-code) - Meta's Muse Code agent packaging for Arch Linux (AUR) and Android (Termux ARM64), with session management and legacy CPU support.<br>
  <img src="https://img.shields.io/github/last-commit/Twilight0/muse-code?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/Twilight0/muse-code?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/Twilight0/muse-code?style=flat-square" alt="GitHub stars">

- [termux-repo](https://github.com/Twilight0/termux-repo) - Custom Termux APT repository packaging muse-code alongside other CLI tools (wrangler, opencode, antigravity-cli, oh-my-pi).<br>
  <img src="https://img.shields.io/github/last-commit/Twilight0/termux-repo?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/Twilight0/termux-repo?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/Twilight0/termux-repo?style=flat-square" alt="GitHub stars">

## Guides, Tutorials & Examples

High-quality walkthroughs, reference projects, videos, articles, and starter kits. Prefer material that teaches a durable technique rather than merely announcing Muse Code.

- [Agent Command Atlas](https://github.com/kishormorol/agent-command-atlas) - Searchable, source-linked reference for commands, flags, shortcuts, permissions, skills, and sessions across Muse Code and five other coding agents. Each entry records its official source and verification state.<br>
  <img src="https://img.shields.io/github/last-commit/kishormorol/agent-command-atlas?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/kishormorol/agent-command-atlas?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/kishormorol/agent-command-atlas?style=flat-square" alt="GitHub stars">

- [musecodes.io](https://musecodes.io/) - Unofficial multilingual reference site covering installation, core concepts, pricing, comparisons, cookbook recipes, articles, and release changes. Important details such as pricing and data policies should be checked against Meta's official documentation.

- [Meta Model API Cookbook: Muse Code](https://github.com/dadaccai/meta-model-cookbook/tree/main/04_muse_code) - Ten end-to-end recipes for auditable sessions, deterministic replay, staged approvals, contained execution, immutable guardrails, subagent fan-out, goal tracking, bundled skills, scheduled work, and side chats.<br>
  <img src="https://img.shields.io/github/last-commit/dadaccai/meta-model-cookbook?style=flat-square" alt="Last commit"> <img src="https://img.shields.io/github/license/dadaccai/meta-model-cookbook?style=flat-square" alt="License"> <img src="https://img.shields.io/github/stars/dadaccai/meta-model-cookbook?style=flat-square" alt="GitHub stars">

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
