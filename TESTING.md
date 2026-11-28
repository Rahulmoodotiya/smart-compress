# SmartCompress QA Test Plan

## Test status rules
- **PASS**: The test was run and its expected result was observed.
- **REPORTED PASS**: The user previously reported it passing; not independently re-run in this QA session.
- **FAIL**: Test was run and the observed result did not meet expectations.
- **NOT TESTED**: No reliable execution evidence yet.
- Do not mark tests as passed without evidence. Record the browser/device, input fixture, result, and date when executing tests.

## Confirmed app constraints from source
- Maximum batch size: **20 images** (therefore, a 30-image test is invalid and has been removed).
- Maximum input file size: **30 MB**.
- Maximum input dimensions: **30 megapixels**.
- Output dimension/area guardrails: **12,000 px per side and 50 MP**.
- Supported image formats: JPG/JPEG, PNG, WebP.
- Processing is intended to occur locally in the browser.

## Previously reported as passing on Android (not re-run in this session)
- [x] Select image(s) — REPORTED PASS
- [x] JPG compression — REPORTED PASS
- [x] Individual download — REPORTED PASS
- [x] Multiple image selection — REPORTED PASS
- [x] ZIP download — REPORTED PASS
- [x] ZIP extraction — REPORTED PASS
- [x] PNG output created, extracted, and opened — REPORTED PASS

## Functional QA matrix

### Upload and input validation
- [ ] Select one supported image
- [ ] Select multiple supported images
- [ ] Drag-and-drop supported image(s)
- [ ] Unsupported file type is rejected with a clear message
- [ ] Zero-byte/corrupt image handled safely
- [ ] File larger than 30 MB rejected with clear message
- [ ] Exactly 30 MB boundary checked
- [ ] Image above 30 MP rejected or safely handled per UI messaging
- [ ] Duplicate filenames handled without overwriting
- [ ] Batch above 20 images rejected/limited with clear message
- [ ] Clear/remove selected files works
- [ ] Cancel file picker leaves state unchanged

### Format conversion and output integrity
- [ ] JPG → JPG compression: output opens and is smaller or explains no reduction
- [ ] JPG → PNG: output opens and visual content matches source
- [ ] PNG → PNG: output opens; transparency preserved
- [ ] PNG → JPG: output opens; transparent areas become expected white background
- [ ] WebP → WebP: output opens and visual content matches
- [ ] WebP → JPG: output opens and visual content matches
- [ ] WebP → PNG: output opens and visual content matches (if selectable)
- [ ] Output extension matches actual MIME/format
- [ ] Output file has non-zero size
- [ ] Output dimensions are correct when resize is not enabled
- [ ] Output dimensions are correct when resize is enabled
- [ ] EXIF orientation is respected for portrait photos
- [ ] Quality setting changes output size/quality as expected
- [ ] Target-size mode converges or reports failure clearly
- [ ] Repeated compression does not crash or freeze

### Preview and result UI
- [ ] Original preview renders
- [ ] Compressed preview renders
- [ ] Preview updates after settings change/reprocessing
- [ ] Broken preview/error state is clear and recoverable
- [ ] File names, sizes, dimensions, and statuses are accurate
- [ ] Progress updates during processing
- [ ] Success state is shown only after output is ready
- [ ] Failure state identifies failed file(s)
- [ ] Retry failed file works
- [ ] Retry-all works and progress remains accurate
- [ ] Reset/clear returns UI to initial state

### Batch, download, and ZIP
- [ ] 2-image batch completes
- [ ] 10-image batch completes
- [ ] 20-image maximum batch completes (stress test)
- [ ] Mixed JPG/PNG/WebP batch
- [ ] Batch with one invalid file handles partial failure correctly
- [ ] Individual download works for each successful output
- [ ] ZIP contains all successful outputs and no unexpected files
- [ ] ZIP filenames are unique and correct
- [ ] ZIP opens/extracts with a standard archive tool
- [ ] ZIP download can be retried after failure

### Error handling and resilience
- [ ] Processing error does not crash remaining files
- [ ] Browser tab remains responsive during large batch
- [ ] Cancel/stop behavior tested if available
- [ ] Refresh during processing behavior is understood
- [ ] No uncaught JavaScript errors during test flows
- [ ] Memory usage returns to reasonable level after clearing results

## Device/browser coverage
- [ ] Android Chrome
- [ ] Android Firefox or another browser
- [ ] iOS Safari
- [ ] Desktop Chrome
- [ ] Desktop Firefox
- [ ] Desktop Edge
- [ ] Small viewport (320–375 px)
- [ ] Tablet viewport
- [ ] Desktop viewport
- [ ] Landscape orientation

## QA evidence log
| Date | Test | Device/browser | Input | Expected | Actual | Status | Evidence/notes |
|---|---|---|---|---|---|---|
| Earlier user report | Basic selection/JPG/download/ZIP | Android (details not recorded) | Not recorded | Works | REPORTED PASS | Prior user-reported results; not independently re-run |

## Known unresolved items from previous QA notes
- Preview rendering issue was previously observed; needs reproduction and verification.
- JPG-to-PNG content validity needs checking.
- PNG-to-JPG conversion needs checking.
- WebP output/conversion needs checking.
- Batch test sizes must stay within the app's 20-image limit.
- Large-image handling, memory behavior, quality comparison, and desktop testing remain unverified.
