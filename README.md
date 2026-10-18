# prorajnikant.github.io

Personal site for Harshit Kochar. Plain HTML and CSS: no build step, no JavaScript, no dependencies.

- `index.html`: the whole site (the CSS is inline)
- `404.html`: the not-found page GitHub Pages serves
- `favicon.svg`: the icon
- `fraunces-600.woff2`: the heading font, hosted here so the page makes no outside requests. It is Fraunces SemiBold (latin subset), released under the SIL Open Font License.
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
