# [Humanizer](https://imnotshashwat.github.io/Humanizer/)

<p align="left">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT" /></a>
  <a href="https://imnotshashwat.github.io/Humanizer/"><img src="https://img.shields.io/badge/Demo-GitHub%20Pages-blue" alt="Live Demo" /></a>
</p>

A single-file web tool that flags AI writing tells and cleans them up. 

Everything runs inside one `index.html` file. No build steps, no Node.js backend, and no dependencies. Double-click to open it locally in any browser or use the hosted GitHub Pages link.

---

## What it does

### Offline Scanner
Runs entirely in your browser using pattern matching. It does not send your text anywhere and requires no API keys.
* Flags common AI tells like significance inflation, negative parallelism, filler phrases, and excessive hedging.
* Calculates an AI score based on how many patterns triggered.
* Underlines issues directly in your text (red for warnings, gold for quick swaps).
* Automatically fixes simple 1:1 phrase replacements and gives you a clean copy.

### AI Rewrite
For deeper revisions, you can plug in an API key from Anthropic (Claude Sonnet), Google (Gemini 2.0 Flash), or Groq (Llama 3.3 70B).
* Runs a two-pass review: first pass rewrites the text, second pass catches remaining stylistic issues.
* Shows a side-by-side comparison between draft and final versions along with notes on what changed.
* Keys are kept only in browser session memory and never stored or sent anywhere else.

---

## Features
* **Dark & Light theme**: Toggle between deep espresso dark mode and a warm editorial paper theme. Your preference saves automatically.
* **Completely client-side**: Works offline out of the box for rule-based scanning.
* **Based on real Wikipedia guidelines**: Pattern rules adapted from Wikipedia's essay on signs of AI-generated text.

---

## Acknowledgements & Credits
* Rules adapted from [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) and inspired by [blader/humanizer](https://github.com/blader/humanizer).
* Built by [Imnotshashwat](https://github.com/Imnotshashwat).

## License
Open source under the [MIT License](LICENSE).