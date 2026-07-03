# Resume — [cv.shrd.in](https://cv.shrd.in)

Resume of Sharad Shinde, served as a single static page.

- `Resume.pdf` — the resume itself (source of truth)
- `resume-page-*.webp` — pre-rendered page images, shown on small screens where inline PDFs are unreliable
- `index.html` — dark-themed viewer shell matching [shrd.in](https://shrd.in): native browser PDF rendering on desktop, page images on mobile. No JS, no build step, no third parties.

## Update the resume

1. Replace `Resume.pdf`
2. Regenerate the page images (any PDF-to-image tool works, ~2.2× scale, webp):
   ```sh
   npx -y pdf-to-img # or: pdftoppm -png -r 160 Resume.pdf resume-page
   ```
3. If the page count changed, update the `<img>` tags in `index.html`
4. Push
