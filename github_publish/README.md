# B14 東涌田野調查 — 照片地圖

A three-panel interactive archive map (Filters | Interactive Map | Photograph & Metadata)
for the Tung Chung B14 field-survey photo collection, built on a qgis2web export.

**Live site** (GitHub Pages): `https://<username>.github.io/<repo>/`

## Structure

| Path | Content |
|---|---|
| `index.html` | Main page — filter panel, Leaflet map with marker clustering, photo + metadata panel |
| `css/` | Leaflet & MarkerCluster styles (+ marker/layers control icons in `css/images/`) |
| `js/` | Leaflet 1.x and leaflet.markercluster |
| `data/B14_2.js` | 38 photo records (GeoJSON) |
| `data/OPM100_2025_0.png` | Base raster map |
| `data/63G9SE13C00_1.jpg` | Large-scale raster overlay (see note below) |
| `images/` | 38 survey photographs referenced by `photo_path` |

## Notes

- Marker colour encodes `location_precision`: green = Exact, amber = Village-level, dashed = Approximate.
- Several photos share identical coordinates, so their clusters never split by zooming — click a cluster to spiderfy it.
- Photo filenames contain spaces and Chinese characters by design (derived from the survey database); do not rename them.
- `63G9SE13C00_1` was originally exported as a 49.6 MB PNG whose alpha channel was a uniform
  35.3% over the entire sheet. It is distributed here as a high-quality JPEG (4.2 MB, 3744×3015,
  half resolution) rendered with an equivalent `opacity`, which is visually identical.
  The original full-resolution PNG remains in the source project.
