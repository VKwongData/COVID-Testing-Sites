# Choosing COVID-19 Testing Site Locations Using Solver in Excel

This is a repository for an assignment from the course OPM9500
Decision Models and Analytics (Spring 2022 semester) at the Zicklin School of Business. 
This was an individual assignment and involved using Solver in Excel
to tackle the problem detailed below.

## The Problem

Create a linear model to solve the following:

Below are two maps: to the left, a map of a city with 28 neighborhoods and their respective populations; to the right, 
a map of the same 28 neighborhoods and the cost of establishing a test site in each neighborhood. 

![test_data](https://user-images.githubusercontent.com/94913441/182252035-e0f97567-dee2-4bed-bada-9894db1f71bd.png)

Please note the following assumptions for this problem:
1) 90% of the population of a neighborhood will be tested if a test site is established in that neighborhood
2) 60% of the population of a neighborhood will be tested if that neighborhood is adjacent (i.e., north, south, east, 
west, northeast, southeast, northwest or southwest) to a neighborhood with a test site
3) The city has a budget of $11,000 to establish test sites


The goal is to determine in which neighborhoods 
the city should establish test sites such that the number of people tested is maximized. 

## The Solution

The model lets Solver assign a neighborhood as a neighborhood with a test site, a neighborhood adjacent to a test site, or neither. The population tested for each neighborhood is calculated for both scenarios (90% and 60%, respectively). Solver assigns test site neighborhoods such that the total cost of test sites cannot be greater than the budget. Solver also assigns which neighborhoods are adjacent neighborhoods to at least one test site. We have two binary Decision Variables ("DVs") for each neighborhood to decide: 1) whether a neighborhood has a test site, and 2) whether a neighborhood is adjacent to one. We are trying to maximize the number of people tested (while calculating that only 90% of the population in neighborhoods with test sites are tested and 60% in adjacent neighborhoods), so the objective is maximizing the combined population being tested in all neighborhoods.
 
 
The model's constraints are: 
1) DVs are binary (and non-negative)
2) Total cost (i.e., the sum of the cost of established test sites) is less than or equal to $11,000
3) Each neighborhood is assigned as a test site or as an adjacent neighborhood (or neither) but cannot be assigned as both (i.e., the sum of the test site and adjacent DVs for each neighborhood is less than or equal to 1)
4)  Each neighborhood assigned as an adjacent neighborhood must be adjacent to a test site (i.e., the adjacent DV for a neighborhood must be less than or equal to the sum of established test sites nearby)


The solution 
is saved in this repository <a href="https://github.com/VKwongData/COVID-Testing-Sites/blob/main/COVID-19%20Testing%20Sites.xlsx">here</a>. 
Please note that there are two tabs: 
<ol>
<li><b>Model:</b> Includes all the data used and the Solver model that uses Simplex LP</li>
<li><b>Explanation:</b> Includes the above explanation of the model describing the decision variables, constraints and objective</li>
</ol>
