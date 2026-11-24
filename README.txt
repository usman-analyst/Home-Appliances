HomeFix Fixed Production Build
==============================
Deploy all files in this archive directly to your Vercel project root
(keep index.html, vercel.json, and assets/ together).

Key fixes in this build:
1. Eliminates render-blocking CSS by inlining deduplicated, minified styles in index.html.
2. Fixes NO_LCP / TBT errors by scoping hero image preload to desktop (min-width: 801px)
   and deferring Meta Pixel + Microsoft Clarity external script loading until window load
   or first user interaction (preserving full PageView & session tracking).
3. Adds exact responsive WebP breakpoints (240w/360w/480w/640w for covers, 320w/480w/640w/800w
   for bundle preview, 360w for hero/AI Fixer/certificate) while preserving visual sharpness
   and keeping 64x64 customer avatars byte-for-byte original.
4. Fixes WCAG AA contrast issues (.disclaimer -> #4f5d70, .priceBonusFlag -> #076e59).
5. Configures 1-year immutable Cache-Control headers for /assets/* in vercel.json.
