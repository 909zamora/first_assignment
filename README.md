# Kickstarting with Excel

## In this project I analyzed the Outcomes of fundraising campaigns for plays based on their launch dates
and their goals. This helped indicate whether some plays were more successful at a certain time of the year
and whether their initial goals were correlated with their success or failure

## Analysis and Challenges
Challenge 1: I began this by making a pivot table from the kickstarter tab and renaming the sheet to 
"Theater Outcomes by Launch Date" 
Columns = Outcomes
Values = Count of Outcomes
Filters = Parent Category & Year
Rows = Data Created Conversion
One of the issues I came across on this challenge was enabling the "Data Created Conversion" to be
changed into months, they automously filled in as years but I had to go to the "group" setting
in order to filter them to "months". This is a new feature I learned.

Challenge 2: I followed the instructions to build the table on a new tab called "Outcomes Based on Goals"
I filled in the #Successful & # Failed & # Canceled with the following formulas
Successful =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"successful",Kickstarter!$P:$P,"plays")
Failed =COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"Failed",Kickstarter!$P:$P,"plays")
Canceled = COUNTIFS(Kickstarter!$D:$D,"<1000",Kickstarter!$F:$F,"Canceled",Kickstarter!$P:$P,"plays")
The ranges changed but the referenced columns on the Kickstarter sheet were locked so the formula could
be replicated. I also filled in the totals to get the percentages of them. From here I made a line graph
that showed the trends of the % successful, failed & canceled on the chart. The X axis was the range 
and the Y axis showed the percentages of those failed/successful.
	

### Analysis of Outcomes Based on Launch Date
On this challenge the data showed that the most successful campaigns for plays are launched in May & June
so my recommendation would be to mirror those launch dates to get a higher probability of success

### Analysis of Outcomes Based on Goals
The chart indicated that campaigns had a higher success rate if they had a goal of 0-5000, it also indicated
that the failed campaigns had a higher failure rate if their goals were from 25K-35K.

### Challenges and Difficulties Encountered
I had a hard time converting my years to months on challenge one but the excel videos helped with that and
I learned something new that day. The Countif function was also confusing at first because when you are referencing
a range, it does not have a variable but it simply has a ">1000" whereas in if statements, you reference
another cell or number to indicate that. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Launch in May / June

- What can you conclude about the Outcomes based on Goals?
Set a goal less than 10K to have a success rate of 60% or higher.

- What are some limitations of this dataset?
The graph does not showcase the weight of the data points on the range, for example, there was a high % of success
on the range from 45K-49.9K (100%) but that is because there was only 1 successful campaign at that range.
It is not indicative of a future successful campaign within the same range.

- What are some other possible tables and/or graphs that we could create?
We could create a a secondary axis on the outcomes based on goal to show the amount of data point in that range.
That way, we are more confident on the success rate because it is backed up by multiple data points instead of a few
that really skew the graph. 
