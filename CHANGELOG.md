# Changelog

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
