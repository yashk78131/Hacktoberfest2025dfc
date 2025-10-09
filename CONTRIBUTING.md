# Contributing

Thanks for your interest in contributing! We welcome first-time contributors and maintain a friendly, beginner-focused workflow.

## Basic workflow

- Fork the repo
- Create a topic branch (git checkout -b feature/your-feature)
- Make changes, commit, push to your fork
- Open a Pull Request (PR)

We have templates to help: issue templates and a PR template are available in `.github/`.

## Previewing the website locally

You can preview the static site using a simple HTTP server. Below are cross-platform instructions.

Windows (PowerShell):

```powershell
# From repository root
python -m http.server 8000
# or, if python is python3 on your system:
python3 -m http.server 8000
```

macOS / Linux:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000/index.html in your browser.

## PR Checklist

Before submitting a PR, please make sure:

- [ ] Your PR has a clear title and description explaining the change
- [ ] You followed the coding / formatting style used in the repo
- [ ] You updated documentation or README if required
- [ ] You created or updated tests where appropriate (small projects may not have tests)
- [ ] You linked any related issue (use the issue templates to open new ones)

## Website deployment branch

- A branch named `website-pages` is used to host the static site for GitHub Pages. You can create a PR from this branch to `main` or configure Pages to publish from it directly.
- To preview the site from that branch locally, check out the branch and run the simple HTTP server as shown above.

## Community and code of conduct

Please follow the project's `CODE_OF_CONDUCT.md`.

If you are unsure about a change, open an issue first or join the community WhatsApp linked in the README.

