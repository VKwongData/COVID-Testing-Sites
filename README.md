# Choosing COVID-19 Testing Site Locations Using Solver in Excel

This is a repository for an assignment from the course OPM9500
Decision Models and Analytics (Spring 2022 semester) at the Zicklin School of Business. 
This was an individual assignment and involved using Solver in Excel
to tackle the problem detailed below.

## The Problem

Create a linear model to solve the following:

Below are two maps: to the left, a map of a city with 28 neighborhoods and their respective populations; to the right, 
a map of the same 28 neighborhoods and the cost of establishing a test site in each neighborhood. 

![test_data](https://user-images.githubusercontent.com/94913441/182185907-7e424f17-f3c1-4b4f-901b-771f766ec3a1.png)

Below are the assumptions for this problem:
1) 90% of the population of a neighborhood will be tested if a test site is established in that neighborhood
2) 60% of the population of a neighborhood will be tested if that neighborhood is adjacent (i.e., north, south, east, 
west, northeast, southeast, northwest or southwest) to a neighborhood with a test site
3) The city has a budget of $11,000 to establish test sites


The goal is to determine in which neighborhoods 
the city should establish test sites such that the maximum number of people is tested. 

## The Solution

The solution 
is saved in this repository <a href="https://github.com/VKwongData/COVID-Testing-Sites/blob/main/COVID-19%20Testing%20Sites.xlsx">here</a>. 
Please note that there are two tabs: 
<ol>
<li><b>Model:</b> Includes all the data used and the Solver model that uses Simplex LP</li>
<li><b>Explanation:</b> Includes a brief explanation of the model describing the decision variables, constraints and objective</li>
</ol>
