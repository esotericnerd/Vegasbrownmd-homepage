# vegasbrownmd.com recovery audit

Audit date: October 21, 2026. Status: recovery in progress; no deployment or DNS changes made.

## Evidence recovered

- Local sources directory is empty. Project notice says 11 sources failed to sync; local reference coverage is incomplete.
- Direct origin fetch timed out, including a retry outside the restricted network. This does not prove that every origin service is unavailable.
- Search indexes contain a recent homepage and newer interactive clinical pages. Indexed text is evidence, not a backup of HTML, scripts, images, or all content.
- Internet Archive availability API identifies a homepage capture at 20260421012605. Its raw HTML was downloaded to `homepage-20260421.html` (106,850 characters).
- Archive CDX inventory returned 427 distinct URL keys with recorded 200 responses: 201 HTML, 79 CSS, 68 JavaScript, 49 images, one MP4, and other resources. These are indexed captures, not 427 verified working resources. Collapsing by URL key returns representative captures, not necessarily the newest versions.
- 18 priority HTML page bodies downloaded successfully. Three priority downloads failed: medical-mysteries, privacy-policy, thegauntlet. See download-log.csv.
- Original portrait downloaded. Banner and homepage stylesheet retrieval did not succeed; see asset-download-log.csv. Download success alone does not constitute visual verification.

## Priority recovery map

| Area | Evidence | Remaining work |
| --- | --- | --- |
| Branding/about | Homepage and about-me HTML, portrait file | Recover current logo, typography, palette, header/footer and verify against current appearance |
| Emergency Briefcase | Archived /emergency-briefcase/ body | Recover latest library, original links, course content and case trainer |
| Fast Facts carousel | Seven topics visible in indexed homepage | Recover actual visual cards, their destinations, order and controls; do not replace cards with invented medical content |
| Interactive cases | Recent indexed pages show answer commitment, teaching reveals, scoring, resets and calculators | Recover latest source where possible; older archives mostly contain Canva embeds rather than the newer interactions |
| Residency/simulation | /ems/ body; indexed /thegauntlet/ and /procedure-facilitator-guides/ | Recover medical mysteries, SIMWARS landing page and all facilitator tools |
| SEO | Archive inventory and exact indexed paths | Preserve existing paths, metadata, canonical intent and inbound query URLs; verify redirects on staging |
| External services | Canva, GitHub Pages case trainer, Substack and JeopardyLabs embeds | Verify availability and ownership; distinguish embedded material from locally recovered content |

## Important discrepancies

1. Archive has `/2025/08/18/emergency-briefcase-fact-facts-testicular-torsio/`; recent index has the final segment ending in `torsion/`. Keep both in the migration map; choose the canonical after checking historical redirects and user preference.
2. Archive sepsis lesson is `/2025/08/17/14855/`; newer index uses `/2025/08/17/myocardial-dysfunctional/`. Treat as a possible historical alias, not a proven redirect.
3. RMSF title at `/2025/11/08/elementor-27462/` points to the same Canva design as Guillain–Barré syndrome in the recovered archive. Do not silently republish this mismatch.
4. The April homepage is older than the recently indexed homepage; it contains older navigation and embedded teaching tools. The newer homepage includes Emergency Briefcase, residency/simulation, community projects, and Fast Facts.
5. Old course, membership, checkout, dashboard and query-string URLs occur in the inventory. They require classification; public HTML cannot recover users, passwords, payments, enrollments, databases or server-side functionality.
6. Several indexed URL keys have identical digests or irrelevant template queries. An archive 200 response does not establish a unique legitimate page. Review before inclusion.

## Proposed rebuild and staging acceptance

Select the implementation after confirming the GoDaddy product: Managed WordPress, cPanel hosting, or Websites + Marketing have different capabilities. Reconstruct public content in editable templates and retain original permalink paths. Keep raw archive files as evidence; do not upload them wholesale as the live website.

Staging must be isolated from production, access-restricted where supported, marked noindex, and use staging-safe links. Disable live checkout/email integrations until deliberately configured. Preserve domain email records during any later approved cutover.

Before requesting publication approval, validate mobile/desktop layouts, keyboard navigation, Fast Facts previous/next controls, case answers/reveals/score/reset, calculators against agreed examples, simulation tools, media/embeds, all migrated internal links, historical aliases, genuine 404 behavior, page titles, descriptions, sitemap and canonical settings. Confirm HTTPS and staging indexing restrictions. Review clinical content discrepancies with the owner.

No staging URL exists yet in this work. Browser interaction tests, hosting tests and end-to-end verification have not been performed.

## Needed from owner

- GoDaddy product/plan and dashboard URL.
- Existing temporary/staging URL, if any; whether the destination is empty or contains work to preserve.
- Access through delegate permissions or user-controlled browser sign-in. Do not put passwords into chat or recovery files.
- Canva/GitHub source ownership or access if public embeds are unavailable.
- Any unsynced source files, brand assets, prior screenshots, and clinical corrections when available.

Explicit approval is required before publishing or changing DNS. Staging setup/upload also needs to be agreed once destination and access are known.

## Sources

- Origin: https://vegasbrownmd.com/
- Availability API: https://archive.org/wayback/available?url=vegasbrownmd.com
- Homepage snapshot: https://web.archive.org/web/20260421012605/https://vegasbrownmd.com/
- Archive inventory query: https://web.archive.org/cdx/search/cdx?url=vegasbrownmd.com%2F%2A&output=json&filter=statuscode%3A200&collapse=urlkey
- Recent index includes https://vegasbrownmd.com/2025/08/18/emergency-briefcase-fast-facts-stroke/ and https://vegasbrownmd.com/thegauntlet/.

See url-inventory.csv for every indexed URL and snapshot address, download-log.csv for fetched page bodies, and recovered-page-manifest.json for extracted titles and embeds.
