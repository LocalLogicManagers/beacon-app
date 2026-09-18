# Beacon

Product/marketing page for Beacon, Local Logic Management's SEO and campaign
command center — keyword rank tracking, on-page SEO audits, a content
calendar, backlink monitoring, campaign/budget tracking, and a social post
scheduler.

Static site, no build step — same pattern as threshold-site/marshal-site:
`index.html` for markup/content, `styles.css` for shared design tokens and
chrome (nav, footer, buttons, rank-check mock). Served via GitHub Pages at
`beacon.locallogicmanagement.com`.

The hero's "rank check" panel and the sample keyword table are both
illustrative — Beacon is in private beta, and real tracking will pull from
Google Search Console and daily SERP checks once a site is connected. The
signup form has no backend wired yet; it opens a `mailto:` draft to
hello@locallogicmanagement.com. Swap in a real endpoint (Formspree,
ConvertKit, Mailchimp, etc.) before launch.

## Deploy it (same pattern as Kronos / Threshold / Warden / Marshal)

1. Create a new GitHub repo in the `LocalLogicManagers` org — e.g. `beacon-app`.
2. Push `index.html`, `styles.css`, and `CNAME` (already set to
   `beacon.locallogicmanagement.com`) to the repo's default branch.
3. In the repo's Settings → Pages, set the source to that branch (root).
4. In Wix DNS (where the domain's DNS is managed), add a CNAME record for
   `beacon` pointing at `<your-github-username>.github.io`, matching the
   setup already used for kronos/threshold/warden/vigil/marshal.
5. Once DNS + Pages propagate, the page is live at
   `beacon.locallogicmanagement.com`, and the existing "Beacon →" link on
   the main site's Selected Engagements section resolves correctly.

## Files here

- `index.html` — the marketing page.
- `styles.css` — shared tokens, nav, footer, buttons, rank-check mock, rank table.
- `CNAME` — GitHub Pages custom-domain file for `beacon.locallogicmanagement.com`.
