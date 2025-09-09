# Unitree G1 Reinforcement Learning Simulation in Unity

This repository contains the implementation of a reinforcement learning (RL) pipeline for the humanoid robot **Unitree G1**, developed as part of the CloudWalk technical evaluation.  
The project uses **Unity ML-Agents** to simulate humanoid locomotion and train an RL agent (PPO/SAC) to autonomously learn tasks such as walking and obstacle traversal.

---

## 🚀 Features
- Unity environment configured with the **Unitree G1 URDF** (23 DOF).  
- Integration with **Unity ML-Agents** for reinforcement learning.  
- Training pipeline with standard RL algorithms (**PPO / SAC**).  
- Configurable locomotion tasks (e.g., walking, navigation, obstacle traversal).  
- Evidence of experiments: videos, logs, learning curves.  

---

## 🛠️ Setup

### 1. Requirements
- **Unity Editor**: `2022.3.x LTS` (recommended)  
- **Unity ML-Agents**: `Release 20+`  
- **Python**: 3.9+  
- **Packages**:  
  ```bash
  pip install mlagents
  pip install torch numpy matplotlib


2. Clone Repository

git clone https://github.com/<your-user>/unitree-g1-rl-unity.git
cd unitree-g1-rl-unity

⚠️ Development Notes

During the project development, different operating systems and Unity versions were tested:

Ubuntu 20.04 + Unity 3.1 → not functional. The Unity version compatible with this OS is deprecated and no longer supported, leading to instability.

Windows 11 + Unity 6 (6000.x) → Unity 6 is still not fully compatible with the URDF Importer, which is required to load the Unitree G1 model into the environment.

Final Setup → The project was developed on Windows 11 with Unity 2022.3 LTS, which provides stable support for ML-Agents and the URDF Importer.

👉 For best results, it is recommended to use Windows 11 with Unity 2022.3.x LTS and the latest stable version of ML-Agents.

3. Open in Unity

- Launch Unity Hub and open this project.

- Import the URDF Importer and ML-Agents packages.
    [https://github.com/Unity-Technologies/URDF-Importer.gi****](https://github.com/Unity-Technologies/URDF-Importer.git
)

- Place the Unitree G1 URDF under Assets/Robots/G1/.

## 📖 Usage
1. Launch Training
   
mlagents-learn config/g1_rl_config.yaml --run-id=g1-walk-1 --train

2.Inference (Watch Trained Agent)

mlagents-learn config/g1_rl_config.yaml --run-id=g1-walk-1 --inference


## 📊 Results

✅ Agent autonomously learns walking locomotion.

✅ Successfully performs the task consistently.

(to be added: training curves, evaluation metrics, videos)


## 📝 Documentation

ML-Agents Toolkit

Unitree G1 URDF

URDF Importer


## 🔮 Next Steps

Add domain randomization for robustness.

Test more complex behaviors (running, terrain traversal).

Fine-tune hyperparameters for stability and efficiency.


👤 Author

Developed by Arthur Rizzi for CloudWalk Technical Challenge.
