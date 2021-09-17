# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

## Project 1: Standardized Test Analysis

### Problem Statement

As part of the team working in the College Board, we have been tasked by the Board to look at increasing SAT participation rates across the various states.
The Board noticed that lower SAT test participation rates in comparison to our competitor, the ACTs, has impacted our revenue. 

SAT was introduced earlier compared to ACT.However, ACT has become more popular over the years. Looking into a two year trend, we can try and focus on areas where SAT is lacking.

---

### Datasets

Below datasets have been used

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State 
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State 
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State 
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State 
* [`act_data.csv`](./data/sat_2018.csv): 2018 SAT Scores by State [Cleaned]
* [`sat_data.csv`](./data/sat_2018.csv): 2018 SAT Scores by State [Cleaned]
* [`over_data.csv`](./data/sat_2018.csv): 2018 SAT Scores by State [Cleaned]

---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT & SAT|Individual states within the U.S| 
|act_participation_2017|float|ACT|The participation percentage of ACT in the year 2017| 
|act_participation_2018|float|ACT|The participation percentage of ACT in the year 2018| 
|act_composite_2017|float|ACT|The ACT composite score of all subjects taken in 2017| 
|act_composite_2018|float|ACT|The ACT composite score of all subjects taken in 2018| 
|sat_total_2017|float|SAT|The sum of all subject scores taken in the SAT 2017 test| 
|sat_total_2018|float|SAT|The sum of all subject scores taken in the SAT 2018 test| 
|total_average_2017|float|SAT|The mean scores of SAT 2017 test|
|total_average_2018|float|SAT|The mean scores of SAT 2018 test|

---

### Exploratory Data Analysis

Below 2 states Participation for ACT went from 100% to lesser from 2017 to 2018

* Colorado
* Minnesota

Below state Participation for SAT went from 100% to lesser from 2017 to 2018

* District of Columbia

A total of 22 States had more than 50% consecutively from 2017 to 2018 for SAT
A total of 28 States had more than 50% consecutively from 2017 to 2018 for ACT

---

### Visualization through Histogram

* ACT participation is inversely propotionate to SAT participation between 2017 and 2018
* ACT is skewed to the left while SAT is skewed to the right
* SAT has a rise in 100% participation in over 1 year

### Visualization through Scatterplot

* Scatterplot indicates that States with lower participation often scores more comparing to those with 100% participation

---

### Conclusions and Recommendations

* From the assistance of the visuals, we can see that there is an inverse correlation with the participation between the ACT and SAT students.
* Focusing onto SAT, we can see that States with a low participation often have students scoring high marks. This may mean a lack of focus onto the states with maximum participation.
* From an outside source showing that states with higher income tend to participate more in the SAT test. And having states make SAT a mandatory test, it can greatly improve the overall participation
