# Python Pandas Analysis
An analysis of school district data using Pandas.

# Process

## District Summary
After reading in the CSV files (schools_complete.csv, students_complete.csv) I merged them then analyzed their components and data structure. I pulled a few basic values, such as the number of schools, students, and the total budget for the entire district. I gathered percentages for the number of students who passed math, reading, or both, to get a better idea of the overall pass-rate of the district in these subjects. I built a DataFrame called district_summary that included all of these values and formatted them as needed.

## Schools Summary
For a summary by-school I created a new DataFrame that was structured as a row for each school. It included finding the type of each school (district or charter), the number of students in each school by their school id, the budget for each school, spending per capita, and their average math/reading scores. If any student passed math or reading (>= 70 points) then they were included in the % Passing columns remaining in the DataFrame.

## Highest/Lowest Performing Schools (by % of Overall Passing)
Taking the precious DataFrame as my base, I found the top performing schools as "ascending" = False. Likewise the bottom performing schools were found by choosing True in the "ascending" parameter for the .sort_values() function.

## Math/Reading Scores by Grade
By splitting the school_data_complete DataFrame into the separate student grades I then grouped each grade by school and aggregated the math/reading scores by .mean(). Placing each grade/average score into a math or reading DataFrame allowed for a better understanding of the scores by student year.

## Scores by School Spending
Spending bins were set up so that the schools could estimate what their spending range was per-student when compared to the other schools in the district. Using this new bin series we could then create another DataFrame specifically to analyze Average and % of Passing scores for each spending range.

## Scores by School Size
Other bins were created, this time estimating small, medium, or large schools. The per_school_summary DataFrame was then fit with these bins to categorize them. Like above a sister DataFrame was created that estimated the average and % of Passing scores, this time by the size of the school.

## Scores by School Type
The last DataFrame created included a simple analysis of scores by school type (Charter or District.) these are the same Averages and % of Passing series used above.

# Analysis 
  My analysis is attached as a Microsoft Word document for the purpose of a more simplified ReadMe and a more aesthetically pleasing report. 

### Citations
Project instructions and starter code provided by UCF as part of their 2023 Data Analytics Bootcamp. 
