# Pewlett-Hackard_Analysis

## Overview of Analysis

* Using the ERD's we created in this module as a reference and our knowledge of SQL queries, we created a Retirement Titles table that holds all the titles of employees who were born between January 1, 1952 and December 31, 1955. Because some employees may have multiple titles in the database—for example, due to promotions— we used the DISTINCT ON statement to create a table that contains the most recent title of each employee. Then, we also used the COUNT() function to create a table that has the number of retirement-age employees by most recent job title. Finally, because we want to include only current employees in our analysis, we were sure to exclude those employees who have already left the company.

## Results

* We the excluded employees that have already left the company by filtering on the to_date to keep only those date that are equal to 9999-01-01. This enabled us to create a new table which we named Unique titles. We found 133,776 retiring employees, but there are duplicate entries for some employees because they have switched titles over the years, the results shows us only 72,458 employees ready to retire.
<img width="822" alt="retirement_title" src="https://user-images.githubusercontent.com/111805716/212589675-da85c6ee-8ede-4811-a992-11911c961f82.png">


<img width="821" alt="unique_titles" src="https://user-images.githubusercontent.com/111805716/212589852-5ecd39e6-9fb4-432d-9a26-e8878db89b12.png">

* By creating another query and retrieving the number of titles from the Unique titles table, we in turn created another table by using the group function. This sortred out and counted the most recent employees who are retiring categorized by title.


<img width="804" alt="retirment_most_recent" src="https://user-images.githubusercontent.com/111805716/212593753-36ea817c-668e-4c01-9a6e-e4dd7cc23ba7.png">

## Summary

### Mentorship eligibilty
* We retrieved some similar columns from our Employees ttable, Department Employee Table and joined our titles column from our titles table. We then filtered the data from the to_date column for all the current employee. After that we sorted out our table by employee number, This resulted us in determining the mentorship eligibility for our employees.
<img width="822" alt="mentorship_eligibility" src="https://user-images.githubusercontent.com/111805716/212594146-407f2fb3-b665-419d-af01-ab1b3271af3e.png">

Overall, our analyses pointed out some issues of concern:

* The active managers are less than the number of departments, which makes us think that there are departments without a manager and the rest have double the burden of having to deal with those departments. There are only 1,549 employees with the possibility of a Mentoring Program.
* There are repeated names of employees and in different departments, which makes us believe that the databases of the employees and departments have not been updated based on their last position.
* We were able to deduce that there are no salary increases.
