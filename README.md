# traffic-feed-example

> Example install + customization guide for the **Live Traffic Feed** widget — part of the [FeedPulse](https://feed-pulse.com) free widget suite.

## What it does

The Live Traffic Feed shows the last 10 visitors to your site in a scrolling, auto-refreshing feed. Each row shows:

- **Country flag + city** (from anonymized IP geolocation)
- **Referrer** (which site they came from — Google, Twitter, direct, etc.)
- **Time-ago** ("just now", "3m ago", "1h ago")

Auto-refreshes every 3 seconds. No layout shift (the widget reserves its own height so the page stays stable). No cookies. No third-party tracking pixels.

## Why use it

Live activity is one of the strongest [social-proof signals](https://en.wikipedia.org/wiki/Social_proof) on a small website — a moving feed shows visitors that your site is alive and useful right now, not a static graveyard. It's the same principle that made the original [Feedjit](https://web.archive.org/web/2010*/feedjit.com) widget so popular in 2009-2014 across millions of blogs, classified sites, and forums.

## Install

```html
<!-- Paste in your <head> or just above </body> -->
<script async src="https://feed-pulse.com/api/embed/traffic_feed?site_id=YOUR_SITE_ID"></script>
```

Replace `YOUR_SITE_ID` with the site ID you'll get when you [generate the widget at feed-pulse.com](https://feed-pulse.com/free-live-traffic-widget) — no signup required.

## Customization params

All parameters go in the query string of the `<script src="…">`:

| Param | Default | Description |
|---|---|---|
| `w` | `320` | Widget width in pixels |
| `rows` | `10` | Number of recent visitors to show (max 20) |
| `poll` | `3000` | Refresh interval in milliseconds (3 sec default) |
| `bc` | `ffffff` | Background colour (hex, no `#`) |
| `tc` | `0a0a0a` | Text colour (hex, no `#`) |
| `brd` | `e5e7eb` | Border colour (hex, no `#`) |
| `hb` | `002fa7` | Header background |
| `hf` | `ffffff` | Header foreground |
| `font` | `IBM Plex Sans` | Font family (any system font) |
| `lang` | `auto` | UI language — `en`, `es`, `fr`, `de`, `hi`, `pt`, `it`, `ru`, `ja`, `zh`, `ar`, `nl` |
| `nobot` | `0` | Set to `1` to filter known bots (Googlebot, Bingbot, AhrefsBot, etc.) |

## Compatible platforms

| Platform | Where to paste |
|---|---|
| WordPress | Header theme file, or a "Custom HTML" block in any post / sidebar widget area |
| Shopify | `theme.liquid` → `<head>`, or any Custom HTML section |
| Webflow | "Embed" component on the page where you want the feed |
| Ghost | Code injection → site header, or any HTML card in a post |
| Substack | Raw HTML pane in a post |
| Wix | HTML element, drag in, paste |
| Squarespace | Code block |
| Plain HTML | Anywhere inside `<body>` or `<head>` |

## Use cases

- **Indie SaaS landing pages** — show new signup activity even when it's slow
- **Personal blogs** — bring back the early-blogosphere vibe of "people are reading this right now"
- **Marketplaces** — proves traffic to potential sellers without revealing exact numbers
- **Community forums** — surfaces lurker activity to encourage participation

## See it live

The traffic feed is running on [feed-pulse.com](https://feed-pulse.com) itself (scroll to the footer). Generator and customizer at [feed-pulse.com/free-live-traffic-widget](https://feed-pulse.com/free-live-traffic-widget).

## License

[MIT](LICENSE)

## More widgets

19 free embeddable widgets at [feed-pulse.com/widgets](https://feed-pulse.com/widgets). No signup, no paid tier.
