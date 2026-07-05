# The Context Window

AI news blog, live at **https://eltacolibre.github.io** — hosted free on GitHub Pages, built with Jekyll (GitHub builds it automatically on every push; nothing to install).

## How to publish a new article

1. Create a file in `_posts/` named `YYYY-MM-DD-your-url-slug.md` (the slug becomes the URL).
2. Start it with front matter:

   ```markdown
   ---
   title: "Your Headline Here"
   description: "One-sentence summary — this becomes the Google search snippet and social preview. Keep it under 160 characters."
   tags: [news]
   ---

   Article text in Markdown...
   ```

3. Commit and push:

   ```
   git add . && git commit -m "New post" && git push
   ```

   The article is live at `https://eltacolibre.github.io/your-url-slug/` about a minute later.

Easiest workflow: open this folder in Claude Code and say "write a post about X" — then review, edit, and push.

## SEO setup (do these once)

- [ ] **Google Search Console** — go to <https://search.google.com/search-console>, add property `https://eltacolibre.github.io`, verify via HTML tag (paste the tag into `_layouts/default.html` `<head>`), then submit `sitemap.xml`. This is the single most important step for ranking.
- [ ] **Bing Webmaster Tools** — <https://www.bing.com/webmasters>, can import from Search Console. (Bing also feeds DuckDuckGo and ChatGPT search.)
- [ ] Already handled by the site: sitemap (`/sitemap.xml`), RSS (`/feed.xml`), meta/OpenGraph/Twitter tags, JSON-LD structured data, robots.txt, mobile-friendly fast pages.

## SEO strategy that actually works for a new AI blog

- **Don't chase breaking news at first.** You can't outrank The Verge on "OpenAI announcement" in week one. Target specific long-tail questions people search: "what is a context window", "RAG vs fine-tuning", "is [tool] worth it". Explainers and comparisons rank; hot takes don't.
- **Publish consistently** (1–2 posts/week beats 10 posts then silence) and **interlink your articles** like the two starter posts do.
- **Descriptions matter**: the `description` front matter is your search snippet — write it for a human deciding whether to click.
- After ~3 months of consistent posting, check Search Console for queries where you rank on page 2 and beef up those articles.

## Monetization roadmap (in realistic order)

1. **Now — affiliate links.** Amazon Associates, or AI-tool affiliate programs (many AI SaaS products pay 20–30% recurring). Works fine on github.io. Always disclose.
2. **Now — newsletter.** Add a free Substack or Buttondown signup link; the email list is an asset no algorithm can take away, and sponsors pay for it later.
3. **At ~1k visits/month — buy a domain (~$10–12/yr).** The one worthwhile expense. Point it at this site (GitHub Pages supports custom domains free: repo Settings → Pages → Custom domain), then apply for **Google AdSense** — AdSense will not accept a github.io subdomain, so this unlocks ad revenue. Set the domain up early if you can; changing domains later loses accumulated SEO.
4. **At real traffic (10k+/mo) — better ad networks** (e.g. Ezoic, then Mediavine at 50k sessions) and **direct sponsorships** of posts/newsletter.

## Customizing

- Site name, tagline, author: `_config.yml` (and the three `<span class="tok">` words in `_layouts/default.html`).
- Colors and fonts: `assets/css/style.css` (design tokens at the top).
