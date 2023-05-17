# A/B Test Analysis
This project focuses on analyzing the results of an A/B test conducted by an e-commerce website. The goal is to determine whether the new webpage design leads to a higher conversion rate compared to the old webpage. The analysis is performed using Python and various statistical techniques.

## Dataset
The dataset used for the analysis is stored in a CSV file named "ab_data.csv". It contains the following columns:

user_id: Unique ID for each user
timestamp: Timestamp of the user's visit to the webpage
group: Categorization of users into control or treatment group
landing_page: Denotes whether the user visited the old or new webpage
converted: Indicates whether the user decided to pay for the product (0 = no, 1 = yes)
Analysis Steps

1- Data Preparation:

- The initial dataset is read from the CSV file and stored in a pandas DataFrame.
- Inaccurate rows where the group and landing page do not match are removed to create a cleaned dataset.

2- Probability Analysis:

- Various probability calculations are performed using the cleaned dataset:
- Number of unique users
- Proportion of users converted
- Number of times group is treatment but landing page is not new_page

3- Conversion Rate Comparison:

- The conversion rates for the control and treatment groups are calculated and compared.

4- A/B Test Simulation:

- A null hypothesis is formulated assuming equal conversion rates for both groups.
- Simulated samples are generated for the treatment and control groups.
- The difference in conversion rates between the simulated samples is calculated.
- This process is repeated 10,000 times to create a sampling distribution of the difference in conversion rates.

5- Visualization and Conclusion:

- The sampling distribution is visualized using a histogram.
- The observed difference in conversion rates from the actual dataset is marked on the plot.
- The proportion of simulated differences greater than the observed difference is calculated.
- Based on the results, a conclusion is drawn regarding the effectiveness of the new webpage design.