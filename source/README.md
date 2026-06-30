# Source project

This repository stores the published Spark AR export bundle, not a separate editable
`.arproj` directory.

## What is included

The export archive at `export/adrift.arexport` contains:

- `house_yellow_barn_upd.arprojpkg` — packaged Spark AR project
- Platform-specific effect binaries (`.arfx`)
- `export.json` — export metadata (copied to `export/export-metadata.json`)

## Editing the effect

To modify the filter:

1. Import `export/adrift.arexport` into Meta Spark Studio (formerly Spark AR Studio).
2. Edit the project in Spark Studio.
3. Re-export a new `.arexport` bundle and replace `export/adrift.arexport`.
4. Update `export/export-metadata.json` from the new export if metadata changed.
5. Regenerate QR codes if the published effect ID changes.

Re-export is only required when changing the effect itself. Reorganizing files in
this repository does not affect whether an existing export loads in Spark Studio.
