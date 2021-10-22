# collection of methods for spliting dataset
Train-Test Split

ML models requires a set of datasets needed to train-test-validate models.
Your model can be prepared on the training dataset and predictions can be made and evaluated for the test dataset.

If you have only one initil dataset You can split your dataset into training and testing subsets.

This can be done by selecting an arbitrary split point in the ordered list of observations and creating two new datasets. Depending on the amount of data you have available and the amount of data required, you can use splits of 50-50, 70-30 and 90-10.

It is straightforward to split data in Python.

## 1 approach

After loading the dataset as a Pandas Series, we can extract the NumPy array of data values. The split point can be calculated as a specific index in the array. All records up to the split point are taken as the training dataset and all records from the split point to the end of the list of observations are taken as the test set.

## 2 approach

You can use the standard sklearn.model_selection.train_test_split
The suggestion is not correct for time-series, because it does not keep the time-series structure
The function just split arrays or matrices into random train and test subsets

## 3 approach

Use special object sklearn.model_selection.TimeSeriesSplit