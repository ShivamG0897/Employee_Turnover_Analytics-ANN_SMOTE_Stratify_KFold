# Employee_Turnover_analytics

Data was modified from: https://www.kaggle.com/liujiaqi/hr-comma-sepcsv


## Table of Contents

- [Problem Statement](#Problem-Statement)
- [Methodologies](#Scope)
- [DATA](#DATA)
- [Dataset Description](#dataset-description)
- [Installation](#installation)
- [Results and Findings](#results-and-findings)
- [File Structure](#file-structure)
- [License](#license)
- [Contact](#contact)

---

## Problem Statement
Portobello Tech is an app innovator that has devised an intelligent way of predicting employee turnover within the company. It periodically evaluates employees' work details including the number of projects they worked upon, average monthly working hours, time spent in the company, promotions in the last 5 years, and salary level.
Data from prior evaluations show the employee’s satisfaction at the workplace. The data could be used to identify patterns in work style and their interest to continue to work in the company. 
The HR Department owns the data and uses it to predict employee turnover. Employee turnover refers to the total number of workers who leave a company over a certain time period.
As the ML Developer assigned to the HR Department, you have been asked to create ML Program

---

## Methodologies

This section outlines the steps taken in the project, from data preparation to model training and evaluation.

**Data Preprocessing:** The project began with Exploratory Data Analysis (EDA) to understand the dataset's structure, identify key relationships, and prepare the data for modeling. A crucial finding was the significant class imbalance in the target variable left (employee turnover).

**Handling Class Imbalance:** To address this imbalance, we employed Synthetic Minority Over-sampling Technique (SMOTE). SMOTE creates synthetic samples of the minority class (employees who left), which helps the model learn patterns from this group more effectively and prevents it from being biased toward the majority class.

**Feature Engineering:** The dataset features were used to build models without extensive feature engineering, but some categorical variables like salary and Department were one-hot encoded to be used with the machine learning models.

**Model Training and Evaluation:** We used a stratified K-fold cross-validation approach to ensure our models were robust and not overfitting to a specific data split. This method divides the dataset into k folds while preserving the percentage of samples for each class, which is especially important for our imbalanced data. We then trained and evaluated various models, including an Artificial Neural Network (ANN), on these folds.

---

## DATA

The dataset used in this project is publicly available and was obtained from the Kaggle platform. It is a well-known dataset for employee turnover analysis, and its source is a modified version of the original data.

The original data was obtained from a public dataset on Kaggle: [Employee Turnover Analytics Dataset](https://www.kaggle.com/datasets/akshayhedau/employee-turnover-analytics-dataset)
---

## Dataset Description

Provide a clear description of your data, including its source and a breakdown of the key columns or features. Bullet points are excellent for this section as they make the information easy to scan.

* **Source:** [Link to the data source, e.g., Kaggle]
* **Target Variable:** `left` (0 = stays, 1 = leaves)
* **Key Features:**
    * Column Description:
    * satisfaction_level - satisfaction level at the job of an employee
    * last_evaluation - Rating between 0 to 1, received by an employee at his last evaluation
    * number_project	Number of projects, an employee involved in
    * average_montly_hours	Average number of hours in a month, spent by an employee at office
    * time_spend_company	Number of years spent in the company
    * Work_accident - 0 - no accident during employee stay, 1 - accident during employee stay
    * left -	0 indicates employee stays in the company, 1 indicates - employee left the company
    * promotion_last_5years	- Number of promotions in his stay
    * Department -	Department, an employee belongs to
    * salary - Salary in USD

---

## Installation

This section provides a step-by-step guide on how to set up the project. Use code blocks for commands to make them easy to copy and paste.

1.  **Clone the Repository:**
    `git clone https://github.com/your-username/your-repo-name.git`
    `cd your-repo-name`

2. **Open the Command Prompt or PowerShell.**

3. Navigate to the cloned repository directory. For example, `cd C:\Users\your_username\Documents\your-repo-name`.

4.  **Create and Activate a Virtual Environment:**
    * **macOS/Linux:** `python3 -m venv venv && source venv/bin/activate`
    * **Windows:** `python -m venv venv` and `.\venv\Scripts\activate`

5.  **Install Dependencies:**
    `pip install -r requirements.txt`

6. Launch Jupyter Notebook with the command `jupyter notebook`.

7. A new browser window will open, displaying the repository's file structure. You can then click on the `.ipynb` files (e.g., `Employee_Turnover_Analytics_ANN_v1.ipynb`) to open and execute the code cells.

---

## Results and Findings

**Key EDA Insights:** The analysis revealed a strong negative correlation (r=−0.4) between satisfaction_level and an employee leaving the company. This indicates that employees with lower satisfaction levels are more likely to turn over. Additionally, clustering models like K-Means and Gaussian Mixture were used to identify distinct employee segments, revealing groups with similar characteristics who might be at higher risk of leaving.

**Model Performance:** The Artificial Neural Network (ANN) model showed exceptional performance in predicting employee turnover. By using SMOTE and stratified K-fold cross-validation, the model achieved an impressive AUC score of 0.98 and a high accuracy of 98% on the validation data. This demonstrates the model's strong capability to distinguish between employees who will stay and those who will leave.

**Key Takeaways:** The high-performing ANN model can provide the HR department with a powerful tool to proactively identify employees at risk of turnover. The insights from the EDA and clustering can also help the company understand the root causes of turnover and develop targeted retention strategies.

---

## File Structure

Here is a brief overview of the key files and directories in this repository:

* **`notebooks (.ipynb)`**: This directory contains the Jupyter Notebooks used for Exploratory Data Analysis (EDA), model training, and evaluation. Files with `.ipynb` extension
* **`requirements.txt`**: Lists all the necessary Python libraries and their versions.
* **`README.md`**: The document you are currently reading (includes Link to the data)
* **`LICENSE`**: Authorization to use the code for learning or business practices.

---

## License

This project is licensed under the **MIT License**. For more information, please see the `LICENSE` file in the repository.

---

## Contact

For any questions, please feel free to reach out. If the data is removed from the link, I maybe able to stick you up with the dataset used.

* **Name:** Shivam Goel
* **GitHub:** [@ShivamG0897](https://github.com/ShivamG0897)
* **Email:** Shivam.goel0897@gmail.com

---

