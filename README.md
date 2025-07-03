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

## 📊 Sample Visuals
---![Screenshot 2025-07-03 081125](https://github.com/user-attachments/assets/bdeb7e5a-6113-47aa-a7c5-05abef653c51)
![Screenshot 2025-07-03 081147](https://github.com/user-attachments/assets/b1cce08f-50cc-4565-a537-e8fc77fe7d7c)
![Screenshot 2025-07-03 081218](https://github.com/user-attachments/assets/db707dcb-1bff-4c83-a8ac-e4160d104a56)

Dataset :
![Screenshot 2025-07-03 083919](https://github.com/user-attachments/assets/e7e58482-9412-4a47-b2b7-8d52745bb97d)
![Screenshot 2025-07-03 084314](https://github.com/user-attachments/assets/341af1a2-12bc-4df2-bac2-456ebaba61ed)

Analysis:
![Screenshot 2025-07-03 083954](https://github.com/user-attachments/assets/5c3613c9-832c-41a8-a68a-97dc3abb4601)

Flowchart:
![Screenshot 2025-07-03 084042](https://github.com/user-attachments/assets/129b453b-17a3-41f2-b614-a8989466fe0a)

Architecture Diagram:
![Screenshot 2025-07-03 084016](https://github.com/user-attachments/assets/489fb314-1a1f-407a-bd73-7311108bfaee)



