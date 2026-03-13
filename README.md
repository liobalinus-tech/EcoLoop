# EcoLoop: AI-Powered Waste Classification & Carbon Tracking

EcoLoop is an AI system built to advance climate action (UN SDG 13) by bridging the gap between waste identification and environmental impact. It uses Computer Vision to classify waste and calculates its carbon footprint in real-time.

## Key Features
- **Object Detection:** Powered by **YOLOv8 Nano** for efficient, real-time material classification.
- **Carbon Engine:** Maps detected waste to **Life Cycle Assessment (LCA)** data via a modular JSON backend.
- **Production-Ready:** Decouples AI weights from business logic for easy updates to environmental standards.

## Technical Stack
- **Language:** Python 3.12
- **Framework:** Ultralytics YOLOv8
- **Dataset Management:** Roboflow (1,228 annotated images)
- **Infrastructure:** Kaggle GPU (Training)

## Methodology
The system follows a modular architecture:
1. **Vision Engine:** Identifies material classes (Metal, Plastic, Paper, Biodegradable).
2. **Logic Layer:** Applies the formula $E = m \times C_f$ to estimate $CO_2$ equivalents.
3. **Data Layer:** Uses a `carbon_factors.json` file to ensure the system remains scientifically current without retraining.

## Performance
- **mAP:** High mean Average Precision achieved over 50 training epochs.
- **Efficiency:** Optimized for edge deployment using the Nano architecture.

## Project Structure
- `models/`: Contains the trained `best.pt` weights.
- `notebooks/`: The complete training and validation pipeline.
- `data/`: LCA-based carbon factors in JSON format.

---
*Developed as a Capstone Project for the Women Techsters Fellowship (Data Science & Engineering Track).*
