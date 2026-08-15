# deltaprophet.github.io

This site has moved to **[pawanwagh.me](https://pawanwagh.me/)**.

The old URL is kept alive only as a redirect, because it was shared in places that
can no longer be edited (job applications, resumes already sent out).

## How the redirect works

GitHub Pages cannot issue a real `301` — there is no server-side redirect config,
no `.htaccess`, and `_redirects` files are a Netlify/Cloudflare feature. So the
redirect lives in the page itself:

- `index.html` — `<meta http-equiv="refresh">` (works without JavaScript),
  `<link rel="canonical">` pointing at the new site, plus a `location.replace()`
  call and a visible "Go to pawanwagh.me" link as fallbacks.
- `404.html` — identical copy, so any deep path under this domain also lands on
  the new site instead of GitHub's 404 page.
- `.nojekyll` — skips the Jekyll build so both files are served verbatim.

## Requirements for this to actually serve

- Pages must be enabled: Settings → Pages → deploy from branch `main`, root.
- Serving Pages from a **private** repo requires a paid GitHub plan. On the free
  plan this repo has to be public, or `deltaprophet.github.io` returns a 404.

## Old content

The 2021 resume page is kept at `resume-2021.html` (and in git history).
