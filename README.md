# clickme

A single-page date invitation. Two buttons — **Yes** and **No** — except the No
button slowly glides away from the cursor, so there's really only one answer.
Once a date and time are picked, the choice is sent to a Google Sheet.

## Setup

1. Open `index.html` and fill in `CONFIG` at the top of the `<script>`:
   - `webAppUrl` — your Google Apps Script Web App URL (ending in `/exec`)
   - `recipientName` / `senderName` — optional
2. Create a Google Sheet, add the Apps Script from `Code.gs`, and deploy it as a
   Web App (Execute as: Me · Access: Anyone).
3. Deploy this page with GitHub Pages and share the link.

## Files

- `index.html` — the page
- `Code.gs` — Google Apps Script that records each response

## Notes

The page is fully static. Responses are saved via a best-effort `no-cors` POST,
so success is confirmed by checking the sheet, not the browser console.
