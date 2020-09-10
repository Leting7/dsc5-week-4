# dsc5-week-4
INTRODUCTION
-The purpose of this report is to understand electric car usage for a company by Autolib which is a electric car sharing service company based in France much like Bluela and BlueIndy in  Los Angeles & Indianapolis in the US. The closest we have locally is Nopea ride which is not exactly the same but a taxi hailing app for electric cars.
-The provided dataset is a daily aggregation, by date and postal code, of the number of events on the Autolib network (car-sharing and recharging).
-The report is is to be used to communicate my findings and assess the legitimacy of my data analysis procedure

-My Research claim will be that “” is the number of bluecars taken in area 75112 greater  than in area 94130 in the weekends ””
-I chose the two area codes among the ones with the highest number of data entries so as the analysis can be done at a high scale compared to just any randomly chosen area code 
-the hypothesis testing which we will carry out  wil help us know whether there is a difference in terms of number of rentals in certain regions



DATA
-As mentioned early the data we are analysing features a daily aggregation, by date and postal code, of the number of events on the autolib Network. As shown below as an excel spreadsheet;


And to have a better understanding on its here is its glossary: 
                         ( *shows the various column names and their meanings*)

Postal code = Postal code of the area (in Paris)
Date = Date of the row aggregation
Daily data points  = 	Number of daily data points that were available for aggregation, that day
Day Of Week	 = Identifier of weekday (0: Monday -> 6: Sunday)
Day type = weekday or weekend
BlueCars taken sum = Number of bluecars taken that date in that area
BlueCars returned sum = Number of bluecars returned that date in that area
Utilib taken sum = Number of Utilib taken that date in that area
Utilib returned sum = Number of Utilib returned that date in that area
Utilib 14 taken sum = Number of Utilib 1.4 taken that date in that area
Utilib 14 returned sum = Number of Utilib 1.4 returned that date in that area
Slots freed sum = Number of recharging slots released that date in that area
Slots taken sum = Number of recharging slots taken that date in that area

*So basically this data shows how in a day to day life of the company of  cars  which were rented from the company in different areas of  Paris,France. Also to the specifics of how many were returned for charging and the number of slots taken or remaining

-When starting to analyse this data we must always keep in mind the research question in mind that is ;
 “” is the number of bluecars taken in area 75112 greater  than in area 94130 in the weekends ””

-In respect to that  in my full  analysis done in a Google Collaboratory Notebook in Python using its various statistical libraries 

 
When looking into the dataset in terms of  day type in which people rent out the bluecars  we can see people usually rent them out more in the weekdays than in the weekends





-When we take  look into the sum of bluecars taken daily we find  that its outliers lie beyond 300 (>300)


So in our analysis every value greater than 300 is removed so that they don't affect the mean of correlation of data
 
Postal code 75112 has a mean sum of 12.16 number of bluecars taken
Postal code 94130 has a mean sum of  57.82 number of bluecars taken





HYPOTHESIS TESTING
The null hypothesis in question will be the research question in context(this will be done in the google collab notebook)


   Null hypothesis  = 
    “” is the number of bluecars taken in area 75112 greater  than in area 94130 in the weekends ””
    Alternative hypothesis = 
       “” is the number of bluecars taken in area 75112 less than in area 94130 in the weekends ””
 

-We will  not choose the z-test as the test statistic as the sample size is less than 30 but the independent t-test

- The population mean is 34.99
 
-The sample mean is 12.44 which is the mean based of postal code 75112 which is the focus of the null hypothesis
 
-The sample standard deviation is 4.289036
 
-Level of significance chosen will be 0.05 as it is the most commonly used 
 
-And the p-value comes out as 0.5525399713382472

-’’’As we can see from the p-value which is greater than the level of significance which makes us conclude that the retain the null hypothesis’’
Incase i decide to lower the sample size it will be ,much suitable for me to use the t-test as it recommended one for sample sizes less than 30
