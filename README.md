# machine-learning-challenge
By Ai-Jiuan Wu

I experimented with  5 models to classify exoplanets into 3 classes: 1) Confirmed, 2) False positive or 3) Candidate.

The models used included the following:

Model_1: Multi-Variable Linear Regression
- Experiment with a non-classification model to see what the accuracy is and will be the negative control for all subsequent classification models (Models 2 to 5).
- GridSearch was not used to tune the model parameter.
- R2 score for Training Data: 0.499
- R2 score for Testing Data: 0.476
- CONCLUSION: Multi-Variable Linear Regression is a poor model for classification data.

Model_2: Logistic Regression
- GridSearch was not used to tune the model parameter.
- R2 score for Training Data: 0.632
- R2 score for Testing Data: 0.624
- CONCLUSION: Logistic Regression is a poor model for Exoplanet classification.

Model_3: Random Forest
- Experimented with the model by eliminating features where the feature importance is less than 0.01, 0.02, 0.03 and 0.04 (see Ln 16).  
- The model that gave the best R2 score was when features were eliminated that were less than 0.02.  
    - R2 score for Training Data: 1.0
    - R2 score for Testing Data: 0.881
- The model was further tuned using GridSearch (see Ln 17 - 19).  The tuning did NOT improve the R2 score.
    - R2 score for Training Data: 0.889
    - R2 score for Testing Data: 0.879
- CONCLUSION: Random Forest is a good model for Exoplanet classification.
    
Model_4: K Nearest Neighbor
- GridSearch was not used to tune the model parameter.  Instead a for loop was created to experiment vary number of neighbors from 1 to 40 by 2 (see Ln 13).  
- R2 score for Training Data: 0.878
- R2 score for Testing Data: 0.871
- CONCLUSION: K Nearest Neighbor is a good model for Exoplanet classification.

Model_5: Support Vector Machine
- GridSearch was used to tune the model parameter.
- R2 score for Training Data: 0.864
- R2 score for Testing Data: 0.844
- CONCLUSION: Support Vector Machine is a good model for Exoplanet classification.

OVERALL CONCLUSION: RANDOM FOREST or MODEL 3 IS THE BEST MODEL FOR CLASSIFICATION OF EXOPLANET.  IT CAN PREDICT WITH ~88% ACCURACY WITH K_NEAREST NEIGHBOR or MODEL_4 AT 87%.  MORE DATA WITH RELEVANT FEATURES (EX. ELIMINATE FEATURES WITH FEATURE IMPORTANCE OF LESS THAN 0.3) SHOULD FURTHER IMPROVE THE MODEL MORE.   
