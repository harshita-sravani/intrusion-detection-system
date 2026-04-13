# Intrusion Detection System (ML-Based)

## Overview
This project implements a machine learning-based intrusion detection system using the UNSW-NB15 dataset. It follows a multi-stage pipeline to detect and classify network attacks with improved recall and interpretability.

## Project Structure
- app.py — Main execution script  
- load_data.py — Data loading and preprocessing  
- taskA_binary_baseline_no_id.py — Baseline binary classification model  
- taskB_stage2_attack_only.py — Stage-2 classifier for attack-focused detection  
- taskC_feature_selection_binary.py — Feature selection and optimization  
- train_stageB_math_model.py — Probabilistic classification model  
- UNSW_NB15_training-set.csv — Training dataset  

## Approach
- Designed a two-stage intrusion detection pipeline:
  - Stage 1: Binary classification (normal vs attack)
  - Stage 2: Focused refinement for attack detection
- Implemented Random Forest and probabilistic modeling techniques
- Applied threshold tuning (0.3 vs 0.5) to improve recall
- Performed feature importance analysis and top-k feature selection

## Tech Stack
- Python  
- NumPy  
- Pandas  
- scikit-learn  

## Results
- Improved recall for attack detection through threshold tuning  
- Reduced feature space while maintaining model performance  
- Achieved efficient and interpretable classification  

## How to Run
pip install -r requirements.txt  
python app.py  

## Dataset
UNSW-NB15 dataset is used for training. The dataset included here can be replaced with the full dataset if needed.

## Future Improvements
- Real-time intrusion detection system  
- Deployment using Flask or Streamlit  
- Integration with network monitoring systems  
