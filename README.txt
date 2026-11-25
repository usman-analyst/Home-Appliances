HomeFix Telugu Landing Page
===========================

Files:
- index.html: landing page
- assets/: all image assets used by the page, including the technician hero, ebook covers,
  certificate, bundle image, and six clean circular customer profile photos.

How to preview:
1. Keep index.html and the assets folder together.
2. Open index.html in Chrome or another modern browser.

How to publish:
Upload both index.html and the entire assets folder to the same hosting directory.
Do not rename or separate the assets folder.

Purchase buttons point to:
https://superprofile.bio/vp/telugu-repair-course

Optimised version notes
- Images are WebP (with JPG/PNG fallback) in several sizes; originals were removed.
- Meta Pixel and Microsoft Clarity load on first scroll/tap/key press, or 1.5s after page load.
- vercel.json sets long cache headers for /assets and basic security headers.
  If you replace an image, give it a NEW file name (assets are cached for 1 year).

Sample pages (Sample పేజీలు) - currently switched OFF
- The buttons, pop-up and script are already in index.html, but hidden because the 24 sample-page
  image files are not in assets/ yet.
- To turn them on: add the 24 images (names are listed in index.html, e.g.
  assets/01-1-ac-repairing-768.018259ce51.webp), then change  data-samples="off"  to  data-samples="on"
  in the first line of index.html (<html data-samples="off" ...>).
- Sample పేజీలు: each eBook card has a button that opens a pop-up with that eBook's 2 real Telugu pages
  (assets/01-1-... to 06-2-...). Do not rename these files.
