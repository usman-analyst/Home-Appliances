HomeFix Fixed Optimization Build (v2) - Vercel Deployment Guide
===============================================================

1. Unzip this archive and deploy index.html, vercel.json, and the assets/ folder to your
   Vercel project root.
2. Verify in browser DevTools Network tab:
   - 0 render-blocking CSS/JS requests
   - Mobile (412px) loads six-ebook-bundle-416.*.webp (~24 KiB) and 320w eBook covers (~18-22 KiB)
   - Meta Pixel PageView and Microsoft Clarity fire cleanly without CSP console errors
3. Re-run PageSpeed Insights (Mobile) on https://homeappliances-omega.vercel.app/
