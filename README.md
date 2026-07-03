# Resume — [cv.shrd.in](https://cv.shrd.in)

Resume of Sharad Shinde, HTML-first: the web page **is** the resume, and everything else is generated from or mirrors it. Zero dependencies, no build step, no third parties, ~25 lines of JS.

| File | What it is |
|------|-----------|
| `index.html` | The resume — semantic HTML, schema.org `Person` JSON-LD, light/dark theme (follows system, toggle persisted), compact print CSS |
| `Resume.pdf` | Generated from the page via print CSS — simple text-based 2-page PDF, ATS-friendly |
| `resume.json` | Machine-readable mirror per the [JSON Resume](https://jsonresume.org/) v1.0.0 standard, linked via `rel=alternate` |
| `og.png` | 1200×630 card for link previews |
| `Sharad-Shinde.vcf` | Downloadable contact card ("Save contact" on the page) |
| `robots.txt` / `404.html` | Standard web hygiene |

## Update the resume

1. Edit the content in `index.html` (and mirror the change in `resume.json`)
2. Bump the "Last updated" stamp in `index.html` and `meta.lastModified` in `resume.json`
3. Regenerate the PDF:
   ```sh
   "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
     --headless --disable-gpu --no-pdf-header-footer \
     --print-to-pdf=Resume.pdf "file://$PWD/index.html"
   ```
   (or just open the page and Print → Save as PDF)
4. Push
