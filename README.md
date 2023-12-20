Project Overview
----------------

This project utilizes raw data from a phone accelerometer to predict one of four actions: idle, stair-walking, running, and walking. In addition to the raw data, 17 time domain features, such as median, power, and entropy, were extracted. The extraction process is detailed in the `read_and_process.ipynb` notebook.

### Analysis

*   **Models Used**:
    *   **Random Forest**: Employed with default hyperparameters.
    *   **Support Vector Machine (SVM)**: Utilized with a Linear kernel.
*   **Evaluation Metric**: Accuracy score.
*   **Cross-Validation**: 5-fold cross-validation was applied. Feature selection was conducted separately within each fold to prevent data leakage.

### Feature Sets

Analyses were conducted on six different sets of features:

1.  **Raw Accelerometer Data**: Directly using the raw data from the accelerometer.
2.  **Extracted Time Domain Features**: Includes features like median, power, and entropy.
3.  **Combined Features**: A combination of both raw data and extracted time domain features.
4.  **Top Features Selected Using RFE**:
    *   Top 10, 20, and 30 features were selected using Recursive Feature Elimination (RFE), based on their importance as determined by the SVM linear model.

### Results

The results of the analyses are presented, comparing the performance across different feature sets.
Using all generated (extracted time domain) features was proven most effective, closely followed by top 20 selected features.

![image](https://github.com/KsaweryKapela/Move_Pattern_Classifier/assets/103521727/f1cd7932-0917-4413-8b9c-30ebd32610f3)

[Uploading image.png…]()

![image](https://github.com/KsaweryKapela/Move_Pattern_Classifier/assets/103521727/2df2be50-295c-400d-bcc0-a2bf9976ff33)
