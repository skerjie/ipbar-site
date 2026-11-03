# IPBar Privacy Policy

Effective October 8, 2026 · [Русская версия](PRIVACY.ru.md)

**IPBar collects nothing.** It has no account, no analytics, no crash
reporting, no ads and no tracking, and its developer never receives any data
from it. To show your public IP address it has to ask a service on the
internet; this page says which services, when, and what they receive.

## When IPBar goes online

When you open its menu, press Refresh or Try Again, click the latency card,
pick another latency host or show the latency row again.

**Watch in Background** is off unless you turn it on in the … menu. While it
is on, IPBar also looks up your address when your network changes — a new
Wi-Fi network, a VPN connecting or disconnecting — and when your Mac wakes
from sleep. These lookups go to the same services as below, and do not
measure latency. It also asks ipify for your address once a minute, or your own
lookup service if you set one, to notice a change that raises no network event;
only when the address has changed does a full lookup follow. With it off,
nothing runs while the menu is closed.

## Who receives what

| Service | When | What it receives |
| --- | --- | --- |
| [ipwho.is](https://ipwho.is), run by [ipwhois.io](https://ipwhois.io) | Every lookup | Your public IP address. It answers with the location and internet provider of that address. |
| [ipapi.co](https://ipapi.co) | Only when ipwho.is does not answer | The same. |
| [ipify](https://www.ipify.org) (`api4.ipify.org`, `api6.ipify.org`) | When your Mac has a public IPv6 address, and once a minute while Watch in Background is on | Your public IPv4 address, and your public IPv6 address when there is one. |
| A lookup service you set yourself (… → Lookup Service) | Every lookup, instead of all three above | Your public IP address. With one set, ipwho.is, ipapi.co and ipify are not asked at all. |
| Akamai (`whoami.akamai.net`), and ipwho.is or ipapi.co | Only with a VPN up, Watch in Background on and the DNS alert switched on, when the network changes; never with your own lookup service set | One DNS lookup, which Akamai answers with your DNS server's address. That address goes to ipwho.is, or ipapi.co if it does not answer, once, to learn its country. |
| [bash.ws](https://bash.ws) | Only when you run Check DNS Leaks | Your public IP address, and the addresses of the DNS servers your Mac uses: they look up ten one-off names under bash.ws, which is how the test sees them. |
| STUN servers: stun.cloudflare.com, and stun.l.google.com if it does not answer | Only when you run Check WebRTC Leaks | A few UDP packets carrying no data about you; like every connection, they show your public IP address. |
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
information), [bash.ws](https://bash.ws), [Apple](https://www.apple.com/legal/privacy/),
[Cloudflare](https://www.cloudflare.com/privacypolicy/) and
[Google](https://policies.google.com/privacy).

To stop the latency connections, hide the row: … → Show → Latency.

## What stays on your Mac

- **Your local network address** and the name of the interface are read from
  macOS and never sent anywhere.
- **Settings** — which rows are shown, the latency host, and whether the
  welcome window has been shown — are kept in the app's own preferences.
- **Networks you require a VPN on** are remembered by their router's hardware
  address, in the app's preferences, and never sent anywhere.
- **Launch at Login** is registered with macOS only when you turn it on.
- **The clipboard** receives an address when you click to copy one. IPBar never
  reads the clipboard.
- **Addresses seen this session** are kept in memory to show the Earlier
  list, and are gone when IPBar quits. Nothing from the network is saved to
  disk.

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
