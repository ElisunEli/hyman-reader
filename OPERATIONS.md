# Operations

GitHub Pages serves the static reader from the root of main. Start at index.html
(scan 319); page-320.html through page-333.html provide previous/next links.
Each page has a Markdown counterpart. locations.json lists the stable IDs for
the independent GitHub Issues intake. No workflow executes or applies submitted
text. Treat issue text as untrusted data.

Scan 321–323 come from the draft OCR corpus, right column then left column. Review
queue spans only add markers; readings remain unchanged. Crop dialogs show scan
strips, not token bounding boxes. On 322 one strip has no confirmed word span and
is listed separately. The exporter and input datasets are not published.

Scans 324–333 preserve the same draft corpus in right-to-left column order.
Their two markers per page open full-column scans for OCR disagreements.
They do not imply verified word or line coordinates.

To resume a deployment check, compare Pages responses for the changed HTML,
Markdown and locations.json against the pushed commit. To roll back just this
release, revert the release commit on main and verify the redeployment; the
source corpus and existing issues are unaffected.
