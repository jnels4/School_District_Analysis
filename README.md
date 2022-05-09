# School_District_Analysis

## Project Overview

This project was requested by a school district to gain insights for school metrics involving school size, school type and budget.  The district asked us to look at: 
- Math and Reading Scores
- Math and Reading Pass rates
- Overall passing rates (math + reading)
- scores and pass rates grouped by each school
- highest and loweset performing schools (top & bottom 5)
- Scores and Pass rates grouped by school type (charter vs district)
- Scores and pass rates grouped by per student spending (<$586, $586-630, $631-645, $646-675)
- Scores and pass rates grouped by school size (<1000, 1000-1999, 2000-5000)

## Resources
- studentdata.csv (csv file containing student grades/id number and schools)
- schooldata.csv (csv file contaiing school names, budgets, total school size)
- python3
- python3 pandas 
- python3 numpy
- jupiter notebook
- pyCitySchools.ipynb
- pyCitySchools_Challenge_final.ipynb


## Initial Data Overview (pyCitySchools)

The initial data analysis was done for all students of all schools in this district.  The first step was cleaning the data, we noticed that some of the students had unusual prefixes and suffixes in their names, by pulling out all the prefixes and suffixes we were able to identify the anomalies (DR., MD., DDS., etc) and strip them from the file.  Once we had cleaned up the student data, we were able to merge the student data with the overall school data based on the school name.  The merge allowed us to see all school and student data in one data frame. 

Next, we wanted to find a top-down view for the entire district that included overall budget, scores and pass rates. 

<img width="807" alt="Screen Shot 2022-05-09 at 8 42 42 AM" src="https://user-images.githubusercontent.com/6634774/167412104-789a6d2a-60f3-45af-9b5d-a3068fc8c187.png">

Now that we had the overall district information, we reported this back to our clients and continued with our requested deliverables.

First, we looked at scores & pass rates by school.  With this view, the district leaders can see the overall aggregate view for each school.  This data is good for a surface level view, but does not give us any in-depth analysis. The district also wanted the top 5 and bottom 5 schools based on overall passing rates (percentage of students who passed both math and reading exams).  This data is (mostly) unformatted because we were still working with it and adding to it as we got deeper into the analysis.  (screen shots following)

Overall School Data

<img width="804" alt="Screen Shot 2022-05-09 at 8 50 27 AM" src="https://user-images.githubusercontent.com/6634774/167413407-7c4a208d-df7d-4304-b4d1-4727e493cd81.png">

Top 5 Schools

<img width="804" alt="Screen Shot 2022-05-09 at 8 53 02 AM" src="https://user-images.githubusercontent.com/6634774/167413911-1df51a86-7c46-4cf1-9a1f-b22c69297c6e.png">

Bottom 5 Schools

<img width="804" alt="Screen Shot 2022-05-09 at 8 53 42 AM" src="https://user-images.githubusercontent.com/6634774/167414023-6c7942e8-027f-476f-a7c2-b7a307a68c95.png">

The next four views we looked at were:
- School data accross grade bands

<img width="310" alt="Screen Shot 2022-05-09 at 10 51 59 AM" src="https://user-images.githubusercontent.com/6634774/167436823-84d987ae-a9f5-4be8-93d7-baa60f62c330.png">

- School data accross student spending 

<img width="790" alt="Screen Shot 2022-05-09 at 10 52 56 AM" src="https://user-images.githubusercontent.com/6634774/167437007-e499ae45-f3d4-478f-a9e9-2d8d13cb22dd.png">


- School data accross school size

<img width="681" alt="Screen Shot 2022-05-09 at 11 02 31 AM" src="https://user-images.githubusercontent.com/6634774/167438963-775dce0e-5a4a-4d30-a8f5-f12dd5caaf64.png">


- School data accross school type (charter vs district)

<img width="592" alt="Screen Shot 2022-05-09 at 12 09 05 PM" src="https://user-images.githubusercontent.com/6634774/167451671-f3d49efa-ff65-4329-9cc1-09625d1d9237.png">

## Initial findings

After reviewing the initial analysis on the school data, we c



