# Halloween CTFd Theme

A spooky dark theme for CTFd: pumpkin-orange and moonlit purple on near-black, Creepster display headings, a bobbing jack-o'-lantern, and a landing page full of drifting ghosts, bats and code that scatter from your cursor. Based on the DUCA theme, so every CTFd feature keeps working. Dark only. Built for the CTFd 3.8 series; tested with CTFd 3.8.9. Other versions are untested.

## Install

```bash
cp -r themes/halloween /path/to/CTFd/CTFd/themes/halloween
```

Then pick **halloween** in **Admin > Config > Theme**.

## Customising

- Colours: CSS variables at the top of `static/halloween/halloween.css` (`--hw-pumpkin`, `--hw-accent`, `--hw-bg`, ...).
- Landing copy: `templates/components/landing.html`. Footer ticker: `templates/base.html`.
- After editing `static/halloween/*`, run `./sync-min.sh` (CTFd requests the `.min` copies) and bump the `&v=N` query strings.
- The chart bundles `scoreboard.duca3.js` / `userscore.duca3.js` have orange/purple ECharts options patched in; the names are kept so the manifest stays valid.

Licensing: see `LICENSE-CTFd` (CTFd core, Apache 2.0). Creepster is OFL.
