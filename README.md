<div align="center">

<img src="https://img.shields.io/badge/Geospatial_AI_Engineer-0d1117?style=for-the-badge&labelColor=0d1117&color=2563eb" alt="title"/>

# Samuel Appiah Kubi

### Geospatial AI Researcher & Open-Source Engineer

**From satellite search to interactive maps — building the complete geospatial AI pipeline.**

[![GitHub](https://img.shields.io/badge/GitHub-appiahkubis14-0d1117?style=flat-square&logo=github&logoColor=white)](https://github.com/appiahkubis14)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-samuel--appiah--kubi-0d1117?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/samuel-appiah-kubi)
[![Twitter](https://img.shields.io/badge/Twitter-@appiahkubis14-0d1117?style=flat-square&logo=twitter&logoColor=white)](https://twitter.com/appiahkubis14)
[![Portfolio](https://img.shields.io/badge/Portfolio-samuelappiahkubi.com-0d1117?style=flat-square&logo=vercel&logoColor=white)](https://samuelappiahkubi.com)

</div>

---

## 🛰️ Who I Am

I'm a Geospatial AI researcher and engineer from Ghana. I graduated with **First Class Honours** in Geomatic Engineering from KNUST, where I also received the **Best Final Year Project Award** (highest departmental score of 88%).

I'm currently admitted to the **Copernicus Master's in Digital Earth** (Erasmus Mundus Joint Master Degree) at Paris Lodron University of Salzburg, Austria — starting September 2026.

My research focuses on:
- Multi-modal sensor fusion (camera + IMU + GPS)
- Multi-scale satellite and aerial image processing
- Planetary gully detection and change detection on Mars
- Domain generalization and algorithmic robustness

---

## 📦 My Open-Source Ecosystem

I built three production packages that together form a **complete geospatial AI pipeline** — from data acquisition to AI inference to web publication.

```
┌─────────────────────────────────────────────────────────────┐
│                      COMPLETE SOLUTION                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│            ┌─────────────┐                                  │
│            │ PyGeoFetch  │  ← DATA: 22 satellite providers  │
│            └──────┬──────┘                                  │
│                   │                                         │
│                   ▼                                         │
│            ┌─────────────┐                                  │
│            │ PyGeoVision │  ← AI: 24 subsystems, 14 models  │
│            └──────┬──────┘                                  │
│                   │                                         │
│                   ▼                                         │
│            ┌─────────────┐                                  │
│            │  raster2pm  │  ← WEB: GeoTIFF → PMTiles        │
│            └─────────────┘                                  │
│                                                             │
│     One command: satellite → AI → interactive map           │
└─────────────────────────────────────────────────────────────┘
```

---

### 🔷 PyGeoFetch — Universal Satellite Data Pipeline

[![PyPI](https://img.shields.io/pypi/v/pygeofetch?color=2563eb&label=PyPI&logo=pypi&logoColor=white)](https://pypi.org/project/pygeofetch/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](https://github.com/appiahkubis14/pygeofetch/blob/main/LICENSE)
[![Python](https://img.shields.io/pypi/pyversions/pygeofetch?color=3776ab&logo=python&logoColor=white)](https://python.org)

**Unified CLI and Python API for searching and downloading satellite imagery from 22+ global repositories.**

```bash
pygeofetch search run --bbox -74.1,40.6,-73.7,40.9 --providers planetary_computer
pygeofetch download run --from-search results.geojson --parallel 4
```

- 22+ providers: USGS, Copernicus, Planet, Maxar, NASA Earthdata, Planetary Computer, Sentinel Hub, Airbus, OpenTopography, and more
- Keyring authentication for secure credential storage
- Parallel downloads with checksum verification and resume support
- YAML pipeline orchestration with cron scheduling and webhook notifications
- 10+ post-processing actions: reproject, compress, NDVI, COG, pan-sharpen

📖 [Documentation](https://github.com/appiahkubis14/pygeofetch) | 📦 [PyPI](https://pypi.org/project/pygeofetch/)

---

### 🔷 PyGeoVision — World-Class Geospatial AI Platform

[![PyPI](https://img.shields.io/pypi/v/pygeovision?color=2563eb&label=PyPI&logo=pypi&logoColor=white)](https://pypi.org/project/pygeovision/)
[![License](https://img.shields.io/badge/License-Apache_2.0-green?style=flat-square)](https://github.com/appiahkubis14/PyGeoVision/blob/main/LICENSE)
[![Tests](https://img.shields.io/badge/Tests-208_passing-22c55e?style=flat-square)](https://github.com/appiahkubis14/PyGeoVision)

**Production platform unifying satellite data acquisition and geospatial AI in a single coherent API.**

```python
import pygeovision as pgv

client = pgv.PyGeoVision()
results = client.search(bbox, date_range, providers=["planetary_computer"])
client.geoai.segment.buildings(results[0].path, output_vector="buildings.geojson")
```

- 22+ satellite data providers integrated (USGS, Copernicus, Planet, Maxar, NASA)
- 24 GeoAI subsystems: segmentation, detection, change detection, SAM, Prithvi, DINOv3
- 10 end-to-end pipelines: building footprints, change detection, land cover, water bodies, solar detection, crop monitoring, disaster assessment, deforestation, urban growth, carbon estimation
- 14 model architectures: UNet, SegFormer, DeepLabV3+, FCOS, ViT, ChangeFormer, ESRGAN
- 7 automated labelers: OSM, Microsoft, Google, ESA WorldCover, SAM, foundation models

📖 [Documentation](https://github.com/appiahkubis14/PyGeoVision) | 📦 [PyPI](https://pypi.org/project/pygeovision/)

---

### 🔷 raster2pm — One-Command GeoTIFF to PMTiles Converter

[![PyPI](https://img.shields.io/pypi/v/raster2pm?color=2563eb&label=PyPI&logo=pypi&logoColor=white)](https://pypi.org/project/raster2pm/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](https://github.com/appiahkubis14/raster2pm/blob/main/LICENSE)
[![Python](https://img.shields.io/pypi/pyversions/raster2pm?color=3776ab&logo=python&logoColor=white)](https://python.org)

**Convert any GeoTIFF to web-optimized map tiles in one command.**

```bash
raster2pm ortho.tif -o tiles.pmtiles
raster2pm ndvi.tif --ndvi --auto-stretch -o ndvi.pmtiles
```

- One command: `raster2pm input.tif -o output.pmtiles`
- Smart colormaps: Auto-detects NDVI/NDRE (RdYlGn, viridis, plasma)
- Memory efficient: Block-by-block processing for massive rasters (tested on 64 GB orthomosaics)
- Web-ready: Output works with MapLibre, Leaflet, OpenLayers, pmtiles.io
- Parallel processing: `--workers 8` for multi-core conversion

📖 [Documentation](https://github.com/appiahkubis14/raster2pm) | 📦 [PyPI](https://pypi.org/project/raster2pm/)

---

## 📄 Research Output

**Multi-Modal Fusion Framework (MMFF)** — *In preparation for IEEE Transactions on Intelligent Transportation Systems*

A five-component sensor fusion architecture fusing monocular camera (DepthAnything v2), IMU, and GPS for metric-accurate pothole dimensioning at 30 fps without LiDAR.

- Novel contributions: GADS (metric-scale recovery), ETHHI (event-triggered fusion), MBTP (irregular area estimation), CDKF (temporal stability)
- Validation: 50 manually surveyed ground-truth measurements across 50 km of diverse road surfaces
- Results: Depth MAE 0.28 m · 62% error reduction · 48.9% area-error reduction · 79% jitter reduction

---

## 🔬 Key Research Projects

| Project | Focus | Key Achievement |
|---|---|---|
| Mars Gully Digital Twin | Planetary change detection | IoU > 0.65, F1 > 0.75 on HiRISE/CTX data |
| SMART-FOREST | Forest carbon forecasting | 10-year AGB projections under RCP scenarios |
| Coastal Erosion Digital Twin | Shoreline change | 3-month forecasts, MAE < 8 m |
| IonoForecaster | Space weather prediction | 6-hour S4 forecasts, MAE < 0.08 |

---

## 🛠️ Technical Skills

```
AI/ML:         PyTorch, TensorFlow, YOLOv8, U-Net, SegFormer, SAM, DINOv3, Prithvi
Geospatial:    GDAL, rasterio, geopandas, STAC, COG, PMTiles, Earth Engine, QGIS, ArcGIS
Sensor Fusion: IMU, GPS, Kalman filters, RANSAC, GNNs (GAT + BiLSTM)
Cloud/MLOps:   Docker, AWS (EC2/S3), Linux, CI/CD, ONNX
Languages:     Python, R, SQL, JavaScript, Bash
```

---

## 🎓 Education

| Degree | Institution | Year | Achievement |
|---|---|---|---|
| MSc Copernicus Master's in Digital Earth (Erasmus Mundus) | Paris Lodron University of Salzburg, Austria | 2026–2028 | Tuition + insurance covered by university |
| BSc Geomatic Engineering (First Class Honours) | KNUST, Ghana | 2020–2024 | Best Final Year Project Award (88%, highest departmental score) |

---

## 🏆 Honors & Awards

- **Erasmus Mundus Joint Master Admission** — European Commission, 2026
- **Best Final Year Project** (Highest Departmental Score: 88%) — KNUST, 2024
- **First Class Honours** (Top departmental graduate) — KNUST, 2024
- **2nd Place** — TRECK Annual Research Conference, 2024
- **GhIS-SS Award** — Academic excellence and professional service

---

## 📊 GitHub Stats

<div align="center">

![Samuel's GitHub Stats](https://github-readme-stats.vercel.app/api?username=appiahkubis14&show_icons=true&theme=dark&hide_border=true&bg_color=0d1117&icon_color=2563eb)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=appiahkubis14&layout=compact&theme=dark&hide_border=true&bg_color=0d1117)

</div>

---

## 📫 Connect With Me

- 📧 Email: appiahkubis14@gmail.com
- 🐙 GitHub: [github.com/appiahkubis14](https://github.com/appiahkubis14)
- 💼 LinkedIn: [samuel-appiah-kubi](https://linkedin.com/in/samuel-appiah-kubi)
- 🌐 Portfolio: [samuelappiahkubi.com](https://samuelappiahkubi.com)

---

<div align="center">

*"Built from Ghana, for the world. One command at a time."*

</div>