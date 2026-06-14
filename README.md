# Exploratory Data Analysis (EDA) - AI/ML Study Repository

This repository contains a comprehensive guide to **Exploratory Data Analysis (EDA)**, a fundamental step in data science and machine learning workflows. The project demonstrates various EDA techniques using real-world datasets through an interactive Jupyter notebook.

## 📋 Overview

Exploratory Data Analysis is a critical process in data analysis where we explore, summarize, and visualize data to:
- Understand data structure and characteristics
- Detect patterns and relationships
- Identify anomalies and outliers
- Test assumptions
- Validate data quality before modeling

## 📂 Repository Structure

```
AI-ML/
├── README.md                    # This file
└── EDA/
    ├── eda.ipynb               # Main EDA notebook with examples
    ├── Employee_dataset.csv    # Employee data with demographics and employment info
    ├── Real estate.csv         # Real estate pricing data
    └── Restaurant_revenue.csv  # Restaurant revenue and customer data
```

## 📊 Datasets

### 1. Employee Dataset
Contains employee information including:
- **Columns**: EmployeeID, recorddate_key, birthdate_key, age, length_of_service, city_name, department_name, job_title, gender, STATUS, BUSINESS_UNIT, and more
- **Use Case**: Workforce analytics, demographic analysis, employee retention studies

### 2. Real Estate Dataset
Real estate pricing data with property characteristics:
- **Columns**: Transaction date, house age, distance to MRT station, number of convenience stores, latitude, longitude, house price per unit area
- **Use Case**: Real estate price prediction, location analysis, market trends

### 3. Restaurant Revenue Dataset
Restaurant business metrics:
- **Columns**: Number_of_Customers, Menu_Price, Marketing_Spend, Cuisine_Type, Average_Customer_Spending, Promotions, Reviews, Monthly_Revenue
- **Use Case**: Revenue prediction, customer behavior analysis, marketing effectiveness

## 🔍 EDA Techniques Covered

The notebook demonstrates three main types of analysis:

### 1. **Univariate Analysis** 
Analyzing single variables to understand their distribution:
- **Histograms**: Visualize data distribution and identify skewness
- **Bar Charts/Count Plots**: Display frequency of categorical variables
- **Pie Charts**: Show proportional composition of categories
- **Boxplots**: Identify outliers and understand data spread using five-number summary (min, Q1, median, Q3, max)

### 2. **Bivariate Analysis**
Examining relationships between two variables:
- **Scatter Plots**: Visualize correlations and relationships between continuous variables
- Applications include correlation analysis, regression analysis, clustering, and outlier detection

### 3. **Multivariate Analysis**
Studying three or more variables together:
- **Heatmaps**: Visualize correlation matrices to identify relationships between multiple variables
- **Pair Plots**: Create scatterplot matrices showing relationships between all numerical variable pairs

## 🛠️ Key Python Libraries Used

- **pandas**: Data loading, manipulation, and analysis
- **matplotlib**: Static visualizations and plotting
- **seaborn**: Statistical data visualization with enhanced aesthetics
- **plotly**: Interactive charts (mentioned for future use)

## 📚 Core Concepts & Functions

The notebook demonstrates essential pandas and visualization methods:

| Function | Purpose |
|----------|---------|
| `df.head()` / `df.tail()` | View first/last 5 rows of data |
| `df.shape` | Get dataset dimensions (rows × columns) |
| `df.dtypes` | Check data types of each column |
| `df.info()` | Get concise dataset summary |
| `df.isnull().sum()` | Count missing values per column |
| `df.describe()` | Generate descriptive statistics |
| `df.corr()` | Calculate correlation matrix |
| `sns.histplot()` | Create histogram visualizations |
| `sns.countplot()` | Display count of categorical observations |
| `sns.scatterplot()` | Create scatter plots for bivariate analysis |
| `sns.heatmap()` | Visualize correlation matrices |
| `sns.pairplot()` | Generate pairwise relationship plots |

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas matplotlib seaborn numpy
```

### Running the Notebook

1. Clone this repository:
```bash
git clone <repository-url>
cd AI-ML
```

2. Launch Jupyter Notebook:
```bash
jupyter notebook EDA/eda.ipynb
```

3. Run the cells sequentially to explore the EDA techniques

## 🎯 Learning Outcomes

After working through this repository, you will be able to:

1. ✅ Understand the importance and objectives of EDA
2. ✅ Load and perform initial data exploration using pandas
3. ✅ Identify and handle missing values and data quality issues
4. ✅ Apply univariate analysis techniques to understand individual variables
5. ✅ Use bivariate analysis to explore relationships between variables
6. ✅ Implement multivariate analysis for complex data relationships
7. ✅ Create effective visualizations using matplotlib and seaborn
8. ✅ Interpret correlation matrices and identify multicollinearity
9. ✅ Detect outliers and understand data distribution patterns
10. ✅ Make informed decisions about feature selection for modeling

## 💡 Use Cases

This EDA framework can be applied to:
- **Business Analytics**: Customer segmentation, sales forecasting, market analysis
- **Human Resources**: Workforce planning, retention analysis, diversity metrics
- **Real Estate**: Property valuation, location-based pricing, market trends
- **Hospitality**: Revenue optimization, customer satisfaction analysis
- **Machine Learning**: Feature engineering, data preprocessing, model selection

## 📝 Best Practices Demonstrated

- Systematic approach to data exploration
- Proper documentation with markdown cells
- Clear variable naming conventions
- Step-by-step analysis progression
- Combining statistical and visual analysis
- Commenting code for clarity

## 🤝 Contributing

Feel free to fork this repository and add more EDA techniques or datasets. Contributions are welcome!

## 📧 Contact

For questions or suggestions, please open an issue in this repository.

---

**Note**: This is an educational project focused on demonstrating EDA fundamentals. The datasets are used for learning purposes and may require additional preprocessing for production use cases.
