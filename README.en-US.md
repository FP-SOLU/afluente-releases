# Afluente

**A workspace for people and agents to work together.**  
Built by **FP Solutions** · Windows x64 · Version 0.6.4

[Português (Brasil)](README.md) · [Download the latest release](https://github.com/FP-SOLU/afluente-releases/releases/latest) · [Changelog](CHANGELOG.en-US.md)

## Work with a team in a shared conversation

Give agents their own roles, instructions, skills, models, and tools. Work in channels or direct chats, share references, and follow decisions, deliverables, and files. Codex, Claude Code, and OpenAI-compatible APIs can coexist in one team, with a provider selected for each agent.

### Available capabilities

- **Conversation and continuity:** mentions, specialist handoffs, searchable history, live steering, and a persistent queue. Decisions and artifacts retain their source references.
- **Execution controls:** ask, automatic review, or full access in the composer; step-by-step questions; request-specific approvals; cancellation and resuming.
- **Missions and routines:** stages, checkpoints, schedules, and a draggable board. Manual completion is identified. Uncertain effects after a crash require review.
- **Local browser and previews:** a browser scoped to each conversation and project, visual monitoring, manual sign-in, and optional session persistence. Supervised preview services survive agent handoffs.
- **Files and knowledge:** attachments, pasted screenshots, enlarged images, text/Markdown previews, hashed versions, local sources, and reviewed memory. OKF is optional.
- **Configurable team:** provider model catalogs, skills, selected MCP servers, editable instructions, avatars, and optional browser/local-computer tools.
- **Usage and distribution:** subscription quotas when the provider exposes them, in-app updates, and a custom Afluente installer.

## Get started

1. Download the Windows x64 installer from the [official release channel](https://github.com/FP-SOLU/afluente-releases/releases/latest).
2. Enter your name and workspace name. A profile photo is optional.
3. Connect one or more providers, create your first agent, and open a conversation.
4. Select the project folder, describe the outcome, and choose permissions in the composer.

CLI authentication stays with the provider. API keys use Windows protection and are excluded from team exports. User data and working files are separate from the installation.

A useful request states the outcome, constraints, and acceptance criteria. Subsequent corrections belong in the same conversation; you do not need to repeat the entire brief at each handoff.

## What's new in 0.6.4

Fixed large-message handling and process-loss detection in the Codex transport. Execution details now retain sanitized failure causes and recovery results. A confirmed transient error may trigger one controlled continuation, respecting permissions, cancellation, and uncertain tool effects. Searchable history, checkpoints, progress protection, and direct updates from 0.6.3 remain available. See the [release notes](docs/release-0.6.4.md).

## Operation and limits

Afluente runs locally. It must remain open, including in the system tray, to work. Shutting down the computer stops execution. Browser and computer tools are configurable; no remote computer is included.

A configured connection or model catalog does not prove successful inference. Vision, image generation, MCP tools, and quotas depend on the model, connection, and permissions. Missing capabilities are reported. External OAuth credentials are not automatically copied between clients.

History and agent checkpoints do not grant permission. Reusable memory requires review. A reference cannot restore a deleted or out-of-scope file. Corporate providers and scheduled tasks must be validated on the destination computer.

## Development

```powershell
npm ci
npm run typecheck
node --test --test-concurrency=1 tests/*.test.cjs
npm run build
npm run desktop
```

`npm run dev` provides a UI preview only. Electron tests use disposable profiles and distinguish simulated transports from real-provider calls. Windows packaging requires Python/fontTools and the WPF/.NET Framework build tools; the installed application does not require a separate Node or Python installation.

## Updates and data

The app checks the public release channel and offers explicit download and installation. From 0.6.3 onward, it verifies the newest stable version before installing and rejects an outdated intermediate download. Installation waits for running tasks. Installer signing and validation on a second computer remain separate pending checks.

Source code is private in `FP-SOLU/afluente`; installers are public in `FP-SOLU/afluente-releases`. Do not publish profiles, credentials, or private captures. Back up before downgrading: an older release may not accept newer data.

---
**Afluente — by FP Solutions**  
Developed and maintained by FP Solutions.
