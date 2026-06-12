# Binary-Classification-of-Mammogram-Images
In this project, we performed binary classification on mammogram images using the VinDr- Mammo dataset. The goal was to classify mammograms into two categories: normal (BI- RADS 1) and abnormal (BI-RADS 2 to 5). Our approach involved a series of data preprocessing, model selection, and evaluation steps to predict whether a mammogram.

Methodology:
1. Data Collection and Preprocessing:
 The dataset used in this project was the VinDr-Mammo dataset. It contains images and
corresponding annotations that define whether a mammogram is normal or abnormal.
 Data Preprocessing Steps:
o We cleaned the data by handling missing values and ensuring that only relevant
features (such as breast-level annotations and image paths) were retained.
o The dataset was split into training and testing sets using a 70-30 split, ensuring
that the training data was sufficient for model training.
o Feature scaling was applied to ensure that all features were on the same scale,
which is important for algorithms like SVM and k-NN.
2. Handling Imbalanced Data:
 Initially, the dataset had an imbalanced distribution, with a majority of normal cases
(BI-RADS 1) and a smaller number of abnormal cases (BI-RADS 2 to 5).
 To address this, we used SMOTE (Synthetic Minority Over-sampling Technique) to
balance the classes in the training dataset by generating synthetic samples of the
minority class (abnormal).
 The SMOTE method increased the minority class to match the majority class, improving
the model's ability to detect abnormalities without overfitting.
3. Model Selection:
We experimented with multiple models to select the best performing one for this binary
classification task:
 Logistic Regression (LR): A simple yet powerful model for binary classification.
 Support Vector Machine (SVM): Known for its effectiveness in high-dimensional
spaces and small sample sizes.
 Decision Tree (DT): A non-linear model that provides easily interpretable results.
 Random Forest (RF): An ensemble method using multiple decision trees to improve
performance.
 k-Nearest Neighbors (k-NN): A simple and intuitive model that classifies based on the
majority label of the nearest neighbors.
Each model was trained on the resampled dataset (after SMOTE) to ensure a balanced class
distribution during training.
4. Model Evaluation:
 For model evaluation, we used a variety of metrics to assess the performance, with
special emphasis on recall due to its importance in identifying abnormal cases (false
negatives are costly in medical diagnostics).
 Metrics used:
o Accuracy: Percentage of correct predictions.
o Precision: Ability of the model to identify only relevant samples for abnormal
cases.
o Recall: Ability of the model to correctly identify abnormal cases.
o F1 Score: Harmonic mean of precision and recall.
o Confusion Matrix: To visualize the model’s true positives, false positives, true
negatives, and false negatives.
5. Confusion Matrix:
The confusion matrix was used to show the performance of the model. We observed:
 True positives (TP) and false negatives (FN) for abnormal cases (BI-RADS 2-5).
 True negatives (TN) and false positives (FP) for normal cases (BI-RADS 1).
6. Model Performance Comparison:
 After training the models, we compared their performance using the evaluation metrics.
The comparison showed that Logistic Regression outperformed other models in terms of
recall and F1 score, making it the best model for this task.
7. Training Procedure:
 We optimized the models by tuning hyperparameters, such as the number of trees in the
random forest and the kernel type in the SVM. This allowed us to select the best
configuration for each model.
 Afterward, each model was evaluated on the test set to assess its performance and
ensure it could generalize effectively, avoiding overfitting to the training data.
Conclusion:
In this project, we focused on developing a binary classification model to predict the presence of
abnormalities in mammogram images from the VinDr-Mammo dataset. The primary objective
was to accurately classify mammograms as either normal (BI-RADS 1) or abnormal (other BI-
RADS categories), using machine learning models trained on the breast-level annotations.
Throughout the project, we followed a structured methodology that included data preprocessing,
feature scaling, model selection, and performance evaluation. The dataset was cleaned to
remove irrelevant or missing data, and relevant features such as breast-level annotations and
image paths were retained. The data was split into training and testing sets using a 70-30 split,
ensuring that the models had sufficient data to train on while leaving a sizable test set for
validation.
We applied various machine learning algorithms, including Logistic Regression, SVM, Decision
Tree, Random Forest, and k-NN. Each model was carefully evaluated using key performance
metrics such as recall, F1 score, accuracy, and precision, with a focus on recall as the primary
evaluation criterion. This focus was driven by the task's nature, where detecting abnormalities
(class 1) is more critical than simply achieving overall accuracy.
The performance of the models was compared, and it was found that Logistic Regression
outperformed the others, achieving the highest recall and F1 score. This result is particularly
noteworthy as Logistic Regression is often viewed as a simpler model compared to more
complex ones like Random Forest. However, in this case, its effectiveness can be attributed to
the well-preprocessed data and its ability to create a clear linear decision boundary between the
two classes.
In addition to the core model evaluation, we performed hyperparameter tuning to improve model
performance. For Logistic Regression, we adjusted key parameters such as regularization
strength and solver to enhance the model’s ability to generalize well on unseen data.
Finally, this project demonstrates the importance of proper data preprocessing, feature
selection, and model evaluation in achieving high performance in binary classification tasks.
Logistic Regression's performance underscores the value of a straightforward approach when
the problem is well-defined and the data is clean, showing that more complex models do not
always outperform simpler ones.
In conclusion, Logistic Regression proved to be the most effective model for this task, making it
the ideal choice for this mammogram classification problem.
