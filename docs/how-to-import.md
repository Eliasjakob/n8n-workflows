# How to import a workflow

This guide applies to every workflow in this repository.

## 1. Download the workflow JSON

Each workflow has a `workflow.json` file inside its folder. Right-click the **Raw** view on GitHub and "Save Link As" to download it.

## 2. Open your n8n instance

Self-hosted, n8n Cloud, or n8n Desktop — all work the same way.

## 3. Import

- Click the **+** in the top-right of the canvas → **Import from File**
- Select the `workflow.json` you just downloaded
- The whole node graph appears on the canvas

## 4. Configure credentials

n8n highlights every node that needs credentials with a red border. Click each red node and:

1. Go to the **Credentials** field
2. Click **Create new credential**
3. Paste your API key / token / OAuth flow

Typical credentials needed across these workflows:
- **OpenAI** — your API key from <https://platform.openai.com/api-keys>
- **Telegram** — bot token from [@BotFather](https://t.me/BotFather)
- **Gmail** — OAuth2 via your Google Cloud project
- **PDFMonkey** — API key from <https://dashboard.pdfmonkey.io/>
- **Tally** — webhook secret (no key needed for the trigger)

## 5. Replace placeholder values

Look at every `Edit Fields` / `Set` node and replace placeholders like:
- `your-business-email@example.com` → your actual email
- `YOUR_CHAT_ID` → your Telegram chat ID
- `YOUR_TEMPLATE_ID` → your PDFMonkey template ID

## 6. Test before activating

Run the workflow manually first (Execute Workflow button). Once a test execution succeeds end-to-end, toggle **Active** in the top-right and save.

---

**Trouble?** Open an [issue](../../issues) with the error message and the node where it failed.
