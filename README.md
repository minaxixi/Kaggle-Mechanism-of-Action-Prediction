# Kaggle-Mechanism-of-Action-Prediction
Kaggle competition: Mechanism of Action (MoA) Prediction
 
This is my solution (top 13%) to the Kaggle competition "Mechanism of Action (MoA) Prediction"
https://www.kaggle.com/c/lish-moa

In this competition, I am predicting multiple targets of the Mechanism of Action (MoA) response(s) of different samples (sig_id), given various inputs such as gene expression data and cell viability data.
 
 ## Data
 - 23K rows
 - Features: Anonymized gene features (772 features) and cell features (100 features)
 - Target: Binary label for 206 targets
 
 ## Metrics
 - Multi log-loss
 
 ## Feature engineering pipeline
 - PCA + Variance thresholding
 
 ## Models
 - Feed-forward neural network with 4 hidden layers
 
 ## Training
 - Pretrain using scored (206) + non-scored (403) targets. Then finetune on scored targets
 - 7-fold cross validation
 
 ## Results
 - Private leaderboard: 0.01620 (ranked 556/4373, top 13%)
 
 ## Software package
 - PyTorch on Google Colab
 
