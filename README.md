# llms.txt Generator

A free, browser-based tool that generates a spec-compliant [`llms.txt`](https://llmstxt.org) file for any website — no signup, no server, nothing uploaded. Paste your site's `robots.txt`, `sitemap.xml`, and page source HTML, and it builds a structured, machine-readable summary designed for AI answer engines, voice assistants, and generative search tools (ChatGPT, Claude, Perplexity, and similar) to read and cite accurately.

**[Live demo →](https://sara-mbl.github.io/llms-txt-generator/)**

## Why llms.txt?

As search shifts from ten blue links to AI-generated answers, `llms.txt` gives language models a clean, factual summary of a site — entity-rich and machine-parseable — instead of forcing them to parse marketing copy and navigation chrome. This is sometimes called AEO (answer engine optimization), GEO (generative engine optimization), or VSO (voice search optimization).

## Features

- **Fully client-side** — parses everything in your browser with `DOMParser`; nothing is sent to a server
- **Structured data extraction** — pulls business name, address, phone, hours, price range, and social links from JSON-LD (`LocalBusiness`, `Organization`, etc.)
- **Action link detection** — finds booking/ordering/menu/reservation links automatically
- **Consistency checks** — flags conflicting schema values across pages (e.g. mismatched price ranges or business names), pages missing from the sitemap, and robots.txt rules that might block a page
- **One-click export** — copy to clipboard or download the finished `llms.txt`

## How to use

1. Open the [live tool](https://sara-mbl.github.io/llms-txt-generator/).
2. Get your site's `robots.txt` and `sitemap.xml` by visiting those URLs directly and copying the contents (the in-tool "How to get robots.txt, sitemap.xml, and page source" panel walks through this step by step).
3. For each page you want documented, right-click → **View Page Source**, copy the HTML, and paste it into a page block along with that page's URL.
4. Click **Generate llms.txt**, review any flagged warnings, then copy or download the file.
5. Place the resulting `llms.txt` at the root of your site (e.g. `https://yoursite.com/llms.txt`).

## Tech stack

Vanilla HTML, CSS, and JavaScript. No build step, no dependencies, no framework — open `index.html` in any browser and it works.

## Limitations

- Can't fetch URLs directly (browser security) — page source must be pasted in
- Sitemap indexes (a sitemap of sitemaps) aren't auto-expanded; paste the child sitemap directly if needed
- Summaries are extracted heuristically from meta tags and schema, not rewritten — messy source input produces a messy first draft

## License

MIT — see [LICENSE](./LICENSE).

## Author

Built by **Sara Bustamante**
[GitHub](https://github.com/sara-mbl/) · [LinkedIn](https://www.linkedin.com/in/sarambl/)

File structure based on the [llmstxt.org](https://llmstxt.org) standard.
