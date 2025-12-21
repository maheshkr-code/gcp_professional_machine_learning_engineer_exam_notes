| Category       | Model Name                    | When to Use                                  | Why (Technical Rationale)                                             | Sample Use Case                                                |
| :------------: | :---------------------------: | :------------------------------------------: | :-------------------------------------------------------------------: | :------------------------------------------------------------: |
| Time Series    | ARIMA\_PLUS                   | You have a single metric tracked over time.  | Automatically handles seasonality, holidays, and outliers.            | Forecasting next month's daily electricity demand.             |
| Time Series    | ARIMA\_PLUS\_XREG             | Time series + external factors.              | Incorporates "outside" variables (e.g., weather) to improve accuracy. | Predicting sales based on history and local weather forecasts. |
| Diagnostics    | CONTRIBUTION\_ANALYSIS        | Explaining the "root cause" of a change.     | Sifts through segments to find exact drivers of a metric shift.       | Explaining why revenue dropped 12% among mobile users.         |
| Classification | LOGISTIC\_REG                 | Fast, simple baseline for labels.            | Highly interpretable; maps data to probabilities (0 to 1).            | Determining if an email is "Spam" or "Not Spam."               |
| Classification | BOOSTED\_TREE\_AS\_CLASSIFIER | Structured data; need top-tier accuracy.     | Uses Gradient Boosting (XGBoost) to learn from previous errors.       | Identifying fraudulent bank transactions.                      |
| Classification | RANDOM\_FOREST\_CLASSIFIER    | Noisy data; want to avoid overfitting.       | Ensemble of decision trees using "majority vote" logic.               | Predicting patient risk tiers based on health metrics.         |
| Classification | DNN\_CLASSIFIER               | Massive datasets; non-linear patterns.       | Deep Neural Networks find hidden relationships in "Big Data."         | Identifying high-value customers from web logs.                |
| Classification | WIDE\_AND\_DEEP\_CLASSIFIER   | Need both memorization and generalization.   | Combines linear models (rules) with deep models (patterns).           | Ranking items in a search result or app store.                 |
| Classification | AUTOML\_CLASSIFIER            | Highest accuracy; no manual tuning.          | Automated Neural Architecture Search (NAS) finds the best model.      | Mission-critical loan default prediction.                      |
| Regression     | LINEAR\_REG                   | Predicting a continuous number (price, etc). | Finds the "best fit" straight line through data points.               | Estimating used car price based on mileage.                    |
| Regression     | BOOSTED\_TREE\_REGRESSOR      | Numerical prediction on tabular data.        | Superior for datasets with "jumps" or non-linear steps.               | Predicting delivery wait times during peak hours.              |
| Regression     | RANDOM\_FOREST\_REGRESSOR     | Robust prediction; ignore outliers.          | Averages many trees to create a stable, reliable output.              | Estimating crop yield based on soil conditions.                |
| Regression     | DNN\_REGRESSOR                | Massive scale; complex targets.              | Best for high-frequency trading or physics simulations.               | Predicting precise energy output of wind farms.                |
| Regression     | WIDE\_AND\_DEEP\_REGRESSOR    | Many categories; need numerical accuracy.    | Excellent for sparse data (many columns with zeros).                  | Predicting "likelihood to pay" scores.                         |
| Regression     | AUTOML\_REGRESSOR             | High-performance; zero manual setup.         | Automated feature engineering and model selection.                    | Predicting annual revenue for global enterprises.              |
| Clustering     | KMEANS                        | Find natural groups in unlabeled data.       | Minimizes distance between points to form segments.                   | Grouping customers into "Budget" vs "Luxury" tiers.            |
| Recommendation | MATRIX\_FACTORIZATION         | User ratings or interaction data.            | Predicts user preferences via latent factor decomposition.            | Recommending movies on a streaming platform.                   |
| Dim. Reduction | PCA                           | Too many columns; need to simplify.          | Condenses high-dimensional data while keeping variance.               | Reducing 1,000 genomic markers into 10 key indicators.         |
| Dim. Reduction | AUTOENCODER                   | Detect anomalies or compress data.           | Learns to rebuild data; failure to rebuild = anomaly.                 | Detecting suspicious patterns in network traffic.              |


</br>

<img width="1525" height="838" alt="image" src="https://github.com/user-attachments/assets/1d5f420b-dc4b-4bcc-96f1-c63d9dd43cae" />
