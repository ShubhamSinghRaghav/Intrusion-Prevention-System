# Intrusion-Prevention-System ![image](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue) ![image](https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white)

## Introduction
IPS are placed in-line and are able to proactively prevent intrusions that are detected. More precisely, IPS can take actions such as dropping malicious packets, sending alarms, resetting the connection, correcting transmission errors, cleaning unwanted network and transport layer options.

## Design
This IPS comprises of two classifiers. Level 1 classifier is time constrained i.e. main concern is over classification of attacks within set amount of time & Level 2 classifier is free to run in its normal time of execution. 
- Level 1 classifier used here is [Decision Tree](https://scikit-learn.org/stable/modules/tree.html).
- Level 2 classifier used here is [Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html).

## Dataset
 This dataset has nine types of attacks, namely, Fuzzers, Analysis, Backdoors, DoS, Exploits, Generic, Reconnaissance, Shellcode and Worms. The Argus, Bro-IDS tools are used and twelve algorithms are developed to generate totally 49 features with the class label.
 [download](https://cloudstor.aarnet.edu.au/plus/index.php/s/2DhnLGDdEECo4ys) 
 
 - For Binary Classification

![plot](https://github.com/ShubhamSinghRaghav/Intrusion-Prevention-System/blob/main/UNSW_NB15-IPS/plots/Binary%20classification.png)
 
 - For Multiclass Classification

![plot](https://github.com/ShubhamSinghRaghav/Intrusion-Prevention-System/blob/main/UNSW_NB15-IPS/plots/Multiclass%20classification.png)

### Models used & their performance
- Binary Classification

|Selection of Model| ML Model  | Accuracy | Precision  | Recall | F1-Measure  | Execution time(s) |
|-| ------------- | ------------- |------------- | ------------- |------------- | ------------- |
|| Logistic Regression | 0.97 |  0.98 | 0.98 | 0.98 | 0.00267  |
||Naïve Bayes |0.74 |0.87| 0.75| 0.76| 0.01101|
|| KNN | 0.98| 0.98| 0.98| 0.98| 4.270561|
|Quick to execute |Decision Tree |0.98 |0.98 |0.98| 0.98 |0.00444|
|Accuracy is high |Random Forest| 0.98| 0.98| 0.98| 0.98| 0.04627|
||AdaBoost |0.98 |0.98 |0.98 |0.98 |0.07368|
||SVM-linear |0.97 |0.98 |0.98 |0.98 |0.75300|
||SVM-rbf| 0.97 |0.98 |0.98 |0.98 |1.50678|
||SVM-sigmoid |0.94 |0.94 |0.94 |0.94 |2.85291|

- Multiclass Classification 

|Selection of Model| ML Model  | Accuracy | Precision  | Recall | F1-Measure  | Execution time(s) |
|-| ------------- | ------------- |------------- | ------------- |------------- | ------------- |
| |Logistic Regression |0.97 |0.97 |0.97 |0.97 |0.00763 |
| |Naïve Bayes |0.95 |0.95 |0.95 |0.95 |0.04636|
| |KNN |0.97 |0.97 |0.97 |0.97 |17.2074|
|Quick to execute  |Decision Tree| 0.97| 0.97| 0.97| 0.97| 0.00661|
| Accuracy is high|Random Forest| 0.97| 0.97| 0.97| 0.97| 0.07719|
| |AdaBoost| 0.75| 0.63| 0.75| 0.67| 0.22904|
| |SVM-linear| 0.97| 0.97| 0.98| 0.97| 1.26248|
| |SVM-rbf| 0.97| 0.97| 0.98| 0.97| 2.14475|
| |SVM-sigmoid |0.97 |0.96 |0.97 |0.96 |2.64214|

`Decision Tree is choosen for L1 Classifier because its quick execution whereas Random Forest is used for L2 Classifier because of high accuracy.`

## IPS ( 2 level Classifier)
- Working of Phase 1 of IPS

![plot](https://github.com/ShubhamSinghRaghav/Intrusion-Prevention-System/blob/main/Models-Phases/phase1.png)

- Working of Phase 2 of IPS

![plot](https://github.com/ShubhamSinghRaghav/Intrusion-Prevention-System/blob/main/Models-Phases/phase2.png)

### Performance metrics of model is 
- Binary Classification

| ML Model  | Accuracy | Precision  | Recall | F1-Measure  | 
| ------------- | ------------- |------------- | ------------- |------------- |
|DT(L1)| 0.981| 0.98| 0.98| 0.98|
|RF(L2)| 0.982| 0.98| 0.98| 0.98|

- Multiclass Classification

| ML Model  | Accuracy | Precision  | Recall | F1-Measure  | 
| ------------- | ------------- |------------- | ------------- |------------- |
|DT(L1)| 0.970| 0.97| 0.97| 0.97|
|RF(L2)| 0.972| 0.97| 0.97| 0.97|


### References
- W. Seo and W. Pak, ”Real-Time Network Intrusion Prevention System 
Based on Hybrid Machine Learning,” in IEEE Access, vol. 9, pp.
46386-46397, 2021, doi: 10.1109/ACCESS.2021.3066620.

- Kamaldeep, M. Dutta and J. Granjal, ”Towards a Secure Internet of
Things: A Comprehensive Study of Second Line Defense Mechanisms,”
in IEEE Access, vol. 8, pp. 127272-127312, 2020

- For diagrams of phases created with BioRender.com



