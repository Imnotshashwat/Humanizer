# Humanizer v1

Paste AI-generated text in. Get human-sounding text out.

Single HTML file. No build step, no dependencies, no server. Just open it.

---

## Two modes

### ⚡ Offline Scan — works without internet, no API key needed

Runs a rule-based pattern scanner on your text. Doesn't rewrite anything -- that's on you -- but it tells you exactly what's wrong and fixes the easy stuff automatically.

What you get:
- **AI Cringe Score** — counts matched patterns, gives a verdict from "Looks good" to "Maximum cringe"
- **Highlighted preview** — red underline for flag-only patterns, gold for auto-fixable ones. Hover any highlight to see what it is
- **Patterns caught** — every match listed with its category and suggested fix
- **Auto-fixed version** — applies all the simple 1:1 swaps and gives you a clean copy to paste

### ✦ AI Rewrite — needs internet + API key

Two-pass rewrite. First pass rewrites the text, second pass audits that draft for remaining tells and rewrites again. You get the draft and final version to compare, a list of AI tells it caught, and a breakdown of changes made.

---

## Providers (AI mode)

**Anthropic (Claude Sonnet 4)**
Best output quality. If you open this inside claude.ai it works without a key -- Anthropic handles auth automatically. Outside claude.ai you need a paid key from [console.anthropic.com](https://console.anthropic.com).

**Gemini (gemini-2.0-flash)**
Good quality, generous free tier (1500 req/day). Key from [aistudio.google.com](https://aistudio.google.com/apikey).

**Groq (llama-3.3-70b)**
Fastest option -- runs on custom LPU hardware. Slightly below the other two for writing tasks but still solid. Free tier at [console.groq.com](https://console.groq.com/keys).

Keys are saved in memory for the session. Never sent anywhere except the provider's API directly from your browser.

---

## What it scans for

Based on [Wikipedia's Signs of AI Writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing):

- **Significance inflation** — `stands as`, `serves as`, `testament to`, `pivotal moment`, `evolving landscape`
- **Promotional language** — `vibrant`, `nestled`, `breathtaking`, `groundbreaking`, `renowned`
- **Chatbot artifacts** — `Great question!`, `Certainly!`, `I hope this helps!`, `Let me know if...`
- **Vague attributions** — `Experts argue`, `Industry observers`, `Studies show`
- **Filler phrases** — `In order to`, `At this point in time`, `It is important to note that`
- **Em dashes** — both `—` and `--`
- **Superficial -ing phrases** — `, highlighting the...`, `, reflecting the...`, `, contributing to a...`
- **Negative parallelism** — `It's not just X; it's Y`
- **Generic conclusions** — `the future looks bright`, `exciting times lie ahead`
- **Excessive hedging** — `could potentially`, `might possibly`

Auto-fixes where there's a clean swap (e.g. `in order to` → `to`, `boasts` → `has`). Flags the rest for manual editing.

---

## Deploy to GitHub Pages

Push `humanizer.html` to a repo, go to Settings → Pages → deploy from main branch. Done.

Live at `https://Imnotshashwat.github.io/repo-name/humanizer.html`. Anyone can use it with their own API key or just the offline scanner.

---

## Author

[Imnotshashwat](https://github.com/Imnotshashwat)
