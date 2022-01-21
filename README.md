# election_analysis

## Overview

The purpose of the project was to perform an analysis on a sample election results file (election_results.csv) using Python and determine the winning candidate and the county with the largest turnout. The results were then saved to election_analysis.txt in an easy to read format. "PyPoll.py" contains the code used for candidate results analysis. "PyPoll_Challenge.py", on the other hand, contains the code for county analysis as well as all the "PyPoll.py" code. 

## Analysis

Python conditional statements and for loops were used to obtain the results. For this section, only the code used for the county analysis will be discussed as the concepts used were similar. 

<img width="519" alt="Loading dependencies and the csv file" src="https://user-images.githubusercontent.com/92544151/150611241-e111583e-4f5a-4c7b-ac5f-785d9271ca7e.png">

The first step consisted of loading dependencies and the paths to the both files, file to load and the one to save. 

<img width="445" alt="Code(1)" src="https://user-images.githubusercontent.com/92544151/150611686-fbf04862-c566-4990-83fd-8a5f7e9ff207.png">
<img width="437" alt="Code(2)" src="https://user-images.githubusercontent.com/92544151/150611687-9eff3a98-83cf-404d-9813-c0959055bd5a.png">

Then it was time to create an empty list named "county_list" and an empty dictionary, "county_votes". The largest_turnout_county was an empty string at this point and the winning_county_votes started from 0. 

<img width="266" alt="Code(3a)" src="https://user-images.githubusercontent.com/92544151/150611737-d18c12b9-f856-4014-86fc-b45c0c7091e1.png">
<img width="360" alt="Code(3b)" src="https://user-images.githubusercontent.com/92544151/150611757-bad386fa-a3ab-4700-89ba-73988d1b9650.png">

After looking at the .csv file, "county_name" was set as index 1 of each row using "for row in header". 

<img width="524" alt="Code(4 5)" src="https://user-images.githubusercontent.com/92544151/150611859-5aa54825-17fa-4e02-8a0e-7f946c2c9d24.png">

If the "county_name" in a row was not a part of our list "county_list", it was appended to latter. This ensured that "county_list" consisted of unique values. For the empty dictionary, "county_votes", I started tracking the county's vote count and for each row the vote was added to respective keys. 

<img width="743" alt="Code(6,7,8)" src="https://user-images.githubusercontent.com/92544151/150612150-90ca2685-2d6e-48fe-b6b7-47f67271ca6c.png">

A for loop was then used to iterate through each county in "county_votes" dictionary, and "county_votes_percentage" was calculated. Inside the loop, an if statement was used to determine the winning county and get it's vote count. The results were printed to the terminal and saved to the text file. 

## Results 

The "election_analysis.txt" file contains the following results: 

<img width="284" alt="Results" src="https://user-images.githubusercontent.com/92544151/150612487-bee92fc8-d255-4e20-8277-a7e700e7c8f6.png">

Denver had the highest turnout (82.78%), followed by Jefferson and Arapahoe. With regards to the winning candidate, Diana DeGette won the election by a large margin (73.8% of total votes cast). Charles Casper Stockham was runners up with 23.0% of votes cast. Raymon Anthony Doane won a measly 3.1% of total votes cast. 

## Summary

The Python script used to analyze the results can be used for many other similar elections. If the .csv file containing the results has an exact layout as the "election_results.csv" file, then no changes need to be made. Just ensure that the path to the file is correct in the following section of the code. If the file is saved somewhere else, make sure the "file_to_load" variable has the correct directory information. 

<img width="519" alt="Loading dependencies and the csv file" src="https://user-images.githubusercontent.com/92544151/150613420-9290e8d5-2c19-4ca8-ae56-9906eeb4450e.png">

On the other hand, if the columns numbers are different in the new file, make sure that the correct column indexes are referred in the following section of the code:

<img width="474" alt="Code(changes_needed)" src="https://user-images.githubusercontent.com/92544151/150613647-60cc697b-92a9-421c-86b0-b9084b57599a.png">

As long as these major details are taken care of, this Python script will save the results to the "election_analysis.txt" file. The results will cover the winning candidate and the county with the largest turnout. 




