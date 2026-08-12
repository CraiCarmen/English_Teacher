# English at A2–B2 Level — Made Easy and Practical!

A one-page website for Carmen Crai's English tutoring: about/CV summary, two downloadable grammar courses (A2 and B2) with PayPal "Buy" buttons, and contact details.

## Files

```
index.html              ← the whole site (single page)
assets/css/style.css    ← styles (gradient-blue theme, matches the course PDFs)
assets/img/             ← favicon + generated gradient banners
courses/
  English_Course_A2.pdf
  English_Course_B2.pdf
```

## How to publish this on github.com/CraiCarmen/English_Teacher

I don't have your GitHub login, so I can't push this for you — but it's a 2-minute copy-paste job:

### Option A — Upload through the browser (easiest, no tools needed)
1. Go to **https://github.com/CraiCarmen/English_Teacher**
2. Click **"Add file" → "Upload files"**.
3. Drag in every file from this folder, **keeping the same folder structure**
   (`index.html` at the root, `assets/...` and `courses/...` as subfolders — GitHub's uploader supports dragging whole folders in most browsers).
4. Scroll down, click **"Commit changes"**.
5. Go to **Settings → Pages** (left sidebar).
6. Under "Build and deployment", set **Source: Deploy from a branch**, **Branch: main / (root)**, then **Save**.
7. After ~1 minute your site is live at:
   **https://craicarmen.github.io/English_Teacher/**

### Option B — Git command line (if you have Git installed)
```bash
git clone https://github.com/CraiCarmen/English_Teacher.git
# copy all files from this folder into the cloned repo folder
cd English_Teacher
git add .
git commit -m "Add English at A2-B2 website"
git push
```
Then enable GitHub Pages as in step 5–6 above.

## Editing later
- **Prices / PayPal**: each course card in `index.html` has a `<form action="https://www.paypal.com/cgi-bin/webscr">` block — edit the `amount` value to change price. `business` is set to `jobcarmen@yahoo.com`, so payments go straight there; no PayPal API keys needed.
- **Text/CV details**: everything in the "About" section is plain HTML in `index.html` — edit directly.
- **Courses**: to update a course, just replace the PDF in `/courses/` with the same filename.

## Notes on the PayPal buttons
These use **PayPal Payments Standard** ("Buy Now" button via `cgi-bin/webscr`) — the simplest option, since it only needs your PayPal email address and works without creating a developer app. Buyers are taken to PayPal to pay, then returned to your site. If you'd like automatic email delivery of the PDF after payment (instead of a manual follow-up), that requires PayPal's paid checkout/IPN integration or a service like Gumroad/Payhip layered on top — happy to help set that up if you want it later.
