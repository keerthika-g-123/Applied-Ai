ExNO1
Data Set used-heart.csv
Deep Neural Network is a machine learning model inspired by the human brain. It consists of multiple layers of neurons that learn complex patterns from data.
In this experiment, the DNN is used to classify transactions as fraudulent (1) or legitimate (0).
Why DNN?
Because fraud detection requires learning hidden and complex transaction patterns that simple models cannot easily detect.
2. Binary Classification
Binary classification means the model predicts one of two possible classes:
0 → Legitimate Transaction
1 → Fraudulent Transaction
The model outputs a probability score, and a threshold (0.5) decides whether a transaction is fraud or not.
3. Class Imbalance & Class Weighting
The dataset is highly imbalanced, meaning:
Most transactions are non-fraud
Very few are fraud
This can cause the model to ignore fraud cases.
Solution: Class Weighting
Higher weight is assigned to the fraud class, forcing the model to:
Pay more attention to fraud cases
Reduce bias toward majority class
This improves fraud detection accuracy.
4. Feature Scaling (StandardScaler)
Transactions have features with different value ranges.
StandardScaler normalizes features so that:
All inputs have similar scale
The model trains faster and more accurately
This improves training stability.
5. Model Architecture (Layers & Activations)
Input Layer
Receives 30 numerical transaction features
Hidden Layers
128 neurons → ReLU
64 neurons → ReLU
32 neurons → ReLU
ReLU activation helps the model learn non-linear patterns efficiently.
Output Layer
1 neuron → Sigmoid
Produces a probability between 0 and 1
6. Regularization Techniques
Used to prevent overfitting (memorizing instead of learning):
Batch Normalization
Stabilizes learning
Speeds up training
Dropout
Randomly removes neurons during training
Forces the model to learn robust features
7. Optimizer & Loss Function
Adam Optimizer
Efficient optimization algorithm that adjusts learning rate automatically.
Binary Cross-Entropy Loss
Measures the difference between:
True label
Model prediction
Lower loss = better performance.
8. Early Stopping
Training stops when validation loss stops improving.
Benefits:
Prevents overfitting
Saves training time
Keeps best-performing model weights
9. Evaluation Metrics for Imbalanced Data
Accuracy
Measures overall correct predictions
(Not reliable alone for imbalanced data)
ROC-AUC Score
Measures how well the model separates fraud vs non-fraud
Higher value = better discrimination
Precision–Recall AUC
Focuses on fraud detection performance
More useful when fraud samples are rare
Confusion Matrix
Shows:
Correct fraud detection
False alarms
Missed fraud cases
10. Train–Test Split Strategies
Different data splits were tested:
80–20
70–30
60–20–20
70–15–15
This ensures the model performs consistently across different data distributions.
11. Stratified Cross-Validation
Data is split into 5 folds, keeping the fraud ratio constant.
Purpose:
Validate model stability
Reduce dependency on a single train-test split
Ensure reliable results
12. ROC Curve & Precision–Recall Curve
ROC Curve
Shows trade-off between true positive rate and false positive rate
Precision–Recall Curve
Shows balance between precision (correct fraud detection) and recall (catching fraud cases)
Both help visualize model performance.
13. Key Outcome of the Experiment
The model successfully:
Learned fraud patterns
Handled severe class imbalance
Achieved strong ROC-AUC and PR-AUC
Demonstrated stable performance across splits
Improved detection using early stopping and class weighting
If you want, I can also explain:
✅ Key topics in very simple student language
✅ Short exam-ready explanations
✅ Viva questions with answers
