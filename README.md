[README.md](https://github.com/user-attachments/files/29655420/README.md)
# Atlas AI Assistant

A single-file HTML chatbot that calls the Claude API to answer absolutely anything — writing, code, planning, math, advice, and more.

## Files

- `index.html` — the entire app (structure, styling, and logic in one file)

## Running It

Just open `index.html` in a browser, or host it (see the hosting guide) — no build step, no dependencies, no installation needed.

## How to Change the Assistant's Name

The name "Atlas" appears in **3 places** inside `index.html`. To rename it (e.g., to "Nova", "Zed", "Kira" — anything you like), open the file in any text editor and replace all 3:

**1. The page title** (near the top, in the `<head>` section):
```html
<title>Atlas — Your AI Assistant</title>
```
Change `Atlas` to your new name.

**2. The header inside the chat** (in the `<body>` section):
```html
<h1>Atlas</h1>
```
Change `Atlas` to your new name.

**3. The AI's personality instructions** (near the bottom, inside the `<script>` section):
```javascript
const SYSTEM_PROMPT = "You are Atlas, an exceptionally capable and reliable AI assistant. ...";
```
Change `Atlas` to your new name here too — this is what the AI reads to know its own identity, so if you skip this step it may still refer to itself as "Atlas" when replying.

**Optional — also update:**
```html
<div class="empty-state" id="emptyState">
  <span class="eyebrow">Atlas</span>
```
This is the small label shown on the welcome screen before any messages are sent.

That's it — no other code needs to change. The colors, layout, and chat logic all stay exactly the same regardless of the name you choose.

## Changing the Personality

While you're in the `SYSTEM_PROMPT` line, you can also rewrite the rest of the sentence to change tone — for example, make it more casual, more formal, or focused on a specific area like coding or writing, instead of "anything."

## Publishing It Publicly — Important

This file currently calls the Claude API directly from the browser. That works fine for local testing and previews, but **before hosting it publicly**, you must route that API call through your own small backend so your API key isn't exposed to anyone who views the page's source code. See the hosting guide for free backend options.

## Related Guides

- `atlas-description-and-hosting-guide.md` — where to upload this file and store-listing description text
- `detailed-guide-google-search-play-store.md` — full free walkthrough for Google Search indexing and Play Store publishing
