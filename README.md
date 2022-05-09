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

After reviewing the initial analysis on the school data, we can see: 
1. Cursory analysis showed the top 5 schools each had a passing rate over 90%.
2. The bottom 5 schools each had a passing rate below 55%.
3. Top 5 schools math and reading passing percentages were within 4 points of each other.
4. Bottom 5 schools math and reading passing percentages were over 10 points apart and all cases math was the lower of the two.
5. Counterintuitively, schools who spent the lowest amount per student (<$585) statistically performed the best accross all metrics.
6. Schools which spent the most per student had the lowest overall passing rate by a large margin. 
7. Medium sized schools performed the best, followed very closely by small schools - large schools performed the worst accross all metrics (by far). 
8. Charter schools performed better than distric schools accross all metrics.


## Further review

After our initial findings were sent to the client, we recieved information that one high school reported wide spread academic dishonesty amongst their freshman class.  Thus, we had to review our findings and recalculate all data for that specific school (and the aggregate), without counting the 9th grade from that particular school.

We created a new variable to store the updated number of students, while removing the amount of 9th grade students from the school in question. 

Next, we had to re-do the metrics for that particular school, and adjust the overall metrics on an as-needed basis.  

After removing the 9th grade class for the high school in question, we re-calculated the top and botom 5 schools.  The results did not change, leaving the same schools in both the top and bottom 5. (keep in mind this data is not fully formatted yet, as we were still working with the numbers, and did not want to risk formatting columns that we would need to manipulate in the future).  

While the data for the affected school did change slight (less than a point), the schools rank did not change.

Top 5

<img width="800" alt="Screen Shot 2022-05-09 at 12 48 51 PM" src="https://user-images.githubusercontent.com/6634774/167458479-66e0570f-c701-4f21-9202-41a46344459a.png">

Bottom 5

<img width="804" alt="Screen Shot 2022-05-09 at 12 49 11 PM" src="https://user-images.githubusercontent.com/6634774/167458534-79334fc9-6f08-4e33-b52e-3f893bcf996f.png">

Schools grouped by spending per student
Due to one school losing their entire 9th grade data, we had to re calculate the average scores/percentages for each spending bracket.  Removing the 9th grade for one of the schools had no impact on the metrics for the spending groups.  

<img width="794" alt="Screen Shot 2022-05-09 at 1 06 50 PM" src="https://user-images.githubusercontent.com/6634774/167461305-90e043cc-9add-4b8a-931c-5c55c6be2fa5.png">

Schools grouped by school size

Again for the schools grouped by school size, the data did not change in any significant way, as we can see by comparing each chart before and after.  This means that removing the 9th grade for one school was not a significant enough of a change to skew the data. 

<img width="690" alt="Screen Shot 2022-05-09 at 1 10 20 PM" src="https://user-images.githubusercontent.com/6634774/167461836-a590bd78-806b-4fe7-b291-d38945b4e6af.png">

Schools by school type

Lastly, the differentiation between charter and district school did not change in any significant way.  Once the data was formatted it looks exactly like the picture before.

<img width="622" alt="Screen Shot 2022-05-09 at 1 12 09 PM" src="https://user-images.githubusercontent.com/6634774/167462108-0623fef8-020a-42a8-97d4-f0cd80820a2a.png">


## Conclusions

Once the 9th grade was removed:

The data for the particular school changed; however not significantly, each metric decreased by a fractional percentage which did not change rankings or overall statistics accross the school district.
  1. Average Math score          Before: 83.41   After:  83.35
  2. Average Reading score       Before: 83.85   After:  83.89
  3. % Passing math              Before: 93.27   After:  93.19%
  4. % Passing reading           Before: 97.31   After:  97.02%
  5. % Overall passing           Before: 90.95   After:  90.63%

Why did the overall statistics not change? 
  1. Formatting - the district asked for 1 decimal place for Averages and 0 decimal places for percentages.  Due to this, the change in data was not significant enough to show up in the final formatted data.
  2. Amount of data - There's a total of 39170 students in the district, the 9th grade of this particular school was 461 students.  Due to the sheer amount of data, this was only 1.1% of the total data that was thrown out, not causing any significant damage to the overall results.

Suggestions to the district:
  1. Overall, math scores are lower than reading accross the board.  We suggest: Investing school funds into math cirricula, Observing classrooms/practices in schools that have math scores >90 or percentages > 90%, investigating the elementary/middle schools that feed the high school districts with low scores.
  2. Schools that performed best had under 2000 students.  We suggest: Looking at the larger schools and seeing if they can be divided up into smaller community schools.  
  3. Re-test the 9th grade of the affected school, and add their data back to the analysis; while this may not have a large impact, it woulud give us (even if very slight) a better picture of how the entire district did as a whole. 
  
