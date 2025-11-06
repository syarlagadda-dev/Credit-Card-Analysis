Hello viewers!

The purpose of this project is to analyze credit card data in order to identify trends that may cause low or high balances. To achieve this, we use clustering to separate people into groups based on their credit usage frequency, and then apply linear regression to determine whether these groups tend to accumulate high balances, as well as to identify other spending behaviors and trends.

We assign the cluster names as follows:
    - Cluster 0: Low Activity Users – Very little credit card utilization.
    - Cluster 1: Structured Spenders – Tend to use credit for planned, large purchases made in installments (such as a TV). Less likely to impulse buy.
    - Cluster 2: Impulse Shoppers – Frequently make one-off purchases, but also have a moderate level of installment purchases.
    - Cluster 3: Cash Advance Reliant – Tend to use credit primarily for short-term liquidity through cash advances. This is a very risky behavior.
    - Cluster 4: Heavy Spenders – High overall credit usage across all purchase categories.

After assigning each entry a cluster based on spending habits, we observe:
    - Heavy Spenders, on average, have the highest credit limits, payments, minimum payments, and balances. Meanwhile, Low Activity Users and Structured Spenders tend to have the lowest values across these same metrics.
    - Impulse Shoppers tend to make payments well above their monthly minimums.
    - For payments, minimum payments, and balance, the data is heavily right-skewed. This suggests that in each spending cluster, a small number of individuals contribute disproportionately to the upper range of values — meaning a few users utilize significantly more credit than the average.
    - Median values for credit limit are relatively close to the mean. This suggests that credit limits are generally consistent across users within each cluster, though the data remains somewhat right-skewed.

We then apply linear regression models to analyze financial behavior within each cluster:
    - The Cash Advance Reliant and Heavy Spenders clusters show a stronger relationship between credit limit and balance, indicating that these groups are more likely to use most of their available credit and carry large balances.
    - Payments beyond the minimum had a strong correlation with balance reduction for Structured Spenders, which aligns with their planned, installment-based repayment habits.
    - Heavy Spenders and Impulse Shoppers showed a weaker positive relationship between payments and balance. This reflects inconsistent repayment behavior within these groups: some individuals actively try to pay balances down, while others pay only the minimum and allow balances (and interest) to grow.

Overall, repayment discipline is strongly tied to spending style: some groups manage debt predictably and consistently, while others display irregular or high-risk credit behavior.

Finally, the broader ethical implications of this analysis are worth noting. Insights like these could be used to promote financial literacy and help individuals avoid debt spirals. However, they could also be misused by predatory lenders or marketing systems to target “vulnerable” consumers. It is important to recognize that the inconsistency of repayment behavior in high-risk groups also makes them financially unpredictable and therefore a poor target for reliable profit.

References/Dataset: https://www.kaggle.com/datasets/arjunbhasin2013/ccdata 
