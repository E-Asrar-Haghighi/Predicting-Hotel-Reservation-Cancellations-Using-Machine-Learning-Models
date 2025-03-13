# Predicting-Hotel-Reservation-Cancellations-Using-Machine-Learning-Models
## *Project Summary*
This project aimed to predict hotel reservation cancellations using machine learning techniques, with a focus on understanding the factors influencing cancellations and optimizing prediction performance.

The dataset used in this project was obtained from Kaggle, a well-known platform for open datasets and machine learning projects. The dataset, titled Hotel Reservations Classification Dataset, is publicly available and structured as a CSV file, making it easy to load and process using Python's pandas library. Since it is publicly accessible, no additional data collection or web scraping was required.

The analysis revealed that certain factors, such as lead time, online market segment, high average room price, and summer season, significantly increased the likelihood of cancellations. In contrast, special requests, offline bookings, winter season, and discounts were associated with lower cancellation risks.

We employed five machine learning models: Logistic Regression, Decision Tree Classifier, Support Vector Machine (SVM), Random Forest Classifier, and Gradient Boosting Classifier. Among these, the Gradient Boosting Classifier consistently outperformed the others, achieving an accuracy of 84.1% and an ROC-AUC score of 88.9%, demonstrating its superior predictive capabilities.

To validate model performance, we applied 5-Fold Cross-Validation, which confirmed the reliability and stability of the Gradient Boosting Classifier across different data subsets.

Addressing the issue of class imbalance was crucial, and the application of SMOTE (Synthetic Minority Over-sampling Technique) effectively increased recall from 67.54% to 74.80%, aligning with the project's goal of minimizing missed cancellations. Although there was a slight decline in precision, the improved recall was deemed a worthwhile trade-off.

Further optimization was achieved through threshold adjustment, where lowering the threshold to 0.4 enhanced recall to 79.91%, facilitating better detection of potential cancellations. This adjustment supports more proactive cancellation management, assisting hotels with staffing, room allocation, and revenue planning.

The study's insights have practical implications for hotel management. Strategies like dynamic pricing, targeted marketing, and channel optimization were identified as effective measures to reduce cancellation rates. Specifically:

Dynamic Pricing and Discounts: Offering discounts during high-risk periods, such as summer, can reduce cancellations.
Targeted Marketing: Engaging repeat guests and those with special requests can enhance booking reliability.
Channel Optimization: Promoting offline and corporate bookings can further reduce cancellation rates.
The project also faced challenges such as class imbalance, which we addressed using SMOTE to generate synthetic samples for the minority class. This technique helped create a more balanced dataset, enabling the models to better capture patterns across different classes. Additionally, feature engineering and normalization played crucial roles in improving model performance by transforming raw data into meaningful inputs. To prevent overfitting, we applied 5-Fold Cross-Validation to evaluate model performance across different data subsets. The hyperparameter tuning process involved adjusting parameters like max_depth and min_samples_split, which control model complexity and reduce the risk of overfitting. While this process required significant computational resources, the resulting improvements in recall and model generalization justified the effort.

In conclusion, the SMOTE-balanced, hyperparameter-tuned Gradient Boosting Classifier was identified as the most effective model for predicting hotel reservation cancellations. With high recall, stable performance, and insightful feature relevance, this model offers valuable predictive capabilities for hotel management.

Future research could explore real-time model retraining and integration with reservation systems to enhance predictive performance and adapt to evolving booking behaviors.
