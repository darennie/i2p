Title: cw1v2  
Author: Daniel Rennie

16 November 2020

Quantitative Methods - Coursework 1 
Investigating Data

Introduction

The premise of coursework 1 was to analyse a selection of real and artificial data relating to 'Condition X'  which denotes childhood obesity across the United Kingdom. The data source manipulated for this assignment was https://data.london.gov.uk/dataset/prevalence-childhood-obesity-borough.

The task defined in the brief was to develop a simple research question, use the tools taught in class to analyse the data and to write a report of the investigation. Section 1 introduces the research question and hypothesis, section 2 explores the data and methodology and section 3 covers the results, discussion and conclusion.

1 Research Question and Hypothesis

Based on an initial review of the brief and data file the research question to explore became what effect, if at all, does population growth when combined with other factors impact the difference in the rate of 'Condition X' per 100,000 people between 2008 and 2018? 

Based on that research question, the simple hypothesis below was chosen; see figure 1 for the complete hypothesis.

![][PastedGraphic4]

2 Data and Methodology

Analysis for this investigation was done primarily in Python; however, Excel was used to complete the summary statistics and outlier identification. Assume that Python was used to conduct subsequent data analysis.

The first step in data analysis was adding three new columns identifying the following factors shown with the code below in Figure 2. These will be used to help drive the investigation.

![][PastedGraphic3]

The second step was to run the summary statistics for these columns to get an initial sense of the data.

![][table1]

Based on the summary statistics, the Tukey fence metric identified several outliers. The three chosen to remove are listed below with the reasons for removal. Those not selected for removal were deemed essential to the pattern.

	1. City of London - F3 was a high outlier, and it did not fit the pattern
	2. Rutland - F3 was a high outlier, and it did not fit the pattern
	3. Isles of Scilly - F2 was a low outlier, and it did not fit the pattern

During the next step, several scatter plots were used with F2 as the response factor while changing the independent factor. Scatter plots helped understand overall trends within the data. During this stage, the local authority spend was broken down into its proportional parts: clean air, clean environ, school awareness, health training, media awareness and sub counselling.

After review of the scatter plots, it appeared that there might be a relationship between F1 and the response factor (F2). Linear regression was run between the two variables to validate this fact and further investigate the hypothesis.

Based on this regression, it appeared that the null hypothesis could be rejected as the p-value (2.5111e-06) is significantly lower than the threshold of 0.05. The hypothesis result will be covered further in further detail in the results section. However, as the R-Squared value is low, this does not appear to cover all of the variance and further analysis is required.

Residual analysis was run and the plot validated the necessary conditions for the initial regression analysis. The plot shows that a linear relationship does exist because the errors appear to be independent, the errors appear to have a normal distribution and appear to have equal variance across all x values. While there were some potential outliers, none remaining appear significant enough to dismiss.

![][fig4]

As the current model has a low R-Squared value, it leaves a large portion of variation unaccounted. To account for more of the variance a logical next step would be to run a multiple linear regression using F1 and a second factor. The proportion of total spend on media awareness (F5) was chosen as the second factor because of the earlier scatter plot analysis.

However, it is critical to check if multicollinearity exists between these factors, especially as some data was artificially manipulated. A Variance Inflation Factors (VIF) test was run to judge the multicollinearity of these factors. The low VIF values shown below indicate that there is not a multicollinearity issue for these two factors.

| -----: | :----- |
| Figure 5 - VIF Test Result | ![][PastedGraphic] |

However, the regression including F1 and F5 as independent variables did not result in a significant increase to the R-Squared value, and still left significant variation unaccounted (Adj. R-Squared - 0.187).

A third multiple linear regression using the local authority type categorical data (transformed into dummy variables) was run and provided a more meaningful R-Squared value. The analysis is shown below in Figure 6.

![][table2]

Figure 6 shows that this new model can explain approximately 60% of the variance in the difference in 'Condition X' rate. However, the high p-value for F1 shows that it is not as significant when the local authority types are included and could potentially be removed from this model.

3 Results, Discussion and Conclusion

Figure 4 indicates to reject the hypothesis and it also appears that as population increases the rate of child obesity decreases strengthening the decision to reject. 

While the R-Squared value in Figure 4 is low, all other simple regressions ran (not included in this essay) also had low R-Squared values. The low R-Squared values highlight the fact that no individual factor has a strong effect on 'Condition X' in isolation. Further analysis may indicate that other factors, when used in combination, like the region, may improve the model.

The media awareness coefficient in Figure 6 also indicates that increasing media spend will not have a significant impact on slowing the rate of childhood obesity. In fact, as it is slightly positive, it may have the opposite effect. Local authority type, especially the London borough type, also appears to have a substantial impact, and further analysis of this area would be warranted.

The analysis shows that as populations in local authorities increase that the rates of childhood obesity fall. Population growth can provide some insight to local authorities on their childhood obesity rates. However, it should not be used on its own as this leaves a high level of variance unaccounted.

995 Words



[PastedGraphic4]: PastedGraphic4.pdf width=381px height=141px

[PastedGraphic3]: PastedGraphic3.pdf width=570px height=147px

[table1]: table1.png width=420px height=241px

[fig4]: fig4.png width=850px height=376px

[PastedGraphic]: PastedGraphic.png width=136px height=105px

[table2]: table2.png width=423px height=189px