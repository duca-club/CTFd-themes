# Haxxor CTFd Theme

A hacker-terminal dark theme for CTFd: black with matrix green, Share Tech Mono headings, CRT scanlines and a glitchy title. The landing page has a falling hex and katakana glyph rain, a hooded-hacker logo, terminal windows ("ACCESS GRANTED") and PWNED skulls standing on a strip of binary, a packet towing a `$ sudo hack --all_` banner, and a terminal-style ticker. Based on the DUCA theme, so every CTFd feature keeps working. Dark only. Built for the CTFd 3.8 series; tested with CTFd 3.8.9. Other versions are untested.

## Install

```bash
cp -r themes/haxxor /path/to/CTFd/CTFd/themes/haxxor
```

Then pick **haxxor** in **Admin > Config > Theme**.

## Customising

- Colours: CSS variables at the top of `static/haxxor/haxxor.css` (`--hx-accent` is the green, `--hx-link` the mint, `--hx-glow` the lime, `--hx-bg`, ...).
- Scanlines: the `html::after` rule near the end of `haxxor.css`; delete it to turn them off.
- Landing copy: `templates/components/landing.html`. Footer ticker: `templates/base.html`.
- After editing `static/haxxor/*`, run `./sync-min.sh` (CTFd requests the `.min` copies) and bump the `&v=N` query strings.
- The chart bundles `scoreboard.duca3.js` / `userscore.duca3.js` have green ECharts options patched in; the names are kept so the manifest stays valid.

Licensing: see `LICENSE-CTFd` (CTFd core, Apache 2.0). Share Tech Mono is OFL.
