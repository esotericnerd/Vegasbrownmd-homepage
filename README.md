# vegasbrownmd.com recovery

Recovery workspace for rebuilding vegasbrownmd.com on GoDaddy.

## Status

This is an incomplete recovery collection, not the latest website or a deployment-ready rebuild. The owner updated the website after the April 21, 2026 homepage snapshot. Prioritize the newer source from previous ChatGPT work when recovered; use archive files only as fallback references.

- `recovery/AUDIT.md`: findings, gaps, URL discrepancies, and staging acceptance criteria.
- `recovery/url-inventory.csv`: 427 archive-indexed URLs, not all verified downloads.
- `recovery/pages/`: 18 recovered historical page bodies.
- `recovery/homepage-20260421.html`: older homepage snapshot.
- `recovery/assets/`: recovered original portrait.
- Logs and manifest record provenance, failures, and file hashes.

Raw archived HTML may depend on missing WordPress files and third-party embeds. Do not deploy it wholesale. Clinical content discrepancies require review.

## Release policy

Build and test on an isolated staging URL first. Publishing and DNS changes require owner approval. No GitHub Pages or deployment workflow is configured by this recovery save.
