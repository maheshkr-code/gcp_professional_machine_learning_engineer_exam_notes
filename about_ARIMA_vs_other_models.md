In BigQuery, the **ARIMA** model (specifically implemented as ARIMA_PLUS) is used for Time Series Forecasting. It allows you to predict future values based on historical data using standard SQL, without needing to write Python code or perform complex statistical manual adjustments.


</br>
>>> Since you are studying for the PMLE exam, it is critical to note that BigQuery does not use standard vanilla ARIMA. It uses a proprietary algorithm called ARIMA_PLUS.
>>>
>>> <img width="840" height="295" alt="image" src="https://github.com/user-attachments/assets/74b94a1e-624f-4509-b6e1-5de6d27de17c" />

**Question: ** </br>
Your company sells corporate electronic products globally and stores historical customer data in BigQuery. You need to build a model that predicts customer lifetime value (CLV) for the next three years. You want to use the simplest and most straightforward approach to achieve this. What should you do?
ANS: No, ARIMA is not the correct model for this specific requirement.

Why ARIMA fails for CLV
------------------------

**The Nature of the Problem:**

-- ARIMA is a Time Series tool. It answers: "Based on the history of this line, where will the line go next?" (e.g., Stock prices, Temperature).

-- CLV is a Regression problem. It answers: "Based on this customer's age, location, and first 3 purchases, how much will they spend in total?"

**The "New Customer" Problem:**

ARIMA requires a long history of data points to detect a pattern.

-- A new customer might only have 1 or 2 transactions. ARIMA cannot predict a trend from 2 points. Regression models, however, can look at other customers who behaved similarly to predict this new customer's future.

**The "Churn" Factor:**
-- ARIMA assumes the pattern continues. If a customer buys monthly, ARIMA assumes they will keep buying monthly forever.
CLV models need to account for the probability that a customer stops buying (churns), which ARIMA doesn't inherently model well.

</br>

<img width="858" height="311" alt="image" src="https://github.com/user-attachments/assets/d908e683-549d-4881-bd26-18d1f1a0e64b" />
