# **Home Credit Default Risk Analysis**

![Home Credit](https://img.shields.io/badge/Home%20Credit-Machine%20Learning-brightgreen)  
> Predicting customer default risk using machine learning to minimize loan defaults and improve credit approval efficiency.

---

## 📋 **Project Overview**
This project analyzes real-world financial data from Home Credit, aiming to build predictive machine learning models for identifying customers' ability to repay loans. By minimizing default risks and improving operational efficiency, the project supports informed decision-making for credit approvals.

---

## 🚀 **Key Objectives**
1. **Risk Mitigation**: Predict potential defaults to minimize financial losses.
2. **Efficiency Improvement**: Streamline the credit approval process with automation and insights.
3. **Business Insights**: Derive actionable insights for loan management strategies.

---

## 🛠️ **Project Workflow**
1. **Exploratory Data Analysis (EDA)**  
   - Identified patterns, correlations, and outliers in the dataset.  
   - Visualized data distributions and feature relationships.

2. **Data Preprocessing**  
   - Handled missing values, outliers, and duplicated data.  
   - Performed feature engineering and transformation.  
   - Addressed class imbalance using techniques like undersampling and SMOTE.

3. **Model Development**  
   - Trained and evaluated models:  
     - Logistic Regression  
     - Random Forest  
     - Light Gradient Boosting Machine (LightGBM)  
     - Extreme Gradient Boosting (XGBoost)  
   - Optimized model performance with hyperparameter tuning.

4. **Business Recommendations**  
   - Automated risk-based decision-making to reduce manual workload.  
   - Monitored false negatives to ensure high-risk cases are not overlooked.

---

## 🧰 **Technologies Used**
- **Programming Language**: Python  
- **Libraries**:  
  - **EDA & Visualization**: Pandas, Matplotlib, Seaborn  
  - **Machine Learning**: Scikit-learn, XGBoost, LightGBM  
- **Development Environment**: Jupyter Notebook  

---

## 📊 **Key Results**
- **Best Model**: Random Forest with undersampling and hyperparameter tuning.  
  - **Train Recall**: 67.5%  
  - **Test Recall**: 66%  
- Identified key predictors of loan defaults:  
  - **DAYS_INSTALLMENT**: Days until installment payment.  
  - **PAYMENT_TO_BALANCE_RATIO**: Ratio of payments to balance.  
  - **UTILIZATION_RATE**: Customer's credit usage percentage.  
- Proposed automation strategies to minimize risks and improve operational efficiency.

---

## 📈 **Business Recommendations**
1. **Automation**:  
   - **IF TARGET = 1** → Auto-reject loan application.  
   - **IF TARGET = 0** → Conduct manual review every 4 months.
2. **Focus on False Negatives**:  
   - Ensure robust monitoring of high-risk cases undetected by the model.
3. **Default Rate Management**:  
   - Provide credit limits based on customer repayment capabilities.  
   - Continuously track patterns of defaulted loans.

---

## 📂 **Repository Structure**
```plaintext
├── data/                    # Dataset files
├── notebooks/               # Jupyter Notebooks for EDA, preprocessing, and modeling
├── docs/                    # Full Project documentation
├── Final Presentation.pdf   # Project Presentation
├── README.md                # Project documentation
```

---

## 🔗 **Data Source**
- **Home Credit Default Risk Dataset**  
  - [Application Train Data](https://www.kaggle.com/competitions/home-credit-default-risk/data)  
  - [Other Datasets can be found on data/]

---

## 🧑‍💻 **Team Members**
This project was completed by **Team Conexus**:
- **Abrar Hidayat**: Data Analyst  
- **Anggun Dwi**: Data Scientist  
- **Benedict Caesario**: Data Scientist  
- **Bramantyo Raka (Lead)**: Project Leader  
- **Pra Setiawan Silaen**: Business Intelligence  
- **Siti Nur Afifah**: Business Intelligence  
- **Tommy Septians**: Data Scientist  

---

## 📬 **Connect with Us**
- [Abrar Hidayat](https://www.linkedin.com/in/abrar-hidayat)  
- [Anggun Dwi](https://www.linkedin.com/in/anggundwilestari)  
- [Benedict Caesario](https://www.linkedin.com/in/benedict-c-975754223)  
- [Bramantyo Raka](https://www.linkedin.com/in/bramaraka666)  
- [Pra Setiawan Silaen](https://www.linkedin.com/in/pra-setiawan-silaen-b44870281)  
- [Siti Nur Afifah](https://www.linkedin.com/in/siti-nurafifah)  
- [Tommy Septians](https://www.linkedin.com/in/tommy-septians)

---

## 🏆 **Acknowledgments**
This project was inspired by real-world problems faced by financial institutions and leveraged machine learning to deliver impactful solutions. Special thanks to Home Credit and the open-source community for providing the dataset.

---

## ⚠️ **License**
This project is for educational purposes only. Data and code should not be used for commercial purposes without proper authorization.
