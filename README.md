# MANVPN Speedtest — Share Result

Public share-result page for the MANVPN Speedtest app. A test result opens as a
web page (Ookla-style link), in the MANVPN theme.

## How it works

No backend, no database. The app puts the result in the link itself and the
page renders it from the URL:

```
https://zizwanphgziz.github.io/manvpn-speedtest-result/result.html?d=191.4&u=58.5&p=31&j=5&m=UDP&ip=103.200.216.184&srv=NewMedia%20Express&id=MV-8F3K2Q&ts=1795560000000
```

| Param | Meaning |
| ----- | ------- |
| `d` | Download (Mbps) |
| `u` | Upload (Mbps) |
| `p` | Ping (ms) |
| `j` | Jitter (ms) |
| `m` | Ping method (HTTP / UDP / TCP) |
| `ip` | IP address |
| `srv` | Server (from IP lookup) |
| `id` | Result ID (`MV-XXXXXX`) |
| `ts` | Test time, epoch ms (shown in MYT) |

Opening `result.html` with no params shows a sample result.

## Files

- `result.html` — the share-result page (single file, Google Fonts via CDN)
- `og.png` — link-preview image for Telegram / WhatsApp

Hosted free on GitHub Pages. `og:title` / `og:description` are static
(generic MANVPN card) — per-result preview text is not possible on a static page.
