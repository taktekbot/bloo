# Demo files

The **Try the demo** button on Bloo's start screen loads the files listed in `manifest.json` from this folder. The button only appears when the manifest lists at least one file, so an empty folder changes nothing.

The demo model is the [Atomic Stack — MCM modular drawer valet system](https://www.printables.com/model/1784047-atomic-stack-mcm-modular-drawer-valet-system) by **Thunder Butter Designs**. All credit for the model goes to the designer — the printable files and the full listing live on their Printables post, which is linked next to the demo button in the app.

## Adding the files

1. Download the STL files from the Printables post (check the model's license permits redistributing them here first).
2. Drop them into this folder, **keeping the original filenames** — Bloo recognizes parts by name (`leg`, `valet`, `drawer`, `container_bottom`, …) to pick default colors and assemble them.
3. List each filename in the `files` array of `manifest.json`:

```json
{
  "name": "Atomic Stack",
  "credit": "Thunder Butter Designs",
  "url": "https://www.printables.com/model/1784047-atomic-stack-mcm-modular-drawer-valet-system",
  "files": ["atomic_stack_leg.stl", "atomic_stack_drawer.stl"]
}
```

Only `.stl` and `.obj` files load; keep them directly in this folder (no subfolders). The demo works when Bloo is served over HTTP (e.g. GitHub Pages) — browsers block these fetches for a page opened straight from disk, so the button stays hidden there.
