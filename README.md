# Fraud Detection

This notebook presents a fraud detection model using a dataset available on Kaggle. The dataset contains information about various transactions, including features such as the transaction amount, merchant category code, and transaction type.

## Dataset

- step: maps a unit of time in the real world. In this case, 1 step is 1 hour of time. Total steps 744 (30 day simulation).
- type: CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER. (inbox, outbox, debit, payment and transfer)
- amount: transaction amount in local currency.
- nameOrig: customer who initiated the transaction
- oldbalanceOrg: opening balance before transaction
- newbalanceOrig: new balance after transaction
- nameDest: customer who is the recipient of the transaction
- oldbalanceDest: recipient of the initial balance before the transaction. Please note that there is no information for customers starting with M (Merchants).
- newbalanceDest: new balance recipient after transaction. Please note that there is no information for customers starting with M (Merchants).
- isFraud: Transactions made by fraudulent agents within the simulation. In this particular dataset, agents' fraudulent behavior is aimed at profiting by taking control of customers' accounts and attempting to empty funds by transferring to another account and then withdrawing from the system.
- isFlaggedFraud: The business model aims to control massive transfers from one account to another and flag illegal attempts. An illegal attempt on this dataset is an attempt to transfer more than 200,000 in a single transaction.

## Data Preparation
Before creating the fraud detection model, the data was pre-processed and prepared for training. Some of the data preparation steps included:

- Scaling the transaction amount feature
- Encoding categorical features
- Splitting the dataset into training and testing sets
- Fraud Detection Model
To detect fraudulent transactions, a Random Forest Classifier model was used. The model was trained using the transaction characteristics as independent variables and the class as the dependent variable.

The model was evaluated using classification metrics such as accuracy, precision, recall, and F1 score. The results showed that the model had an accuracy of 99%, indicating that it could accurately detect fraudulent transactions.

## Conclusion
This notebook presented a fraud detection model using a dataset available on Kaggle. The Random Forest Classifier model can accurately detect fraudulent transactions, allowing financial institutions to identify and prevent fraudulent activity.

## Contribution
Contributions are welcome! If you find any bugs or have any suggestions for improvement, please open an issue in the repository or submit a pull request.
a pull request.
