# deltaprophet.github.io

This site has moved to **[pawanwagh.me](https://pawanwagh.me/)**.

This repo exists only to keep the old URL working, because it was shared in
places that can no longer be edited (job applications, resumes already sent).
It holds a redirect and nothing else.

## How the redirect works

GitHub Pages cannot issue a real `301` — there is no server-side redirect
config, no `.htaccess`, and `_redirects` is a Netlify/Cloudflare feature that
GitHub ignores. So the redirect lives in the page itself:

- `index.html` — `<meta http-equiv="refresh">` (works with JavaScript disabled),
  `location.replace()` (fast, and keeps this stub out of back-button history),
  `<link rel="canonical">` to the new site, and a visible "Go to pawanwagh.me"
  button if both are blocked.
- `404.html` — the same page, so any deep path under this domain also lands on
  the new site instead of GitHub's 404.
- `.nojekyll` — skips the Jekyll build so both files are served verbatim.

## Settings this depends on

- Repository visibility: **public** (Pages only serves from a private repo on a
  paid plan).
- Settings → Pages → Source: **Deploy from a branch**, `main`, `/ (root)`.
