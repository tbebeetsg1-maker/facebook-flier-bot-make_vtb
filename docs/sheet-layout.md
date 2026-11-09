# 📋 Flier Queue — Google Sheet Layout

The Make.com bot reads and updates one Google Sheet tab named **Queue**. Each row is one month's flier.

| Column | Header | What goes in it | Filled by |
|---|---|---|---|
| A | Month | e.g. `Nov 2026` | Me |
| B | Theme | Flier theme/headline, e.g. `Fall in Love` | Me |
| C | Flier Link | Google Drive **Web View** link to the flier image | Me |
| D | Caption | Facebook post caption with hashtags | Me |
| E | Post Date | Date the flier should go live | Me |
| F | Status | Dropdown: `Pending` → `In Review` → `Approved` → `Posted` | Me + the bot |
| G | Posted On | Date the flier was posted | The bot |
| H | Notes | Anything extra (internal only) | Me |

## Status dropdown

| Status | Color | Meaning |
|---|---|---|
| Pending | Yellow | Ready to send for review |
| In Review | Orange | Review email sent to the client |
| Approved | Green | Client approved, ready to post |
| Posted | Purple | Live on Facebook |

## Tips
- Status values must match **exactly** (spelling and capitals), because the Make filters look for those words.
- Use the **Web View Link** from Drive (`drive.google.com/file/d/…/view`). The bot pulls the file ID out of that format.
- Leave **Posted On** blank; the bot fills it in.

## Example row

| Month | Theme | Flier Link | Caption | Post Date | Status | Posted On | Notes |
|---|---|---|---|---|---|---|---|
| Nov 2026 | Fall in Love | drive.google.com/file/d/…/view | 🍂 Fall in love with your hair this season! … | 11/5/2026 | Posted | 11/5/2026 | First real flier! |
