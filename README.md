# Samuel Appiah Kubi 🌍🛰️

**MSc Candidate, Copernicus Master in Digital Earth (GeoDSc Track)**  & **Radar Remote Sensing & GeoAI Researcher**  

I design and build reproducible, physics-informed machine learning frameworks for Synthetic Aperture Radar (SAR) and multi-sensor Earth Observation. My work bridges the gap between physical geodetic models and deep learning, enforcing physical invariants (e.g., phase closure, integer ambiguity) while leveraging geometric deep learning for robustness in complex, real-world terrain.

---

## 🏗️ Research & System Architecture

My open-source ecosystem is designed as a modular, end-to-end pipeline—from federated data ingestion to rigorous geodetic validation:

`pygeofetch` (Ingestion & Preprocessing) → `pyunwrap` / `ps-gnn` (Algorithmic Core) → `pygeovision` (Orchestration & Deployment)

### 🔬 Algorithmic Core (Staged Release / Intensive Testing)

- **[ps-gnn](https://github.com/EOCoreINT/ps-gnn)** — DOI: [10.5281/zenodo.22706887](https://zenodo.org/records/22706887)  
  *Re-engineering Persistent Scatterer (PS) selection.* Reframes point-target identification from heuristic thresholding to spatial node classification via an 8-head **Graph Attention Network (GAT)**. Includes a custom velocity-accuracy audit to ensure training labels align with long-term phase reliability.  
  *Status: Closed Beta | Validation: Simulated stacks & EGMS/GNSS underway.*

- **[pyunwrap-insar](https://github.com/EOCoreINT/pyunwrap)** — DOI: [10.5281/zenodo.22209219](https://zenodo.org/records/22209219)  
  *Physics-informed phase unwrapping.* Features **AmbiguityNet**, a ResNet-34 U-Net that resolves complex radar phase boundaries by enforcing discrete integer ambiguity matrices $K$ through straight-through estimator rounding layers. Includes a closure-checked "island rescue" integer program that reduced coherent pixel errors from 30.9% to 3.2% in simulation.  
  *Status: Closed Beta | Validation: Beat SNAPHU on hard scenes by 5.6 points (95% CI 4.1–7.2).*

### ⚙️ Ingestion & Production Pipelines

- **[pygeofetch](https://github.com/EOCoreINT/pygeofetch)** — DOI: [10.5281/zenodo.22087230](https://zenodo.org/records/22087230)  
  *Federated satellite data access & processing.* A programmatic layer spanning 24+ providers (Copernicus, ASF, NASA) with built-in pre-download burst screening (`PreflightGate`). Features a native, pure-Python, Windows-compatible InSAR processing chain (ESD coregistration, ERA5/IONEX correction, SBAS) with automated baseline and network connectivity checks.  
  *Status: Stable | Public Production | Tested via pytest & GitHub Actions.*

- **[pygeovision](https://github.com/EOCoreINT/pygeovision)** — DOI: [10.5281/zenodo.22258220](https://zenodo.org/records/22258220)  
  *End-to-end GeoAI orchestration.* Supports 49+ automated task pipelines, chainable preprocessing, and an audited model registry (Prithvi-EO-2.0, DINOv3, SAM). Adapts optical foundation models for Sentinel-1 VV/VH data and includes a FastAPI inference server with ONNX export for low-latency deployment.  
  *Status: Closed Beta.*

---

## 📊 Scientific Validation Campaigns

I prioritize honest, rigorous evaluation. Documenting where models fail is as critical as reporting peak accuracy.

- **[Mexico City Subsidence Project](https://github.com/EOCoreINT/mexico-subsidence-project)**  
  End-to-end programmatic SBAS time-series analysis over a **502.5 GB / 67-scene Sentinel-1 SLC stack**. Mapped extreme urban subsidence vertical velocities up to **−35.5 cm/year**, in close agreement with published peaks (−39.1 cm/year, Cigna & Tapete, 2021) and local GNSS stations. Prevented 360 GB of redundant downloads via intelligent orbital track pre-filtering.
  
- **Ongoing Validation Frontiers:**  
  - *Upper Silesian Coal Basin:* Deliberate C-band-only test comparing physics-informed methods against SNAPHU on sharp, mining-induced deformation gradients.  
  - *Portuguese Bend, CA:* Integrating NISAR along-track offsets and downslope-flow priors to resolve north-south motion in a fast (1.6 m/yr) coastal landslide.  
  - *Blatten, Switzerland:* Retrospective analysis of the May 2025 rock-ice avalanche, testing whether misfit warnings in physics-informed models can flag pre-failure acceleration that traditional unwrapping misses.

---

## 🌐 Community, Credentials & Ecosystem

- **ORCID iD:** [0009-0002-1376-108X](https://orcid.org/0009-0002-1376-108X)
- **EOCoreINT GitHub:** [github.com/EOCoreINT](https://github.com/EOCoreINT)
- **EOCoreINT Website:** [eocoreint.com](https://eocoreint.com) *(Open-source EO software & GeoAI academy for African students and professionals)*

---

> *"Much of my work is evaluation: building benchmarks with known answers, testing models on real data, and working out exactly why they fail."*
