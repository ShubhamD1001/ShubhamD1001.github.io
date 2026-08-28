# Shubham Dhyani — Business Analyst Portfolio

A single-file portfolio site. Everything lives in `index.html`; images and your CV live in folders next to it.

---

## 1. Folder structure

Create these folders next to `index.html` (they must exist before you push):

```
shubham-portfolio/
├── index.html
├── README.md
├── assets/
│   ├── Shubham_Dhyani_Resume.pdf     ← your CV (exact filename matters)
│   └── ai-ethics-paper.pdf           ← optional
└── images/
    ├── profile.jpg                   ← headshot, square, ~600×600px
    ├── certificates/
    ├── projects/
    └── proof/
```

If an image is missing, the site shows a striped box with the filename it's looking for — nothing breaks, and you'll see exactly what to add.

---

## 2. What's already in place

The `images/` folder already contains **28 certificates**, **2 internship certificates**, and your **headshot** — all extracted from the ZIP you sent, compressed, and named. Nothing to do there.

Only two image slots are still empty:

| File | What to put there |
|---|---|
| `images/projects/lead-scoring.png` | Screenshot from your lead-scoring notebook — the ROC curve or score distribution |
| `images/projects/safety-stock.png` | Screenshot of the supplier risk matrix in Tableau or Power BI |

The capital-structure project loads its preview straight from your GitHub repo, so it already displays.

**Tips:** JPG for scans, PNG for screenshots. Keep each under 500 KB — [squoosh.app](https://squoosh.app) compresses in-browser.

---

## 3. What you must fill in before publishing

Search `index.html` for **`needs-input`**. Only **one** block is left:

**The Kritavin internship bullets.** Company, role and dates are filled in from your certificate — but only you know what you actually worked on. Replace the three `[bracketed]` lines, then delete `needs-input` from the `class="..."` and delete the `<span class="needs-input-tag">` line. The amber dashed border disappears.

That's the last thing standing between this and publishable.

---

## 4. How to edit anything else

Every section is marked with a comment block like `<!-- ══ PROJECTS ══ -->`.

- **Add a certificate** — copy any `<div class="cert-card">…</div>` block, paste it below, change the image filename, title, issuer, date, and `data-cat` (`data`, `ai`, `leadership`, or `research`).
- **Add a project** — copy an `<article class="project-card">…</article>` block and edit it.
- **Add an experience entry** — copy a `<div class="timeline-item">…</div>` block.
- **Change a colour** — everything comes from the `:root` block at the top of the file. Change `--navy-900` or `--gold` and the whole site follows.
- **Change your headline** — it's in the `<!-- HERO -->` section, in `.hero-subtitle`.

---

## 5. Publishing on GitHub Pages

1. Go to github.com → **New repository**
2. Name it **exactly** `ShubhamD1001.github.io` (your username, then `.github.io`) — this gives you the clean URL. Set it **Public**, and create it.
3. Click **uploading an existing file**, then drag in `index.html` and your `images` and `assets` folders. Commit.
4. Go to **Settings → Pages**. Under *Source*, pick **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. Wait 1–2 minutes. Your site is live at **https://shubhamd1001.github.io**

To update later: open the file on GitHub, click the pencil icon, edit, commit. Or drag in a new image to replace an old one. Changes go live in about a minute.

---

## 6. Getting it to show up on Google

Being online doesn't mean being indexed. Do these three things:

1. **Google Search Console** — go to [search.google.com/search-console](https://search.google.com/search-console), add `https://shubhamd1001.github.io` as a URL-prefix property, verify with the HTML tag method (paste the tag into `<head>`), then use **URL Inspection → Request Indexing**. Usually live within a few days.
2. **Link to it from LinkedIn** — add the URL to your LinkedIn profile's Website field and to your featured section. Google follows links, and LinkedIn is a strong signal.
3. **Add it to your resume, email signature, and GitHub bio.**

One caveat: searching your own name may still surface LinkedIn first. That's normal and fine — what matters is that recruiters can open the link you send them.

---

## 7. Before you publish — quick checklist

- [ ] All `needs-input` blocks filled in and their amber styling removed
- [ ] CV saved as `assets/Shubham_Dhyani_Resume.pdf`
- [ ] Headshot at `images/profile.jpg`
- [ ] GitHub repo link added to the lead-scoring project
- [ ] Opened it on your phone to check the layout
- [ ] Clicked every certificate to confirm the image loads
- [ ] Read every claim and confirmed you can defend it in an interview

**No phone number is on the site by design.** Public pages get scraped by spam bots. Email and LinkedIn are enough — add it back only if you want it.
