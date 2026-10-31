# Summer CTFd Theme

A sunny dark theme for CTFd: a deep night-ocean background with sun-orange and turquoise accents, Pacifico headings, a sunglasses-wearing sun, and a landing page full of drifting waves, shells, palms and ice cream. A banner plane flies along the bottom over palms, beach umbrellas and scuttling crabs, above a beach-towel striped ticker. Based on the DUCA theme, so every CTFd feature keeps working. Dark only. Built for the CTFd 3.8 series; tested with CTFd 3.8.9. Other versions are untested.

## Install

```bash
cp -r themes/summer /path/to/CTFd/CTFd/themes/summer
```

Then pick **summer** in **Admin > Config > Theme**.

## Customising

- Colours: CSS variables at the top of `static/summer/summer.css` (`--sm-accent` is the sun orange, `--sm-link` the turquoise, `--sm-glow` the yellow, `--sm-bg`, ...).
- Landing copy: `templates/components/landing.html`. Footer ticker: `templates/base.html`.
- After editing `static/summer/*`, run `./sync-min.sh` (CTFd requests the `.min` copies) and bump the `&v=N` query strings.
- The chart bundles `scoreboard.duca3.js` / `userscore.duca3.js` have orange ECharts options patched in; the names are kept so the manifest stays valid.

Licensing: see `LICENSE-CTFd` (CTFd core, Apache 2.0). Pacifico is OFL.
