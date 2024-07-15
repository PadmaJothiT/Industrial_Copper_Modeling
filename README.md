# Industrial_Copper_Modeling
Industrial Copper Modeling project aims to deals with dataset which is less complex data related to sales and pricing.

## Introduction
The Industrial Copper Modeling project focuses on predicting the selling price and status (won or lost) in the industrial copper market using machine learning regression and classification algorithms. By exploring the dataset, performing data cleaning and preprocessing, and applying various machine learning techniques, we aim to develop models that can accurately predict the selling price and status in the copper market.

## Technologies Used
#### Numpy
#### Pandas
#### Scikit-Learn
#### Seaborn
#### Matplotlib
#### Pickle

## Project Learnings
### Data extraction- Extracting the Copper_Set excel file using the pandas. Understaing the data conrains in the dataset. Evaluating the dataset head,shape,column data types, information contains in the data columns.

### Feature Engineerng- Converting the columns which are data related columns into datatime and numeric realted columns into numeric values.

### Data preprocessing- The dataset contains 14 columns which is about the copper product purchased customer detail, about the product detail and selling price with the particular product.As the dataset conatins the more null values in some particular rows imputing or removing the columns based on dataset whether its is needed to prediction or not.Especially in material_refernce column some values contains unrelated data like "0000", using numpy it is removing. In id column null values are presented as it is not much useful for prediction directly removing the column in the dataset.For other null values columns, columns splitted as what are the columns which are not outliers are presented for those null values imputations MEDIAN used. For those columns like not a measurable columns are imputing MODE values. After data preprocessing the data loaded as csv file as it sused for future purpose.

### Exploratory Data Analysis-The dataset converts as per the data values and Viewing the dataset columns distribution using boxplot for visualising the outliers and distplot for distribution. The data's which are not normally distributed as per boxplot and distplot are presenting outliers and skewness. For skewness numpy logarithm is used to reduce the skewness level and for outliers inter quartile range is used to remove the outliers (i.e.) the data values which are below 25 percentile and above 75 percentile values are removed with regards from mean value. Using heatmap the correlation with the target values from  predictor values is visualized.

### Encoding- Encoding the categarical columns like status and type column using LabelEncoder zip it in a file and using pickle loading it as .pkl file. to use it in streamlit part.

 ### Scaling- Scaling the all data columns with respect to the target columns, to leveling the all data columns into same level. For each Regression and Categorical categaries and loading it in as .pkl file to use it in streamlit part.
 
 ### Model Evaluation- In Regression category to predict the target column RandomForestRegressor, ExtraTreeRegressor and DecisionTreeRegressor is used to predict the selling price and for Categorical category  XGBClassifier, ExtraTreeClassifier, RandomForestClassifer is used to predict the status column. Using the models which giving more accuracy score loading ita as .pkl file and use it in streamlit part.
