# Specification

## Summary
**Goal:** Remove all “Premium” branding by regenerating the Petopia logo system, and fix release-blocking image reliability issues by standardizing in-app images to TypeScript imports with consistent fallbacks.

**Planned changes:**
- Create a new Petopia logo system (icon + wordmark) where the only displayed brand text is “Petopia”, and replace all existing logo usages across the app with a single reusable logo component/module.
- Update the favicon to a simplified mark derived from the new logo icon (not a letter) and ensure `frontend/index.html` references the new favicon asset.
- Refactor in-app image usage across content modules and pages/components to use TypeScript-imported assets (replacing hardcoded `"/assets/..."` paths for non-favicon image rendering).
- Add consistent lazy-image loading behavior and a unified fallback/placeholder presentation when images fail to load, avoiding broken-image icons and layout collapse.
- Perform a release-blocking QA sweep to confirm: no “Premium” remains in brand/logo contexts, no broken images across routes (including refresh/direct URL), and Adoption/Product/Service/Blog images load reliably.

**User-visible outcome:** All pages consistently show the Petopia logo (no “Premium” anywhere), the browser tab favicon matches the new icon, and images across listings/detail pages load reliably on navigation and refresh with graceful fallbacks if an image fails.
