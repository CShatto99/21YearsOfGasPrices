# 21 Years of Gas Prices

### Introduction

For the first programming class that I took, I was assigned this semester project. The professor provided a large file of gas price data from the years 1993-2013. Each line in the file contained the month (MM), day (DD), year (YYYY) and price of gas (#.###) in this order (e.g., 08-23-1999:1.273).

The requirements of the project included manipulating the data in various ways. More specifically, the project required 6 essential member functions: avgYearlyPrice(), avgMonthlyPrice(), highYearlyPrice(), lowYearlyPrice(), highToLow() and lowToHigh(). Below, I will cover each of these functions in order as well as provide some graphs that represent the data.

### What I Learned

* Used the principles of OOP to structure the code.
* Utilized the c++ Standard Template Library to implement the algorithms.
* Manipulated input files and generated output files using the fstream object class.

### Implementing The Member Functions

Each of the sections below will contain similar content. For each section, I will briefly explain the algorithm and provide some graphical representation of the resulting data. The project was created in Visual Studio and the code for the original project is [here](https://github.com/CShatto99/Resume-Projects/tree/master/21YearsOfGasPrices) or you can look at the project with an exhaustive explanation [here](https://github.com/CShatto99/Resume-Projects/tree/master/21YearsOfGasPricesDescriptive). Also, the code for just the member functions below can be found [here](https://github.com/CShatto99/Resume-Projects/blob/master/21YearsOfGasPrices/21YearsOfGasPrices/NewLineMethods.h) or [here](https://github.com/CShatto99/Resume-Projects/blob/master/21YearsOfGasPricesDescriptive/21YearsOfGasPrices/NewLineMethods.h) (exhaustive explanation).

#### Average Yearly Price of Gas

In this member function the goal is to find the average price of gas for each year, store them all in an array and display the result.
Below will be a high-level description of the algorithm.

* Add the price of gas to the yearly sum and keep track of the number of days in the year until the year changes.
* Insert the average gas price to the output array, reset the yearly sum and number of days in the year when the year changes.
* Display the output array when the loop exits.

![AvgYearlyPrice](https://github.com/CShatto99/Resume-Projects/blob/master/READMEImg/AverageYearlyPriceImage.png)

According to the input data, the average yearly price of gas had consistently risen from 1993 to 2013. The data shows an all-time low average of $1.070 per gallon in 1998 and an all-time high average of $3.686 per gallon in 2012.

#### Average Monthly Price of Gas

In this member function the purpose is to calculate the average price of gas for every month in each year, store all of the averages in a c++ vector and display the results to the terminal.
Below is a high-level description of the algorithm.

* Add the price of gas to the monthly sum and keep track of the number of days in the month until the month changes.
* If the month changes, insert the average into the vector, reset the monthly total, reset the number of days in the month and reset the current month counter accordingly.
* Display the output array using a current month and current year counter when the loop exits.

![AvgMonthlyPrice](https://github.com/CShatto99/Resume-Projects/blob/master/READMEImg/AverageMonthlyPrice.png)

According to the input data, the average monthly price of gas had a consistent increase from years 1993 to 2008. The average monthly price then significantly lowered at the end of 2008 followed by a consistent rise to 2013. The data shows an all-time low average of $0.959 per gallon in February of 1999 and an all-time high average of $4.125 per gallon in June of 2008.

#### Highest Yearly Price of Gas

This member function will perform one task, it will find the highest price of gas in each year from 1993 to 2013, store all of these values in an array and display them to the terminal.
Below is a high-level description of the algorithm:

* Set the max price equal to the current price if the year has not changed and the current price is greater than the current max.
* Insert the object corresponding the the current price into the array.
* If the year changes, increment the year counter, reset the max price and increment the current year counter.

![HighYearlyPrice](https://github.com/CShatto99/Resume-Projects/blob/master/READMEImg/HighestYearlyPrice.png)

The results of the highest yearly prices is very similar the the results of the average monthly prices. There is a consistent rise from 1993 to 2008, a significant drop at the end of 2008 and another consistent rise to 2013. The lowest of the highest yearly prices was $1.107 per gallon on May 31, 1993 and the highest of the highest yearly prices was $4.165 per gallon on July 7, 2008.

#### Lowest Yearly Price of Gas

The purpose of this member function is the same as the previous. The lowest prices of gas for each year will be stored in an array and then displayed to the terminal. 
Below is a high-level description of the algorithm.

* Set the min price equal to the current price if the year has not changed and the current price is less than the current min.
* Insert the object corresponding the the current price into the array.
* If the year changes, increment the year counter, reset the min price and increment the current year counter.

![LowYearlyPrice](https://github.com/CShatto99/Resume-Projects/blob/master/READMEImg/LowestYearlyPrice.png)

The trend of the data show a consistent increase in the lowest yearly prices from 1993 to 2013. The lowest of the lowest yearly prices is $0.949 per gallon on February 22, 1999 and the highest of the lowest yearly prices is $3.377 per gallon on January 14, 2013.

#### High To Low and Low To High

These two member function will perform practically the same task. HighToLow() will sort every datapoint by its price in non-increasing order and lowToHigh() will sort every datapoint by its price in non-decreasing order.

The member functions will simply utilize a map that was initialized and filled with every price from the input file in the constructor. Because inserting these values into the map automatically sorts them, all that is needed is a loop that writes every datapoint to an output file.

The output file for the highToLow() member function can be found [here](https://github.com/CShatto99/21YearsOfGasPrices/blob/master/21YearsOfGasPrices/highToLow.txt) and the output file for the lowToHigh() member function can be found [here](https://github.com/CShatto99/21YearsOfGasPrices/blob/master/21YearsOfGasPrices/lowToHigh.txt).
