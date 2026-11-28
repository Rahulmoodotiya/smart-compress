# SmartCompress

SmartCompress is a free, browser-based image compression, resizing, and conversion tool. It is a static single-page application—no build step or image-upload backend is required.

## Live site

https://smart-compress.pages.dev/

## Features

- Compress JPG, PNG, and WebP images in your browser
- Batch processing (up to 20 images per batch)
- Convert between JPG, PNG, and WebP, or retain the original format with Auto
- Adjustable quality for lossy formats
- Resize using presets or custom width and height
- Keep aspect ratio or use exact dimensions
- Optional target file size for supported lossy formats
- Before/after preview and size/savings information
- Download images individually or as a ZIP
- Retry failed items and batch progress/cancellation controls
- EXIF orientation handling
- Input/output safety limits and error messages

## Privacy

Images are processed locally in the browser. The app does not upload selected image files to a compression server.

## Limits

- Maximum 20 images per batch
- Maximum input file size: 30 MB per image
- Maximum input dimensions: 30 megapixels
- Maximum output dimensions: 12,000 pixels per side and 50 megapixels
- ZIP generation is limited for browser memory safety; very large results should be downloaded individually

## Supported formats

- Input: JPG/JPEG, PNG, WebP
- Output: JPG, PNG, WebP, or Auto/original

Note: JPG output does not preserve transparency; transparent areas are flattened against white. PNG is lossless and its quality slider does not reduce file size. Target-size control is supported for lossy JPG/WebP output, but a requested size may not always be achievable.

## Run locally

Open `index.html` in a modern browser. The app uses browser Canvas and Blob APIs.

## Deployment

The repository is configured as a static-site project and is deployed using Cloudflare Pages. See [CLOUDFLARE_DEPLOY.md](CLOUDFLARE_DEPLOY.md) for deployment details.

## Testing

The code includes safeguards and status messages, but this README does not claim exhaustive cross-browser/device testing. Please see [TESTING.md](TESTING.md) for the current testing notes and checklist.

## Repository

- `index.html` — app and interface
- `robots.txt` — crawler rules
- `sitemap.xml` — sitemap
- `TESTING.md` — test notes
- `CLOUDFLARE_DEPLOY.md` — deployment notes
- `CHANGELOG.md` — changes
