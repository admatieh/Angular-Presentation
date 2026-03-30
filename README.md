# Angular GitHub Presentation Starter

A simple Reveal.js presentation that can be hosted on GitHub Pages.

## Files

- `index.html` — Reveal.js presentation shell
- `slides.md` — Your slide content in Markdown
- `assets/` — Images or other files

## Local preview

Because browsers may block local markdown loading from `file://`, use a local server.

### Option 1: Python

```bash
python3 -m http.server 8000
```

Then open:

```bash
http://localhost:8000
```

## Publish on GitHub Pages

1. Create a new GitHub repo.
2. Upload all files from this folder.
3. Push to the `main` branch.
4. In GitHub, go to **Settings → Pages**.
5. Under **Build and deployment**, choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
6. Save.
7. Your presentation will be live on the GitHub Pages URL GitHub gives you.

## How to edit slides

Update `slides.md`.

- `---` creates a new slide
- standard Markdown works
- code blocks are supported
- HTML is also supported for custom layouts

## Suggested next step

Replace the default sections in `slides.md` with your Angular outline.
