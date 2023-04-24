Preprocessor Python Package

The Preprocessor Python package provides a simple and easy-to-use interface for data preprocessing in machine learning projects. It includes various methods for data cleaning, scaling, and encoding.

Installation

You can install the Preprocessor package using pip:

Copy code
pip install Preprocessor
Usage

The Preprocessor class is the main class of this package. You can create an instance of this class by providing the filepath of the CSV file that you want to preprocess.

python
Copy code
from Preprocessor import Preprocessor

preprocessor = Preprocessor('path/to/your/csv/file.csv')
Data Cleaning
Filling Missing Values
The fillwithmean, fillwithmedian, and fillwithmode methods can be used to fill the missing values in a column with the mean, median, or mode value of that column, respectively. You can pass the column name or a list of column names as an argument.

python
Copy code
preprocessor.fillwithmean('column_name')
preprocessor.fillwithmedian(['column_name_1', 'column_name_2'])
preprocessor.fillwithmode('column_name')
Removing Columns
The removeColumn method can be used to remove a column from the dataset. You can pass the column name as an argument.

python
Copy code
preprocessor.removeColumn('column_name')
Checking for Null Values
The nullValues method returns a dictionary containing the number of null values in each column.

python
Copy code
null_values = preprocessor.nullValues()
print(null_values)
Data Scaling
Standardization
The standardizeColumn and standardizeData methods can be used to standardize the data by subtracting the mean and dividing by the standard deviation. You can pass the column name or a list of column names as an argument.

python
Copy code
preprocessor.standardizeColumn('column_name')
preprocessor.standardizeData()
Normalization
The normalizeColumn and normalizeData methods can be used to normalize the data by scaling the values between 0 and 1. You can pass the column name or a list of column names as an argument.

python
Copy code
preprocessor.normalizeColumn('column_name')
preprocessor.normalizeData()
Data Encoding
Categorical Encoding
The categoricalEncoding method can be used to perform one-hot encoding on a categorical column. You can pass the column name as an argument.

python
Copy code
preprocessor.categoricalEncoding('column_name')
Data Compression
Lossy Compression
The compressLossy method can be used to compress the data using the K-Means algorithm. You can pass the number of clusters as an argument.

python
Copy code
preprocessor.compressLossy(10)
Non-Lossy Compression
The compressNonLossy method can be used to compress the data using Principal Component Analysis (PCA). You can pass the number of components as an argument.

python
Copy code
preprocessor.compressNonLossy(5)
Saving Processed Data
The save method can be used to save the preprocessed data to a CSV file.

python
Copy code
preprocessor.save(preprocessed_data)
Conclusion

The Preprocessor Python package provides a simple and effective way to preprocess data for machine learning projects. It includes various methods for data cleaning, scaling, encoding, and compression. It can save a lot of time and effort for data scientists and machine learning engineers.