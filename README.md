# Dave-IT-guy-marketing

Marketing webpage for [Dave IT Guy](https://pypi.org/project/dave-it-guy/) — deploy AI stacks with one command. Theme aligned with [Neuro Gaming Lab](https://neurogaminglab.github.io/Neuro-Gaming-Lab/) (e.g. [Neuro-Adaptive-Robotron-ML](https://neurogaminglab.github.io/Neuro-Adaptive-Robotron-ML/)).

## What’s in this repo

- **`docs/`** — GitHub Pages site. **`docs/index.html`** is the single-page marketing site: hero, quick start, features, commands, pricing, footer.
- **`instruction.txt`** — Original brief for the page.

## GitHub Pages

The site is in the **`docs/`** folder (standard GitHub Pages layout). To publish:

1. Open the repo **Settings** → **Pages**.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Choose **Branch:** `main`, **Folder:** **`/docs`**.
4. Click **Save**.

The site will be available at **https://neurogaminglab.github.io/Dave-IT-guy/**.

## View locally

Open the page in a browser:

```bash
open docs/index.html
```

Or serve from the repo root (so paths match production):

```bash
python3 -m http.server 8000
# open http://localhost:8000/docs/
```

## Links

- **PyPI:** [dave-it-guy](https://pypi.org/project/dave-it-guy/)
- **Project repo:** [NeuroGamingLab/dave-it-guy](https://github.com/NeuroGamingLab/dave-it-guy)
- **Neuro Gaming Lab:** [neurogaminglab.github.io/Neuro-Gaming-Lab](https://neurogaminglab.github.io/Neuro-Gaming-Lab/)

## License

MIT.

---

Built by [NeuroGamingLab](https://github.com/NeuroGamingLab).
