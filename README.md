# Autonomous-Vehicle-Weather-Simulation
Developed a realistic autonomous driving simulation using CARLA to evaluate sensor reliability (Camera, LiDAR, Radar) under fog, storm, and rainy-night scenarios.
# 🧠 Autonomous Vehicle Simulation in Adverse Weather

This project simulates and evaluates the performance of autonomous vehicle sensors (Camera, LiDAR) under adverse weather conditions like fog, storm, and rainy nights using the [CARLA Simulator](https://carla.org/).  
The goal is to analyze how different deep learning models respond to visual degradation and improve driving policy prediction using preprocessing techniques and model fusion.

---

## 🚗 Project Overview

- Simulator: **CARLA 0.9.13**
- Weather Presets: `Fog`, `Heavy Rain`, `Rainy Night`, `Storm`, `Sunny Day`
- Sensors Used: 4 RGB Cameras + 1 LiDAR
- Total Dataset: **26GB** | **12,500+ frames**
- Labels: Steering, Throttle, Speed, Collision, Trajectory, Lane Info

---

## 🛠️ Tools & Technologies

- **Python 3.8**, **PyTorch**
- **CARLA Simulator**, **Ubuntu**
- **NumPy**, **Pandas**, **OpenCV**
- **FLARE VM**, **VMware** (for related cyber experimentation)
- **GAN & CLAHE** for image restoration

---

## 🧪 Models Compared

| Model              | Description                        | Parameters | Preprocessing | Completion Rate |
|-------------------|------------------------------------|------------|---------------|------------------|
| Advanced CNN       | ResNet-based controller             | ~25M       | GAN + Denoising| >75%             |
| CNN + CLAHE        | Basic CNN with enhanced input       | ~10M       | CLAHE         | ~71%             |
| TransFuser++       | Sensor-fusion transformer           | ~15M       | Raw + Fusion  | ~74%             |
| ReasonNet          | LSTM-based sequence model           | ~8M        | Smoothed RGB  | ~70%             |
| Simple TransFuser  | Lightweight transformer             | ~5M        | None          | ~67%             |

---

## 🎯 Key Results

- **Storm scenario** was most challenging: poor visibility, motion blur
- **GAN preprocessing + Advanced CNN** achieved the best real-time inference
- Trained on **DGX A100** and tested on **RTX 3060**, avg inference < 100ms

---

## 📊 Sample Visuals

> _(Add 2–3 images or a `.gif` from your presentation/PDF showing model output, weather scenes, etc.)_  
> You can use: `/media/weather_fog.png`, `/media/output_model.gif`

---

## 📁 Repository Structure

```bash
├── data/               # Sample preprocessed dataset (small version)
├── models/             # Trained weights or architecture scripts
├── preprocessing/      # CLAHE, GAN scripts
├── evaluation/         # Accuracy, route-completion analysis
├── media/              # Screenshots, graphs, demo GIFs
└── README.md           # This file
