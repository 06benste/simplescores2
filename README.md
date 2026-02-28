# Simple Scores

**Live (well almost!) football scores and league tables** for the main English leagues and cups.

👉 **Open the site:** [https://06benste.github.io/simplescores2/](https://06benste.github.io/simplescores2/)

---

## But why is this needed?

When I was attending home matches at Newcastle United's St James Park thgere were significant signal bottlenecking with 52000 people all trying to access their phones. Simple webpages would ocassioanlly load however more complex sites (such as sports scores sites) would not load.
Hence this site. With all the processing completed serverside, all the phone needs to do is load a very small simple HTML file (scores circa 4kb, tables circa 5kb) with no JS, CSS etc.
Why not update every minute or more though? While the scores and tables HTML files are hosted on github pages, the script and backend to create them actually run locally on my Home Assistant through a custom integration I have created. The PY scripts here scrape various sports scores and tables sources, create the scores and tables HTML pages and push these to GITHUB. Each time this happens a commit is made and github actions re-deploy the pages site. Every minute or more would be extemely intensive on both systems (and actually would not complete one run before the next starts, hence the 5 minute update interval)
---

## What’s on the site

- **Scores** – Today’s matches with live or final scores, kick-off times, and (when available) minutes played for games in progress.
- **Tables** – Current league standings: position, team, games played, goal difference, and points for Premier League, Championship, League One, and League Two.
- **Cups** – FA Cup and Carabao Cup scores (no league tables for these).
- **Scraper status** – When the data was last updated and when the next update is due.

---

## When it updates

- **Match days:** Scores and tables refresh **every 5 minutes** from shortly before the first kick-off until after the last match (plus a final update a bit later).
- **Daily:** A full refresh runs once per day in the early hours (UTC) so the schedule and pages are ready for the next day.

So on days with fixtures you get updates every 5 minutes during the match window; on other days the site may not change until the next daily run.

---

[☕ Buy me a coffee](https://buymeacoffee.com/06benstecode)
