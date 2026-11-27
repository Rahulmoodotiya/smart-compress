# SmartCompress

A lightweight, browser-based image compression prototype. The current build is a static single-page app and requires no build step or backend.

## Features in this prototype
- Select multiple JPG, PNG, and WebP images
- Browser-side compression
- Output format selector: JPG, PNG, WebP, or Auto/original format
- Compression quality control (primarily applies to lossy JPG/WebP output)
- Individual downloads
- Batch ZIP download
- Before/after preview and file-size savings display

## Run locally
Open `index.html` in a modern browser. For best compatibility, use a browser that supports Canvas and Blob downloads.

## Privacy
Image processing is intended to run locally in the browser. This prototype does not include an image-upload backend.

## Status
Prototype—not production-ready. The owner has manually tested image selection, JPG compression, individual download, ZIP download, ZIP extraction, and PNG output on Android. More testing is required for conversion correctness across formats, preview rendering, large files, and large batches.

## Repository
This repository is intended to be deployed as a static site (for example, GitHub Pages or Cloudflare Pages) after further testing.
