---
layout: post
title: "1.5 Evaluating Model Performance"
date: 2026-03-21 12:00:00 -0800
categories:
   - machinelearning
---

Metrics are indicators if a model is performing well or poorly. They also signal if one must change the hyperparameters to continue training iterations. Accuracy metrics include: Accuracy, Precision, Recall, F1 score, and Area under the ROC curve

Accuracy is the fraction of correct over total predictions. For binary classifications, accuracy is calculated with true positives (TPs), true negatives (TNs), false positives (FPs), and false negatives (FNs) with the formula: Accuracy = (TP + TN) / (TP + TN + FP + FN). Note that with highly imbalanced datasets, accuracy is not a good metric to assess performance becaus the model can predict majority classes and still retain high accuracy.

Precision is an alternative accuracy measurement that quantifies only the TPs and FPs with the formula: Precision = TP / (TP + FP). This method is used when fewer FPs are desired.

Recall highlights model sensitivity by quantifying the positive predictions made out of all the actual positives. This is given by: Recall = TP / (TP + FN). Use this method when false positives are fine, but you want fewer false negatives.

F1 score is a  combination of precision and recall given by: F1 = 2 * ((Precision * Recall) / (Precision + Recall). This works well for imbalanced data.

Area under the ROC curve (AUC) measures accuracy and visualizes prediction rankings across true and false positive rates. If false positives matter more, optimizing on AUC is the preferred approach. An AUC score of 0.5 indicates that the model is no better than a random guess, while scores deviating away closer to 0 or 1 indicate the model is worse and better than a random guess, respectively.

Additional evaluation metrics include logarithmic loss (log loss), which gives uncertainty for model predictions by penalizing the assignment of low probabilities to the correct classes. The confusion matrix which creates an N X N matrix, where N is the number of categories to predict. Regression metrics including Mean Absolute Error, Mean Squared Error, Root Mean Squared Error, Root Mean Squared Logarithmic Error, and R-squared (R^2) metrics. An R^2 value close to 1 indicates that the model effectively explains most of the data variance. Clustering metrics include silhouette score and the Davies-Bouldin Index. 

The confusion matrix is a table summarizing prediction results for a classification model. Incorrect and correct predictions are summarized with count values and divided by class, giving more guidance for model errors. It shows the TP, FP, FN, and TN in a 2 x 2 matrix. This information may be presented as an actual matrix or a visual diagram for intuition. One may use the values provided and the formulae above to calculate accurracy, precision, recall, and F1 score for a particular data set. Confusion matrices can be expanded to three or more class values by adding additional rows or columns. 

Metrics indicate how well a model is performing and if hyperparameters need tweaking. Regression metrics include R^2, mean squared error, root mean square error, and mean absolute error. R^2 calculates differences between actual values and model predictions. The difference between these values is the "residual" and is key to assess model performance.

While R^2 is a relative measure, MSE and RMSE are absolute measures showing how much a predicted value deviates from the actual number. Mean absolute error (MAE) is a direct representation of sum of error predictions. It is given by: MAE = sumof(actual_j - predict_j) / (total_predict). MAE is used to determine how close predictions are to actual values on avearge. A lower MAE value indicates better predictions, and vice versa for larger MAEs. MSE and RMSE indicates if the model has large errors in predictions higher/lower than the actual values. 

Finding the most important features is key to predicting a desired target in an ML model. Each feature impacts the final prediction, but some features are more equal than others. The goal is to find the important features to reduce computational cost and time with better predictions. Retraining the model for those important features can make the model easier to explain, since it is usually a black box, and boosts confidence in the model. 

Some models, like tree-based methods from Scikit-learn, random forest, and gradient boost already incorporate feature importance. Using the attribute feautre, "feature_importances_" shows feature relevance visually, and the number of the most important features may be selected. One may retrain the model with only those features and assess the differences in model performance. After retraining the model, one may re-calculate the regression metrics to assess if training using the trimmed features is better than the older model. Remember that using fewer features is better because it corresponds with less overfitting and higher generalization by eliminating undesired noise and biases.

It is important to consider and combat bias when training an ML model. If the model does not know there are other types of data in the world, it cannot predict them, and will freak out when it encounters that new data. An example is if an ML model is trained to recognize turtles and fish in the training data only, but is then given a seabird to classify. It will not know how to classify that data.

Bias can show up in the raw data, the algorithm, or the model if there is an imbalance or does not accurately represent the deployed environment. This is where collaboration helps to find problems early than ML engineers cannot reasonably be expected to account for. Algorithmic bias is also an important factor. One may play with different algorithms to find the ones with better performance. XGBoost tends to outperform other algorithms, but the selected algorithm should be consistent with the needs of your project. Bias can also appear in models as the relationship between target variables drift, or change over time. An example is ademographic shift in a regional area as wealthier people more towards or away from the area, this will have an effect on the features, and affect model accuracy. Weighting features may be helpful to combat such biases.
