# E-Commerce Customer Spending Pattern Analysis
## owner: HRUUUTIKKK

## Overview
This project analyzes customer spending patterns for an e-commerce company. The dataset contains 5000 rows of customer data, including demographic information, purchasing history, and the types of products purchased. The objective is to visualize and explore relationships between these variables using Seaborn.

Dataset
The dataset used in this project contains the following columns:

Age: The age of the customer.
Gender: The gender of the customer (Male/Female).
Income: The annual income of the customer in USD.
Total_Spend: The total amount spent by the customer.
Num_Purchases: The total number of purchases made by the customer.
Product_Category: The category of the product purchased (Electronics, Clothing, Groceries).
Sample Data:
python
Copy code
Age   Gender   Income   Total_Spend   Num_Purchases   Product_Category
56    Male     112421   4035.07       40              Electronics
69    Female   122244   2215.84       42              Clothing
...



pip install pandas seaborn matplotlib
Download the dataset:
The dataset is generated as a CSV file. You can download it here.



# Load the dataset
data = pd.read_csv('ecommerce_customer_data.csv')
Visualizations:
Several visualizations are provided to analyze customer spending patterns. These visualizations are created using Seaborn and Matplotlib. You can run each code block separately for generating different graphs.

Distribution of Age:

sns.histplot(data['Age'], kde=True, color='skyblue')
Boxplot of Income by Gender:

sns.boxplot(x='Gender', y='Income', data=data, palette='Set2')
Distribution of Total Spend:

sns.histplot(data['Total_Spend'], kde=True, color='lightcoral')
Barplot of Product Category by Gender:

sns.countplot(x='Product_Category', hue='Gender', data=data, palette='husl')
Scatterplot: Income vs Total Spend:

sns.scatterplot(x='Income', y='Total_Spend', hue='Gender', data=data, palette='coolwarm')
Pairplot for Relationships:

sns.pairplot(data[['Age', 'Income', 'Total_Spend', 'Num_Purchases']], hue='Product_Category', palette='viridis')
Project Structure
bash
Copy code
ecommerce-customer-analysis/
│
├── ecommerce_customer_data.csv   # Dataset
