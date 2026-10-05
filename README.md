> **Portfolio showcase** — the complete implementation is kept private to protect intellectual property. This public repository intentionally contains documentation only. A live demo or private code review can be provided for a serious project discussion.

# LocalCommander macOS

A local Model Context Protocol server that lets an AI assistant work with an authorized macOS machine through a controlled tool layer.

## What it demonstrates
- filesystem and terminal tooling exposed through MCP
- Git and process operations
- macOS UI and browser automation helpers
- durable/background job management
- resource locking for concurrent agent work
- observability and recent-call diagnostics
- optional relay/gateway architecture for remote access
- a terminal-oriented ChatGPT workflow
- extensive smoke and integration tests

## Architecture
AI client → MCP tool server → controlled macOS operations.

The project focuses on keeping operations explicit and scoped instead of giving an agent an opaque unrestricted shell.

## Stack
TypeScript, Node.js, Model Context Protocol, macOS automation, SQLite-backed state in selected modules, Docker for gateway components.

## Security
- secrets belong in environment variables or the operating-system credential store
- public configuration uses example values only
- production API keys and private host identifiers are excluded from this portfolio snapshot
- file and process operations are exposed through explicit tools rather than implicit access

## Development
Install dependencies with npm ci and run npm test. See the source and docs directories for the tool catalogue and architecture details.

## Usage and licensing

This repository is source-available for portfolio evaluation. You may inspect the code and run an unmodified local copy for evaluation, but commercial use, redistribution, republishing and derivative distribution are not permitted without written permission. See [LICENSE.md](LICENSE.md).

