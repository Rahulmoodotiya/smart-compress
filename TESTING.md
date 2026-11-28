# SmartCompress QA status

Last checklist review: 2026-11-28.

## Reported manual checks (owner-reported; not independently re-run here)
- [x] Android: select image(s)
- [x] Android: JPG compression
- [x] Android: individual download
- [x] Android: multiple image selection
- [x] Android: ZIP download
- [x] Android: ZIP extraction
- [x] Android: PNG output file created and extracted/opened

## Static source checks completed in this review
- [x] Input allowlist supports JPG/JPEG, PNG and WebP by MIME/extension.
- [x] Batch cap is 20 images.
- [x] ZIP archive size guard: 100 MB output data.
- [x] Classic ZIP 4 GB guard.
- [x] Output filename sanitization and duplicate-name handling.
- [x] PNG-to-JPG transparency is explicitly flattened against white.
- [x] PNG is retained if re-encoding would increase size.
- [x] Batch cancellation control exists.
- [x] Failed-image retry exists.
- [x] Processing canvas is cleared after processing.
- [x] No image-upload API/network call was found in the compression source.
- [x] Homepage SEO metadata and structured data present.
- [x] Sitemap and robots file present.
- [x] Added standalone FAQ, JPG, PNG, WebP guides, privacy and terms pages; linked from homepage and sitemap.

## Runtime tests still required (not marked PASS without actual device/browser execution)
- [ ] JPG -> JPG output decodes and visually compares.
- [ ] JPG -> PNG conversion.
- [ ] PNG -> JPG conversion and white transparency flattening.
- [ ] PNG -> PNG transparency preserved.
- [ ] WebP -> WebP and cross-format conversion.
- [ ] Preview loads for all formats.
- [ ] 10-image batch.
- [ ] 20-image batch (limit edge).
- [ ] Reject 21st image without corrupting existing batch.
- [ ] Duplicate filenames in individual downloads and ZIP.
- [ ] ZIP integrity: all entries open and match expected file contents.
- [ ] Cancel batch mid-run; verify completed results remain downloadable.
- [ ] Retry one deliberately failed item.
- [ ] 30 MB input boundary and over-limit input.
- [ ] 30 MP input boundary and over-limit image.
- [ ] Output max-dimension and max-pixel safety boundary.
- [ ] Large-file memory stability / repeated batches.
- [ ] Android Chrome responsive UI and downloads.
- [ ] Desktop Chrome, Firefox and Safari compatibility.
- [ ] Live production deployment matches latest main commit.
- [ ] Live URL uptime and page-by-page HTTP response check.
- [ ] Search Console sitemap submission and indexing status.

## Release notes
Static code inspection is not equivalent to runtime QA. Do not report the unchecked runtime tests as passed until they have been executed on the actual website/device.
