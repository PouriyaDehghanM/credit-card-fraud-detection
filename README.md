# 💳 Credit Card Fraud Detection with LightGBM

This repository features a high-performance, end-to-end pipeline designed to detect fraudulent credit card transactions. The project leverages effective **Feature Engineering**, **LightGBM** for classification, and manages extreme class imbalance through **cost-sensitive learning**.

---

## ✨ Key Features

*   **⏳ Temporal Feature Engineering**: Extracts rolling window statistics (e.g., transaction count and mean over the last 24 hours) and time-delta features.
*   **📍 Geospatial Analysis**: Calculates the Euclidean distance between cardholder and merchant locations to identify suspicious movements.
*   **⚖️ Imbalance Handling**: Utilizes the `scale_pos_weight` parameter in LightGBM to effectively tackle the scarcity of fraud cases.
*   **🏷️ Advanced Encoding**: Applies ordinal encoding for high-cardinality categorical features such as `Merchant` and `Job`.

---

## 🛠 Tech Stack

*   **Language:** Python
*   **Data Manipulation:** Pandas, NumPy
*   **Preprocessing & Metrics:** Scikit-Learn
*   **ML Model:** LightGBM (Gradient Boosting Framework)

---

## 🔍 Feature Engineering Details

The heart of this project is the `add_features` function, which transforms raw transaction data into high-signal variables:

| Feature | Description |
| :--- | :--- |
| **`trans_count_24h`** | Number of transactions made by the same user in the last 24 hours. |
| **`seconds_from_last_transact`** | Time elapsed since the user's previous transaction. |
| **`dist`** | Spatial distance between the user's home coordinates and the merchant. |
| **`age`** | The cardholder's age at the exact time of the transaction. |

---

## 📈 Performance & Logic

The model is fine-tuned with a high precision threshold of **0.8** to minimize false positives, which is vital for maintaining customer trust in financial systems.

---

For the dataset, email me ==> pouriyadehghan666@gmail.com
