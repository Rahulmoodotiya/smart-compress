# SmartCompress SEO Audit & Action Plan

Audit started: 2026-11-28
Branch: seo/technical-foundation
Production was NOT changed during this audit.

## Verified from source (main)

- [x] HTML language is set to English.
- [x] SEO title and meta description exist and describe supported formats, batch limit (20), browser-local processing.
- [x] Robots meta allows index/follow.
- [x] Canonical exists and currently points to https://smart-compress.pages.dev/
- [x] Open Graph metadata exists.
- [x] Twitter card metadata exists.
- [x] SoftwareApplication JSON-LD exists.
- [x] Google Search Console verification meta tag exists.
- [x] robots.txt allows crawling and declares sitemap.
- [x] sitemap.xml includes canonical homepage URL only.
- [x] Homepage has descriptive visible copy and quick-use sections.

## Pending validation

- [ ] Fetch live HTML and compare it to source (network checks previously inconclusive).
- [ ] Verify live robots.txt and sitemap.xml HTTP status and content-type.
- [ ] Verify Search Console ownership, indexing status and sitemap processing.
- [ ] Recheck canonical URL after custom-domain decision; do not change it until domain is connected and redirects verified.
- [ ] Validate JSON-LD.
- [ ] Check heading hierarchy, image alt text, crawlable internal links and content uniqueness.
- [ ] Run Lighthouse/PageSpeed and Core Web Vitals.
- [ ] Check mobile usability/accessibility.
- [ ] Keyword research.
- [ ] Create distinct, useful landing pages only after keyword strategy; avoid thin/doorway pages.
- [ ] Review trust pages (privacy/contact/support) as appropriate.

## Priorities

### P0 — Technical discovery and indexing
1. Confirm live homepage, robots.txt and sitemap.
2. Confirm Search Console indexing and sitemap status.
3. Check canonical, redirects, HTTPS and host consistency.
4. Resolve crawl/indexing errors.

### P1 — On-page SEO
1. Review title and description for keyword intent and click-through.
2. Review H1/H2 structure and copy.
3. Validate structured data.
4. Add helpful, accurate trust/privacy/FAQ content.

### P2 — Growth
1. Research keyword clusters/search intent.
2. Build focused pages for supported intents (JPG/PNG/WebP compression, resizing, conversion) only when each page provides distinct value.
3. Add natural internal linking.
4. Publish helpful guides and earn relevant backlinks; avoid mass-generated thin pages.

## Status definitions
PASS = evidence verified. REPORTED PASS = user-reported, not independently reproduced. INCONCLUSIVE = access/network limitations. PENDING = not tested.
