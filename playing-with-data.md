# 📊 Playing with Data

### "Python is my favorite Programming Language"

<table data-view="cards"><thead><tr><th></th><th></th><th></th><th data-hidden data-card-cover data-type="files"></th><th data-hidden data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td></td><td></td><td></td><td><a href=".gitbook/assets/b51b78ecc9e5711274931774e433b5e6.jpg">b51b78ecc9e5711274931774e433b5e6.jpg</a></td><td><a href="https://github.com/Dexter829/Resume-Predictor.git">https://github.com/Dexter829/Resume-Predictor.git</a></td></tr></tbody></table>

##

## Resume Classifier Project

This project is a Python application that uses Natural Language Processing (NLP) and machine learning to classify resumes into categories such as Python Developer, Tester, etc. The application uses a variety of Python libraries, including pandas, matplotlib, seaborn, scikit-learn, and streamlit.

### Project Description

The application allows users to upload a resume through a Streamlit frontend. The resume is then processed and classified into a category, such as Python Developer or Tester. This classification is based on the content of the resume and the model trained on a dataset of categorized resumes.

### Code Overview

The code provided includes several key components:

1. **Data Loading and Preprocessing**: The code begins by loading a CSV file containing the resume dataset using pandas. The ‘Category’ column is converted to a categorical data type.

```python
df = pd.read_csv('UpdatedResumeDataSet.csv')
```

1. **Data Visualization**: The seaborn and matplotlib libraries are used to create a count plot of the different categories in the dataset.

```python
import seaborn as sns
import matplotlib.pyplot as plt

# Convert 'Category' column to categorical data type
df['Category'] = df['Category'].astype('category')

plt.figure(figsize=(15,5))
sns.countplot(data=df, x='Category')
plt.xticks(rotation=90)
plt.show()
```

**Text Cleaning**: The resumes are cleaned by removing URLs, special characters, and extra whitespace using regular expressions.

**Feature Extraction**: The cleaned resumes are transformed into a matrix of TF-IDF features.

**Model Training**: The dataset is split into a training set and a test set. A K-Nearest Neighbors classifier is trained on the training set.

**Model Evaluation**: The accuracy of the model is evaluated on the test set.

**Model Saving and Loading**: The trained model and the fitted TfidfVectorizer are saved using pickle for future use.

### Libraries Used

* **pandas**: Used for data manipulation and analysis. It provides data structures and functions needed to manipulate structured data.
* **matplotlib**: A plotting library for creating static, animated, and interactive visualizations in Python.
* **seaborn**: A Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
* **scikit-learn**: A machine learning library for Python. It features various classification, regression, and clustering algorithms, and is designed to interoperate with the Python numerical and scientific libraries NumPy and SciPy.
* **streamlit**: An open-source Python library that makes it easy to create and share beautiful, custom web apps for machine learning and data science.

In conclusion, this project demonstrates the power of combining NLP and machine learning to perform complex tasks such as resume classification. It also showcases the use of Python’s scientific and data analysis libraries to preprocess data, train models, and visualize data.
