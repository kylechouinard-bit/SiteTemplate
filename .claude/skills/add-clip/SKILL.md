---
name: add-clip
description: Add a new article to the Clips section of Kyle's homepage (index.html) and publish it. Use when Kyle asks to add, post or put a new story, article or clip on the site.
---

# Add a clip

Kyle's clips live in the Clips section of `index.html`, inside `<ul class="clips">`.

## 1. Get the details from Kyle

Each clip needs:

- **Headline**: exactly as Kyle gives it.
- **Link**: the full URL to the story.
- **Publication name**: exactly as Kyle gives it (for example, `Las Vegas Sun`).
- **Date**: exactly as Kyle gives it. Existing clips use the format `November 12, 2026 11:23 a.m.`, but don't reformat what Kyle sends.

If Kyle gives a link without a headline, publication name or date, ask for what's missing. Don't open the link to fill it in, and don't guess. If he wants it posted anyway, put `[Date to come]`, `[Headline to come]` or `[Publication to come]` in that spot and tell him.

Kyle's message may be a Markdown link like `[Headline](https://...)`. The text in the brackets is the headline, and the part in parentheses is the link.

## 2. Add it to the page

Unless Kyle says where it goes, add the new clip as the **first** item in the list. Copy this format exactly, matching the existing indentation:

```html
        <li>
          <a href="LINK">HEADLINE</a> — PUBLICATION
          <span class="date">DATE</span>
        </li>
```

- Keep Kyle's punctuation exactly: curly quotes (‘ ’ “ ”), dashes (—) and capitalization.
- In the headline and date, write `&` as `&amp;`, `<` as `&lt;`, and `>` as `&gt;`. In the link, also write `"` as `&quot;`.
- Don't change, reorder or remove any other clips unless Kyle asks.
- If Kyle wants to swap one out (for example, to keep five), confirm which clip to remove first if he didn't say.

## 3. Publish

Follow CLAUDE.md: commit straight to `main` with a short message such as `Add clip: <headline>`, then push. If the push fails, tell Kyle plainly what went wrong.

## 4. Tell Kyle

In plain words, say which clip was added and where it sits in the list. Mention anything left as a placeholder, and say the live site at https://kylechouinard-bit.github.io/SiteTemplate/ can take a minute or two to update.
