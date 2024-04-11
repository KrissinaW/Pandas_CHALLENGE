# Pandas_CHALLENGE
Module 4 

Creating and manipulating Pandas Data Frames to analyze school and standardized test data.

**Background**
I am the new Chief Data Scientist for your city's school district. 
In this capacity, I will be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.

Foe my first assignment, I have been asked to analyze the district-wide standardized test results. I have been given access to every student's math and reading scores, as well as various information on the schools they attend. I will aggregate the data to showcase obvious trends in school performance.



The following analysis will be stored in a Jupyter Notebook and the code will be broken up in segments outlined below: 

**District Summary**
In this section I will perform the necessary calculations and create a high-level snapshot of the district's key metrics in a DataFrame.

The following is to be included:

- Total number of unique schools
- Total students
- Total budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

**School Summary**
I will perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

For this summary the following is to be included:

- School name
- School type
- Total students
- Total school budget
- Per student budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

**Highest-Performing Schools (by % Overall Passing)**
For this block of the challenge I am going to sort the schools by % Overall Passing in descending order and display the top 5 rows and save the results in a DataFrame called "top_schools".

**Lowest Performing Schools (by % Overall Passing)**
 The schools will be sorted by % Overall Passing in ascending order and display the top 5 rows then save the results in a DataFrame called "bottom_schools".

**Math Scores by Grade**
I will perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

**Reading Scores by Grade**
I will create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

**Scores by School Spending**
I will create a table that breaks down school performance based on average spending ranges (per student).

The code provided below will be used to create four bins with reasonable cutoff values to group school spending.

spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
Use pd.cut to categorize spending based on the bins.

The following code will be used to then calculate mean scores per spending range.

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
Use the scores above to create a DataFrame called spending_summary.

The following metrics will be included in the table:

- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)
- Scores by School Size

The following code will be used to bin the per_school_summary.

size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.

I will create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

**Scores by School Type**
I will use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.

This new DataFrame will show school performance based on the "School Type".

**Challenges met:**
The biggest challenge that I met was having to reformat objects into floats.  I spent most of my time in Chat GPT trying to figure out why my averages were not calculating and desplaying the way that they should in the output.  Once I was able to convert all objects to floats I was able to produce the correct outputs. 

**Strategy for overcoming Challenges:**
In this challenge I compaired my code to other coddes found in Git Hub from previous students who have completed the challenge, since the past assignments were so different I did not find it very useful, but ChatGOT was able to provide me with the guidance needed to over come the obstical while learning the reason why the values needed to be converted. 
