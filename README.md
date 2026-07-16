# Data Structures with Python — Course Site

A small static site for lecture notes and lab practicals, meant to be pushed to
GitHub and served with GitHub Pages.

```
.
├── index.html          # course home page
├── notes.html          # lecture notes, by unit
├── practicals.html     # all 15 practicals, linking to code/
├── css/style.css
├── js/script.js
└── code/                # starter .py file for each practical — edit these in VS Code
    ├── prac01_recursion.py
    ├── prac02_singly_linked_list.py
    ├── ...
    └── prac15_binary_search.py
```

## Putting it on GitHub

1. Create a new repository on GitHub (e.g. `data-structures-course`).
2. In this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial site + practical stubs"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**, and under "Build and deployment" set
   **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. After a minute, the site will be live at
   `https://<your-username>.github.io/<repo-name>/`.

## Day-to-day workflow

1. Open the repo folder in VS Code.
2. Write each practical inside its matching file in `code/` — the function
   signatures and docstrings already match the lab sheet, so you only need to
   fill in the `# TODO` sections.
3. Test locally with `python code/prac05_stack.py` (etc.).
4. Commit and push:
   ```bash
   git add code/prac05_stack.py
   git commit -m "Complete practical 5: stack"
   git push
   ```
5. The **practicals.html** page already links to `code/prac05_stack.py` — once
   it's pushed, that link shows your finished code on the live site.

## Notes

- The site is plain HTML/CSS/JS — no build step required.
- To preview locally before pushing, just open `index.html` in a browser, or
  run a tiny local server from this folder: `python -m http.server 8000`.
