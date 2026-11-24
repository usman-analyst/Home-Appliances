HomeFix performance optimization build
======================================

Deploy the contents of this folder to the Vercel project root. Keep index.html,
vercel.json, and the assets/ folder together. The HTML references content-hashed
WebP assets, optimized CSS, and optimized first-party JavaScript in assets/.

What this build changes:
- Resizes and recompresses every first-party page image into responsive WebP sizes.
- Adds srcset/sizes to hero, eBook covers, sample pages, certificate, and AI preview.
- Adds explicit dimensions and async decoding to all image elements.
- Prioritizes and preloads the hero/LCP candidate.
- Removes obsolete CSS selectors that do not match current markup, minifies CSS,
  and moves it to a content-hashed stylesheet.
- Moves custom modal/carousel JavaScript to a content-hashed deferred file.
- Reworks the review carousel to use IntersectionObserver instead of repeated
  offsetLeft geometry reads that can trigger forced reflow.
- Adjusts low-contrast text colors identified by the PageSpeed accessibility audit.
- Adds long immutable caching for content-hashed first-party assets and revalidation
  for index.html.

Important limitation:
Meta Pixel and Microsoft Clarity remain enabled to preserve your tracking. Their
cache TTL and legacy JavaScript are served by Meta/Microsoft and cannot be changed
by this site. Removing those external scripts (or replacing the analytics setup)
would be required to eliminate those specific third-party audit warnings.

Validation performed:
See QA_REPORT.txt. This build was statically validated and asset/image references
were checked. The available Chromium runtime blocked local navigation with
ERR_BLOCKED_BY_ADMINISTRATOR, and the live site could not be opened by the web
inspection environment. Therefore no honest claim of a live Lighthouse/PageSpeed
retest or full browser interaction test is made. Deploy this build and rerun
PageSpeed Insights to verify runtime metrics and third-party audits.
