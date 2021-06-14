# Employee Database with SQL

## Overview
The objective is to help Pewlett Hackard future-proof the company by using Postgres to create a database with employees' informations.  With this database, an analysis will be performed to determine:

  1. How many employees will be retiring and how many of those employees will be eligible for a retirement package?
  2. Determine the number of retiring employees per title.
  3. Identify employees who are eligible for a mentorship program.   

## Resources
- Data Source: [CSV files](https://github.com/junepwk/pewlett-hackard-analysis/tree/main/data)
- Software: pgAdmin 4 v5.2, PostgreSQL

## Results

### Retiring Employees by Job Title

- The first analysis was to create a table with all the titles of current employees who were born between January 1, 1952 and December 31, 1955.  However, this list includes old and new job titles for multitude of employees.
- In order to prevent duplicate employee numbers, such as those who may have multiple titles due to promotions, the 'DISTINCT ON' and the 'COUNT' functions were utilized.  These functions will filter the output to create a table that contains the most recent title for each employee. 

![retiring_titles_output](https://github.com/junepwk/pewlett-hackard-analysis/blob/main/output/retiring_titles_output.png)

### Employees Eligible for the Mentorship Program

- Pewlett Hackard is interested in introducing a mentor program to alleviate losing a large amount of workforce to retirement.  This program would allow experienced and successful employees to partake in mentoring new hires part-time.
- By using the 'COUNT' function on the [mentorship_eligibility](https://github.com/junepwk/pewlett-hackard-analysis/blob/main/data/mentorship_eligibility.csv) table, we will get a table of number of employees who are eligible for the program for each title.
- The table shows that the 'manager' department does not have any eligibility for mentorship despite having the possibility of 2 managers retiring.

![mentors_count_output](https://github.com/junepwk/pewlett-hackard-analysis/blob/main/output/mentors_count_output.png)

## Summary

