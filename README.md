# Node Hunter

A playable, pixel-art guide to **radial and angular nodes** in s, p, d and f orbitals.

- **World 1:** what a node is, going from a vibrating string (1D) to a drumhead (2D) to the atom (3D)
- **World 2:** the counting rules (total = n − 1, angular = ℓ, radial = n − ℓ − 1) and a node calculator
- **World 3, the Nodescope:** any orbital from 1s to 7f in 3D. Drag to rotate, cut it open, show its nodal surfaces, and see a 2D slice and the radial function r²R²
- **World 4:** radial nodes as onion layers (ns, np, nd, nf for n up to 7)
- **World 5:** all 16 angular shapes (1s, 2p, 3d, 4f) and their nodal planes and cones
- **World 6:** the node table for n = 1 to 7
- **World 7:** a 10-question quiz

Orbitals are real hydrogen-like orbitals (Z = 1), computed in the browser: the 3D view is a WebGL raymarcher and the 2D views are drawn on canvas. The whole site is one file, `index.html`, with no build step and no dependencies. The only external resource is two Google Fonts (Press Start 2P and VT323).

## Publish on GitHub Pages

**From the website (no command line):**

1. Create a new public repository on GitHub, for example `node-hunter`.
2. Choose **Add file → Upload files**, drag in `index.html` and `.nojekyll`, and commit. `.nojekyll` is hidden in Finder; press `Cmd + Shift + .` to show it. The site works without it.
3. Go to **Settings → Pages**. Under **Build and deployment**, pick **Deploy from a branch**, then branch `main` and folder `/ (root)`, and save.
4. After a minute or two the site is live at `https://<your-username>.github.io/node-hunter/`.

**From the terminal** (after creating an empty repository called `node-hunter` on GitHub):

```bash
cd ~/Downloads/node-hunter
git init -b main
git add index.html .nojekyll README.md
git commit -m "Node Hunter"
git remote add origin https://github.com/<your-username>/node-hunter.git
git push -u origin main
```

Then turn on Pages in **Settings → Pages** as in step 3 above.

## Preview locally

```bash
cd ~/Downloads/node-hunter && python3 -m http.server 8000
```

Then open http://localhost:8000.
