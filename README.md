# patricklavictoire.com

Personal site. Static HTML, no build step, hosted on GitHub Pages.

## Files

- `index.html` — the site
- `CNAME` — tells GitHub Pages to serve at `patricklavictoire.com`
- `headshot.jpg` — square photo (you add this)
- `resume.pdf` — current résumé (you add this)

## Before going live

In `index.html`, replace `your@email.here` (appears twice) with the email you want public.

Confirm the external links still resolve to the right places:
- arXiv: `https://arxiv.org/a/lavictoire_p_1`
- LessWrong: `https://www.lesswrong.com/users/orthonormal`
- LinkedIn: `https://www.linkedin.com/in/patricklavictoire/`

## Deploy

The repo name `orthonormal.github.io` is what activates user-pages mode — push to `main` and GitHub Pages serves it automatically. No Settings configuration needed initially.

```
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/orthonormal/orthonormal.github.io.git
git push -u origin main
```

Visit `https://orthonormal.github.io` after a minute or two.

## Custom domain (later step)

The `CNAME` file already declares the domain. To make `patricklavictoire.com` actually serve this site, you'll need to update DNS at Squarespace:

- Four `A` records on the apex (`@`) pointing to GitHub's IPs:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- One `CNAME` record on `www` pointing to `orthonormal.github.io`

Then in the GitHub repo: Settings → Pages → wait for the DNS check to pass, then tick "Enforce HTTPS." Cert provisioning takes up to an hour.

## Editing later

Edit `index.html` directly. To preview locally, just open the file in a browser — no server needed (the Google Fonts request needs internet, but everything else is local).
