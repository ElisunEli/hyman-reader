# Corpus reader operations

GitHub Pages publishes static HTML from the root of `main`. `contents.html`
indexes scan pages (not printed pagination). New drafts use
`v{volume}/page-{scan index, four digits}.html`. Volume II scans 319–388 keep
their existing root URLs, text and scan crops; scan 319 remains at the site root.
Other pages display original corpus OCR without new annotations or alignment.

## Coverage and release

- Volume I: pilot 1–5, then 6–150, 151–300, 301–447.
- Volume II: 1–150, 151–300, 301–318 and 389–415. Previously published 319–388
  count toward coverage and are not duplicated under another URL.
- Volume III: 1–150, 151–300, 301–414.
- Each batch is verified and committed locally; the final fast-forward deploys the
  combined set after the separate pilot deployment is verified.

The workspace runner is
`work/hyman-corpus-release/release.py` (read-only input:
`hyman-text-edition-20261029/corpus.jsonl` under `doros-remote-half/work`).
Resume with `scripts/bgrun.sh hyman-corpus-release work/hyman-corpus-release/run.sh`
from the OpenClaw workspace. Check `work/hyman-corpus-release/checkpoint.json`
and `ledger.tsv` against remote main and the GitHub Pages build commit.
Use only the separate `work/hyman-reader-corpus-site` checkout as the writer;
do not resume the old five-page scheduler or push its dirty checkout.
The runner checks the remote base before each non-forced push.
Rollback by reverting the affected release commits on current main, then verify
the Pages build and the affected URLs. Do not reset or force-push main.
