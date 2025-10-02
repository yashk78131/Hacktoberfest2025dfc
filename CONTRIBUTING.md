# Contributing

Thanks for your interest in contributing! Basic workflow:

- Fork the repo, create a branch, make changes, open a PR.

Previewing the website locally:

1. From the repository root run:

```bash
python3 -m http.server 8000
```

2. Open http://localhost:8000/index.html

Website deployment branch:

- A branch named `website-pages` is used to host the static site for GitHub Pages. You can create a PR from this branch to `main` or configure Pages to publish from it directly.
- To preview the site from that branch locally, check out the branch and run the simple HTTP server.
