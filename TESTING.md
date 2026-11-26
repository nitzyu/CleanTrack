# Testing checklist and results

## Test environment
Execution environment: source-level checks only in the generated project package. A live browser session was not available during package creation. Complete the manual tests below in Chrome or another modern browser before submission.

| Test | Expected result | Result |
|---|---|---|
| Open `index.html` | Page loads and form/list are visible | Not run in browser |
| Submit valid report | Report appears in saved list | Not run in browser |
| Submit with empty fields | Error message appears; no report is saved | Not run in browser |
| Area shorter than 3 characters | Validation message appears | Not run in browser |
| Description shorter than 5 characters | Validation message appears | Not run in browser |
| Refresh page | Previously saved report remains | Not run in browser |
| Delete a report | Report disappears and is removed from localStorage | Not run in browser |
| Desktop layout | Form and list display in two columns | Not run in browser |
| Mobile layout | Sections stack and remain readable | Not run in browser |
| Storage unavailable/full | Save failure message appears | Not run in browser |

## Source-level checks performed
- Confirmed the project uses one `index.html` file.
- Confirmed CSS is embedded in a `<style>` element.
- Confirmed JavaScript is embedded in a `<script>` element.
- Confirmed the source includes localStorage read and write operations.
- Confirmed required form fields and validation checks are present.

These source-level checks do not replace running the application in a browser. Record actual browser results after testing. Do not mark a test as passed until you have performed it.
