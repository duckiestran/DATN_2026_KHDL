# Fraud Detection Project Documentation

## Project Overview
This project aims to develop a comprehensive fraud detection system using machine learning techniques. The goal is to identify fraudulent transactions in various domains, ensuring safety and security in financial operations.

## Dataset Information
The dataset used for this project is sourced from Google Drive and contains various features crucial for identifying fraudulent activities. It includes:
- **Transaction ID**: Unique identifier for each transaction
- **Amount**: Transaction amount
- **Timestamp**: Date and time of the transaction
- **User ID**: Identifier for the user making the transaction
- **Merchant ID**: Identifier for the merchant associated with the transaction
- **Is Fraud**: Label indicating whether the transaction is fraudulent

Link to the dataset: [Google Drive Dataset](#)

## Setup Instructions
1. **Clone the repository**:
   ```
   git clone https://github.com/duckiestran/DATN_2026_KHDL.git
   cd DATN_2026_KHDL
   ```
2. **Install dependencies**:
   ```
   pip install -r requirements.txt
   ```
3. **Download the dataset** from Google Drive and place it in the `data` directory.
4. **Run the application**:
   ```
   python main.py
   ```

## Features
- Real-time fraud detection
- User-friendly interface
- Detailed transaction reports
- Customizable threshold settings for fraud detection

## Model Architecture
The fraud detection system leverages machine learning models such as:
- Logistic Regression
- Decision Trees
- Random Forests
- Neural Networks

These models are trained on historical transaction data and tested for accuracy.

## Usage Guidelines
- Upon running the application, users need to input transaction details to check for fraud.
- The system will return a prediction of whether the transaction is fraudulent or not.
- Users can adjust the model parameters as needed to improve detection rates.

## Conclusion
This fraud detection system is a valuable tool for organizations looking to minimize financial losses and enhance security protocols. Through continuous learning and model updates, it aims to adapt to emerging fraudulent patterns.

---