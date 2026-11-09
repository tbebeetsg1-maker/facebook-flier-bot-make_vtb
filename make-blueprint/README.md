# 🔧 Make.com Blueprint

`flier-bot-blueprint.json` is the exported Make.com scenario for the Facebook Flier Bot, **sanitized** for sharing: connections, IDs, emails, and client details have been removed.

## How to import it
1. In Make.com, create a new scenario.
2. Click **⋯ → Import Blueprint** and choose `flier-bot-blueprint.json`.
3. Reconnect each module to your own accounts (Google Sheets, Google Drive, Gmail, Facebook Pages).
4. In each Google Sheets module, pick your own spreadsheet and the **Queue** tab (see [../docs/sheet-layout.md](../docs/sheet-layout.md)).
5. In the Facebook Pages module, pick your Page.
6. Update the email recipients in the Gmail module.
7. Run once with a test row before posting anything real.
