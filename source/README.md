# Source project

The editable Spark AR project is extracted at `source/house_yellow_barn_upd/`.

## Contents

| Path | Description |
|------|-------------|
| `house_yellow_barn_upd.arproj` | Main Spark AR project file |
| `objects/` | 3D assets (house, anchor) |
| `blocks/` | Reusable Spark AR blocks (ripple, instructions, animation) |
| `patches/` | Patch assets |
| `scripts/` | JavaScript (e.g. license attribution) |
| `shaders/` | Custom shaders |

This was extracted from `export/adrift.arexport` (exported 2023-08-01, Spark Studio v168).

## Open in Meta Spark Studio

1. Install [Meta Spark Studio](https://spark.meta.com/).
2. **File → Open** and select:

   ```
   source/house_yellow_barn_upd/house_yellow_barn_upd.arproj
   ```

3. Edit the scene, materials, or interaction.
4. **File → Export** to create a new `.arexport` bundle.
5. Replace `export/adrift.arexport` and refresh `export/export-metadata.json`.
6. Regenerate QR codes in `assets/qr/` if the published effect ID changes.

You can also import the pre-built bundle directly without opening the source project:

```
export/adrift.arexport
```

## Alternative: download the export

A packaged `.arexport` is attached to [GitHub Releases](https://github.com/adamsimms/adrift-ar/releases)
for use without cloning the repository or Git LFS.

## When to re-export

Re-export is only required when changing the effect itself. Moving or reorganizing files
in this repository does not affect whether an existing project loads in Spark Studio.
