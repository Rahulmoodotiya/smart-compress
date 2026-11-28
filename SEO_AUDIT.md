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

## Step 2 — Google indexing check (2026-11-28)

- [x] Search Console URL Inspection screenshot: homepage `https://smart-compress.pages.dev/` is ON GOOGLE and Page is indexed (user-provided evidence).
- [x] HTTPS: page served over HTTPS (user-provided evidence).
- [x] Sitemap submission exists for `/sitemap.xml` (user-provided evidence).
- [ ] Sitemap status: Search Console screenshot shows `Couldn't fetch` (user-provided evidence); investigate live response and resubmit only after validation.
- [x] User screenshot confirms `https://smart-compress.pages.dev/sitemap.xml` opens and displays valid sitemap XML with homepage URL.
- [ ] HTTP status/content-type not independently verified; browser XML rendering is evidence of accessibility, not a full HTTP audit.
- [ ] Inspect sitemap details for last-read/errors/discovered URLs and retry submission after validation.
- [ ] User account/Search Console access is not available to this audit, so account-specific checks rely on screenshots.

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


## Step 3 — Initial keyword intent map (research draft)

Keyword targets below are intent-based hypotheses, not verified search-volume or difficulty metrics. Validate with Search Console and a keyword tool before prioritizing.

### Primary homepage intent
- image compressor online
- compress image online
- image size reducer
- reduce image file size

### Format-specific intents (potential dedicated pages only if the page offers genuinely useful, distinct guidance/tool UX)
- compress JPG / JPEG online
- compress PNG online
- compress WebP online

### Task/use-case intents (do not create thin pages; page must support the promise)
- compress images for website
- reduce photo size for upload
- compress multiple images / batch image compressor
- compress image without uploading / private image compressor
- compress image free

### Differentiators to emphasize accurately
- Browser-side processing / images not uploaded
- Batch up to 20 images (current product limit)
- JPG, PNG, WebP support
- Image format conversion among supported output formats (confirmed in source: output MIME options JPEG/PNG/WebP)
- Individual downloads and ZIP batch download
- Free tool

### Competitor SERP observations (qualitative)
- Competitors commonly emphasize browser-local privacy, batch processing, format selection, quality control, target-KB sizing, resize controls and preview comparisons.
- SmartCompress should only advertise features actually implemented. Target-size mode, resize controls, extra formats and preview comparison are potential product gaps—not SEO copy to claim today.

### Next validation
- [ ] Export Search Console Performance queries once impressions accumulate.
- [ ] Check keyword volumes/difficulty with a dedicated keyword tool before selecting exact titles/URLs.
- [ ] Review homepage title/H1 and supporting copy against the primary intent.
- [ ] Build an SEO landing-page plan with URL, intent, unique content, feature fit and internal links; avoid mass/thin pages.


## Step 4 — Homepage on-page SEO draft (SEO branch only)

- [x] Proposed and applied title emphasizing image compressor + converter and JPG/PNG/WebP (SEO branch; production main unchanged).
- [x] Meta description updated to describe compression, conversion, free use, batch up to 20, and browser privacy (SEO branch).
- [x] Open Graph and Twitter title/description aligned (SEO branch).
- [x] H1 changed from brand-only slogan to descriptive compression/conversion intent, retaining a secondary benefit line (SEO branch).
- [x] SoftwareApplication description and feature list updated to include conversion (SEO branch).
- [ ] Review visual appearance and functionality in preview/deployment before merge.
- [ ] Check title/meta length, page headings, and feature claims against live app.


## Step 5 — On-page content and FAQ optimization (SEO branch only)

- [x] SEO section heading now targets image compression and conversion.
- [x] Intro copy explains compressor/converter use cases and output-format selection.
- [x] Added conversion explainer for JPG, PNG and WebP, including JPG transparency flattened to white.
- [x] Added visible conversion FAQ.
- [x] Added matching FAQ structured-data question/answer.
- [ ] Validate FAQ schema and page structure after preview.
- [ ] Check internal links and page UX on mobile.
- [ ] Merge/deploy only after review and QA.
