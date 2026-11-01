<div align="center">

<img src="docs/icon.png" width="84" alt="Relay">

# Relay

### Collections, environments and a transmission log — on your own machine.

A local API client with a loopback proxy, no account and no cloud sync.

[![Download for Windows](https://img.shields.io/badge/Download-Windows%20x64-1E3A4C?style=for-the-badge&logo=windows11&logoColor=white)](https://github.com/KHHH2312/relay/releases/latest)
[![Latest release](https://img.shields.io/github/v/release/KHHH2312/relay?style=flat-square&color=1E3A4C)](https://github.com/KHHH2312/relay/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11%20x64-EDE7DA?style=flat-square)](#requirements)
[![License](https://img.shields.io/badge/license-MIT-EDE7DA?style=flat-square)](LICENSE)

<img src="docs/relay-desk.png" alt="Relay" width="100%">

</div>

> **New — 1.16.0** — environments that extend a parent band and inherit its variables.
> [Changelog →](CHANGELOG.md)

---

## Why Relay

**Cloud API clients want an account for data that never needed to leave the desk.**

**A local proxy avoids CORS without a browser extension or a remote relay.**

**A signal desk, not a form.** The request, the response and the history are one instrument.

## Features

| | |
|---|---|
| **Frequency banks** | Searchable collections, folders and requests with duplicate and move controls. |
| **Request builder** | Method, URL, per-request timeout, headers, auth, JSON/text or multipart form data. |
| **Environments** | Named variable sets with {{autocomplete}}, duplicate and JSON export/import; a band can extend a parent and inherit its variables; unresolved variables warn before send and link to the manager. |
| **Loopback proxy** | CORS-free sends with timeout, redirect, size caps and metadata-host blocking. |
| **RX monitor** | Status, time, size, hops, headers, parsed cookies, a collapsible JSON tree, pretty/raw body, Ctrl+F find and save-to-file. |
| **Transmission log** | The last 50 requests, persisted and clickable. |
| **Copy as cURL / fetch / PowerShell** | One click from a request to a reproducible curl command, an await fetch() snippet or a PowerShell Invoke-RestMethod block, with headers, auth and bodies. |
| **Import cURL** | Paste a curl command; URL, method, headers, auth and body import as a request. |
| **Import / export** | Collections as JSON; no lock-in. |

<div align="center">
<img src="docs/relay-env.png" alt="Relay" width="49%">
<img src="docs/relay-response.png" alt="Relay" width="49%">
<img src="docs/relay-curl.png" alt="Relay" width="49%">
</div>

## Requirements

- Windows 10 or 11, x64
- No account, no runtime install

## Install

1. Download **Relay-1.16.0-win32-x64.zip** from [Releases](https://github.com/KHHH2312/relay/releases/latest).
2. Verify it against `SHA256SUMS.txt`:
   ```powershell
   Get-FileHash .\Relay-*-win32-x64.zip -Algorithm SHA256
   ```
3. `FILEMANIFEST.txt` lists the SHA-256 and size of every file in the archive — diff it against what you unpacked.
4. Unzip anywhere and run **Relay.exe**.

> Self-signed development certificate: SmartScreen will warn until an OV/EV certificate is used.
> The SHA-256 checksum is the trust anchor.

## Using it

1. Install and launch Relay.
2. Create a bank (collection) and a request; set the URL, headers or body.
3. Create an environment, add variables and activate it.
4. Press Ctrl+Enter; inspect the response and reuse the entry from the transmission log.

## Verified

- Model/API suite: 100 checks green, including nested environment inheritance, cycle refusal, cookie forwarding, fetch and PowerShell snippets and the echo proxy.
- Browser golden path: 44 checks green — nested bands inheriting into the variable picker, copy-as-fetch, copy-as-PowerShell, JSON tree, cookies, preflight, multipart send and find-in-body.
- Earlier flow: 200 / 5 ms / 307 B response, no console exceptions.
- Packaged app passes the source-parity integrity gate and ships with SHA-256 sums and a per-file manifest.

## Security and privacy

- Local-first: the app runs on loopback, stores data on your machine and sends no telemetry.
- Strict renderer policy, sandboxed window, denied navigation/window-open by default.
- Releases are integrity-gated, signed and published with SHA-256 sums and a per-file manifest.
- Found a flaw? Open a private security advisory instead of a public issue.

## FAQ

**Does it need an account?** No.

**Where is my data?** In the app's local data folder, not on a server.

**Why is the source not in this repository?** This repository distributes the application and its
documentation. The source is private.

## License

MIT — see [LICENSE](LICENSE). Third-party components in [THIRD-PARTY.md](THIRD-PARTY.md).

---

## The rest of the desk

Five local-first tools, one philosophy: your files, your machine, no telemetry.

- **Pressroom** — [deck studio](https://github.com/KHHH2312/pressroom)
- **Folio** — [PDF bindery](https://github.com/KHHH2312/folio)
- **Relay** — [API client](https://github.com/KHHH2312/relay)
- **Slate** — [markdown notebook](https://github.com/KHHH2312/slate)
- **Boardroom** — [whiteboard](https://github.com/KHHH2312/boardroom)
