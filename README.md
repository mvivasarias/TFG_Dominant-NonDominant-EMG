# TFG_Dominant-NonDominant-EMG

This repository contains the complete code, data, and statistical analysis used in the final-year biomedical engineering thesis titled:

**"Comparison of EMG signals between dominant and non-dominant arms during elbow flexion-extension movements"**  
Universidad CEU San Pablo – Grado en Ingeniería Biomédica

---

## Overview

The study investigates neuromuscular differences between the dominant and non-dominant upper limbs using surface electromyography (sEMG) and inertial data collected via the mDurance system. The pipeline includes:

- Synchronization of EMG and IMU data
- Segmentation of movement cycles into flexion/extension and acceleration/deceleration phases
- Extraction of Range of Motion (ROM), Coactivation Coefficients (CC), and muscle synergy metrics
- Statistical analysis using R (paired tests, ANOVA, and graphical outputs)

---

## Files included

- `TFG_Alg.ipynb`  
  Jupyter notebook in Python used to process raw EMG and joint angle signals exported from mDurance. It performs segmentation, synchronization, and computes neuromuscular metrics such as ROM, CC, and muscle synergies.

- `TFG_Analysis.Rmd`  
  R Markdown file used for statistical analysis. It includes data import from Excel, preprocessing, normality and outlier testing, as well as paired comparisons and repeated-measures ANOVA for between-arm and between-load conditions.

- `MduranceDataParticipantsData.xlsx`  
  Final results spreadsheet containing all processed and structured metrics used for statistical analysis. Each row corresponds to a unique combination of subject, arm (dominant/non-dominant), load condition, movement phase (acceleration/deceleration), and computed values (e.g., ROM, CC, synergy metrics).

---

## Tools and versions

- Python 3.9  
- Jupyter Notebook 6.4.5  
- RStudio 4.5.0  
- Main packages: `numpy`, `pandas`, `matplotlib`, `scipy`, `scikit-learn`, `ggplot2`, `dplyr`, `ez`, and custom implementations of NMF

---

## Metrics extracted

- **Range of Motion (ROM)**: computed dynamically using angular data from the IMU signal  
- **Coactivation Coefficient (CC)**: quantifies the simultaneous activation of antagonist muscles during different movement phases  
- **Muscle synergies**: estimated using Non-negative Matrix Factorization (NMF) to identify low-dimensional patterns of coordinated muscle activation  
- **Statistical analysis**: comparisons between arms, loads, and movement phases using non-parametric and parametric tests

---

## Citation

If you reference this repository in academic work:

> Vivas Arias, M. (2025). *Comparison of EMG signals between dominant and non-dominant arms during elbow flexion-extension movements* [Bachelor's thesis, Universidad CEU San Pablo]. GitHub. https://github.com/mvivasarias/TFG_Dominant-NonDominant-EMG

---

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.


