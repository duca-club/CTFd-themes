# Cyberpunk CTFd Theme

A neon dark theme for CTFd: deep violet-black with hot-pink, cyan and yellow accents, Orbitron headings, CRT scanlines and a glitchy chromatic-aberration title. The landing page has a katakana and hex glyph rain, a hover-car towing a "HACK THE PLANET" banner over a neon skyline, and a hazard-tape ticker. Based on the DUCA theme, so every CTFd feature keeps working. Dark only. Built for the CTFd 3.8 series; tested with CTFd 3.8.9. Other versions are untested.

## Install

```bash
cp -r themes/cyberpunk /path/to/CTFd/CTFd/themes/cyberpunk
```

Then pick **cyberpunk** in **Admin > Config > Theme**.

## Customising

- Colours: CSS variables at the top of `static/cyberpunk/cyberpunk.css` (`--cp-accent` is the pink, `--cp-link` the cyan, `--cp-glow` the yellow, `--cp-bg`, ...).
- Scanlines: the `html::after` rule near the end of `cyberpunk.css`; delete it to turn them off.
- Landing copy: `templates/components/landing.html`. Footer ticker: `templates/base.html`.
- After editing `static/cyberpunk/*`, run `./sync-min.sh` (CTFd requests the `.min` copies) and bump the `&v=N` query strings.
- The chart bundles `scoreboard.duca3.js` / `userscore.duca3.js` have pink ECharts options patched in; the names are kept so the manifest stays valid.

Licensing: see `LICENSE-CTFd` (CTFd core, Apache 2.0). Orbitron is OFL.
