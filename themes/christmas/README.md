# Christmas CTFd Theme

A festive dark theme for CTFd: Christmas red, gold and pine green on a deep forest background, Mountains of Christmas headings, a glowing tree, and a landing page full of drifting snowflakes, presents and bells with Santa's sleighs flying along the bottom. Based on the DUCA theme, so every CTFd feature keeps working. Dark only. Tested against CTFd 3.8.x.

## Install

```bash
cp -r themes/christmas /path/to/CTFd/CTFd/themes/christmas
```

Then pick **christmas** in **Admin > Config > Theme**.

## Customising

- Colours: CSS variables at the top of `static/christmas/christmas.css` (`--xm-accent` is the red, `--xm-glow` the gold, `--xm-bg`, ...).
- Landing copy: `templates/components/landing.html`. Footer ticker: `templates/base.html`.
- After editing `static/christmas/*`, run `./sync-min.sh` (CTFd requests the `.min` copies) and bump the `&v=N` query strings.
- The chart bundles `scoreboard.duca3.js` / `userscore.duca3.js` have red/green ECharts options patched in; the names are kept so the manifest stays valid.

Licensing: see `LICENSE-CTFd` (CTFd core, Apache 2.0). Mountains of Christmas is OFL.
