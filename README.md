# Prosper Loan Data Exploration

## Agbons Ekata-Inuaghata

## Dataset

This data set contains 113,937 loans with 81 variables on each loan, including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others. The dataset can be found in the
repository for R's ggplot2 library [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv),
with feature documentation / data dictionary available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0).


## Summary of Findings

In the exploration, I found that The distributions of statedmonthlyincome is highly right screwed. Most stated monthly incomes are less than 30k, but some of them are incredibly high, like greater than 100k. Surprisingly, most of borrowers with greater than 100k monthly income only loan less than 5k. So, the very large stated monthly income may be made up or errors/outliers. Overall, Less than 0.3 percent borrowers have stated monthly income greater than 30k, these can be seemed as outlier for the following analysis, so it is better to remove borrower records with income greater than 30k. There was no need to perform any transformations.

I also discovered that The borrower rate is negatively associated with the loan original amount, which mean the more the loan amount, the lower the interest rate. It also shows that at different size of the loan amount, the interest rate has a large range, but the range of interest rate decreases with the increase of the loan amount. The borrower rate is steady across income ranges, higher income ranges have higher available credits in the bank along with higher stated monthly incomes, but borrower rate seems to be slightly lower for higher earners. 

The loan original amount is positively correlated with the stated monthly income, it makes sense since borrowers with more monthly income could loan more money. 

Borrower rate fluctuated between 2005-2007, became steady from 2008-2010, and has been gradually decreasing since 2011 to 2014. Borrower rate had a negative correlation with original loan amount across all years except 2005. Finally, I observed that there is a gradual increase in the loan amounts across the years


## Key Insights for Presentation

The distribution of borrower rate looks bimodal. The highest point is at around 0.15 and the second peak is at around 0.32. No loans have interest rates up to 0.4. For original loan amount there are very large spikes in frequency are at 5k, 10k, 15k, 20k, 25k and a little spike at 35k. Most of the loans are multiples of 5k.

Borrower rate fluctuated between 2005-2007, became steady from 2008-2010, and has been gradually decreasing since 2011 to 2014.

Borrower rate is negatively correlated with loan amount. The higher the loan amount, the lower the interest rate. Borrower rate is negatively correlated with the available bank card credit. The interest rate is negative at some point for bank card credits from 20000 to 60000 plus. Negative borrower interest rates encourage borrowers with higher bank card credits to borrow more

Aside from year 2005 which is an outlier because it has just 22 entries, Borrower rate seems to have a negative correlation with original loan amount across all other years. Another observation here is that there is a gradual increase in the loan amounts across the years


A large category of defaulters seem to have taken smaller loans. I wonder why they are unable to pay their loans, despite their loan amounts being less than the borrowers who completed their loan payments. It could also mesn that the defaulters earn less and may not have very stable employment status
      
