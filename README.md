
Credit Card Fraud Detection



dataset link:-  https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud


1. Library Imports:
   - Libraries used include numpy , pandas for data handling, matplotlib, and `seaborn` for visualization, and plotly for interactive plots. scikit-learn is employed for data splitting.

2. Data Loading and Initial Inspection:
   - The dataset, creditcard.csv, is loaded into a DataFrame.
   - Memory usage and dataset shape are printed, showing a memory usage of approximately 67.36 MB*and a shape of  (284,807 rows, 31 columns).

3. Data Splitting:
   - The data is split into authentic (non-fraud) and fraudulent transactions.
   - The dataset is further split into training, validation, and testing sets with train_test_split.

4. Visualization:
   - Pie charts display the distribution of authentic and fraudulent transactions across training, validation, and test sets.
   - Histograms and feature visualizations include:
     - Time and Hour Histograms to observe transaction distributions over time.
     - Amount transformation with a logarithmic scale for better feature distribution visualization.

5. Feature Engineering and Selection:
   - New features like day, hour, minute, and second are created from the Time feature.
   - Certain features are dropped, including Time and Amount.
   - Selected features for modeling include columns like V4, V11, V12, and Hour.

 6. Anomaly Detection Model:
   - A density-based anomaly detection method is used to model the probability distribution of features.
   - Functions normal_density and normal_product are defined for calculating density.
   - Model Training: Mean and standard deviation are calculated for training data.

7. Model Evaluation and Optimization:
   - A function to tune the model threshold alpha using the F2-score is implemented.
   - Optimal threshold  alpha  identified for validation data is `0.009` with an F2-score of 0.834.

 8. Testing and Metrics:
   - The model's predictions on the test set are evaluated using metrics like:
     - Accuracy: ~99.67%
     - Precision: ~79.84%
     - Recall: ~82.11%
     - F1-score: ~80.96%
     - MCC (Matthews correlation coefficient): High, indicating robust model performance.
   - A Confusion Matrix visualizes true/false positive/negative rates.

9. Conclusion:
   - Final runtime and memory usage are reported, indicating  343 seconds  and  601.33 MB  of memory usage.
