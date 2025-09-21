# Hermes---AI
I'm currently developing Hermes AI, a modular deep learning framework for post-disaster flood, damage, and debris segmentation — leveraging datasets like FloodNet, RescueNet, and SpaceNet-8.  My focus is on blending satellite imagery, drone footage, and multi-head segmentation models to support FEMA critical infrastructure recovery operations. 

# 🛰️ Hermes AI
*Geospatial Damage Intelligence for a New Era of Disaster Response*

**Hermes AI** is a modular deep learning framework built for **UAV-based damage mapping**, **flood segmentation**, and **infrastructure resilience assessment** in post-disaster scenarios. Leveraging high-resolution aerial imagery and satellite data, Hermes integrates multi-head semantic segmentation models to automate damage detection at scale for use by FEMA, public agencies, and disaster management contractors.

Hermes is the flagship project of **GEMS AI**, a Florida-based emergency tech company focused on applying computer vision, AI, and GIS to real-world disaster relief operations.

---

## 🌪️ Why Hermes?

In the critical hours after a hurricane, flood, or earthquake, the ability to rapidly map structural damage and flooded roads can mean the difference between chaos and coordinated response.

Traditional damage assessments are:
- **Slow**: Manual field inspections can take weeks.
- **Subjective**: Paper-based PDA systems vary across jurisdictions.
- **Inaccessible**: Delays in data centralization and sharing.

Hermes solves this by:
- Using UAVs and satellite imagery to **detect damage autonomously**.
- Integrating **multi-class segmentation models** to label water, debris, roofs, and structural failure.
- Fusing with GIS to allow **real-time, map-based visualization** for response teams and agencies.

---

## 🧠 Core Architecture

Hermes AI uses a multi-task, multi-head architecture where each model performs a specific geospatial task:

| Sub-Model        | Task                                      | Dataset           | Backbone         |
|------------------|-------------------------------------------|-------------------|------------------|
| `FloodNetHead`   | Flood segmentation                        | FloodNet, SpaceNet8 | DeepLabV3+ (ResNet-101) |
| `DamageNetHead`  | Building damage classification (none/minor/major/destroyed) | xBD, RescueNet    | DeepLabV3+       |
| `DebrisNetHead`  | Road debris segmentation                  | Custom UAV labels | UNet             |
| `FireNetHead`    | Burn scar detection (WIP)                 | FireNet, MODIS    | EfficientNet     |

All models are modular and can be run **individually or as an ensemble**, depending on the deployment scenario.

---

## 🧪 Key Features

✅ Multi-task segmentation (flood, damage, debris)

✅ Pre-/post-event change detection (using dual inputs)

✅ UAV + Satellite compatibility (.tif, .jpeg, .png)

✅ Google Colab A100-ready training notebooks

✅ Export to GeoTIFF and ArcGIS integration

✅ Designed for on-site field operation via local inference or cloud-streamed inputs

---
