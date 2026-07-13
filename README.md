# Robin Engineering Hub — Portfolio

Single-file website (`index.html`) plus a small `documents.json` file for
self-managed downloads. No build tools needed.

## 1. Deploy for free (one time)

1. Create a GitHub account: https://github.com/signup
2. Create a new **public** repository, e.g. `robin-engineering-hub`.
3. Upload every file from this folder — `index.html`, `documents.json`,
   `robots.txt`, `sitemap.xml`, `images/`, `assets/` — using "Add file →
   Upload files" on github.com.
4. Go to **Settings → Pages** → Source: **Deploy from a branch**, branch
   `main`, folder `/ (root)` → Save.
5. Your site goes live in 1–2 minutes at:
   `https://<your-username>.github.io/robin-engineering-hub/`
6. Open `robots.txt` and `sitemap.xml` in the repo and replace
   `YOUR-USERNAME` and `YOUR-REPO` with your real GitHub username and
   repository name, so they point at the real URL.

## 2. Get found on Google

1. Go to https://search.google.com/search-console and add your site URL
   (the github.io link from step 5 above).
2. Submit your `sitemap.xml` URL there
   (e.g. `https://<your-username>.github.io/robin-engineering-hub/sitemap.xml`).
3. Google typically indexes a new page within a few days to a few weeks —
   there's no way to guarantee an exact time.

## 3. Add a document yourself — no coding

Documents are organized by expertise category, matching the items inside
the Line Protection / Transformer Protection folders on the site. Each
category already has its own folder under `assets/documents/`:

```
assets/documents/
  Line Protection:
    L87/      → Line Differential Protection
    L21/      → Line Distance Protection
    SOTF/     → Switch-on-to-Fault Protection
    PSB/      → Power Swing Block Protection
    VTFF/     → VT Fuse Failure Protection
    L5051/    → Overcurrent Protection
    L50N51N/  → Earth Fault Protection
    L79/      → Auto-Reclose
    BCD/      → Broken Conductor Protection
    CS85/     → Carrier Scheme Protection
    STUB/     → Stub Protection
    L59/      → Over Voltage Protection
    L27/      → Under Voltage Protection

  Transformer Protection:
    87T/      → Transformer Differential Protection
    REF/      → Transformer REF Protection
    49/       → Thermal Overload Protection
    24/       → Over Flux Protection
    46/       → Negative Sequence Protection
    OCEF/     → Overcurrent & Earth Fault Protection
```

To add a PDF:

1. On github.com, open `assets/documents/<category>/` (e.g. `L87/`) and
   **Add file → Upload files** with your PDF.
2. Open `documents.json`, click the pencil (✏️) to edit, and add an entry
   with the matching `category`:

```json
[
  {
    "category": "L87",
    "title": "Line Differential Protection (87L) Notes",
    "file": "assets/documents/L87/notes.pdf",
    "date": "2026-07"
  }
]
```

   Add a comma after `}` for each extra document — they can be in the
   same category or different ones; the website groups and labels them
   automatically.
3. Click **Commit changes**. The Documents section on the site updates
   automatically, grouped under the right heading — nothing else to
   touch.

## 4. Add your photo / company logo

- Upload a photo as `images/profile.jpg` and a logo as `images/logo.png`
  (same file names the page already expects) — they'll appear
  automatically once uploaded. If they're missing, the page just shows a
  clean fallback, so nothing breaks in the meantime.

---

## বাংলায় সংক্ষেপে

- **Live করা:** GitHub-এ একটা public repository বানিয়ে সব ফাইল আপলোড
  করুন, তারপর Settings → Pages থেকে on করে দিন (ধাপ ১ দেখুন)।
- **Google-এ পাওয়া যাওয়া:** Live হওয়ার পর Google Search Console-এ site
  ও sitemap.xml submit করুন (ধাপ ২)। সময় লাগতে পারে কয়েক দিন থেকে কয়েক
  সপ্তাহ।
- **File/Document যোগ করা:** `assets/documents/` এর ভেতরে প্রতিটা
  subject-এর জন্য আলাদা ফোল্ডার আছে (87T, REF, 5051, 67, 21, 2759, 86,
  RC, ETAP)। সংশ্লিষ্ট ফোল্ডারে PDF আপলোড করুন, তারপর `documents.json`-এ
  category/title/file/date লিখে দিন — website নিজে থেকেই সঠিক subject-এর
  নিচে গুছিয়ে দেখাবে। কোনো কোডিং লাগবে না।
- **ছবি/লোগো:** `images/profile.jpg` আর `images/logo.png` নামে ফাইল
  আপলোড করলেই স্বয়ংক্রিয়ভাবে দেখাবে।
