# prorajnikant.github.io

Personal site for Harshit Kochar. Plain HTML and CSS: no build step, no dependencies. One inline line of JavaScript keeps the "years in security" figure current (without JS the page shows the value written into the HTML), and one script tag loads [GoatCounter](https://www.goatcounter.com) for privacy-friendly, cookie-free visit counts.

- `index.html`: the whole site (the CSS is inline)
- `404.html`: the not-found page GitHub Pages serves
- `favicon.svg`: the icon
- `fraunces-700.woff2`: Fraunces Bold for headings. `atkinson-hyperlegible.woff2`: Atkinson Hyperlegible Next (a variable font, weights 400-700) for body text, chosen for readability. They are hosted here so the page makes no outside requests. Both are latin subsets released under the SIL Open Font License.
- `.nojekyll`: tells GitHub Pages to serve files as-is

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```

## Edit

Change the text in `index.html` directly. Each section is a `<section>` with an `<h2>`.

## Publish to https://prorajnikant.github.io

For a user site the repo must be named exactly `prorajnikant.github.io` and be public. Run these from this folder:

```sh
gh auth login                      # log in as prorajnikant (if gh is on another account: gh auth switch)
gh repo create prorajnikant/prorajnikant.github.io --public
git push -u origin main
```

`origin` already points at `git@github.com:prorajnikant/prorajnikant.github.io.git`. If you push over HTTPS instead of SSH, run this first:

```sh
git remote set-url origin https://github.com/prorajnikant/prorajnikant.github.io.git
```

GitHub publishes a user-site repo from `main` automatically. If it doesn't appear within a few minutes, open **Settings → Pages** and set the source to "Deploy from a branch", `main`, `/ (root)`. Every later change goes live when you commit and push.
