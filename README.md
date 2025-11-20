# 🔋 Digital Synthesis of Battery Electrode Microstructure

This research focuses on **data-driven microstructure generation and inverse modeling** for lithium-ion battery electrodes.  
The project was developed as part of my work as a **Research Assistant at Northern Illinois University (NIU)**.  
It combines electrochemical simulation, deep learning, and generative modeling to establish a complete *simulation → prediction → generation* pipeline.

---
## 📁 Project Structure
```Digital-synthesis-of-Battery-electrode-microstructure/
├── Composite electrode.ipynb           # PyBaMM-based DFN simulation for composite electrodes  
├── Graphite anode electrode.ipynb      # Simulation for single-electrode cases  
├── VAE 1.ipynb                         # Variational Autoencoder for pore and solid components  
├── VAE 2.ipynb                         # Variational Autoencoder for pore, graphite, silicone and CBD components    
├── Conditional VAE 1.ipynb             # CVAE with conditional inputs as pore and solid component percentages
├── Conditional VAE 2.ipynb             # CVAE with conditional inputs as pore, graphite, silicone and CBD component percentages
└── README.md                           # Project overview
```

---

## 🎯 What This Project Does
This study explores how **machine learning and electrochemical modeling** can be combined for digital synthesis of battery electrodes.  
We developed an **inverse design framework** that predicts and regenerates electrode microstructures based on performance metrics.

- **PyBaMM** simulates electrochemical performance data (voltage, overpotential, temperature).  
- **RNNs** predict electrode properties such as porosity or voltage response from simulation data.  
- **VAE/CVAE models** generate realistic microstructures conditioned on these parameters.

---

## ⚙️ Model Components

### 🧪 PyBaMM Simulations
- Built on the **Doyle–Fuller–Newman (DFN) model**.  
- Simulates charge–discharge behavior by varying design parameters (porosity, C-rate, etc.).  
- Extracted outputs: voltage profiles, temperature, concentration, and overpotential data.

### 🤖 RNN-Based Prediction Models
- Implemented **SimpleRNN**, **LSTM**, and **GRU** architectures using TensorFlow/Keras.  
- Trained to predict voltage and porosity trends from simulation outputs.  
- Forms the *inverse prediction layer* between electrochemical and structural domains.

### 🧠 VAE / CVAE Generative Models
- VAE: baseline microstructure regeneration from electrode datasets.  
- CVAE: enables *conditional generation* based on physical parameters (dataset-dependent).  
- Includes advanced training for clearer reconstructions.

---

## 🔍 Key Findings
- Demonstrated a **complete inverse design pipeline** linking simulation → ML prediction → generative modeling.  
- CVAE successfully generated microstructures reflecting realistic electrode morphology.  
- RNNs achieved high predictive performance (R² ≈ 0.98) on PyBaMM-simulated data.  
- Enables **digital synthesis** of microstructures tuned by performance characteristics.

---

## 🛠 How to Run
1. Open Jupyter Notebook.  
2. Run simulation notebooks (`Composite electrode.ipynb` or `Graphite anode electrode.ipynb`).  
3. Train RNN notebooks for prediction tasks.  
4. Train VAE/CVAE notebooks for image generation.  
5. Visualize results.

---

## 💡 Tools & Frameworks
- **Python**, **TensorFlow/Keras**, **PyBaMM**, **NumPy**, **Matplotlib**, **scikit-learn**, **VGG16 (perceptual loss)**  
- Jupyter Notebooks for experimentation and visualization



---

## 📜 License
This repository is shared for academic and research purposes only.

