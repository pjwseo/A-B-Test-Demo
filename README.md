# A-B-Test-Demo
## By Paul Seo

### Purpose:
In this case study, I took a look at a A/B test data for a sample website and performed A/B testing with hypothesis testing.

### Dataset:
This dataset contained 294,478 rows with 5 columns, user id, page view time, test group, type of page, and conversion status. The data was relatively very clean with a few minor clean ups: 1) A small portion of rows contained incorrect information, such as being in the control group, but accessing the new web page. Since I cannot be sure which one of these information is true, I removed all approximately 4,000 rows that contained wrong information. 2) Rows with duplicate user_id was removed.

### Summary of Findings:
Hypothesis Test was set up as follows: 
* Null: New Page CTR performance does not differ from Old Page
* Alternate: New Page CTR performance is different from Old Page
with p-value of 0.05

The collected data produced the following results:
* Old Page CTR: 12.04%
* New Page CTR: 11.88%

New Page is performing worse in CTR and I conducted a test to see if this difference of 0.16% was significant. I created 10,000 random samples with replacement with the size same as the test population. I simulated this sample distribution under the null, mean centered at 0, and found that our observed difference produced a p-value of 0.0974, greater than 0.025 (two-tailed test).

### Conclusion:
Since 0.0974 > 0.025 tells us that our observed differences sits inside the confidence interval of 95%, we fail to reject the null hypothesis. The new page does not perform better or worse than the old page.
