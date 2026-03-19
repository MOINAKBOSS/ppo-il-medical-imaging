# Reinforced Active Learning with Explainability for Label-Efficient Medical Imaging

This repository provides the implementation of a reinforcement-guided active learning framework that integrates:
- Reinforcement Learning (PPO)
- Imitation Learning (DAgger-style aggregation)
- Explainability-driven insights

for label-efficient medical image classification across CT and X-ray modalities.

---

## 📌 Paper
**Title:** Reinforced Active Learning with Explainability for Label-Efficient Medical Imaging  
**Status:** Under review (IJPRAI 2026)

---

## 🚀 Key Contributions

- Reformulates active learning as a sequential decision-making problem  
- Uses Proximal Policy Optimization (PPO) for adaptive sample selection  
- Incorporates imitation learning (DAgger) for robust classifier refinement  
- Supports cross-modality generalization (CT → X-ray)  
- Demonstrates robustness to label noise  
- Achieves strong performance with less than half of labeled data  

---

## 🧠 Method Overview

Pipeline:

1. Extract features using VGG16 + PCA  
2. Initialize a small mentor set  
3. Train PPO agent to select informative samples  
4. Aggregate selected samples (DAgger)  
5. Train classifier (Logistic Regression / MLP)  
6. Evaluate across CT, X-ray, and unseen datasets  

---

## 📂 Repository Structure
ppo-il-medical-imaging/
├── notebooks/
│ └── patl_rl_extension.ipynb
├── src/
│ └── patl_rl_extension.py
├── README.md
├── requirements.txt
├── .gitignore
