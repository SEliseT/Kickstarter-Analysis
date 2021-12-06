Part 1 – Overview of Project

The purpose of this project is to assist our client, Louise, in making an informed decision regarding her fundraising efforts for her play. As we worked together through the module research, we discovered a myriad of factors that can impact the success (or failure) of a campaign. However, Louise is most interested in the following factors and their potential effects on campaign outcomes:

•	Launch Dates
•	Funding Goals

In this document, I have visualized the campaign outcomes of various plays based on launch dates and funding goals. This is what I plan on presenting to help the client enter this process with eyes wide open. 

Part 2 – Discussion of Analysis and Challenges


Theater Outcomes by Launch Date

I started this process with a large master dataset containing campaign data for various categories. That sheet is titles “Kickstarter_Challenge.” One column was added (column U) outlining the year each campaign was launched. This was for the sake of assembling the first pivot table, used to outline the campaign outcomes by month. Upon creating that table, I made a line graph that helps visualize the relationship between campaign outcome and launch date. 

It was evident that campaigns launched in the month of May had the highest success rate. Those rates of success declined steadily each month after, causing the gap between failure and success rate trendlines to gradually come to a close. 


Theater Campaign Outcomes by Fundraising Goal

The second part of my analysis was a bit more in depth, and required the use of both the “COUNTIFS()” and “SUM()” functions. In this section, I’ve shown Louise the theater play campaign outcomes based on fundraising goal (also the verbatim title of the 3rd Excel worksheet). The table outlines the total number of projects, further broken down by outcome, as well as the percentage for each category:

•	Number/Percentage Successful
•	Number/Percentage Failed
•	Number/Percentage Canceled

In order to derive the table values, I began by using the COUNTIFS() function. The function was applied in combination with columns D (goal), F (outcomes), and R (Subcategory) from the Master dataset (Kickstarter_Challenge). This portion yielded some unique challenges that I’ll discuss later in the document. However, the COUNTIFS() function was only used directly in the first 3 columns of my “Outcomes Based on Goals” table  to derive the numbers. Column E (Total Projects) was the only column that the SUM() function was utilized. In order to get the total number of projects in each fundraising goal category, I used the sum of columns B, C, and D. Furthermore, to arrive at the percentages of each outcome (successful, failed, canceled), I took the number of the outcome and divided it by the total number of projects (column E). 


Challenges Encountered During Analysis

The main challenges that were encountered throughout this process was ensuring that all necessary factors were included in my COUNTIFS() formula. With a large dataset such as this, it’s very easy to overlook certain categories. For example, the final format of my formula is as follows:

=COUNTIFS(Kickstarter_Challenge!$D:$D, ">=1000", Kickstarter_Challenge!$D:$D, "<=4999", Kickstarter_Challenge!$F:$F, "Successful", Kickstarter_Challenge!$R:$R, "Plays") 

The highlighted portion at the end was not originally included. Had I not revised that, my table outcomes would have included every single category as opposed to isolating it to just plays, which is what Louise is interested in. Hence, despite having the right idea, excluding that piece would not have been of any help to her. 

Another challenge I encountered along the way was assembling the line graph to display the correct values on the Y and X axes. Originally the percentages were on the Y axis, however, the fundraising goal intervals were not listed on the X axis. It wasn’t until I found a way to alter the data shown on the axes that the correct information was revealed. 


Part 3 – Results 

Two conclusions regarding Theater outcomes by launch date are as follows:

•	Theater campaigns launched in the month of May appear to have the highest success rate, while the same campaigns launched in the month of December have the lowest success rate. 
•	While May has the highest success rate for Theater campaigns, it also has the highest failure rate as well. However, there’s roughly a 67% chance that one will succeed in May while only a 31% chance of failure, which means that a campaign in the month of May is more than twice as likely to succeed as it is to fail.  

Two. Conclusions about theater outcomes by fundraising goal is as follows:

•	Plays with a budget of $1000 or less are most likely to succeed. 75% success rate to be exact. 
•	The goal interval with the lowest percentage of success is in the budget range of $45,000 - $49,999. If Louise is considering a budget around those numbers, she should consider finding a way to produce the play with less money. 
•	Generally speaking, the success rate declines as the fundraising goal increases (with the exception of the $35,000-$44,999 range. 
o	There’s a possibility that other factors are influencing why this is. 

Limitations of dataset

•	The average donation was not factored into this breakdown. Analyzing the median, mode and quartiles of the average donation could have exposed certain outliers (if any), and possibly may have helped explain why there is a slight peak in success rate around the $35,000 - $44,999 range. 
•	The number of backers was not factored in. Higher fundraising goals typically mean that a higher number of backers will be necessary to fulfil that goal. Analyzing the success rate based on backer count could have also been useful as another avenue to support or contrast what we have already discovered. 

Other Possible Tables or graphs

•	A table outlining the mean, median, upper quartile, and lower quartile of theater campaign goals could have been created along with a boxplot to display the distribution.
o	We could have done the same for amount pledged with master data, so we could compare goals vs. what’s likely to be pledged. 
•	The same process we did in this analysis could have been completed, replacing outcome based on month with outcome based on country. This could have indicated to Louise if there is a certain country that is more likely to yield success. 




![image](https://user-images.githubusercontent.com/94502363/144787534-20224f48-4a84-405c-9533-f1297ef0ddd4.png)
