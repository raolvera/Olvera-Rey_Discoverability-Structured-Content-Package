# Discoverability and Structured Content Package

Rey Olvera
GIT 515 Advanced Web Coding
Professor Hillerman
Module 6 Discoverability and Structured Content Package
October 4, 2026
ASU Sun Devils Football Gameday Hub

## Overview

This package builds on my Module 5 accessibility work and turns it into a discoverability plan for the Gameday Hub. The site is a small HTML and CSS project with no framework, where all six pages share one header, one primary navigation bar, and one footer, so what sets a page apart is its own h1, its title, its meta description, and the content under them. The same choices that help people, clear headings, honest alt text, and plain-language links, also give search engines and social crawlers something accurate to read, so the accessibility work and the discoverability work pull in the same direction. For each page I tie the main task a visitor is there to finish to a unique title, a meta description drawn from visible content, the headings and internal links that carry the structure, a canonical decision, the images that matter, and the validation checks I ran. I kept every value tied to what a visitor actually sees, since Google builds its title links and snippets from visible page signals and will rewrite a title or description that does not match the page (Google Search Central: Title Links; Google Search Central: Snippets).

## 1. Metadata Inventory and Page Purpose

The site has six pages, and each one answers a single thing a gameday visitor is trying to do. Every page gets a title and description that stand in for it in search, plus a canonical decision for when the domain is set.

Home (index.html) is the front door. A visitor gets their bearings here and jumps to the right topic through the Quick Links grid and the Gameday at a Glance stats. Its title is Home | ASU Sun Devils Gameday Hub, and its description promises clear-bag rules, parking, light rail, traditions, and the fall schedule in Tempe. Its primary heading is Everything You Need for Sun Devils Gameday, and it takes a self-referencing canonical once the domain is live.

Gameday Traditions (traditions.html) is where a fan picks up the rituals: Forks Up, the Tillman Tunnel run-out, the fight song, tailgating, and the Pat Tillman tribute. Its title is Gameday Traditions | ASU Sun Devils Gameday Hub, and its description names those traditions. Its primary heading is Gameday Traditions, and it takes a self-referencing canonical.

Stadium Guide and Policies (stadium.html) is the page to read before heading over. It covers the clear-bag policy, prohibited items, and gate times. Its title is Stadium Guide & Policies | ASU Sun Devils Gameday Hub, and its description lists those policies. Its primary heading is Stadium Guide & Policies, and it takes a self-referencing canonical.

Transportation and Parking (transportation.html) is where someone weighs parking lots against the Valley Metro light rail and finds the stadium on the map. Its title is Transportation & Parking | ASU Sun Devils Gameday Hub, and its description names lots, prices, accessible options, and light rail. Its primary heading is Transportation & Parking, and it takes a self-referencing canonical.

Fall Schedule (schedule.html) is where a fan looks up dates, opponents, locations, and kickoff times. Its title is Fall Schedule | ASU Sun Devils Gameday Hub, and its description names those columns. Its primary heading is Fall Football Schedule, and it takes a self-referencing canonical.

FAQ and Contact (faq.html) is where a visitor gets fast answers and sends a note through the contact form. Its title is FAQ & Contact | ASU Sun Devils Gameday Hub, and its description names the common questions plus the form. Its primary heading is FAQ & Contact, and its self-referencing canonical is already in the head as a working model.

Each title and description points at content that is really on the page, so Google can lean on it rather than grabbing a weaker scrap from the body (Google Search Central: Title Links; Google Search Central: Snippets).

## 2. Titles and Descriptions

Every page uses the same title pattern, the page name, a divider, then the site name, so Home reads Home | ASU Sun Devils Gameday Hub. The page name leads so it reads first in a browser tab and in a search result, with the site name trailing for context. All six titles are unique, each matches the h1 a visitor sees, and each stays near sixty characters so there is less reason for Google to rewrite the title it shows. The descriptions each sum up the page in a single sentence of roughly 150 to 160 characters, built from the visible content, so the snippet in search reflects what a visitor will really find instead of a weaker fragment pulled from the body. Because the titles and descriptions echo the headings and the content, the browser tab, the search result, and the page itself all tell the same story (Google Search Central: Title Links; Google Search Central: Snippets).

## 3. Semantic Headings and Crawlable Links

Each page uses one h1 that names the page, followed by h2 section headings that match the visible blocks, so the heading outline reads like a real table of contents rather than styling. Stadium Guide and Policies, for example, runs h1 Stadium Guide & Policies, then h2 Clear-Bag Policy, h2 Prohibited Items, and h2 Gate Times & Screening, which lines up one to one with what a visitor scrolls past, and the data tables under those headings use captions and scope attributes so their structure is clear to both people and machines. For internal links, every page carries the shared primary navigation and footer navigation, which connect all six pages to each other with plain, descriptive anchor text, so any page is reachable from any other page. On top of that, most content pages include a forward Next link that walks a visitor through the natural order, Traditions to Stadium Guide, Stadium Guide to Transportation, Transportation to Schedule, and Schedule to FAQ. Every internal link uses a real href with human-readable anchor text rather than click here, which helps both visitors and search engines see how the pages connect (Google Search Central: Links).

## 4. Canonical, Robots, and Sitemap Notes

Canonical applies after publication. Each page should carry a self-referencing canonical that points at its own preferred URL once the deploy domain is known, so duplicate or parameter URLs fold into one preferred page. I have already added that tag to all six pages, pointing at the published host, https://raolvera.github.io/Olvera-Rey_Discoverability-Structured-Content-Package/. Canonical is a hint to search engines rather than a guarantee, so I treat it as helping disambiguation, not forcing it (Google Search Central: Canonicalization).

Robots does not apply as a blocking tool now, and it should stay permissive after publication. This is a public informational site where every page is meant to be found, so there is no page I want to hide with a robots meta tag or a Disallow rule. After publication I would add a minimal robots.txt that allows all crawlers and points to the sitemap. I would not place noindex on any page, since all six are meant to be discoverable (Google Search Central: Robots).

A sitemap applies after publication, not now, because an XML sitemap only makes sense once the pages have real public URLs. Once the domain is live I would generate a small sitemap.xml listing the six canonical URLs with last-modified dates and reference it from robots.txt. The site is tiny and fully cross-linked through the shared navigation, so a sitemap is a nice-to-have rather than a strict need, but it is a cheap way to speed discovery (Google Search Central: Sitemaps).

## 5. Social Metadata

I set up Open Graph and Twitter card metadata on all six pages so a shared link renders a controlled preview card instead of whatever a platform guesses, and the FAQ and Contact page carries the most complete set, shown in the snippet below. Each page declares an og:type of website, an og:title and og:description that echo the visible title and description, an og:url set to the page's canonical URL, an og:image written as an absolute path because social crawlers do not resolve relative URLs, and an og:image:alt that reuses the photo's alt text so the preview image still has a text alternative. Home points its image at the hero crowd photo, Traditions at the Pat Tillman number 42 tribute, Stadium Guide at the empty-seats photo, Schedule at the football-on-grass photo, and Transportation at the hero crowd photo, so each preview shows an image that genuinely represents that page. Because the og:title and og:description mirror the visible title and description, the preview, the search snippet, and the page itself stay consistent (Open Graph Protocol; Google Search Central: Snippets).

The Open Graph and Twitter card snippet, as added to the head of faq.html:

```html
<meta property="og:type" content="website">
<meta property="og:title" content="FAQ & Contact | ASU Sun Devils Gameday Hub">
<meta property="og:description" content="Quick answers about ASU Sun Devils gameday: digital tickets, re-entry, heat, kids, and accessible parking and seating, plus a contact form.">
<meta property="og:url" content="https://raolvera.github.io/Olvera-Rey_Discoverability-Structured-Content-Package/faq.html">
<meta property="og:image" content="https://raolvera.github.io/Olvera-Rey_Discoverability-Structured-Content-Package/images/gameday-crowd-1280.jpg">
<meta property="og:image:alt" content="A fan raises a yellow foam pitchfork hand above a packed maroon-and-gold gameday crowd in Tempe.">
<meta property="og:site_name" content="Sun Devils Gameday Hub">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="FAQ & Contact | ASU Sun Devils Gameday Hub">
<meta name="twitter:description" content="Quick answers about ASU Sun Devils gameday: digital tickets, re-entry, heat, kids, and accessible parking and seating, plus a contact form.">
<meta name="twitter:image" content="https://raolvera.github.io/Olvera-Rey_Discoverability-Structured-Content-Package/images/gameday-crowd-1280.jpg">
```

## 6. Structured Data

I added structured data to one page, the FAQ and Contact page, and used exactly one type, FAQPage, because it is the only page whose visible content is a genuine list of questions and answers built from details and summary elements. I wrote it as JSON-LD in a script of type application/ld+json in the head, with a mainEntity array of five Question objects whose acceptedAnswer text matches the visible accordion word for word, and no invented or hidden entries, which is what Google requires for FAQPage markup. I deliberately did not add Event or SportsEvent markup to the schedule page, even though a gameday site seems like a natural fit, because the schedule table is clearly labeled placeholder capstone data with a note to verify everything on official sources, so marking it as real dated events would misrepresent the content; structured data should describe what is genuinely on the page, so I deferred schedule markup until the data is real and verified (Google Search Central: Structured Data). The full FAQPage JSON-LD block lives in the head of faq.html.

## 7. Image Discoverability

The photos that carry meaning each get a descriptive filename, an alt decision, surrounding text, dimensions, and a note on page relevance. The decorative SVG icons and trident logos are left off this list, because they carry aria-hidden of true and focusable of false and need no alt text (W3C WAI Images Tutorial).

On Home the hero photo is gameday-crowd-1280.jpg in a responsive set at 1280 by 1920. Its alt describes a fan raising a yellow foam pitchfork over a maroon-and-gold crowd with players on the sunlit field. It sits beside the hero heading and a visible credit, and it sets the gameday tone for the front door. Home also carries the spotlight photo stadium-seats-400.jpg in a responsive set at 900 by 600. Its alt is short, about rows of empty seats sweeping toward the upper deck, because the First time at Mountain America Stadium text next to it already carries the point.

On Stadium Guide and Policies the feature photo is stadium-900.jpg in a responsive set at 900 by 600. Its alt describes empty maroon and gold seats around the field before gates open, and it sits next to the lede and the Clear-Bag Policy section. On Fall Schedule the feature photo is football-900.jpg in a responsive set at 900 by 600. Its alt describes a Wilson NCAA football on bright green grass, and it sits next to the schedule intro and the 2026 Season Matchups table. On Gameday Traditions the tribute photo is tribute-42-640.jpg in a responsive set at 900 by 600. Its alt describes a grunge number 42 painted in yellow on aged metal that echoes Pat Tillman's retired number, and it sits next to the Honoring Pat Tillman text about the number 42 and the Tillman Tunnel.

Every content photo uses width, height, and CSS aspect ratio to reserve its space so the layout does not jump on load. Each one serves WebP with a JPEG fallback through the picture element and carries a visible credit (W3C WAI Images Tutorial).

## 8. Validation Evidence

I validated this package through both source inspection and an official tool. In source inspection I read each page's head to confirm one unique title and one meta description per page, all six titles unique, a canonical tag present on every page, and the Open Graph, Twitter, and JSON-LD blocks sitting in valid head markup, and I confirmed by reading the rendered content that every FAQ question and answer in the JSON-LD matches the visible accordion word for word. For the official-tool check I validated the FAQPage structured data with the Schema.org Markup Validator by pasting the faq.html markup into its code input, and the validator detected the FAQPage with zero errors and zero warnings and read back all five Question entries with their acceptedAnswer text exactly as written; a screenshot of that result is included with this submission (Google Search Central: Structured Data). The remaining checks need a live, public URL, so they are deferred as post-publish work: once the domain is live I will run the real URLs through Google's Rich Results Test and the Schema.org validator in live-URL mode, preview the Open Graph cards in the Facebook Sharing Debugger and the LinkedIn Post Inspector, and run the pages through the W3C Markup Validation Service. The canonical, og:url, og:image, and twitter:image on every page already use the real published host, https://raolvera.github.io/Olvera-Rey_Discoverability-Structured-Content-Package/, so no placeholder swap is needed before those live checks (Open Graph Protocol; W3C: Markup Validation Service).

## 9. Ranking Claims I Will Not Make

Good metadata and structured data change how content is understood and displayed, not where it ranks. There are two claims I am specifically not making, because they go beyond what my evidence shows.

First, I will not claim this work raises the site's search ranking or puts it on the first page of results. Titles, descriptions, canonical tags, and FAQPage markup help search engines understand and present the pages. Ranking, though, depends on many factors outside this package, including content depth, inbound links, competition, and site authority. A clean validator pass proves the markup is correct, not that the page will rank higher.

Second, I will not promise that the FAQ rich result, the question-and-answer dropdown, will appear in Google. Rich result display is at the search engine's discretion. Google has in recent years limited FAQ rich results largely to authoritative government and health sites, and it can withdraw the treatment at any time, so valid markup makes a page eligible but does not guarantee the enhanced appearance.

In short, this package supports accurate understanding, honest previews, and clean machine-readable structure. It does not guarantee position, traffic, or a specific rich-result appearance (Google Search Central: Structured Data; Google Search Central: Snippets).

## 10.  AI-Assisted with Disclosure

AI may helped draft alternatives, organize inventories, and explain documentation. I must verified accuracy against visible content and avoid unsupported ranking claims.

## References

Google Search Central. Control your title links in search results. Google. https://developers.google.com/search/docs/appearance/title-link

Google Search Central. Control your snippets in search results. Google. https://developers.google.com/search/docs/appearance/snippet

Google Search Central. Links and Google Search. Google. https://developers.google.com/search/docs/crawling-indexing/links-crawlable

Google Search Central. Canonicalization and how to specify a canonical URL. Google. https://developers.google.com/search/docs/crawling-indexing/canonicalization

Google Search Central. Robots meta tag, data-nosnippet, and X-Robots-Tag specifications. Google. https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag

Google Search Central. Build and submit a sitemap. Google. https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap

Google Search Central. Intro to structured data markup. Google. https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data

Open Graph Protocol. The Open Graph protocol. https://ogp.me/

W3C WAI. Images tutorial. World Wide Web Consortium. https://www.w3.org/WAI/tutorials/images/

W3C. Markup Validation Service. World Wide Web Consortium. https://validator.w3.org/
