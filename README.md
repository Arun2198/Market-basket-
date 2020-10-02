# Market-basket-
An attempt to understand the working of apriori algorithm

1. Import pandas library 
2. Install the mlxtend library if not installed by running the following command on the command line as an admin user: 
command pip install mlxtend 
3. Dataset used is fetched from the url as follows (the dataset file is also uploaded):
http://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx
4. Read the file using read_excel attribute of pandas library by either giving the above url or by giving the absolute path of where the file is stored on your local setup.

Cleanse the available data first before processing it further as follows:

5. Remove the leading and trailing spaces in the fields by using .strip() function.
6. Use the dropna function to filter out which rows or columns in a file are to be left out from processing the data further.
7. Convert the integer (int) data present in invoice column as a string (str).
8. Drop the rows that don’t have invoice numbers and remove the credit transactions (i.e. invoice numbers beginning with C).
9.After the cleanup, we need to consolidate the items into 1 transaction per row with each product 1 hot encoded. For the sake of keeping the data set small, only sales of france and germany are considered.
10. There are a lot of zeros in the data but we also need to make sure any positive values are converted to a 1 and values 0 is set to 0.
11. Now the data is structured properly, we can generate frequent item sets that have a support of at least 7% (7% to get enough examples for processing the data.)
12. The final step is to generate the rules with their corresponding support, confidence and lift.
13. We can filter the dataframe using standard pandas code. In this case, consider a large lift (6) and high confidence (.8).
14. Similarly we can findout the patterns of online purchase in Germany as well.
