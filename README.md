# Sage Advice

Hand-picked clothing for Sage. Snap a photo of anything she stops at in a store and Claude identifies the piece, searches the web for where to buy it, and files it in **Sage’s Hand Picked** with a buy link. It also pulls fresh picks in her style every day, and learns from what she saves and skips.

## Use it

1. Open the GitHub Pages site on your phone (Settings → Pages → deploy from `main`, root).
2. Go to **Sage’s style → Settings**, paste your Claude API key (from console.anthropic.com), and save.
3. Add her sizes and budget.
4. Tap **+ Add photos she likes**. Each photo becomes a Hand Picked piece with a link to buy it.
5. On iPhone, Share → **Add to Home Screen** to use it like an app.

## How it works

- Single file: `index.html`. No build step, no server.
- Claude is called straight from the browser with your key (`claude-sonnet-5-5` by default, with the web search tool so links point at real product pages).
- Saves, lists and photos live in this browser (localStorage + IndexedDB). **Copy backup** in Settings copies everything to the clipboard.
- `seed.json` and `photos/` are the pieces from the first Macy’s Herald Square trip; they load on first visit.

The key stays in the browser and is sent only to `api.anthropic.com`, but anyone using that browser can use it. Don't set it on a shared computer.
