# Webflow Integration — 紅字，然後呢？

You've been asked to integrate this landing page into ĒSEN's existing Webflow site. The page is already designed, built, and tested as a static HTML page. Your job is to embed it into Webflow so it lives at `esenclinic.com/no-more-red` (or wherever the team decides).

**Total estimated time:** 45-60 minutes if you're comfortable with Webflow Custom Code; 90 minutes if it's your first time using Embed elements.

---

## What's in this folder

```
webflow-export/
├── README.md                  ← You are here
├── styles.css                 ← Upload to a static host (see Step 2)
├── head-custom-code.html      ← Paste into Webflow Page Settings → Head
├── embed-1.html               ← Webflow Embed element #1 (7,845 chars)
├── embed-2.html               ← Webflow Embed element #2 (6,419 chars)
└── body.html                  ← The full HTML body (for reference only)
```

---

## Prerequisites

- ĒSEN's Webflow site is on **CMS plan or higher** (required — Starter blocks Custom Code)
- You have **Designer access** (Editor access alone won't work)
- You have access to a **static file host** for the CSS and images. The simplest option: a Netlify account (free tier is fine).

---

## Architecture overview

This is a hybrid setup:

- **The page URL** lives on Webflow (`esenclinic.com/no-more-red`)
- **The CSS and image assets** live on Netlify (or another static host)
- **The HTML body** sits inside Webflow Embed elements that reference the Netlify-hosted CSS and images

Why this approach? The CSS alone is 18,500 characters, and Webflow's Custom Code limit is 10,000 per location. Externalizing the CSS solves that. It also means future style updates can be made by editing one CSS file rather than re-doing Webflow integration.

---

## Step 1: Host the CSS and assets

You have the companion ZIP file `esen-no-more-red.zip` (sent in the same email). That ZIP contains the full static site, including all images, fonts references, and the CSS.

1. Go to [netlify.com](https://netlify.com) and create a free account if you don't have one.
2. From your team dashboard, drag `esen-no-more-red.zip` onto the deployment area. Netlify will give you a URL like `https://thoughtful-marshmallow-abc123.netlify.app`.
3. **Save this URL** — you'll use it everywhere in the next steps.
4. Confirm it works: visit `https://[your-netlify-url]/styles.css` in a browser. You should see CSS code (not 404).
5. Also confirm: `https://[your-netlify-url]/assets/og-image.jpg` should display the Rose laughing photo.

---

## Step 2: Find-and-replace the Netlify URL

Three files in this folder use a placeholder for the Netlify URL. Open each in a text editor and find/replace:

- Find: `YOUR-NETLIFY-SITE.netlify.app`
- Replace: your actual Netlify domain (e.g., `thoughtful-marshmallow-abc123.netlify.app`)

Files to update:
- `head-custom-code.html`
- `embed-1.html`
- `embed-2.html`

---

## Step 3: Create the page in Webflow

1. Open the ĒSEN Webflow project in Designer
2. Pages panel → + → **Static Page**
3. Name: `No More Red`
4. URL slug: `no-more-red`

---

## Step 4: Configure Page Settings

Open the page's Settings panel:

**SEO Settings:**
- **Title Tag:** `紅字，然後呢？｜ĒSEN Clinic`
- **Meta Description:** `你的報告沒問題，不代表你的身體沒問題。Rose 鄒開蓮的健康優化故事，與一場 30 分鐘的諮詢起點。`

**Open Graph Settings:**
- **OG Title:** `紅字，然後呢？｜ĒSEN Clinic`
- **OG Description:** (same as meta description)
- **OG Image:** Upload via the `og-image.jpg` from the assets folder, OR paste this URL: `https://[your-netlify-url]/assets/og-image.jpg`

**Custom Code → Inside `<head>` tag:**
Paste the entire contents of `head-custom-code.html` (after you've done the find/replace).

---

## Step 5: Build the page body

In Designer, on your new page:

1. **Delete the default Section** that Webflow auto-generates at the top.
2. **Set the page Body background** to `#7a1d27` (Webflow → Body tag → Background Color).
3. **Add two HTML Embed elements**, stacked vertically:
   - Add elements panel → Components → **Embed**
   - Paste `embed-1.html` contents into the first
   - Add a second Embed below it → paste `embed-2.html` contents

Save. Preview. The page should render identically to the standalone version.

---

## Step 6: Test thoroughly before publishing

Publish to staging first. Test:

- [ ] Page loads at the staging URL
- [ ] All images load (check Network tab in DevTools — should all be 200 OK, no 404s)
- [ ] Video plays inline (YouTube embed should work)
- [ ] CTA "點擊預約「消滅紅字」諮詢門診" opens Beautinq booking in a new tab
- [ ] Mobile layout looks correct (use Chrome DevTools device emulator)
- [ ] **Critical test:** share the staging URL in a LINE chat. Preview card must show the Rose laughing photo and the article title.
- [ ] **Critical test:** open the staging URL inside LINE's in-app browser, tap the CTA. Confirm it opens Beautinq in Safari/Chrome (not stuck inside LINE).

Once all checks pass, publish to production.

---

## Common issues & fixes

**Blank page in preview.**
The CSS isn't loading. Check DevTools → Network → look for `styles.css`. If 404, the URL in head-custom-code.html is wrong, or you haven't deployed `esen-no-more-red.zip` to Netlify yet.

**Page renders but fonts look wrong.**
Webflow may be injecting its own font-family on the body. In Designer → Body tag → Typography, set font to "Inherit" or clear any default font.

**Webflow's nav/footer appears on the page.**
If ĒSEN's site has global nav/footer via Webflow Symbols, this page will inherit them. Decide with the team whether to keep or remove. To remove on this page only: use Webflow's "Disable on this page" toggle on the Symbol.

**Video shows "Video unavailable".**
Not a Webflow issue. The YouTube video must be: Unlisted or Public (not Private), Allow Embedding checked, Not Made for Kids.

**One Embed shows but the other doesn't render.**
You may have pasted the HTML wrapped in `<html>` or `<body>` tags by mistake. Each embed file should start directly with a `<!-- =====` comment or an HTML element like `<div>` or `<section>`. No wrapper.

---

## How to update text later

**Small text edits (typos, dates, etc.):** edit the relevant Embed element's HTML directly in Webflow Designer.

**Style edits (colors, spacing, typography):** edit `styles.css` on Netlify. Webflow picks up changes automatically — no re-deploy needed.

**Image swaps:** upload to Netlify's `assets/` folder. Keep filenames the same for zero Webflow changes.

**Video swap:** find the `<iframe>` in `embed-1.html`, change the 11-character video ID after `youtube.com/embed/`, paste updated HTML into Webflow Embed.

---

## Questions?

If something doesn't work or you hit a Webflow-specific issue not covered here, contact the person who sent you this package. They've been working on this for several weeks and know the page intimately.
