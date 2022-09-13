# Credit_Risk_Analysis
Supervised Machine Learning and Credit Risk


### Overview

In this analysis machine learning is used to solve a credit card risk challenge. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Different techniques are used to train and evaluate models with unbalanced classes. First, the data is oversampled using the _*RandomOverSampler*_ and SMOTE algorithms, and undersampled using the ClusterCentroids algorithm. Then a combinatorial approach of over-and undersampling is used with the SMOTEENN algorithm. Next, machine learning models are used that reduce bias - BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

### Tools Used

  - imbalanced-learn & scikit-learn libraries
  - RandomOverSampler, SMOTE, ClusterCentroids & SMOTEEN algorithms
  - BalancedRandomForestClassifier & EasyEnsembleClassifier
  - Python 3.7 & Pandas Library
  - Jupyter Notebook

### Results

  #### Naive Random Oversampling

  - Balanced Accuracy Score: 62.5%
  
  <img width="341" alt="NRO_BAS" src="https://user-images.githubusercontent.com/104603128/189970411-1ecc96ce-20fc-4983-badd-d45619703146.png">

  
  - Precision 1% & Recall score 60% for high_risk with f1 score of 2%
  - Precision 100% & Recall score 65% for low_risk with f1 score of 80%. This is due to the high number of low_risk population.  
    
  <img width="502" alt="NRO_ICR" src="https://user-images.githubusercontent.com/104603128/189970470-1e800786-6396-427e-9275-524d3e604437.png">

  
  #### SMOTE Oversampling
  
   - Balanced Accuracy Score: 65.1%
   
   <img width="485" alt="SO_BAS" src="https://user-images.githubusercontent.com/104603128/189971175-1a693636-0789-43eb-b07a-33f8cd4ddaeb.png">

   
   - Precision 1% & Recall score 64% for high_risk with f1 score of 2%
   - Precision 100% & Recall score 66% for low_risk with f1 score 80%
    
   <img width="494" alt="SO_ICR" src="https://user-images.githubusercontent.com/104603128/189971774-993814a0-e468-4067-bb06-6d3a9b498072.png">

     
  #### Cluster Centroids Undersampling
  
   - Balanced Accuracy Score: 51%
   
   <img width="511" alt="US_BAS" src="https://user-images.githubusercontent.com/104603128/189972415-ea8754ee-6fdd-47d3-8c55-a19d7adbca0a.png">

   
   - Precision 1% & Recall score 59% for high_risk with f1 score of 1%
   - Precision 100% & Recall score 43% for low_risk with f1 score of 60%
    
   <img width="503" alt="US_ICR" src="https://user-images.githubusercontent.com/104603128/189972599-855cedc3-e52b-44bd-b6f6-dc4ba45fe7b6.png">

 
  #### SMOTEENN Combination Sampling

  - Balanced Accuracy Score: 65%

  <img width="500" alt="CSS_BAS" src="https://user-images.githubusercontent.com/104603128/189974494-5e30ab78-e5c2-4ac2-8001-c4d180e3639c.png">

    
   - Precision 1% & Recall score 72% for high_risk with f1 score 2%
   - Precision 100% & Recall score 58% for low_risk with f1 score 73%
   
   <img width="497" alt="CSS_ICR" src="https://user-images.githubusercontent.com/104603128/189974624-f9adec5b-0992-48c5-94b5-8d6cda7bed9d.png">

   
  #### Balanced Random Forest Classifier
  
   - Balanced Accuracy Score: 78.8%
  
   <img width="502" alt="BRFC_BAS" src="https://user-images.githubusercontent.com/104603128/189982293-9365c2bc-9769-4c55-8ca5-e8282814a267.png">

   
   - Precision 4% & Recall score 67% for high_risk with f1 score 7%
   - Precision 100% & Recall score 91% for low_risk with f1 score 95%
 
   <img width="496" alt="BRFC_ICR" src="https://user-images.githubusercontent.com/104603128/189982480-d04295d3-300c-4a72-9f18-43a7e11cf4dd.png">

     
  #### Easy Ensemble Classifier
  
  - Balanced Accuracy Score 92.5%
  
  <img width="506" alt="EEC_BAS" src="https://user-images.githubusercontent.com/104603128/190007855-ad9b8171-cbff-4cf3-bf6e-4cea58d10f51.png">

  
  - Precision 7% & Recall 91% for high_risk with f1 score 14%
  - Precision 100% & Recall 94% for low_risk with f1 score 97%

  <img width="535" alt="EEC_ICR" src="https://user-images.githubusercontent.com/104603128/190007899-f72051b6-9b0f-4413-8606-cff5f74f57c1.png">



### Summary

  - While Easy Ensemble Classifier model shows an accuracy of 92.5% all other models show a relatively low accuracy indicating they are not good at classifying the credit risk.
  - For Easy Ensemble Classifier model the precision for high_risk group is low, indicating a large number of false positive, which indicates an unreliable positive classification. The recall is high for both the groups indicating a small number of false negatives.
  - Overall out of all the models Easy Ensemble Classifier performed best but still produced a large number of false positives with a low f1 score of 14% because of these reasons none of the models can be recommended for use in a real world situation.
