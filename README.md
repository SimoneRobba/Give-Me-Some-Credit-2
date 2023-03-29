# Give-Me-Some-Credit-2
Classify good borrowers with pipeline, APA, hyperparameter tuning, k-fold cross-evaluation, lr, svc, Adaboost


# Overview
In this work, the dataser regarding the credit provision is used again. The goal is not only implement a set of different models to predict the default of a potential borrower, but to select the best Hyperparameter among a set provided.

Three models are tested:

- Logistic Regression (LR)
- Support Vector Machine (SVM),
- Ada Boost with Decision Tree (TREE) as base classifier

Each classifier is incorporated in a pipeline that first standardize the features, then extract them in a set of Principal Components (PC). The pipeline then undertake a Grid Search analysis to evaluate the best hyperparametes. For each model, one or two hyperparameters are set as variable, and a set of values is evaluated for each of them. The performance of each model is estimated through accuracy score with a K-fold cross-validation technique. Finally, the performance of the models, with the relative selected hyperparameters, is calculated on the test dataset.

Logistic Regression Hyperparameters evaluated:

- Penalty (l1, l2)
- C: (0.001, 1, 10, 100.0)
- Test accuracy: Test accuracy: 0.985 (C: 0.001 Penalty: l1)

Support Vector Machine Hyperparameters evaluated:

- Kernel: linear
- C: (0.001, 100)
- Test accuracy: 0.985 (C: 0.001)

Ada Boost

- estim_range:(10, 100, 500)
- max_depth: (1, 2, 3)
- Test accuracy: 0.985 (estimators: 10 max_depth: 1)
