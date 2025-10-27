# Digital synthesis of battery electrode microstructure

This repository includes all the code implementations developed during my work as a Research Assistant at Northern Illinois University, focused on data-driven microstructure generation and inverse modeling for lithium-ion battery electrodes.


It integrates three key components:

1. **VAE and CVAE Models**  
   - Variational Autoencoder (VAE) and Conditional Variational Autoencoder (CVAE) architectures for regenerating electrode microstructures.  
   - The CVAE enables *controlled generation* of microstructures conditioned on relevant physical or structural parameters depending on the dataset.

2. **PyBaMM Simulations**  
   - Generation of electrochemical data using the **DFN model** in PyBaMM by varying key design parameters such as porosity, C-rate, or other electrode-specific factors.  
   - Extracted data include voltage, overpotentials, and concentration profiles.

3. **RNN-Based Prediction Models**  
   - Recurrent Neural Network (RNN), LSTM, and GRU models trained to predict electrochemical or structural properties from PyBaMM-simulated data.  
   - Enables inverse design by linking battery performance metrics with electrode structure.


This work demonstrates an **end-to-end inverse design pipeline**:
- PyBaMM simulates battery performance data.  
- RNN models predict structural or material properties.  
- CVAE models regenerate realistic electrode microstructures based on predicted parameters.  

Together, these models enable **digital synthesis of electrode microstructures** that reflect the underlying electrochemical behavior.
