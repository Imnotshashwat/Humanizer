# [Humanizer](https://imnotshashwat.github.io/Humanizer/)

Paste AI-generated text in. Get human-sounding text out.

One HTML file. No build step, no server, no npm install. Open it in a browser and it works.

---

## Two modes

### ⚡ Offline Scan — no internet, no key

Runs a rule-based scanner on your text. Doesn't rewrite -- that's on you -- but it tells you exactly what's wrong and handles the easy fixes automatically.

What you get:
- **AI Cringe Score** — counts matched patterns, verdict ranges from "Looks good" to "Maximum cringe"
- **Highlighted preview** — red underline for flag-only patterns, gold for auto-fixable ones. Hover to see what each one is
- **Patterns caught** — every match with its category and suggested fix
- **Auto-fixed version** — applies all the clean 1:1 swaps, gives you a copy to paste

### ✦ AI Rewrite — needs internet + API key

Two passes. First pass rewrites the text, second pass catches what the first missed and rewrites again. You get the draft and final to compare, a list of tells it found, and a breakdown of what changed.

---

## Providers

**Anthropic (Claude Sonnet 4)**
Best quality. Inside claude.ai it works without a key. Outside you need a paid key from [console.anthropic.com](https://console.anthropic.com).

**Gemini (gemini-2.0-flash)**
Good quality, free tier is 1500 req/day. Key from [aistudio.google.com](https://aistudio.google.com/apikey).

**Groq (llama-3.3-70b)**
Fastest -- runs on LPU hardware, not GPUs. Slightly weaker on writing tasks but free and stupid fast. Key from [console.groq.com](https://console.groq.com/keys).

Keys live in browser memory for the session. Nothing gets stored, nothing leaves your browser except the API call itself.

---

## What it scans for

Based on [Wikipedia's Signs of AI Writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing):

- **Significance inflation** — `stands as`, `serves as`, `testament to`, `pivotal moment`, `evolving landscape`
- **Promotional language** — `vibrant`, `nestled`, `breathtaking`, `groundbreaking`, `renowned`
- **Chatbot artifacts** — `Great question!`, `Certainly!`, `I hope this helps!`, `Let me know if...`
- **Vague attributions** — `Experts argue`, `Industry observers`, `Studies show`
- **Filler** — `In order to`, `At this point in time`, `It is important to note that`
- **Em dashes** — both `—` and `--`
- **Tacked-on -ing phrases** — `, highlighting the...`, `, reflecting the...`, `, contributing to a...`
- **Negative parallelism** — `It's not just X; it's Y`
- **Generic conclusions** — `the future looks bright`, `exciting times lie ahead`
- **Excessive hedging** — `could potentially`, `might possibly`

Simple swaps get fixed automatically. The rest gets flagged so you can fix it yourself.

---

## Author
[Imnotshashwat](https://github.com/Imnotshashwat)
