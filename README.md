# phantom-scan

Static analysis CLI that finds dead AI-generated code in TypeScript / Node.js projects.

> **Status:** pre-release. First working version (v0.1) targeting Q2 2026.

## What is this?

When AI agents (Cursor, Claude Code, Cline, Aider, and similar) write code at scale, a specific class of bug emerges:

- A new service file is created and exported — but never imported.
- A new command handler is registered — but the command is never wired into the router.
- A new database model is defined — but nothing reads from it.
- A new npm dependency is installed — but never imported anywhere.

This is **phantom code** — code that compiles, passes type-checks, looks correct in isolation, but is never reached at runtime. Conventional linters miss it because no individual file is wrong. The bug lives in the **gap** between files.

phantom-scan finds the gap.

## Roadmap

- [ ] CLI v0.1 — minimum viable scanner
- [ ] GitHub Action wrapper
- [ ] Configuration file support
- [ ] JSON output for CI integration

## License

MIT — see [LICENSE](./LICENSE).
