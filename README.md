# n8n Workflows

> A curated collection of production-ready **n8n automation workflows** I've built — covering AI pipelines, multi-channel integrations, and human-in-the-loop approvals.

[![JSON Lint](https://github.com/Eliasjakob/n8n-workflows/actions/workflows/json-lint.yml/badge.svg)](https://github.com/Eliasjakob/n8n-workflows/actions/workflows/json-lint.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![n8n](https://img.shields.io/badge/n8n-1.x-EA4B71)](https://n8n.io)

---

## Workflows in this repo

| Workflow | What it does | Tech | Link |
|---|---|---|---|
| **service-quote-generator** | Auto-generate customer quotes with GPT-4.1-mini classification, Telegram approval, and Gmail delivery | OpenAI · Telegram · Gmail · PDFMonkey · Tally | [↗ folder](workflows/service-quote-generator/) |

*More workflows landing soon — see [open issues](../../issues) for what's next.*

## How to use one

Every workflow has its own folder under `workflows/<name>/` with:

- `workflow.json` — the n8n export you can import directly
- `README.md` — use case, tech stack, setup steps, cost estimate
- `architecture.md` — flow diagram (mermaid) + node-by-node walkthrough
- `screenshots/` — n8n editor screenshots

Generic import guide: [`docs/how-to-import.md`](docs/how-to-import.md).

## Why this collection?

These workflows are real, working production templates — not toy examples. Each one:

- **Solves a concrete business problem** (lead capture → quote generation → approval → delivery, in the case of `service-quote-generator`)
- **Uses AI where it earns its keep** — classification, summarization, generation — not as a gimmick
- **Has a human-in-the-loop step** where a critical decision should not be fully automated
- **Is documented end-to-end** so you can read the architecture before importing the JSON

The goal: showcase **agentic automation patterns** that scale beyond simple "trigger → email" workflows.

## Contributing

Have an idea for a workflow? Open a [workflow request](../../issues/new?template=workflow_request.md).

Want to contribute one? See [`PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) for the checklist.

## Compliance

These workflows process real user data when deployed. Read [`docs/compliance-notice.md`](docs/compliance-notice.md) before going live.

## License

[MIT](LICENSE) — © 2026 Elias Mahesh Jakob.
