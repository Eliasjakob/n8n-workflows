# Compliance & Privacy Notice

> The workflows in this repository are published as **educational templates**. You are responsible for compliant operation when you run them.

## Data flow awareness

When you import and run a workflow, customer / user data may flow through multiple third-party services. Typical flows:

- **Tally** receives form submissions
- **OpenAI** receives the prompt text (and any data in it) for classification or generation
- **Telegram** receives approval requests with quoted content
- **Gmail** receives outbound emails and recipient addresses
- **PDFMonkey** receives the data used to render PDFs

Each service has its own data-processing terms. **You must inform your end users** which third parties their data passes through and obtain consent where required (GDPR, CCPA, etc.).

## API keys = secrets

- Never commit API keys, OAuth refresh tokens, or any credential to the repo.
- n8n stores credentials separately from workflow JSON — the export you find here is **already stripped**.
- If you fork and re-export from your own n8n: double-check no `credentials` blocks ended up in your JSON before pushing.

## No warranty

Workflows are provided as-is. The author cannot guarantee uptime, accuracy of AI-generated content, or correctness for your specific business context. Always test with a small sample before going live.

## Reporting issues

For security-sensitive issues (e.g. a workflow accidentally exposes a credential): do **not** open a public issue. Email the maintainer directly.
