# Intrusion Detection System (ML-Based)

## Overview
This project implements a machine learning-based intrusion detection system using the UNSW-NB15 dataset. The system is designed to classify network traffic as normal or malicious using a multi-stage pipeline, improving detection performance and interpretability.

## Problem Statement
Modern networks are vulnerable to various cyber attacks such as DoS, exploits, and reconnaissance. Traditional detection systems struggle with evolving attack patterns, making it necessary to develop adaptive machine learning-based intrusion detection systems.

## Project Structure
- app.py — Main execution script  
- load_data.py — Data loading and preprocessing  
- taskA_binary_baseline_no_id.py — Baseline binary classification model  
- taskB_stage2_attack_only.py — Stage-2 classifier for refined attack detection  
- taskC_feature_selection_binary.py — Feature selection and optimization  
- train_stageB_math_model.py — Probabilistic classification model  

## Approach
- Designed a two-stage intrusion detection pipeline:
  - Stage 1: Binary classification (normal vs attack)
  - Stage 2: Focused refinement for attack detection
- Used Random Forest and probabilistic modeling techniques
- Applied threshold tuning (0.3 vs 0.5) to improve recall
- Performed feature importance analysis and top-k feature selection

## Pipeline
Data → Preprocessing → Feature Selection → Model Training → Prediction

## Tech Stack
- Python  
- NumPy  
- Pandas  
- scikit-learn  

## Results
- Improved recall for attack detection using threshold tuning  
- Built a two-stage model improving detection reliability  
- Reduced feature space while maintaining performance  
- Achieved interpretable predictions using feature importance  

## Sample Output
- Classifies network traffic as normal or attack  
- Provides probability-based predictions  
- Handles imbalanced data through threshold optimization  

## How to Run
pip install -r requirements.txt  
python app.py  

## Dataset
The project uses the UNSW-NB15 dataset, which contains modern network traffic with multiple attack categories such as DoS, exploits, and reconnaissance. The dataset is not included in this repository due to size constraints and can be downloaded separately.

## Future Improvements
- Real-time intrusion detection system  
- Deployment using Flask or Streamlit  
- Integration with network monitoring systems  
- Extension to multi-class attack classification  
