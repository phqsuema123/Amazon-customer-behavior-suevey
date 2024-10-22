
---

# **Amazon Customer Behavior Survey: Cart Abandonment Analysis**  

## **Overview**  
This project aims to explore Amazon customer behavior by analyzing customer interactions, shopping habits, and decision-making patterns on the Amazon platform. The focus is on building a **Cart Abandonment Analysis Model** to predict whether customers will abandon their carts and identify the factors contributing to this behavior.  

---

## **Dataset Information**  
The dataset includes a variety of variables capturing customer demographics, interactions, reviews, and browsing patterns within the Amazon ecosystem. The data contains:  
- **23 columns**  
- **602 rows**  

### **Data Cleaning**  
- Identified and removed 2 missing values from the `Product_Search_Method` column (Rows: 119, 382).  
- Unnecessary column `Timestamp` was removed.  

---

## **Grouping the Data**  
Key variables used to group and analyze customer behavior include:  
- **Gender**  
- **Purchase_Frequency**  
- **Purchase_Categories**  
- **Personalized_Recommendation_Frequency**  
- **Browsing_Frequency**  
- **Add_to_Cart_Browsing**  
- **Cart_Completion_Frequency**  
- **Cart_Abandonment_Factors**  
- **Save_for_Later_Frequency**  
- **Review_Helpfulness**  
- **Recommendation_Helpfulness**

---

## **Model Objective**  
The goal is to build a **Cart Abandonment Analysis Model** using **Random Forest Classifier** to predict whether customers will abandon their carts.  

---

## **Model Building Steps**  

### **1. Data Preparation**  
- **Label Encoding**: Categorical features converted to numerical values.  
- **Data Splitting**: 70% training set, 30% test set.  

### **2. Model Building**  
- **Algorithm**: Random Forest Classifier  
- **Hyperparameters**:  
  - `n_estimators` = 100  
  - `random_state` = 42  

### **3. Model Features**  
1. **Add_to_Cart_Browsing_Gr**  
2. **Personalized_Recommendation_Frequency**  
3. **Product_Search_Method**  
4. **Browsing_Frequency_Gr**  
5. **Customer_Reviews_Importance**  

**Target Variable**: `Abandonment_Gr`  

---

## **Evaluation Metrics**  
- **Accuracy**  
- **Confusion Matrix**  
- **Precision**  
- **Recall**  
- **F1-Score**  

---

## **Results and Performance**  

### **Model Accuracy**  
- **Overall Accuracy**: **48%**

### **Confusion Matrix and Classification Report**  

| **Category**        | **Precision** | **Recall** | **F1-Score** | **Support** |
|---------------------|--------------|-----------|-------------|-------------|
| Decision-related    | 0.36         | 0.39      | 0.37        | 64          |
| Other               | 0.33         | 0.07      | 0.11        | 15          |
| Price-related       | 0.56         | 0.59      | 0.58        | 101         |

- **Macro Average**:  
  - Precision: 0.42  
  - Recall: 0.35  
  - F1-Score: 0.35  

- **Weighted Average**:  
  - Precision: 0.47  
  - Recall: 0.48  
  - F1-Score: 0.47  

---

## **Analysis of Results**  
- **Price-related group**:  
  - Highest **Precision** and **Recall** values, suggesting the model performs reasonably well in predicting this category.  

- **Other group**:  
  - Extremely low Precision and Recall values, possibly due to **insufficient or unbalanced data**.  

- **Overall Accuracy**:  
  - The model achieved **48% accuracy**, indicating that further improvements are needed for better performance.

---

## **Conclusion**  
This project demonstrates the potential of using Machine Learning to analyze cart abandonment behavior. However, with a current accuracy of 48%, the **Random Forest model** requires further tuning and optimization to make more accurate predictions. Possible improvements include:  
- Balancing the dataset to improve predictions for all categories.  
- Exploring other algorithms and feature engineering techniques.  
- Fine-tuning hyperparameters to improve model accuracy.

---

## **Future Work**  
- Experiment with **different algorithms** (e.g., XGBoost, SVM).  
- Use **SMOTE** or other balancing techniques for underrepresented categories.  
- Perform **hyperparameter optimization** using GridSearch or RandomSearch.  
- Analyze the importance of each feature to improve feature selection.

---

## **How to Run**  
1. Install the required libraries:  
   ```bash
   pip install pandas scikit-learn
   ```  
2. Load the dataset and perform cleaning.  
3. Split the data and train the model using the provided Random Forest parameters.  
4. Evaluate the model using the accuracy score and confusion matrix.

---

## **Acknowledgments**  
This project was built as part of a data science exploration into **customer behavior analysis** and demonstrates the importance of machine learning in **e-commerce optimization**.

---
