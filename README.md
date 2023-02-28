# using insurance data to carry out exploratory-data-analysis
i have started with loading the data to the juypiter notebook.
once the data is loaded i have shown basic information about the data starting with showing the first five rows, the last five rows, dimension of the data in terms of rows and columns then information of the datatypes and number of null values for each valuables then finally the summary statistics of the data. the commands used are data.head(), data.tail(), data.shape(), data.info() and data.describe()
next is plotting a histogram with kernel density estimation for the variables using command sns.pairplot(data) 
next was to calculate the correlation matrix through commands corr_matrix = data.corr() and plotting it as a heatmap using command sns.heatmap(corr_matrix, annot=True) 
NEXT STEPS: 
Convert the variable children to a datetime object
data = data.set_index('children')   # Set the datetime variable as the index
data.resample('M').mean()   # Resample the data to monthly intervals and calculate the mean
sns.lineplot(data=data)   # Plot a line plot of the time series data
finally i have removed the rows with missing values using command my_data = my_data.dropna(subset=['children'])
