# IPBar Privacy Policy

Effective September 19, 2026 · [Русская версия](PRIVACY.ru.md)

**IPBar collects nothing.** It has no account, no analytics, no crash
reporting, no ads and no tracking, and its developer never receives any data
from it. To show your public IP address it has to ask a service on the
internet; this page says which services, when, and what they receive.

## When IPBar goes online

Only when you open its menu, press Refresh or Try Again, click the latency card,
pick another latency host or show the latency row again. Nothing runs in the
background while the menu is closed.

## Who receives what

| Service | When | What it receives |
| --- | --- | --- |
| [ipwho.is](https://ipwho.is), run by [ipwhois.io](https://ipwhois.io) | Every lookup | Your public IP address. It answers with the location and internet provider of that address. |
| [ipapi.co](https://ipapi.co) | Only when ipwho.is does not answer | The same. |
| [ipify](https://www.ipify.org) (`api4.ipify.org`, `api6.ipify.org`) | Only when your Mac has a public IPv6 address | Your public IPv4 address and your public IPv6 address, one each, so both can be shown. |
| The latency host: apple.com unless you choose Cloudflare (1.1.1.1), Google (8.8.8.8) or a host you type | While the latency row is shown | Up to three connections that are opened and closed without sending any data, to time the round trip. |

Every service you connect to sees your public IP address — that is how the
internet works, and it is also the one thing IPBar needs from them. Requests
use HTTPS. Besides the standard details every request carries, such as the
app's name and version and the macOS version, IPBar sends nothing about you:
no identifier, no cookie, nothing stored from an earlier request. The names of
these services and of the latency host are looked up by your Mac's DNS
resolver, as for any connection.

These services have their own privacy policies:
[ipwhois.io](https://ipwhois.io/privacy),
[ipapi.co](https://ipapi.co/privacy/),
[ipify](https://www.ipify.org) (which states that it logs no visitor
information), [Apple](https://www.apple.com/legal/privacy/),
[Cloudflare](https://www.cloudflare.com/privacypolicy/) and
[Google](https://policies.google.com/privacy).

To stop the latency connections, hide the row: … → Show → Latency.

## What stays on your Mac

- **Your local network address** and the name of the interface are read from
  macOS and never sent anywhere.
- **Settings** — which rows are shown, the latency host, and whether the
  welcome window has been shown — are kept in the app's own preferences.
- **Launch at Login** is registered with macOS only when you turn it on.
- **The clipboard** receives an address when you click to copy one. IPBar never
  reads the clipboard.
- **No history.** Each lookup replaces the last one, and neither the answers
  nor anything else from the network is saved to disk.

To remove everything IPBar keeps, quit it and move it to the Trash, then
delete `~/Library/Containers/com.andreipalonski.ipbar`.

## Downloads

Downloading IPBar from GitHub is covered by
[GitHub's privacy statement](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement).

## Changes

This policy lives in a public repository, so its history shows every change.
If IPBar ever starts to send anything new, this page changes before the app
does.

## Questions

Open an issue at [github.com/skerjie/ipbar-site/issues](https://github.com/skerjie/ipbar-site/issues).
There is nothing to ask the developer to delete: none of your data reaches
them.
