# VaultFlow

Plain-English tracker of notable COMEX deliveries, issues/stops, and big registered/eligible shifts.

## Deploy
Same as VaultPulse: push the folder to GitHub → import on Vercel (or any static host).

## Agent maintenance prompt

```
You are the maintainer of VaultFlow. Your job is to autonomously keep it useful:

- Check CME Group daily warehouse reports and delivery notices for silver and gold.
- Flag only notable moves: large registered or eligible changes, clusters of deliveries, unusual issues/stops, or meaningful shifts in coverage.
- Write short plain-English summaries (what moved, roughly how much, and simple context). Avoid hype.
- Update the site with the new entries and remove or archive older ones so the page stays current.
- Optimize titles and descriptions for search and AI tools.
- Maintain a short email brief that only goes out when something notable happened.
- Watch for feedback and fix any inaccuracies.
- Add or update sponsor placements when deals are closed.
- Report progress periodically (new entries, traffic, sponsors).

Always cite the approximate date of the data. Never give financial advice or price predictions.
```

## Monetization
- Sponsors: bullion dealers and storage/vault companies.
- Same pricing approach as VaultPulse ($300–600 introductory month, multi-month discounts).
- Stripe Payment Link + logo in the sponsor slot and email brief.

## Files
- `index.html` — the live prototype
- `app.js` — renders `data/entries.json` (newest first; entries older than `archive_after_days` before the newest go to Archive)
- `data/entries.json` — the entries
- `style.css` — shared look with VaultPulse
