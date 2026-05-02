# my-books

Landing page at [vadekkapat.com](https://vadekkapat.com) — a small directory of the open technical books I'm writing.

The page itself is a single static `index.html` (no build step). Each book lives in its own repo with its own subdomain:

- [`math.vadekkapat.com`](https://math.vadekkapat.com) — *Math for Machine Learning* — [`nv-mldev/math-bootcamp`](https://github.com/nv-mldev/math-bootcamp)
- [`ml.vadekkapat.com`](https://ml.vadekkapat.com) — *Machine Learning*

## Deploying

Pushing to `main` triggers `.github/workflows/publish.yml`, which copies the static files to the `gh-pages` branch. GitHub Pages then serves them at `vadekkapat.com` (apex), wired up via the `CNAME` file and DNS records pointing at GitHub Pages IPs.

## Adding a new book

1. Edit `index.html` — copy an existing `<a class="book">` block and update the title, domain, tagline, and tags.
2. Commit and push.

That's it. No build, no Quarto, no dependencies.
