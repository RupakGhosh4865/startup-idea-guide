# Billu Bhaiya guides: how to publish

Instructions for anyone (person or AI assistant) adding a guide to this repo.

## Two repos

| Repo | Holds | Visibility |
|---|---|---|
| `RupakGhosh4865/startup-idea-guide` (this one, GitHub Pages) | each guide's `index.html` + `pages/page-NN.jpg` | public |
| `RupakGhosh4865/startup-idea-guide-pdfs` (local: `../startup-idea-guide-pdfs`) | the PDFs, in a folder with the **same name** as the guide folder | **private** |

upaaylabs.com finds a guide by itself when the public repo has `<folder>/index.html` **and** `<folder>/pages/page-01.jpg`, and the private repo has `<folder>/<anything>.pdf`. The new guide appears first on upaaylabs.com/learn and in the site's announcement bar within about 5 minutes. No website change is needed.

Readers get a PDF only from upaaylabs.com, after confirming their email. So:

- **Never put a PDF in this repo.** `.gitignore` blocks `*.pdf`; don't remove that rule.
- **Every PDF button links to `https://upaaylabs.com/learn/<folder>.pdf`**, never to a `.pdf` file here.

## Publish a new guide

1. **Folder name** (`<folder>`): lowercase words joined by hyphens, e.g. `backend-stack`. It becomes the permanent link `upaaylabs.com/learn/<folder>`, so never rename it after publishing.
2. **Page** `<folder>/index.html`: copy `frontend-stack/index.html` and change the content. Keep:
   - `<title><Guide title> · Billu Bhaiya</title>` (the site drops " · Billu Bhaiya" for the card title)
   - `<meta name="description" content="Billu Bhaiya ka free <topic> guide: <one-line summary>" />` (the site drops the "Billu Bhaiya ka free … guide:" part for the card's one-liner; keep the summary under ~120 characters)
   - optional `<meta name="upaay:date" content="YYYY-MM-DD" />` (without it, the date of the first push decides "newest")
   - the back link: `<a class="back" href="https://upaaylabs.com/learn">← Saare guides</a>`
   - the top buttons, with `<folder>` replaced:
     ```html
     <!-- PDF buttons go through https://upaaylabs.com/learn/<folder>.pdf (free, email popup). For a new guide, change <folder>. -->
     <div class="btns">
       <a class="btn primary" href="https://upaaylabs.com/learn/<folder>.pdf">⬇ Download PDF</a>
       <a class="btn" href="https://upaaylabs.com/learn/<folder>.pdf?view=1" target="_blank" rel="noopener">Open PDF</a>
       <a class="btn" href="https://upaaylabs.com/learn#quiz">🏆 Free quiz khelo</a>
     </div>
     ```
   - the bottom button `<a class="btn primary" href="https://upaaylabs.com/learn/<folder>.pdf">⬇ Download PDF</a>`
   - the footer's "Saare guides" link to `https://upaaylabs.com/learn`
   - no "View on GitHub" button. Check that every match of `grep -n '\.pdf' <folder>/index.html` is an upaaylabs.com link.
3. **Images** `<folder>/pages/page-01.jpg` (the cover, required) … `page-NN.jpg`, 720×1280, with alt text.
4. **README.md**: add the cover to the cover strip, a row in the "📄 Guides" table with `[Free PDF](https://upaaylabs.com/learn/<folder>.pdf)` and `[Read online](https://rupakghosh4865.github.io/startup-idea-guide/<folder>/)`, and a numbered section like the others. No direct `.pdf` links.
5. **PDF** to `../startup-idea-guide-pdfs/<folder>/<File-Name>.pdf` (`git pull` there first). Then check the private repo is still hidden: `curl.exe -s -o NUL -w "%{http_code}" https://api.github.com/repos/RupakGhosh4865/startup-idea-guide-pdfs` must print `404`.
6. **Push** the private repo first ("Add <title> PDF"), then this repo ("Add <title> guide (landing page)").
7. **Check** after about 5 minutes:
   - `https://rupakghosh4865.github.io/startup-idea-guide/<folder>/` shows the page.
   - `https://upaaylabs.com/api/guides.json` shows `"latest"` = the new folder and `"pdfs"` with `"public":0`.
   - In a private window, `https://upaaylabs.com/learn/<folder>.pdf` opens the email popup on upaaylabs.com/learn.
8. **Quiz**: upaaylabs.com/admin → Quiz → "Write quiz" next to the guide → Copy prompt → claude.ai with the PDF → paste the answer → Fill the form → Save & make live.

## Never

- Commit a `.pdf` here, or make `startup-idea-guide-pdfs` public.
- Rename or delete a published guide folder, or change another guide's links.
- Put tokens or passwords in either repo.
