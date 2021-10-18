# MechaCar_Statistical_Analysis

### Resources 
* Soft Ware: RStudio and R
* Data Tools: tidyverse, dplyr, ggplot2.
* Data Source: MechaCar_mpg.csv and Suspension_Coil.csv


### Background 

The company AutoRU's has a new prototype, MechaCar is suffering from production troubles that are blocking the manufacturing teams progress. The production data needs to be reviewed and constructive feedback should be given on the analysis to help the team. 

The required actions are as follows:
* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings

### Deliverable 1: Linear Regression to Predict MPG

variables/ coefficents p-values (Pr(>|t|)) are:


![Screenshot (235)](https://user-images.githubusercontent.com/64110317/137650463-7a32e7db-611b-4de6-9004-520a1812c051.png)


* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The vehicle length, and vehicle ground clearance are statistically likely to provide non-random amounts of variance to the model. That is to say, the vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. Conversely, the vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that indicate a random amount of variance with the dataset.

* Is the slope of the linear model considered to be zero? Why or why not?

The desired significance level is 0.05 - 1 = 0.95 or 95%. All three of the tested coefficients are outside the 95% min significance level based on the linear model. P-Values: 5.35e-11, there is enough information to reject our null hypothesis. 

* Does the linear model predict mpg of MechaCar prototypes effectively? Why or why not?

the r-square value is 0.7149, which means that approximately 71% of all mpg predictions will be determined when using this specific model.


### Deliverable 2 : Summary Statistics on Suspension Coils

Creating a summary statistics table to show:

* The suspension coil’s PSI continuous variable across all manufacturing lots

* The following PSI metrics for each lot: mean, median, variance, and standard deviation.

The total for all the manufacturing lots are as follows


![Screenshot (236)](https://user-images.githubusercontent.com/64110317/137651331-5c988c73-4e4b-4fc4-8218-c7e46d1692a4.png)

* mean us at 1498.78 in all 150 rows of the total_summary table. 
* Standard deviation is at 7.892627 for all 150 rows of the total_summary table. 
* median value of the table varies between 1452 and 1542. 
* The variance of the PSI sample distribution and the standard deviation are well within the design specifications for all 3 lots and doesn't exceed 100 pounds per square inch.


![Screenshot (237)](https://user-images.githubusercontent.com/64110317/137651642-8843e7b1-ae32-41b5-9698-46c875ebc726.png)

* Lot 1 & are within the 100 PSI variance requirements, with variance of 0.98 and 7.47.
* Lot 3 that is showing much larger variance in performance and consistency, with a variance of 170.29. Lot 3 is disproportionately causing the variance at the full lot level.


### Deliverable 3 T-Tests on Suspension Coils

* An RSciprt is written for t-test that compares all manufacturing lots against mean PSI of the population. 


![Screenshot (239)](https://user-images.githubusercontent.com/64110317/137656339-1c603b61-5547-4b75-9312-fd33bab667c6.png)

![Screenshot (240)](https://user-images.githubusercontent.com/64110317/137656424-35fb7dfc-3077-4d5f-854f-0a839dba9e9a.png)

![Screenshot (242)](https://user-images.githubusercontent.com/64110317/137656541-c2b6d613-4f1b-4c96-a00e-c28e0a7df3a5.png)


* Results show p-value for all the lots is .06028, which is outside the significance level, with a confidence of 93.972%
* Lot 1 has a p=value of 1, null hypothesis cannot be rejected 
* Lot 2 has a p-value of .0672, null hypotesis cannot be rejected
* Lot 3 has a p-value of 0, reject the null hypothesis

### Deliverable 4: study Design: MechaCar vs Competition

To quantify how the MechaCar performs against the competition, an independent t-test could be used to compare the safety ratings of MechaCar against the competition. An independent t-test could be used because it will compare the means of the two different groups, MechaCar and the competition, to determine whether the associated population means are significantly different.To run this statistical test, ordinal data on the safety ratings for each group is needed. The null hypothesis would be that there is no difference in safety ratings between MechaCar and the competition and the alternative hypothesis is that there is a difference in the safety ratings between those two groups. Further analysis could be done using the results from the t-test.




