# VeloQuote frontend

A portable, dependency-free rebuild of the public VeloQuote marketing page, reviewed September 17, 2026. This is a source-code deliverable, not a deployed site or a rebuild of the lending application.

## Preview

Unzip this folder and open `index.html` in a browser. No installation or build is required. Alternatively, from this folder run `python3 -m http.server 8000` and visit `http://localhost:8000`.

## Edit

- `index.html`: page text, section ordering, links, and FAQ answers.
- `styles.css`: branding, typography, spacing, desktop and mobile layouts.
- `app.js`: accessible mobile menu behavior. FAQs use native HTML details and work without JavaScript.
- `assets/`: locally bundled source-site imagery and font.

All paths are relative, so the page can be served at a domain root or a subdirectory. No React, Node server, database, Framer subscription, API key, or compilation is needed for production.

## Hosting handoff

Upload `index.html`, `styles.css`, `app.js`, and the entire `assets` folder together. Keep this README and review notes out of the public web root.

- **AWS:** suitable for static hosting, for example a private S3 origin behind CloudFront with HTTPS. Use `index.html` as the default root object. No application server is required. Configure the actual account, domain, TLS, and cache behavior when the hosting choice is finalized.
- **GoDaddy:** suitable for a hosting plan that permits uploading ordinary HTML/CSS/JavaScript files, such as cPanel web hosting. Upload into the configured document root, commonly `public_html`. Owning a GoDaddy domain alone does not include file hosting; Website Builder is a separate product.

No AWS or GoDaddy resources have been created, and the current website/DNS has not been changed.

## Rebuild notes and launch review

- Preserves the original blue/yellow identity, building hero, brand mark, feature imagery, major sections, public product positioning, and existing Calendly/Airtable/privacy destinations. Layout is reimplemented and responsive, not a pixel-perfect Framer export.
- The wordmark is accessible styled text beside the original logo mark. Manrope is bundled locally when available; Arial is the fallback.
- Retains the healthcare beta qualification and the two Coming Soon features from the current page.
- Retains the original 3x, 80%, and 95%+ marketing figures and the encryption claim. These were copied from the source website, not independently verified. Confirm the evidence and current accuracy before launch.
- The source Terms & Condition link points back to the homepage. It is intentionally omitted from this rebuild until approved terms and a real destination are supplied. No legal text has been fabricated.
- The source contains an obsolete Lemon Squeezy template contact destination in an alternate layout. All rebuilt contact buttons use the existing VeloQuote Calendly URL instead.
- The original security Read more labels have no useful destination exposed in the page. The rebuilt security action invites visitors to ask the team through the existing booking link; it does not invent a security policy.
- Only the first FAQ answer was available in the retrieved page content. The remaining four answers are new draft copy based on the page's visible feature descriptions, with onboarding referred to the team rather than an invented timeline. Review them before launch.
- Original analytics and Framer tracking scripts are not copied. Add the approved analytics and consent setup separately if needed.
- Calendly, Airtable, and the Google Drive privacy document remain external destinations. The frontend has no form submissions, upload handling, login, data extraction, or loan sizing backend.

## Validation

JavaScript syntax, HTML nesting, unique IDs, anchor targets, and local HTML/CSS asset references were checked. All site images were downloaded from the current website. Desktop/mobile CSS and no-JavaScript navigation paths are implemented. A live browser preview of the rebuilt static package was unavailable in this environment, so visual layout and interaction testing on real desktop and mobile browsers remains required before launch. The original site was visually inspected in a browser.

## Source assets

Original assets were retrieved from `https://veloquote.com` and its linked Framer image CDN for this requested rebuild. Retain the necessary rights to your original imagery and brand assets. Asset source URLs are recorded in `asset-sources.json`. Manrope is an open-source font distributed under the SIL Open Font License; its license is included if downloaded successfully.
