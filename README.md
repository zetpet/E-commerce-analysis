# Conducting E-commerce Purchase Analytics Using Cohort and RFM Analysis

**Project Status:** Completed.

**Project Description:**
Performed EDA, analyzed customer behavior, order statuses, and purchase frequency by weeks. Conducted cohort analysis of users. RFM segmentation of users was performed to study the audience.

**Project Tasks:**
1. How many users made only one purchase?
2. How many orders per month, on average, are not delivered for various reasons (provide a breakdown by reasons)?
3. Determine the most common day of the week for each product to be purchased.
4. How many purchases per week, on average, does each user make (per month)?
5. Conduct a cohort analysis of users. Identify the cohort with the highest retention in the 3rd month from January to December.
6. Perform RFM segmentation of users to qualitatively assess the audience. You can choose the following metrics for clustering: R - time since the user's last purchase until the current date, F - the total number of purchases by the user over all time, M - the total purchase amount over all time. Describe in detail how you created the clusters. For each RFM segment, establish boundaries for the recency, frequency, and monetary metrics for interpreting these clusters.

**Skills and Tools:** `Python`; `Pandas`; `Matplotlib`; `NumPy`; `Seaborn`; `Plotly`.

**General Conclusion:** >95% of all customers made only one purchase, which may indicate that the company's product has a long consumption cycle (~1 purchase in one or two years). Additionally, we do not know the unit of price for the product, so it can be assumed that the data was collected for the sales of large appliances/electronics or cars (e.g., from an unofficial dealer).

Thus, it seems logical to divide customers into the following segments:

VIP Customers - purchased relatively frequently, for a large sum, and their last purchase was recent (R-score 3-4; F-score 3-4; M-score 3-4)

Cannot Be Lost - purchased frequently for a large sum, but it has been a while since their last purchase (R-score 1-2; F-score 3-4; M-score 3-4)

Require Attention - purchased infrequently for a large sum, but it has been a while since their last purchase (R-score 1-2; F-score 1-2; M-score 3-4)

Loyal - made two purchases, with the last one being recent and for a large sum (R-score 3-4; F-score 2; M-score 3-4)

Potentially Loyal - made one recent purchase for a large sum (R-score 3-4; F-score 1; M-score 3-4)

Promising - made 2-3 purchases, with the last one being recent, but for small amounts (R-score 3-4; F-score 2-3; M-score 1-2)

Recent - made a recent purchase for a small amount (R-score 3-4; F-score 1; M-score 1-2)

Dormant - purchased frequently, but it has been a while and for small amounts (R-score 1-2; F-score 2-4; M-score 1-2)

Lost - made a single purchase a long time ago for a small amount (R-score 1-2; F-score 1; M-score 1-2)
