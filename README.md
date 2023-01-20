# MechaCar_Statistical_Analysis

# Deliverable 1
## Linear Regression to Predict MPG

summary (lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD, data = mecha_mpg))
![image](https://user-images.githubusercontent.com/40743420/213351327-437bd31e-fb1d-4181-84aa-990a416ceb24.png)

address the following questions:

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
- The vehichle length, ground clearnace and the y intercept coefficent are statistically likely to provide a non-random amount of variance to the mpg values in the dataset as their p-values are much smaller than our significance level of 0.05%. Additionally, when the intercept has significant predicitive impact, there may be other variables of interest that can better explain variability of mpg that are not included in the model.

- Is the slope of the linear model considered to be zero? Why or why not?
We can reject the null hypothesis of our regression analysis test that the slope of the linear model is not considered to be zero. This interpretation is due to the fact that there are at least two known independent variables with significant predictability of the MechCar's mpg. 

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
- The linear model has an r-squared value of 0.7149, which means approximately 71.5% of all mpg predicitions will be correct when using this model. Thus, we can confirm that this multiple linear regression does predict mpg of the MechaCar prototypes effectively. 

#Deliverable 2

## Summary Statistics on Suspension Coils

![image](https://user-images.githubusercontent.com/40743420/213354079-8510119e-9a92-4ea9-97a9-073ccf34c46c.png)

The design specifications for the MechaCar suspension coils dicate that the variance of the suspension coils must not exceed 100 pounds per square inch (PSI). Based on the technical analysis above, which summarizes the results of testing the weight capacities of various suspension coils from multiple production lots.

#Deliverable 3 

## T-Tests on Suspension Coils

# summarize your interpretation and findings for the t-test results

The above t-tests evaluate the null hypothesis, which states that true mean of the sample population's PSI is statistically similar to that of the total population's PSI (mu = 1500)

1. From the first t-test, which summarizes results across all manufacturing lots, we can see that the true mean of sample 1498.78 with a p-value of 0.06 . With this being higher than the assumed significance level of 0.05, we can conclude that there is not enough sufficient evidence to reject the numm hypothesis. In other words, in totalitym, the mean PSI of all three manufacturing lots is statistically similar to the presumed population mean of 1500.

2. Sample dataset Lot1 has a p-value of 1, which is much larger than our assumed significance level of 0.05. That means that the probability of another sample prototype producing the same PSI measurement from lot 1 is 100%. Alternatively, there is a 0% chance that another sample population from lot 1 would be statistically different from the population mean. 

3.Lot 2 has a similar result output to the first t-test performed of all manufacturing lots, with a p-value of 0.61. Therefore, there is not sufficient evidence to reject the null hypothesis, and the sample mean is statistically similar to the populaiton mean of 1500.

3.	Lot 3's t-test results produce a different scenario compared to lot1 and lot2; however, this is not surprising based on our evaluation of its summary statistics of suspension coil's PSI. The p-value output is 0.04, which is less than our assumed significance level of 0.05. Thus, we can say that there is enough evidence to reject our null hypthesis, and the sample population mean PSI is NOT statistically similar to the population's mean.

This is valuable information to the production division: Lot 3's MechaCar protoypes do not meet quality assurance requirements, specifically concerning the suspension coils, and the process in which these cars were manufactured needs to be closely reviewed moving forward.


-
#Deliverable 4 

#Part 4: Design a Study Comparing the MechaCar to the Competition

## Study Design: MechaCar vs Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

In your description, address the following questions:
What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?

When evaluating the MechaCar compared to its competitors, a consumer would be interested in understanding the manintanance cost of the car prior to making a purchasing decision. Thus, we can design a statistical study to quantify how the MechaCar's repair/maintenance cost, a KPI performance indicator, shakes out compared to the competition.If we were able to quantifiably show that the MechaCar's repair cost is lower than its competitors, we can utilize this information whilst promoting the car, which can boost sales once the car is introduced to market. 

When ideating how to test for maintainance cost, as continuous variable, it is important to ask if there should be a complementary variable to consider to enunciate the true value of lower repair cost as a "performance metric". Cost as a continuous variable should be correlated to miles driven, and miles driven can quantify "long life of car usage. As a car gets more use, on average it should in theory need marginal repairs. 

What statistical test would you use to test the hypothesis? And why?
The testing method would be a two-way ANOVA test. 

-Independent variable 1 : Miles Driven, 
- Independent variable 2 : Car Manufacturer (Categorical)
-Dependent Variable : Maintenance Cost

Data Needed :

- A large sample size of cars, including the MechaCar and its Competitors
- Summary statistics of Miles Driven to break up into Quartiles for categorical use
- Maintenance Cost of Car over time

Technical Analysis would require the aov() and summary() functions of R to produce the results. This would be predicatedon first delving into summary statistics of each cars Miles driven to effectively group the bucket ranges by quartile, essentially a new summary dataframe to then perform the aov() test. 


What data is needed to run the statistical test?
