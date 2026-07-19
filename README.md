# Radio Time Machine

Pick a country and a vibe — get live internet radio streaming that matches it.

**Live demo:** https://hardikrepo.github.io/radio-time-machine/

## What it does

- Loads a live country list from the [Radio Browser](https://api.radio-browser.info/) API
- Lets you pick a "vibe" (80s Synth, Jazz & Lounge, Lo-fi & Chill, Latin, News & Talk, etc.), each mapped to a set of real station tags
- Searches, deduplicates, and ranks matching stations by popularity (click count)
- Streams the selected station directly in the browser, auto-skipping to the next result if a stream is dead or offline
- Registers a play with Radio Browser's click-counter endpoint, helping keep its popularity stats accurate

## Running locally

No build step — it's a single static HTML file.

```bash
git clone https://github.com/Hardikrepo/radio-time-machine.git
cd radio-time-machine
python -m http.server 8000
# open http://localhost:8000
```

Or just open `index.html` directly in a browser.

## Notes

- Station data and stream URLs are community-submitted via Radio Browser, so some streams may be offline or geo-restricted — the player skips these automatically.
- Stations served over plain `http://` (not `https://`) may be blocked as mixed content by the browser, since this site itself is served over HTTPS.

## Credits

Powered by the [Radio Browser API](https://api.radio-browser.info/), a free, community-maintained database of internet radio stations.
