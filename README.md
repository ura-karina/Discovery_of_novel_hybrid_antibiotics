# Chemical Space Exploration and Reinforcement Learning for Discovery of Novel Benzimidazole Hybrid Antibiotics

Benzimidazole hybrids represent a promising class of therapeutic agents due to their pronounced antibacterial properties. However, the growing threat of antibiotic resistance underscores the necessity for novel compounds with improved antimicrobial activities. Our project aims to address this challenge by leveraging artificial intelligence (AI) to generate novel antibacterial compounds focusing on benzimidazole derivatives.

## Project Objectives

- **Dataset Creation**: We curated a comprehensive dataset of benzimidazole hybrids to explore their chemical space and identify the most promising scaffolds.
- **Model Training**: An interpretable machine learning model was trained to predict the bioactivity of benzimidazole hybrids, achieving an R² of 0.81 on the test set.
- **Compound Generation**: Using reinforcement learning (RL), we generated novel hybrid antibiotics via three approaches: fragment-based, linker-based, and de novo generation.
- **Candidate Selection**: Promising candidates were selected based on bioactivity, off-target effects, and other key drug criteria.

## Project Implementation

### Data Collection

We collected data on benzimidazole hybrids from open scientific sources. The dataset includes features such as:
- Molecular structures
- Minimum inhibitory concentrations (MICs)
- Lipinski's Rule of Five and Three compliance
- QED Score
- ADMET properties

### Data Preprocessing

- **Feature Engineering**: Generated new descriptors such as molecular fingerprints and physicochemical properties to enhance predictive modeling.
- **Cleaning and Imputation**: Missing values were filled using the KNN method.
- **Normalization**: Scaled numerical features for better model performance.

### Model Training

An interpretable machine learning model was developed to predict the bioactivity of benzimidazole hybrids. The model was validated using standard metrics and achieved high accuracy, with an R² of 0.81 on the test set. Feature importance analysis provided insights into key determinants of antibacterial activity.

### Compound Generation

- **Fragment-Based Approach**: Combined bioactive fragments to create new compounds.
- **Linker-Based Approach**: Utilized linkers to connect functional groups and form novel hybrids.
- **De Novo Generation**: Designed new molecules from scratch using generative models.

### Candidate Evaluation

Generated compounds were evaluated based on:
- Bioactivity: Predicted using the trained model.
- Off-Target Effects: Assessed to minimize undesirable interactions.
- Drug-Likeness: Evaluated using QED and Lipinski’s rules.
- Binding Affinity: Compared to approved antibiotics to ensure enhanced protein targeting.

### Results

The process yielded 56 novel, synthetically feasible compounds with:
- Reduced minimum inhibitory concentrations.
- Improved QED scores.
- Minimized off-target effects.

## Data Visualization

- **Chemical Space Exploration**: Visualized using t-SNE and PCA.
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

- `Data/`: Contains the dataset used in this project.
- `Scripts/`: Scripts for compound generation using RL.
- `Visualizations/`: Plots and figures for data analysis and model interpretation.

---
