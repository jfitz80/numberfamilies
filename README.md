# Number Families support website

A standalone, parent-facing static website for the Number Families iPhone and iPad app. The site uses only HTML and CSS, with no frameworks, JavaScript, external fonts, trackers, cookies, or analytics. Branding and content are exclusively for Number Families.

## Files

- `index.html` — app introduction and links.
- `support.html` — getting started, purchases, sound, progress, and contact guidance.
- `privacy.html` — **draft** privacy policy, effective September 28, 2026.
- `styles.css` — shared responsive styling.

## Before publishing

1. Replace `YOUR_SUPPORT_EMAIL` in both HTML pages with your working support email. It is intentionally plain text rather than a broken mail link. Once replaced, optionally make it a `mailto:` link.
2. **Complete the iOS implementation privacy audit.** This repository contains Number Families workbook materials and an unrelated project, but no discoverable Swift/Objective-C sources, Xcode project, app privacy manifest, entitlements, or iOS dependency manifest. Searches for analytics, crash reporting, cloud synchronization, third-party SDKs, network calls, and local storage in relevant Number Families files found no app implementation to inspect. That is not evidence that the app has no data collection. No implementation conflict could be established or ruled out.
3. Review the actual Xcode app, package dependencies, privacy manifests, entitlements, analytics/crash services, CloudKit/iCloud or other sync, network requests, purchase handling, and any collected identifiers or data. Verify each policy statement, including local-only storage, against that implementation. Report conflicts and resolve the policy with the developer rather than silently rewriting the requested claims. Remove the visible draft notice only after verification.
4. Confirm the support instructions and commercial statements match the released app. The policy is not publication-ready until the audit and email replacement are complete.

## Publish with GitHub Pages

After completing the checks above and pushing these files to `main`:

1. Open the GitHub repository **Settings**.
2. Select **Pages**.
3. Under **Source**, select **Deploy from a branch**.
4. Select branch **main**.
5. Select folder **/(root)**.
6. Click **Save**.

GitHub will display the published URL after deployment. Use `support.html` at that URL for the App Store support URL and `privacy.html` for the privacy policy URL. Relative links work with GitHub Pages repository subpaths.

This workspace also contains unrelated workbook/project folders. Prefer a dedicated website repository containing just the five site files before enabling root publishing, so those other materials are not published alongside the site. No deployment has been performed by this task.

## Preview and checks

Open `index.html` directly in a browser, or run `python3 -m http.server 8000` from this folder and visit `http://localhost:8000`.

Check Home, Support, and Privacy Policy links in the header and footer, the home-page buttons, keyboard focus, the skip link, and narrow layouts (320px and 375px). Also check enlarged text. The CSS uses responsive grids, wrapping navigation, system fonts, and no fixed content heights.
