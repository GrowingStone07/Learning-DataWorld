

When there is requirement to append new columns/ or new columns is being created then follow the below approach:
Store the data in a dictionary
employee_dict = {'Employee Name':['Rajeev', 'Sumit', 'Aviral'], 'Income':[200000, 140000, 90000]}
Create DataFrame
employee_df = pd.DataFrame(employee_dict)
Print the dataframe
employee_df



When a row gets increased in the new dataset then follow the below approach:
Initialise the list of dictionaries
list_of_dicts = [{'a': 1, 'b': 2, 'c':3}, {'a':10, 'b': 20, 'c': 30}]
Create the DataFrame
df = pd.DataFrame(list_of_dicts)
Print the dataframe
df


Slicing in dataframe is not same as slicing in list. 
There are two methods for slicing in dataframe i.e. iloc and loc

# iloc: (index locators)
Let us get a subset which consists of first 8 rows and first 4 columns
df.iloc[:8,:4]

# loc:(giving column names for slicing)
Now let us subset our dataframe in which we want to have first 8 rows identified with their rows labels and some named columns
df.loc[50:60,['vin','state','condition']]


loc uses labels or names for indexing, while iloc uses integer positions.
loc includes the end label in a slice, while iloc excludes the end position.
loc is more suitable for label-based selection, especially when dealing with non-integer row and column labels, and it allows for boolean indexing.
iloc is more suitable for integer-based selection and numeric slices.


Below will give the same result:

df[['year','make','model']][0:9]
df.loc[0:9,['year','make','model']]
df.iloc[:10][['year','make','model']]


# Merge & Join:
Between merge and join the difference is join bydefault will join on basis of index. But in merge we have more options and we can select the column on which we want to join two datasets.


