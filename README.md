# Adrift AR Filter

An augmented reality effect for Facebook and Instagram. A digital house floats on the
Atlantic Ocean, drifting and turning as the viewer moves through the scene.

![Adrift AR filter preview](assets/preview.png)

## Try it

| Platform | QR code | Link |
|----------|---------|------|
| Facebook | ![Facebook QR](assets/qr/facebook.svg) | [Open in Facebook](https://www.facebook.com/fbcameraeffects/testit/1038807263776570/YWJkYjY2M2VhMzZiYzIwNTIwYjYzYzZkMTU1ZjNhMzQ=/) |
| Instagram | ![Instagram QR](assets/qr/instagram.svg) | [Open in Instagram](https://www.instagram.com/ar/1038807263776570/?ch=YWJkYjY2M2VhMzZiYzIwNTIwYjYzYzZkMTU1ZjNhMzQ%3D) |

Scan a QR code with your phone camera, or open the link on a mobile device with the
app installed.

## Artist statement

Adrift elides physical and virtual space while challenging ephemeral notions of home.
The digital structure floats perpetually on the Atlantic Ocean. As the viewer
experiences the piece, the house drifts and turns as if floating in physical space.

Adrift is a historical representation of my grandmother's experience of her
resettled home and, by extension, all resettled homes. The house also acts as another
form of resettlement to a third, imaginary dimension still influenced by its
geographical context: whereby the image prevails over the thing it is an image of
(Virilio 25). The virtual space, linked to an actual place, becomes a "third space of
hybridity" accessed by the window of technology (Ang 170). While technology allows us
to access this hybrid space, it also challenges the real and actual, the near and far.
It reminds us that neither a resettled resident nor their home can ever return to
their origins.

Learn more at [adamsim.ms](https://adamsim.ms).

## Repository layout

```
.
├── export/
│   ├── adrift.arexport          # Spark AR export bundle (ready to import/publish)
│   └── export-metadata.json     # Export date, Spark version, target platforms
├── assets/
│   ├── icon-adrift.png          # Effect icon
│   ├── preview.png              # Preview image for docs and listings
│   └── qr/
│       ├── facebook.svg         # QR code for Facebook
│       └── instagram.svg        # QR code for Instagram
└── source/
    └── README.md                # How to edit and re-export the effect
```

## Spark AR compatibility

**You do not need to re-export just because this repository was reorganized.** The
`export/adrift.arexport` file is the same Spark AR bundle; only its path in git
changed.

| Action | Re-export needed? |
|--------|-------------------|
| Clone or reorganize this repo | No |
| Import `export/adrift.arexport` into Meta Spark Studio | No |
| Publish or republish the existing effect | No (use the existing export) |
| Edit the 3D scene, materials, or interaction | Yes |
| Update for a newer Spark Studio version | Recommended |
| Published effect ID changes after republishing | Yes, and regenerate QR codes |

### Export details

From `export/export-metadata.json`:

- **Project name:** `house_yellow_barn_upd`
- **Exported:** 2023-08-01
- **Spark Studio version:** 168.0.0.25 (codename Skylight)
- **Target platforms:** Facebook, Instagram

Meta has renamed and evolved Spark AR tooling (now Meta Spark Studio). Older exports
usually still import, but republishing may require a newer Studio version depending on
current platform requirements.

## Development

1. Install [Meta Spark Studio](https://spark.meta.com/).
2. Import `export/adrift.arexport`.
3. Make changes and export a new `.arexport` bundle.
4. Replace `export/adrift.arexport` and refresh `export/export-metadata.json`.
5. If the published effect URL changes, regenerate the QR codes in `assets/qr/`.

See [source/README.md](source/README.md) for more detail.

## License

This project is licensed under [CC BY-NC 4.0](LICENSE).

The effect's availability on Facebook and Instagram is governed by Meta's platform
terms.

## Credits

- **Artist:** [Adam Simms](https://adamsim.ms)
- **References:** Paul Virilio, *The Vision Machine*; Ien Ang, *On Not Speaking Chinese*
