# MechaCar_Statistical_Analysis

# Deliverable 1
## Linear Regression to Predict MPG

summary (lm(mpg ~ vehicle_length + vehicle_weight + spoiler_angle + ground_clearance + AWD, data = mecha_mpg))
![image](https://user-images.githubusercontent.com/40743420/213351327-437bd31e-fb1d-4181-84aa-990a416ceb24.png)

address the following questions:

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

- Is the slope of the linear model considered to be zero? Why or why not?

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

#Deliverable 2

## Summary Statistics on Suspension Coils

![image](https://user-images.githubusercontent.com/40743420/213354079-8510119e-9a92-4ea9-97a9-073ccf34c46c.png)

#Deliverable 3 

## T-Tests on Suspension Coils

# summarize your interpretation and findings for the t-test results
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
