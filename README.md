# Chemical Space Exploration and Reinforcement Learning for Discovery of Novel Benzimidazole Hybrid Antibiotics

Benzimidazole hybrids represent a promising class of therapeutic agents due to their pronounced antibacterial properties. However, the growing threat of antibiotic resistance underscores the necessity for novel compounds with improved antimicrobial activities. Our project aims to address this challenge by leveraging artificial intelligence (AI) to generate novel antibacterial compounds focusing on benzimidazole derivatives.

## Project Objectives

- **Dataset Creation**: We curated a comprehensive dataset of benzimidazole hybrids to explore their chemical space and identify the most promising scaffolds.
- **Model Training**: An interpretable machine learning model was trained to predict the bioactivity of benzimidazole hybrids, achieving an R² of 0.81 on the test set.
- **Compound Generation**: Using reinforcement learning (RL), we generated novel hybrid antibiotics via three approaches: fragment-based, linker-based, and de novo generation.
- **Candidate Selection**: Promising candidates were selected based on bioactivity, off-target effects, and other key drug criteria.

## Project Implementation

### Data Collection

We collected a dataset of 419 benzimidazole hybrids, containing molecular structures represented in SMILES format and experimental MIC against *E. coli* for each molecule. After preprocessing, the resulting dataset included 326 samples. The dataset includes features such as: 
- Molecular structures
- Minimum inhibitory concentrations (MICs)
- Lipinski's Rule of Five
- QED Score
- ADMET properties



### Data Preprocessing

- **Feature Engineering**: Generated new descriptors such as molecular fingerprints and physicochemical properties to enhance predictive modeling.
- **Cleaning and Imputation**: Missing values were filled using the KNN method.
- **Normalization**: Scaled numerical features for better model performance.

### Model Training

An interpretable machine learning model was developed to predict the bioactivity of benzimidazole hybrids. The model was validated using standard metrics and achieved high accuracy, with an R² of 0.81 on the test set. Feature importance analysis provided insights into key determinants of antibacterial activity.

### Chemical Space Analysis

To identify the most promising starting scaffolds for further generation, we analyzed the chemical space of benzimidazole hybrids. Molecules were represented as a TMAP and colored based on their corresponding lgMIC values.

### Compound Generation

To ensure diversity and novelty, three distinct approaches were employed:

1. **Fragment-Based Generation**:
   - FREED++ was used to design new molecules with benzimidazole as the starting scaffold to reduce the risk of cross-resistance.
   - 11,277 unique molecules were generated, with 30 best candidates selected based on criteria including QED > 0.3, Docking Score for gyrase A and B ≤ -11, SAscore < 4, MIC < 0.01, and compliance with the Brenk filter.

2. **De Novo Molecular Generation**:
   - FREED++ was used without a predefined starting fragment, allowing free exploration of the chemical space.
   - 12,763 unique molecules were generated, with 15 benzimidazole-containing molecules selected using the same constraints.

3. **Linker Design**:
   - Libinvent and REINVENT4 were used to design novel linkers between benzimidazole and quinoline scaffolds.
   - 125 new scaffolds were created, filtered for QED > 0.3, SAscore < 4, and docking scores ≤ -11. One promising scaffold with the lowest docking scores was further optimized using FREED++, generating a library of nearly 9,006 unique molecules.

### Candidate Evaluation

Generated compounds were evaluated based on:
- **Bioactivity**: Predicted using the trained model.
- **Drug-Likeness**: The average QED score of 0.39 for generated molecules suggests an improvement over literature compounds.
- **Synthetic Accessibility**: The average SAScore of 3.28 indicates that generated molecules remain within the acceptable range for bioactive compounds.
- **Antibacterial Activity**: The distribution of logMIC values shows that generated molecules are predominantly more active, with significantly lower MIC values compared to the collected dataset.
- **Chemical Space Novelty**: The mean Tanimoto similarity of 0.21 highlights the novelty of generated molecules, further supported by their separation in UMAP plots.

### Results

The process yielded 56 novel, synthetically feasible compounds with:
- Reduced minimum inhibitory concentrations.
- Improved QED scores.
- Minimized off-target effects.

## Data Visualization

- **Chemical Space Exploration**: Visualized using TMAP.
- **Feature Importance**: Highlighted through SHAP values.
- **Comparative Analysis**: Displayed as heatmaps and scatterplots comparing generated compounds with approved antibiotics.

## Key Findings

- Generated molecules exhibit better binding affinities to their target proteins compared to approved antibiotics.
- The RL-based approaches effectively balance synthetic feasibility and bioactivity.
- The interpretable ML model provides actionable insights into designing next-generation benzimidazole hybrids.

## Conclusion

Our project demonstrates the potential of AI in accelerating the discovery of novel antibacterial agents. By integrating data-driven approaches and generative models, we successfully generated compounds with promising therapeutic profiles, contributing to the fight against antibiotic resistance.

---

### Repository Structure

- `data/`: Contains the dataset used in this project.
- `scripts/`: Scripts for compound generation using RL.
- `visualizations/`: Plots and figures for data analysis and model interpretation.

---
