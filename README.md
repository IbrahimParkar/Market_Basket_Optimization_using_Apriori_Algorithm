# Market_Basket_Optimization_using_Apriori_Algorithm

In this project, we explore the concept of Market Basket Optimization using the Apriori algorithm. We implement the algorithm using both the apyori package and the mlxtend.frequent_patterns package to demonstrate different approaches.

# Apriori Algorithm with Apyori Package
To begin with, we import the necessary packages, including pandas and numpy for data manipulation and the apyori package for implementing the Apriori algorithm. We load the market basket dataset and perform data cleaning by replacing empty values with 0.

Next, we preprocess the data by converting it into a list format suitable for the Apriori algorithm. We call the apriori function, setting parameters such as minimum support, minimum confidence, minimum lift, and minimum length. The function generates association rules, which we store in the 'rules' variable.

We create a dataframe to present the results, including the antecedent item, consequent item, support, confidence, and lift values. Finally, we sort the dataframe based on the lift values to display the top results.

# Apriori Algorithm with mlxtend.frequent_patterns Package
In the second part of our project, we address some limitations of the previous approach by utilizing the mlxtend.frequent_patterns package. We import pandas, as well as the apriori and association_rules functions from mlxtend.frequent_patterns.

We load the dataset and perform data preprocessing, focusing on a specific country (France) for analysis. We create a pivot table with the quantity sum as values and convert it into a binary matrix, representing whether an item appears in a transaction or not. We then remove insignificant items such as 'POSTAGE'.

Using the apriori function, we generate frequent itemsets with a minimum support threshold. We set the metric as 'lift' and establish a minimum lift value of 1. The association_rules function is called to obtain the association rules based on the frequent itemsets.

Finally, we display the association rules with a lift value greater than or equal to 4 and a confidence value greater than or equal to 0.8.

# Understanding the Results
When analyzing the results of the association rules, several measures are considered:

1. Antecedent support: This measure indicates the frequency of the antecedent item in all the transactions.
2. Consequent support: This measure indicates the frequency of the consequent item in all the transactions.
3. Support: This measure indicates the frequency of the itemset in all the transactions.
4. Confidence: This measure defines the likelihood of finding the consequent item in the cart given that the cart already contains the antecedents.
5. Lift: This measure defines the likelihood of finding the consequent item in the cart given that the cart already contains the antecedent, while considering the popularity of the consequent item.
6. Leverage: Leverage measures the difference between the occurrence of X and Y appearing together in the dataset and what would be expected if X and Y were statistically independent.
7. Conviction: This parameter is not much useful in most situations and can be ignored.
These measures help us identify significant associations between items and understand customer behavior, which can be valuable for optimizing market baskets and improving business strategies.
