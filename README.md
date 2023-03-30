The following program uses a CNN model to classify if a chest x-ray image is healthy or not. This function will be able to differentiate multiclass categories where label names are present: normal, virus, and bacteria. To solve this problem CNN modelling (Convolutional Neural Network) is used, due to its excellent image-splitting ability.

Dataset used:
- The dataset used in this project could be found and installed from the Kaggle link mentioned below, https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia. 
- The entirety of the dataset is approximately 1.3 GB consisting of three sub folders. The constituents and description of these sub folder is mentioned below:  
    This is the main folder which contains 3 main sub folders named test, train and val (validation).  
  - The training dataset is generally the largest dataset as the model needs to be created from the data it provides.  
  - The testing dataset is generally smaller to the training dataset but larger than the validation dataset as this generally provides the accuracy of the model            by testing the model.  
  - The validation dataset generally is the smallest dataset and provides the validation to the model.  

- The training dataset comprises Normal or healthy lungs (1341 images) with the existence of a total of 766 people’s x-rays and Pneumonia or people having unhealthy lungs (3875 images), among which 1345 and 2530 samples for virus and bacteria respectively. There exists singular or multiple x-rays images of individual people. In the second case, there are in total 1945 people’s x-rays. Whereas, the test dataset comprises two output classes such as healthy lungs (234 images) and people having unhealthy lungs (390 images).

- The data is read by the program and then depending on the images’ characteristics the model is made which can now classify if a pair of lungs are healthy or unhealthy and if they are unhealthy then does the person have virus or a bacterial infection. The contents of the validation dataset are used to validate the classifier after it has been made. It could be considered as a part of the training dataset. It usually is not a large dataset. Usually out of a hundred percent 70 percent of the data belongs to the training dataset while the remaining 30 percent usually belongs to the validation set. This sub folder contains two more sub-sub folders such as Normal (8 images) and Pneumonia (8 images). All the images in this sub-sub folder are x-rays of people having healthy and unhealthy lungs (bacteria or virus). It prevents overfitting of the classifier and helps to tune the parameters of the model.

Results:  
- Accuracy, Misclassification rate, Precision, Sensitivity (Recall), Specificity and F1-score can be calculated using the formulae mentioned bellow:
  - Accuracy: (TP + TN) / (TP + TN + FP + FN): 
  - Misclassification rate: (FP + FN) / (TP + TN + FP + FN) or (1 - Accuracy): 
  - Precision: (TP) / (TP + FP):
  - Sensitivity: (TP) / (TP + FN):
  - Specificity: (TN) / (TN + FP):
  - F1-score: (2 x Precision x Sensitivity) / (Precision + Sensitivity) or (2 x TP) / ((2 x TP) + FP + FN):

|Variable:|TP:|TN:|FP:|FN:|Accuracy:|Misclassification rate:|Precision|Sensitivity:|Specificity:|F1-score:|
|--- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ---|
|Bacteria:|230|333|12|49|90.22%|9.78%|95.04%|82.44%|96.52%|88.29%|
|Normal:|170|379|64|11|87.98%|12.02%|72.65%|93.92%|85.55%|81.93%|
|Virus:|109|421|39|55|84.94%|15.06%|73.65%|66.46%|91.52%|69.87%|
|Average (Mean):|||||87.71%|12.29%|80.45%|80.94%|91.20%|80.03%|
