# Resume — [cv.shrd.in](https://cv.shrd.in)

Resume of Sharad Shinde, HTML-first: the web page **is** the resume, and the PDF is generated from it via print CSS. Single source of truth, no build step, no third parties.

- `index.html` — the resume: semantic HTML, schema.org `Person` JSON-LD, dark themed on screen, light and compact in print
- `Resume.pdf` — generated artifact for download / job applications (simple text-based PDF, ATS-friendly)

## Update the resume

1. Edit the content in `index.html`
2. Regenerate the PDF:
   ```sh
   "/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
     --headless --disable-gpu --no-pdf-header-footer \
     --print-to-pdf=Resume.pdf "file://$PWD/index.html"
   ```
   (or just open the page and Print → Save as PDF)
3. Push
