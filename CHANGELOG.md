# Changelog

## 1.6.0 — 2026-10-30

- Per-request timeout in seconds (1-120), saved with the request and honoured by the proxy.
- History records the timeout used; suite grows to 79 checks, browser path to 17.

## 1.5.0 — 2026-10-30

- Search the request tree by name; matches auto-expand, no-match state, Escape clears.
- Browser check grows to 16.

## 1.4.0 — 2026-10-30

- Duplicate a request in place with a fresh id and the same method, URL, headers, auth and body.
- Browser check grows to 13.

## 1.3.0 — 2026-10-30

- Save any response body to a file; the name comes from the target path and Content-Type.
- Browser check grows to 12 and verifies the download.

## 1.2.0 — 2026-10-30

- FORM bodies: name=value fields plus file attachments, sent as real multipart data.
- File bytes stay in the browser until send; 5 MB per file, 10 files, 12 MB total.
- cURL -F fields import; -G with -F and @file references are rejected explicitly.
- Fix: the body-type buttons were wiped when no request was open; they now stay mounted.
- Suite grows to 77 checks; browser path grows to 11.

## 1.1.0 — 2026-10-30

- Import cURL commands as requests: URL, method, headers, cookies, basic auth and JSON/text bodies.
- Explicit rejections for multipart, file references and malformed commands.
- Suite grows to 66 checks; a new 8-check browser path covers the importer.

## 1.0.0 — 2026-10-30

- First public release of Relay.
