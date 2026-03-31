# AT&T SMS Spam Detection Project

This project aims to develop an effective spam detection model for SMS messages, utilizing machine learning techniques to accurately classify incoming messages as either legitimate (ham) or spam. The model will be deployed to automatically flag spam messages in real-time for AT&T's SMS service.

## Dataset

The dataset used for this project is the "SMS Spam Collection" containing 5,572 SMS messages labeled as ham (legitimate) or spam. The data was preprocessed to handle encoding issues, remove duplicates, and engineer relevant features.

## Methodology

1. **Exploratory Data Analysis (EDA)**
   - Analyzed class distribution, message length, word frequency, and special character usage
   - Identified key differences between ham and spam messages using statistical tests and visualization

2. **Preprocessing**
   - Tokenized messages and built vocabulary
   - Scaled numerical features extracted during EDA
   - Applied TF-IDF vectorization for machine learning models
   - Created custom dataset for LSTM model with padding and encoding

3. **Modeling**
   - Logistic Regression (baseline)
   - XGBoost with GridSearch (improvement)
   - LSTM neural network

4. **Evaluation**
   - Focused on F1-score, Precision, and Recall due to class imbalance
   - Compared performance across all three models

## Results

| Model                | F1-score | Precision | Recall |
|----------------------|----------|-----------|--------|
| Logistic Regression  | 0.964    | 1.000     | 0.931  |
| XGBoost              | 0.966    | 0.966     | 0.966  |
| LSTM                 | 0.903    | 0.955     | 0.857  |

The XGBoost model achieved the highest F1-score of 0.966, demonstrating its effectiveness in accurately identifying spam messages while minimizing false positives.

## Conclusion

This project showcases a comprehensive data science workflow for developing a robust SMS spam detection model. The XGBoost classifier, with its strong performance, is suitable for deployment in AT&T's production environment to automatically flag incoming spam messages.

## Next Steps

- Enhance the LSTM model by integrating handcrafted features with embeddings
- Test the improved LSTM on new, unseen SMS data to validate robustness
- Monitor model performance over time to detect concept drift
- Analyze misclassified messages to refine feature engineering and improve detection accuracy

## Repository Structure

- `notebooks/`: Jupyter notebooks for EDA, preprocessing, modeling, and evaluation
- `README.md`: Project overview and documentation

Feel free to explore the code and notebooks for more detailed implementation and analysis.

## Author
Mounia Tonazzini, Agronomist and data scientist

