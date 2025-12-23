# A123-LFP-Cell-Model
A123 Cell SPM model
# Single Particle Model (SPM) for LFP Cell using PyBaMM

This repository contains the development, calibration, and validation of a **Single Particle Model (SPM)** for a **Lithium Iron Phosphate (LFP)** lithium-ion cell using **PyBaMM**.  
The model is based on the **Prada et al. (2013)** experimental dataset, corresponding to a cell with a nominal capacity of approximately **2.3 Ah**.

---

## Project Overview

The objective of this work is to:
- Develop an **SPM-based electrochemical model** for an LFP/graphite cell
- Calibrate key electrochemical parameters using **experimental voltage data**
- Validate model performance during **charging and discharging** conditions

---

## Cell Chemistry

- **Positive electrode:** LiFePO₄ (LFP)
- **Negative electrode:** Graphite
- **Nominal capacity:** ~2.5 Ah
- **Model framework:** Single Particle Model (SPM)

Since the Prada (2013) dataset does not provide an explicit open-circuit potential (OCP) function for LFP, the **LFP OCP formulation from Afshar et al. (2017)** is used.

---

## 📊 Experimental Data Used

- **Discharge voltage–capacity data at 1C rate (~2.5 A)**  
  Used to match the voltage performance of the model during discharge.
  
- **Charge voltage performance data**  
  Used together with discharge data for **model calibration**, ensuring consistency during both charging and discharging.

The voltage performance data is utilized to calibrate the model parameters such that the simulated voltage response closely matches the experimental behavior.

## Other Files Description

- **HPPC_protocol_retractor.ipynb**  
  Contains helper functions to extract a charging protocol compatible with **PyBaMM**.  
  The output of this notebook is the file:  
  `HPPC_PyBaMM_Experiment_with_Timing.xlsx`

- **LFP_2.5Ah_V1_code.pdf**  
  PDF version of the Jupyter Notebook with **all cells fully executed**.

- **LFP_2.5Ah_V1_documentation.pdf**  
  Provides the **overall project documentation**, including modeling approach, assumptions, and results.


## ▶️ How to Run the Model

- **Download the complete project folder and ensure all files are present, including the Jupyter notebook `LFP_2.5Ah_V1.ipynb` and beginning_of_life.xlsx test data.**
---


## Requirements

- Python ≥ 3.9
- PyBaMM
- Replace Prada2013.py with the existing Prada file in the saurce code
Install required packages using:
```bash
pip install pybamm numpy matplotlib scipy






