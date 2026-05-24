<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=ea580c&height=120&section=header&text=Samuel%20Appiah%20Kubi&fontSize=32&fontColor=ffffff&fontAlignY=45&desc=Geospatial%20AI%20Researcher%20%26%20Open-Source%20Engineer&descSize=14&descAlignY=70&descColor=fdba74)

[![GitHub](https://img.shields.io/badge/GitHub-appiahkubis14-1a1a1a?style=flat-square&logo=github&logoColor=ea580c)](https://github.com/appiahkubis14)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-samuel--appiah--kubi-1a1a1a?style=flat-square&logo=linkedin&logoColor=ea580c)](https://linkedin.com/in/samuel-appiah-kubi)
[![Portfolio](https://img.shields.io/badge/Portfolio-samuelappiahkubi.com-1a1a1a?style=flat-square&logo=vercel&logoColor=ea580c)](https://samuelappiahkubi.com)

</div>

---

**First Class Honours, Geomatic Engineering · KNUST, Ghana**
Admitted · Copernicus Master's in Digital Earth (Erasmus Mundus) · Salzburg, 2026

I build geospatial AI systems — sensor fusion, multi-scale satellite image processing, and planetary change detection. Currently preparing a paper for *IEEE Transactions on Intelligent Transportation Systems* on multi-modal fusion for infrastructure assessment.

---

## Open-Source Packages

Three tools. One pipeline: **satellite → AI inference → interactive web map.**

| Package | What it does | License |
|---|---|---|
| [**PyGeoFetch**](https://github.com/appiahkubis14/pygeofetch) | Search & download from 22+ satellite providers in one command | MIT |
| [**PyGeoVision**](https://github.com/appiahkubis14/PyGeoVision) | 24 geospatial AI subsystems, 14 model architectures, 10 end-to-end pipelines | Apache 2.0 |
| [**raster2pm**](https://github.com/appiahkubis14/raster2pm) | Convert any GeoTIFF to web-ready PMTiles in one command | MIT |

```bash
# The whole pipeline in three commands
pygeofetch search run --bbox -74.1,40.6,-73.7,40.9 --providers planetary_computer
pygeovision geoai segment buildings --input scene.tif --output buildings.geojson
raster2pm output.tif -o tiles.pmtiles
```

---

## Research

**MMFF — Multi-Modal Fusion Framework** · *IEEE ITS, in preparation*
Camera + IMU + GPS fusion for metric-accurate road assessment at 30 fps · Depth MAE 0.28 m · 79% jitter reduction · validated on 50 km of ground-truth data

| Project | Result |
|---|---|
| Mars Gully Digital Twin | IoU > 0.65, F1 > 0.75 on HiRISE/CTX |
| Coastal Erosion Digital Twin | 3-month shoreline forecasts, MAE < 8 m |
| IonoForecaster | 6-hour S4 scintillation forecasts, MAE < 0.08 |
| Atewa Illegal Mining Detector | Recall 82%, F1 0.79 on SAR + optical fusion |

---

## Stack

```
AI/ML        PyTorch · TensorFlow · YOLOv8 · U-Net · SegFormer · SAM · DINOv3
Geospatial   GDAL · Rasterio · GeoPandas · STAC · PMTiles · Earth Engine · QGIS
Fusion       IMU · GPS · Kalman filters · RANSAC · GAT + BiLSTM
Infra        Docker · AWS · Linux · CI/CD · ONNX
```

---

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=appiahkubis14&show_icons=true&theme=dark&hide_border=true&bg_color=0d1117&icon_color=ea580c&title_color=ea580c&text_color=fdba74)

![Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=appiahkubis14&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=ea580c&text_color=fdba74)

![footer](https://capsule-render.vercel.app/api?type=waving&color=ea580c&height=80&section=footer)

</div>