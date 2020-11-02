
## Flight Routes Analysis

#### Overview
######  To Analyze Flight Routes around the world.

#### Technologies Used
###### python, pandas, matplotlib

#### The Data

###### Data Source - openflights.org 






Analysis
The methodology I used was to grab a small, fixed region around some coordinate point and count how many bars were in the region. I used square regions of 1000x1000 ft to capture a few city blocks. To form a baseline I made a grid and iterated through the city of Austin counting how many bars were in each region. The average number of bars was 0.295.

I then looked at each crime with a lat/long coordinate, counted the number of bars in the region centered at that coordinate point, and compared the two. This was done for each criminal offense type in the top 20. For example, the average bars per region for DWIs is 3.525. This difference is clearly large, but is it statistically significant? To answer this question I did 20 one-tailed t tests at significance level of 0.05. To account for the number of comparisons I used a Bonferroni correction, which brings the significance level to .0025.

The full EDA can be found under data_exploration.ipynb.

Results
I wanted to know if bars were associated with crime, i.e. if crime occurs more frequently around bars than elsewhere. I considered the top 20 categories from 2016 through 2019. A remarkable 18 of 20 crimes were found to occur more often around bars at a statistically significant level.