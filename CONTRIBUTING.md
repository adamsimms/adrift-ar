# Contributing to Adrift

Thank you for your interest in this project. Adrift is an art piece and AR filter — contributions
might include bug fixes, documentation, asset optimization, or technical improvements to the Spark AR
project.

Please read and follow our [Code of Conduct](CODE_OF_CONDUCT.md). We are committed to a welcoming,
respectful community.

## Quick start

```bash
# 1. Fork and clone (Git LFS is required)
git clone https://github.com/adamsimms/adrift-ar.git
cd adrift-ar
git lfs install
git lfs pull

# 2. Open the project in Meta Spark Studio
#    File → Open → source/house_yellow_barn_upd/house_yellow_barn_upd.arproj

# 3. Make your changes, then export a new bundle
#    File → Export → save as adrift.arexport

# 4. Update repo artifacts (see checklist below)

# 5. Open a pull request against main
```

**Don't have Git LFS?** Download the export from
[GitHub Releases](https://github.com/adamsimms/adrift-ar/releases) instead of cloning large binaries.

## Prerequisites

| Tool | Purpose |
|------|---------|
| [Git](https://git-scm.com/) | Version control |
| [Git LFS](https://git-lfs.com/) | Large binary assets (`.arproj`, `.fbx`, `.arexport`, etc.) |
| [Meta Spark Studio](https://spark.meta.com/) | Edit and export the AR effect |

## What to contribute

Good first contributions:

- Documentation fixes and clarifications
- README or QR code improvements
- Asset size optimization (images, SVGs)
- CI and repo hygiene improvements

Larger contributions (please open an issue first):

- Changes to the 3D scene, shaders, or interaction design
- Replacing or adding Spark AR blocks
- Republishing workflow updates for newer Meta Spark Studio versions

## Pull request checklist

When your change touches the AR effect, include all of the following:

- [ ] Opened and tested `source/house_yellow_barn_upd/house_yellow_barn_upd.arproj` in Meta Spark Studio
- [ ] Exported an updated `export/adrift.arexport` (if the effect changed)
- [ ] Updated `export/export-metadata.json` from the new export
- [ ] Regenerated `assets/qr/*.svg` if the published effect URL changed
- [ ] Updated `assets/preview.png` if the visual appearance changed significantly
- [ ] Documented any new third-party blocks or assets in the PR description

For documentation-only PRs, the export steps are not required.

## Project structure

| Path | Purpose |
|------|----------|
| `source/house_yellow_barn_upd/` | Editable Spark AR project — **start here for effect changes** |
| `export/adrift.arexport` | Published export bundle — import into Spark Studio or Meta's publisher |
| `export/export-metadata.json` | Export version, date, and platform metadata |
| `assets/` | Icons, preview image, and QR codes |
| `source/README.md` | Detailed source project guide |

## Third-party assets

The Spark AR project includes blocks and patches from the Spark AR community and Meta templates:

- **3D Ripple Plane** — jeetesh_singh_209
- **Real World Instruction** — community block (v141)
- **Quick Animation, Ripple, manip_ring** — Spark AR blocks/patches
- **Meta Spark Studio Templates** — see `source/house_yellow_barn_upd/scripts/License.js`

Preserve existing attribution when modifying or redistributing these assets. Do not remove
`scripts/License.js` unless you also remove all dependent Meta template content.

## Regenerating QR codes

If the published effect ID changes after republishing, decode the new URLs and regenerate SVGs:

```bash
pip install qrcode[pil]
python3 - <<'PY'
import qrcode, qrcode.image.svg

def write_qr(path, url):
    qr = qrcode.QRCode(version=None, error_correction=qrcode.constants.ERROR_CORRECT_M,
                       box_size=10, border=4)
    qr.add_data(url)
    qr.make(fit=True)
    img = qr.make_image(image_factory=qrcode.image.svg.SvgPathImage)
    with open(path, "wb") as f:
        img.save(f)

# Replace with your new effect URLs
write_qr("assets/qr/facebook.svg", "https://www.facebook.com/fbcameraeffects/testit/...")
write_qr("assets/qr/instagram.svg", "https://www.instagram.com/ar/...")
PY
```

Update the links in `README.md` to match.

## Code style

- Keep changes focused — one logical change per pull request when possible
- Use clear commit messages (e.g. `docs: clarify LFS clone steps`, `export: update house material`)
- Match existing file naming and directory layout
- Do not commit Spark AR temp files (see `.gitignore`)

## Questions and discussions

Open a [GitHub Issue](https://github.com/adamsimms/adrift-ar/issues) for:

- Bugs in the repo, docs, or export workflow
- Questions about getting started
- Proposals for larger changes before you invest significant time

## License

By contributing, you agree that your contributions will be licensed under the same
[CC BY-NC 4.0](LICENSE) license as the project, except where third-party Spark AR assets
carry their own terms.

## Maintainers: GitHub repository settings

Ensure the following are set under **Settings → General** on GitHub:

| Setting | Recommended value |
|---------|-------------------|
| Description | `Adrift — an AR filter for Facebook and Instagram. A floating house on the Atlantic Ocean by Adam Simms.` |
| Website | `https://adamsim.ms` |
| License | CC BY-NC 4.0 |
| Topics | `spark-ar`, `meta-spark`, `augmented-reality`, `ar-filter`, `facebook`, `instagram`, `digital-art` |

GitHub may show **Other** for the license until CC BY-NC 4.0 is selected in the repository settings UI.
