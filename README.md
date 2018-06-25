# Python-for-Datascience: Datacamp

## Introduction: 

* Python developed by Guido Van Rossum 
* General purpose, open source language 
* Packages developed for data science 
* 2 versions 2.7, 3.5.  
* Course is based on python 3.x 
* Python scripts end in .py 

# Variables 
Check the type of variables using type(vars) 
Integers – whole numbers 
Float – real numbers with both whole and fractional components for a number 
Boolean - yes/no outcomes 
+ operator behaves differently based on data types 
+ would concatenate strings 
What's valid? 
"I can add integers, like " + str(5) + " to strings." 
"I said " + ("Hey " * 2) + "Hey!" = I said Hey Hey Hey 
"The correct answer to this multiple choice exercise is answer number " + 2 = wrong 
True + False = 1 
 
 
 
Lists: 
In [1]: x = [["a", "b", "c"], 
...      ["d", "e", "f"], 
...      ["g", "h", "i"]] 
  
In [2]: x[2][0] 
Out[2]: 'g' 
  
In [3]: x[2][:2] 
Out[3]: ['g', 'h'] 
 
 
Tricky things happen behind the scenes. If you try to assign an equals operator, you are only assigning a reference to the list (pass by reference vs pass by value) 
 
To avoid this, use 
x = [a,b,c,d] 
y = list(x) 
Or  
Y = x[:] 
Functions: 
Round(1.68) = 2 
Round(1.68,1) = 1.6 
Help(round)  
Round(number[,ndigits]) means [] this part is optional 
Familiar functions 
 
Out of the box, Python offers a bunch of built-in functions to make your life as a data scientist easier. You already know two such functions: print() and type(). You've also used the functions str(), int(), bool() and float() to switch between data types. These are built-in functions as well. 
 
# Create lists first and second 
first = [11.25, 18.0, 20.0] 
second = [10.75, 9.50] 
  
# Paste together first and second: full 
full = first + second 
print (full) 
  
# Sort full in descending order: full_sorted 
full_sorted = sorted(full, reverse = True) 
  
# Print out full_sorted 
print(full_sorted) 
 
Output: 
 [11.25, 18.0, 20.0, 10.75, 9.5] 
 [20.0, 18.0, 11.25, 10.75, 9.5] 
 
Methods: Functions that belong to Python objects 
 
Lists have methods associated with them: 
Strings have capitalize(), replace() 
Floats have bit_length(), conjucate() 
Lists have index(), count() 
Fam = [mom, dad, sister, brother] 
Fam.index("mom")  
= 0 
Fam.count("mom")  
= 1  
Mom appears once in the list 
Methods: 
Code  
# string to experiment with: room 
room = "poolhouse" 
  
# Use upper() on room: room_up 
room_up = room.upper() 
  
# Print out room and room_up 
print (room) 
print(room_up) 
# Print out the number of o's in room 
print(room.count("o")) 
 
 
script.py> output: 
    poolhouse 
    POOLHOUSE 
    3 
Page Break
 
# Create list areas 
areas = [11.25, 18.0, 20.0, 10.75, 9.50] 
  
# Print out the index of the element 20.0 
print(areas.index(20.0)) 
  
# Print out how often 14.5 appears in areas 
print(areas.count(14.5))  
# Create list areas 
areas = [11.25, 18.0, 20.0, 10.75, 9.50] 
  
# Print out the index of the element 20.0 
print(areas.index(20.0)) 
  
# Print out how often 14.5 appears in areas 
print(areas.count(14.5)) 
Page Break
 
# Create list areas 
areas = [11.25, 18.0, 20.0, 10.75, 9.50] 
  
# Use append twice to add poolhouse and garage size 
areas.append(24.5); areas.append(15.45) 
  
  
# Print out areas 
print (areas) 
  
# Reverse the orders of the elements in areas 
areas.reverse() 
  
# Print out areas 
print(areas) 
    [11.25, 18.0, 20.0, 10.75, 9.5, 24.5, 15.45] 
    [15.45, 24.5, 9.5, 10.75, 20.0, 18.0, 11.25] 
 
Packages 
Numpy – array manipulation 
Matplotlib – for data visualisations 
Scikit Learn – Machine Learning 
 
How to install Packages fro python? Use PIP which comes bundled with Python 2.7 or 3.6 
Enter the following into cmd 
python -m pip install -U pip setuptools 
 
Using Numpy 
Define arrays: numpy.array([1,2,3]) 
Or  
Import numpy as np 
Np.array([1,2,3]) 
Output: array([1,2,3]) 
Instead of importing the entire package we can call just a specific function we can call: 
from numpy import array 
# Definition of radius 
r = 0.43 
  
# Import the math package 
import math 
  
# Calculate C 
C = 2*math.pi*r 
print (C) 
# Calculate A 
A = math.pi*r**2 
print(A) 
 
Page Break
 
# Definition of radius 
r = 192500 
  
# Import radians function of math package 
from math import radians 
  
# Travel distance of Moon over 12 degrees. Store in dist. 
phi = 12 
dist = r * radians(phi) 
  
# Print out dist 
print(dist) 
Page Break
 
# Create list baseball 
baseball = [180, 215, 210, 210, 188, 176, 209, 200] 
  
# Import the numpy package as np 
import numpy as np 
  
# Create a numpy array from baseball: np_baseball 
np_baseball = np.array(baseball) 
  
# Print out type of np_baseball 
print(type(np_baseball)) 
 
Your First NumPy Array 
100xp 
In this chapter, we're going to dive into the world of baseball. Along the way, you'll get comfortable with the basics of numpy, a powerful package to do data science. 
A list baseball has already been defined in the Python script, representing the height of some baseball players in centimeters. Can you add some code here and there to create a numpy array from it? 
Instructions 
Import the numpy package as np, so that you can refer to numpy with np. 
Use np.array() to create a numpy array from baseball. Name this array np_baseball. 
Print out the type of np_baseball to check that you got it right 
 
# height and weight are available as a regular lists 
  
# Import numpy 
import numpy as np 
  
# Create array from height with correct units: np_height_m 
np_height_m = np.array(height) * 0.0254 
  
# Create array from weight with correct units: np_weight_kg 
np_weight_kg = np.array(weight) * 0.453592  
  
# Calculate the BMI: bmi 
bmi = np_weight_kg / (np_height_m ** 2) 
  
# Print out bmi 
print(bmi) 
Page Break
 
# height and weight are available as a regular lists 
  
# Import numpy 
import numpy as np 
  
# Calculate the BMI: bmi 
np_height_m = np.array(height) * 0.0254 
np_weight_kg = np.array(weight) * 0.453592 
bmi = np_weight_kg / np_height_m ** 2 
  
# Create the light array 
  
light = bmi < 21 
  
# Print out light 
print(light) 
  
# Print out BMIs of all baseball players whose BMI is below 21 
print(bmi[light]) 
Page Break
 
NumPy Side Effects 
50xp 
As Filip explained before, numpy is great for doing vector arithmetic. If you compare its functionality with regular Python lists, however, some things have changed. 
First of all, numpy arrays cannot contain elements with different types. If you try to build such a list, some of the elements' types are changed to end up with a homogeneous list. This is known as type coercion. 
Second, the typical arithmetic operators, such as +, -, * and / have a different meaning for regular Python lists and numpy arrays. 
Have a look at this line of code: 
np.array([True, 1, 2]) + np.array([3, 4, False]) 
Can you tell which code chunk builds the exact same Python object? The numpy package is already imported as np, so you can start experimenting in the IPython Shell straight away! 
Possible Answers 
np.array([True, 1, 2, 3, 4, False]) 
np.array([4, 3, 0]) + np.array([0, 2, 2]) 
np.array([1, 1, 2]) + np.array([3, 4, -1]) 
np.array([0, 1, 2, 3, 4, 5]) 
2D Numpy Arrays 
Np_2d = np.array([[1,2,3,4,5],[10,20,30,40,50]]) 
In: Np_2d.shape 
Out: (2,5) 
Remember the arrays must contain elements of the same type 
 
# Create baseball, a list of lists 
# contains the height and weight of 4 MLB players 
  
baseball = [[180, 78.4], 
            [215, 102.7], 
            [210, 98.5], 
            [188, 75.2]] 
  
# Import numpy 
import numpy as np 
  
# Create a 2D numpy array from baseball: np_baseball 
np_baseball = np.array(baseball) 
  
# Print out the type of np_baseball 
print("The type of the np array is:") 
print(type(np_baseball)) 
  
# Print out the shape of np_baseball 
print("The shape of the np array is:") 
print(np_baseball.shape) 
 
Using Numpy for statistics 
Np.mean(np_array[:,0]) 
Np.median(np_array[:,0]) 
Np.std(np_array[:,0]) 
Np.corrcoef(np_array[:,0]) 
Sum(), sort() 
Generate sample data:  
Height = np.round(np.random.normal(1.75, 0.20, 5000), 2) 
Weight = np.round(np.random.normal(60.32, 15, 5000), 2) 
Average versus median 
100xp 
You now know how to use numpy functions to get a better feeling for your data. It basically comes down to importing numpy and then calling several simple functions on the numpy arrays: 
import numpy as npx = [1, 4, 8, 10, 12]np.mean(x)np.median(x) 
The baseball data is available as a 2D numpy array with 3 columns (height, weight, age) and 1015 rows. The name of this numpy array is np_baseball. After restructuring the data, however, you notice that some height values are abnormally high. Follow the instructions and discover which summary statistic is best suited if you're dealing with so-called outliers. 
Instructions 
Create numpy array np_height that is equal to first column of np_baseball. 
Print out the mean of np_height. 
Print out the median of np_height 
 
# np_baseball is available 
  
# Import numpy 
import numpy as np 
  
# Create np_height from np_baseball 
np_height = np.array(np_baseball[:,0]) 
  
# Print out the mean of np_height 
print(np.mean(np_height)) 
  
# Print out the median of np_height 
print(np.median(np_height)) 
 
Explore the baseball data 
100xp 
Because the mean and median are so far apart, you decide to complain to the MLB. They find the error and send the corrected data over to you. It's again available as a 2D Numpy array np_baseball, with three columns. 
The Python script on the right already includes code to print out informative messages with the different summary statistics. Can you finish the job? 
Instructions 
The code to print out the mean height is already included. Complete the code for the median height. Replace Nonewith the correct code. 
Use np.std() on the first column of np_baseball to calculate stddev. Replace None with the correct code. 
Do big players tend to be heavier? Use np.corrcoef()to store the correlation between the first and second column of np_baseball in corr. Replace Nonewith the correct code. 
# np_baseball is available 
  
# Import numpy 
import numpy as np 
  
# Print mean height (first column) 
avg = np.mean(np_baseball[:,0]) 
print("Average: " + str(avg)) 
  
# Print median height. Replace 'None' 
med = np.median(np_baseball[:,0]) 
print("Median: " + str(med)) 
  
# Print out the standard deviation on height. Replace 'None' 
stddev = np.std(np_baseball[:,0]) 
print("Standard Deviation: " + str(stddev)) 
  
# Print out correlation between first and second column. Replace 'None' 
corr = np.corrcoef(np_baseball[:,0],np_baseball[:,1] ) 
print("Correlation: " + str(corr)) 
 
Blend it all together 
100xp 
In the last few exercises you've learned everything there is to know about heights and weights of baseball players. Now it's time to dive into another sport: soccer. 
You've contacted FIFA for some data and they handed you two lists. The lists are the following: positions = ['GK', 'M', 'A', 'D', ...] heights = [191, 184, 185, 180, ...] Each element in the lists corresponds to a player. The first list, positions, contains strings representing each player's position. The possible positions are: 'GK' (goalkeeper), 'M' (midfield), 'A' (attack) and 'D'(defense). The second list, heights, contains integers representing the height of the player in cm. The first player in the lists is a goalkeeper and is pretty tall (191 cm). 
You're fairly confident that the median height of goalkeepers is higher than that of other players on the soccer field. Some of your friends don't believe you, so you are determined to show them using the data you received from FIFA and your newly acquired Python skills. 
Instructions 
Convert heights and positions, which are regular lists, to numpy arrays. Call them np_heights and np_positions. 
Extract all the heights of the goalkeepers. You can use a little trick here: use np_positions == 'GK' as an index for np_heights. Assign the result to gk_heights. 
Extract all the heights of all the other players. This time use np_positions != 'GK' as an index for np_heights. Assign the result to other_heights. 
Print out the median height of the goalkeepers using np.median(). Replace None with the correct code. 
Do the same for the other players. Print out their median height. Replace None with the correct code. 
# heights and positions are available as lists 
  
# Import numpy 
import numpy as np 
  
# Convert positions and heights to numpy arrays: np_positions, np_heights 
np_positions =np.array(positions)  
np_heights = np.array(heights) 
  
# Heights of the goalkeepers: gk_heights 
gk_heights = np_heights[np_positions == 'GK'] 
print (gk_heights) 
# Heights of the other players: other_heights 
other_heights = np_heights[np_positions != 'GK'] 
print (other_heights) 
# Print out the median height of goalkeepers. Replace 'None' 
print("Median height of goalkeepers: " + str(np.median(gk_heights))) 
  
# Print out the median height of other players. Replace 'None' 
print("Median height of other players: " + str(np.median(other_heights))) 
 
Intermediate Python for Datscience 
import matplotlib.pyplot as plt 
year = [1950, 1970, 1990, 2010] 
pop = [2.519, 2.692, 5.263, 6.972] 
plt.plot(year,pop) # (x,y) 
plt.show() 
 
 
 
Scatterplot 
import matplotlib.pyplot as plt 
year = [1950, 1970, 1990, 2010] 
pop = [2.519, 2.692, 5.263, 6.972] 
plt.scatter(year,pop) # (x,y) 
plt.show() 
 
Line plot (1) 
100xp 
With matplotlib, you can create a bunch of different plots in Python. The most basic plot is the line plot. A general recipe is given here. 
import matplotlib.pyplot as pltplt.plot(x,y)plt.show() 
In the video, you already saw how much the world population has grown over the past years. Will it continue to do so? The world bank has estimates of the world population for the years 1950 up to 2100. The years are loaded in your workspace as a list called year, and the corresponding populations as a list called pop. 
Instructions 
print() the last item from both the year and the pop list to see what the predicted population for the year 2100 is. Use two print() functions. 
Before you can start, you should import matplotlib.pyplot as plt. pyplot is a sub-package of matplotlib, hence the dot. 
Use plt.plot() to build a line plot. year should be mapped on the horizontal axis, pop on the vertical axis. Don't forget to finish off with the show() function to actually display the plot. 
  
  
# Print the last item from year and pop 
print(year[-1]) 
print(pop[-1]) 
  
  
# Import matplotlib.pyplot as plt 
import matplotlib.pyplot as plt 
  
# Make a line plot: year on the x-axis, pop on the y-axis 
plt.plot(year,pop) 
  
  
# Display the plot with plt.show() 
plt.show() 
 
Line plot (3) 
100xp 
Now that you've built your first line plot, let's start working on the data that professor Hans Rosling used to build his beautiful bubble chart. It was collected in 2007. Two lists are available for you: 
life_exp which contains the life expectancy for each country and 
gdp_cap, which contains the GDP per capita (i.e. per person) for each country expressed in US Dollars. 
GDP stands for Gross Domestic Product. It basically represents the size of the economy of a country. Divide this by the population and you get the GDP per capita. 
matplotlib.pyplot is already imported as plt, so you can get started straight away. 
Instructions 
Print the last item from both the list gdp_cap, and the list life_exp; it is information about Zimbabwe. 
Build a line chart, with gdp_cap on the x-axis, and life_exp on the y-axis. Does it make sense to plot this data on a line plot? 
Don't forget to finish off with a plt.show() command, to actually display the plot. 
# Print the last item of gdp_cap and life_exp 
print(life_exp[-1]) 
print (gdp_cap[-1]) 
  
# Make a line plot, gdp_cap on the x-axis, life_exp on the y-axis 
plt.plot(gdp_cap, life_exp) 
  
# Display the plot 
plt.show() 
 
Scatter Plot (1) 
100xp 
When you have a time scale along the horizontal axis, the line plot is your friend. But in many other cases, when you're trying to assess if there's a correlation between two variables, for example, the scatter plot is the better choice. Below is an example of how to build a scatter plot. 
import matplotlib.pyplot as pltplt.scatter(x,y)plt.show() 
Let's continue with the gdp_cap versus life_exp plot, the GDP and life expectancy data for different countries in 2007. Maybe a scatter plot will be a better alternative? 
Again, the matploblib.pyplot package is available as plt. 
Instructions 
Change the line plot that's coded in the script to a scatter plot. 
A correlation will become clear when you display the GDP per capita on a logarithmic scale. Add the line plt.xscale('log'). 
Finish off your script with plt.show() to display the plot. 
# Change the line plot below to a scatter plot 
plt.scatter(gdp_cap, life_exp) 
# Put the x-axis on a logarithmic scale 
plt.xscale('log') 
# Show plot 
plt.show() 
 
 
 
DataCamp 
Course Outline 
5 
Scatter plot (2) 
100xp 
In the previous exercise, you saw that that the higher GDP usually corresponds to a higher life expectancy. In other words, there is a positive correlation. 
Do you think there's a relationship between population and life expectancy of a country? The list life_exp from the previous exercise is already available. In addition, now also pop is available, listing the corresponding populations for the countries in 2007. The populations are in millions of people. 
Instructions 
Start from scratch: import matplotlib.pyplot as plt. 
Build a scatter plot, where pop is mapped on the horizontal axis, and life_exp is mapped on the vertical axis. 
Finish the script with plt.show() to actually display the plot. Do you see a correlation? 
Take Hint (-30xp) 
script.py 
 
# Import package 
# Build Scatter plot 
# Show plot 
Submit Answer 
IPython Shell 
Slides 
In [1]:  
Scatter plot (2) 
100xp 
In the previous exercise, you saw that that the higher GDP usually corresponds to a higher life expectancy. In other words, there is a positive correlation. 
Do you think there's a relationship between population and life expectancy of a country? The list life_exp from the previous exercise is already available. In addition, now also pop is available, listing the corresponding populations for the countries in 2007. The populations are in millions of people. 
Instructions 
Start from scratch: import matplotlib.pyplot as plt. 
Build a scatter plot, where pop is mapped on the horizontal axis, and life_exp is mapped on the vertical axis. 
Finish the script with plt.show() to actually display the plot. Do you see a correlation? 
# Import package 
import matplotlib.pyplot as plt 
  
# Build Scatter plot 
plt.scatter(pop, life_exp) 
  
# Show plot 
plt.show() 
 
 
No clear relationship is found between population size and life expectancy.  
Histogram: 
Shows the distribution of variables based on bins. 
import matplotlib.pyplot as plt 
Plt.hist(x, bins=10, range=none, normed=False, weights = None, cumulative=False, bottom=None, histtype='bar', align='mid', orietations='vertical', rwidth=None, data=None, **kwargs) 
 X is the list of variables 
Number of bins required (10 by default) 
Values = [0,0.6,1.4,1.6,2.2,2.5,2.6, 3.0] 
Plt.hist(values, bins=3) 
Plt.show() 
Build a histogram (1) 
100xp 
life_exp, the list containing data on the life expectancy for different countries in 2007, is available in your Python shell. 
To see how life expectancy in different countries is distributed, let's create a histogram of life_exp. 
matplotlib.pyplot is already available as plt. 
Instructions 
Use plt.hist() to create a histogram of the values in life_exp. Do not specify the number of bins; Python will set the number of bins to 10 by default for you. 
Add plt.show() to actually display the histogram. Can you tell which bin contains the most observations? 
# Create histogram of life_exp data 
plt.hist(life_exp) 
  
# Display histogram 
plt.show() 
 
Build a histogram (2): bins 
100xp 
In the previous exercise, you didn't specify the number of bins. By default, Python sets the number of bins to 10 in that case. The number of bins is pretty important. Too few bins will oversimplify reality and won't show you the details. Too many bins will overcomplicate reality and won't show the bigger picture. 
To control the number of bins to divide your data in, you can set the bins argument. 
That's exactly what you'll do in this exercise. You'll be making two plots here. The code in the script already includes plt.show() and plt.clf() calls; plt.show() displays a plot; plt.clf()cleans it up again so you can start afresh. 
As before, life_exp is available and matploblib.pyplot is imported as plt. 
Instructions 
Build a histogram of life_exp, with 5 bins. Can you tell which bin contains the most observations? 
Build another histogram of life_exp, this time with 20 bins. Is this better? 
# Build histogram with 5 bins 
plt.hist(life_exp, bins=5) 
  
# Show and clean up plot 
plt.show() 
plt.clf() 
  
# Build histogram with 20 bins 
plt.hist(life_exp, bins=20) 
  
# Show and clean up again 
plt.show() 
plt.clf() #clears plot 
 
 
# Histogram of life_exp, 15 bins 
plt.hist(life_exp, bins = 15) 
# Show and clear plot 
plt.show() 
plt.clf() 
  
# Histogram of life_exp1950, 15 bins 
plt.hist(life_exp1950, bins = 15) 
  
# Show and clear plot again 
plt.show() 
plt.clf() 
 
 
 
 
 
 
Labels 
100xp 
It's time to customize your own plot. This is the fun part, you will see your plot come to life! 
You're going to work on the scatter plot with world development data: GDP per capita on the x-axis (logarithmic scale), life expectancy on the y-axis. The code for this plot is available in the script. 
As a first step, let's add axis labels and a title to the plot. You can do this with the xlabel(), ylabel() and title() functions, available in matplotlib.pyplot. This sub-package is already imported as plt. 
Instructions 
The strings xlab and ylab are already set for you. Use these variables to set the label of the x- and y-axis. 
The string title is also coded for you. Use it to add a title to the plot. 
After these customizations, finish the script with plt.show() to actually display the plot. 
# Basic scatter plot, log scale 
plt.scatter(gdp_cap, life_exp) 
plt.xscale('log')  
  
# Strings 
xlab = 'GDP per Capita [in USD]' 
ylab = 'Life Expectancy [in years]' 
title = 'World Development in 2007' 
  
# Add axis labels 
plt.xlabel(xlab) 
plt.ylabel(ylab) 
 
# Add title 
plt.title(title) 
  
# After customizing, display the plot 
plt.show() 
 
 
Ticks 
100xp 
The customizations you've coded up to now are available in the script, in a more concise form. 
In the video, Filip has demonstrated how you could control the y-ticks by specifying two arguments: 
plt.yticks([0,1,2], ["one","two","three"]) 
In this example, the ticks corresponding to the numbers 0, 1 and 2 will be replaced by one, two and three, respectively. 
Let's do a similar thing for the x-axis of your world development chart, with the xticks() function. The tick values 1000, 10000 and 100000 should be replaced by 1k, 10k and 100k. To this end, two lists have already been created for you: tick_val and tick_lab. 
Instructions 
Use tick_val and tick_lab as inputs to the xticks() function to make the the plot more readable. 
As usual, display the plot with plt.show() after you've added the customizations. 
# Scatter plot 
plt.scatter(gdp_cap, life_exp) 
  
# Previous customizations 
plt.xscale('log')  
plt.xlabel('GDP per Capita [in USD]') 
plt.ylabel('Life Expectancy [in years]') 
plt.title('World Development in 2007') 
  
# Definition of tick_val and tick_lab 
tick_val = [1000,10000,100000] 
tick_lab = ['1k','10k','100k'] 
  
# Adapt the ticks on the x-axis 
plt.xticks(tick_val, tick_lab) 
  
# After customizing, display the plot 
plt.show() 
 
 
Sizes 
100xp 
Right now, the scatter plot is just a cloud of blue dots, indistinguishable from each other. Let's change this. Wouldn't it be nice if the size of the dots corresponds to the population? 
To accomplish this, there is a list pop loaded in your workspace. It contains population numbers for each country expressed in millions. You can see that this list is added to the scatter method, as the argument s, for size. 
Instructions 
Run the script to see how the plot changes. 
Looks good, but increasing the size of the bubbles will make things stand out more. 
Import the numpy package as np. 
Use np.array() to create a numpy array from the list pop. Call this Numpy array np_pop. 
Double the values in np_pop by assigning np_pop * 2 to np_pop again. Because np_pop is a Numpy array, each array element will be doubled. 
Change the s argument inside plt.scatter()to be np_pop instead of pop. 
# Import numpy as np 
import numpy as np 
# Store pop as a numpy array: np_pop 
np_pop = np.array(pop) 
# Double np_pop 
np_pop = np_pop * 2 
# Update: set s argument to np_pop 
plt.scatter(gdp_cap, life_exp, s = np_pop) 
# Previous customizations 
plt.xscale('log')  
plt.xlabel('GDP per Capita [in USD]') 
plt.ylabel('Life Expectancy [in years]') 
plt.title('World Development in 2007') 
plt.xticks([1000, 10000, 100000],['1k', '10k', '100k']) 
# Display the plot 
plt.show() 
 
Colors 
100xp 
The code you've written up to now is available in the script on the right. 
The next step is making the plot more colorful! To do this, a list colhas been created for you. It's a list with a color for each corresponding country, depending on the continent the country is part of. 
How did we make the list col you ask? The Gapminder data contains a list continent with the continent each country belongs to. A dictionary is constructed that maps continents onto colors: 
dict = {    'Asia':'red',    'Europe':'green',    'Africa':'blue',    'Americas':'yellow',    'Oceania':'black'} 
Nothing to worry about now; you will learn about dictionaries in the next chapter. 
Instructions 
Add c = col to the arguments of the plt.scatter() function. 
Change the opacity of the bubbles by setting the alphaargument to 0.8 inside plt.scatter(). Alpha can be set from zero to one, where zero is totally transparent, and one is not at all transparent. 
 
# Specify c and alpha inside plt.scatter() 
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8) 
# Previous customizations 
plt.xscale('log')  
plt.xlabel('GDP per Capita [in USD]') 
plt.ylabel('Life Expectancy [in years]') 
plt.title('World Development in 2007') 
plt.xticks([1000,10000,100000], ['1k','10k','100k']) 
# Show the plot 
plt.show() 
Additional Customizations 
100xp 
If you have another look at the script, under # Additional Customizations, you'll see that there are two plt.text() functions now. They add the words "India" and "China" in the plot. 
Instructions 
Add plt.grid(True) after the plt.text() calls so that gridlines are drawn on the plot. 
# Scatter plot 
plt.scatter(x = gdp_cap, y = life_exp, s = np.array(pop) * 2, c = col, alpha = 0.8) 
  
# Previous customizations 
plt.xscale('log')  
plt.xlabel('GDP per Capita [in USD]') 
plt.ylabel('Life Expectancy [in years]') 
plt.title('World Development in 2007') 
plt.xticks([1000,10000,100000], ['1k','10k','100k']) 
  
# Additional customizations 
plt.text(1550, 71, 'India') 
plt.text(5700, 80, 'China') 
  
# Add grid() call 
plt.grid(True) 
  
# Show the plot 
plt.show() 
 
 
Page Break
 
Motivation for dictionaries 
100xp 
To see why dictionaries are useful, have a look at the two lists defined on the right. countries contains the names of some European countries. capitals lists the corresponding names of their capital. 
Instructions 
Use the index() method on countries to find the index of 'germany'. Store this index as ind_ger. 
Use ind_ger to access the capital of Germany from the capitals list. Print it out. 
 
# Definition of countries and capital 
countries = ['spain', 'france', 'germany', 'norway'] 
capitals = ['madrid', 'paris', 'berlin', 'oslo'] 
  
# Get index of 'germany': ind_ger 
ind_ger=countries.index('germany') 
  
# Use ind_ger to print out capital of Germany 
print(capitals[ind_ger]) 
 
Create dictionary 
100xp 
The countries and capitals lists are again available in the script. It's your job to convert this data to a dictionary where the country names are the keys and the capitals are the corresponding values. As a refresher, here is a recipe for creating a dictionary: 
my_dict = {   "key1":"value1",   "key2":"value2",} 
In this recipe, both the keys and the values are strings. This will also be the case for this exercise. 
Instructions 
With the strings in countries and capitals, create a dictionary called europe with 4 key:value pairs. Beware of capitalization! Make sure you use lowercase characters everywhere. 
Print out europe to see if the result is what you expected. 
# Definition of countries and capital 
countries = ['spain', 'france', 'germany', 'norway'] 
capitals = ['madrid', 'paris', 'berlin', 'oslo'] 
  
# From string in countries and capitals, create dictionary europe 
europe = {'spain':'madrid', 'france':'paris', 'germany':'berlin', 'norway':'oslo'} 
  
# Print europe 
print(europe) 
 
End free course: 
Udacity Intro do Datascience 
 
 
 
 
