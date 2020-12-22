
# School Funding & Standardized Test Analysis

### Contents:
- [Problem Statement](#Problem-Statement)
- [Background](#Background)
- [Data](#Data)
- [Visualizations](#Visualizations)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Problem Statement
How effective are government funding programs in assisting lower-income students prepare for college?

## Background
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

CollegeBoard has set benchmarks for both the Math and evidence-based reading & writing (ERW) sections of the exam ([*source*](https://collegereadiness.collegeboard.org/pdf/educator-benchmark-brief.pdf))
* Math Benchmark = 530
* ERW Benchmark = 480

Research on school funding in the state of California, where does the money come from for school funding:

58% of school funds come from the state
21% come from local property tax
12% other local sources
8% from federal sources
1% from the lotttery (source)
At the state and federal level, there are programs in place to help support districts with a high number of lower-income students.

Title I (Federal Program)- provides federal aid program for low income school districts(source)
Local Control Funding Formula (LCFF)- formula which is used to determine how much state funds school districts receive. School districts with higher levels of poverty, foster care and/or districts with ESL students receive more state funding. (source)

## Data

* [`act_2019_ca.csv`](./data/act_2019_ca.csv): 2019 ACT Scores in California by School 
Has the 2019 ACT average scores grouped by district, as well as the percentage of students meeting an average standard of 21 or above on the exam.

* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School
Has the 2019 SAT percentage of those students meeting the college board benchmarks grouped by district. 

|Feature|Type|Dataset|Description|
|---|---|---|---|
|district|object|SAT_FRPM_EXP|School District Names in California| 
|total_enrollment|float|SAT_FRPM_EXP|Total Student Enrollment in a District| 
|total_test_takers|float|SAT_FRPM_EXP|Number of Students taking the SAT in the District| 
|precent_meeting_both_benchmarks|float|SAT_FRPM_EXP|Percent of test-takers meeting both the ERW and Math Benchmarks on the SAT| 
|school_year_expenditure|float|SAT_FRPM_EXP|Total expenditure for the school year per district| 
|average_daily_attendance|float|SAT_FRPM_EXP|The average daily attendance in a district| 
|daily_expenditure|float|SAT_FRPM_EXP|Expenditure per ADA(Average Daily Attendance) for a school district| 
|enrollment_k_thru_12|int|SAT_FRPM_EXP|Total enrollment in a district for K thru 12| 
|num_of_students_eligible_for_frpm|int|SAT_FRPM_EXP|Number of students eligible for FRPM in a district| 
|percentage_eligible_for_frpm|float|SAT_FRPM_EXP|Percent of total enrolled students that are eligible for FRPM| 
|district|object|ACT_FRPM_EXP|School District Names in California| 
|12th_enrollment|float|ACT_FRPM_EXP|Total 12th graders enrolled in a District| 
|12th_number_of_test_takers|float|ACT_FRPM_EXP|Number of 12 Graders taking the ACT in the District| 
|%_socres_greater>=21|float|ACT_FRPM_EXP|Percent of test-takers scoring an average of 21 or above on the ACT| 
|school_year_expenditure|float|ACT_FRPM_EXP|Total expenditure for the school year per district| 
|average_daily_attendance|float|ACT_FRPM_EXP|The average daily attendance in a district| 
|daily_expenditure|float|ACT_FRPM_EXP|Expenditure per ADA(Average Daily Attendance) for a school district| 
|enrollment_k_thru_12|int|ACT_FRPM_EXP|Total enrollment in a district for K thru 12| 
|num_of_students_eligible_for_frpm|int|ACT_FRPM_EXP|Number of students eligible for FRPM in a district| 
|percentage_eligible_for_frpm|float|ACT_FRPM_EXP|Percent of total enrolled students that are eligible for FRPM| 

## Visualizations
![alt text](https://github.com/smohan04/School-Funding/blob/main/img/sat_corr.png)
#### Note: 
The intent of this heat map was to study the effects of daily expenditure on success on the SAT. The heat map shows a negative correlation between the two which is somewhat unexpected.

![alt text](https://github.com/smohan04/School-Funding/blob/main/img/sat_vs_daily_exp.png)
#### Note: 
Again we see a downward trend in the scatter plot.

![alt text](https://github.com/smohan04/School-Funding/blob/main/img/act_corr.png)
![alt text](https://github.com/smohan04/School-Funding/blob/main/img/act_vs_daily_exp.png)

#### Note: 
ACT exams also show the same downward correlation between success on the exam and daily expenditure. From research, we know that school funding at the federal and state level both give more funding to schools with lower income families. Since percentage of students eligible for the Free and Reduced Price Meals (FRPM) can be a good estimate of income status of families, we will study the effects of FRPM and daily expenditure as well as test scores.

![alt text](https://github.com/smohan04/School-Funding/blob/main/img/SAT_FRPM_Corr.png)
![alt text](https://github.com/smohan04/School-Funding/blob/main/img/ACT_FRPM_Corr.png)
#### Note:
Both the ACT and SAT heat map show a strong negative correlation between eligibility for FRPM and test score. Daily expenditure is positively correlated with daily expenditure. These two correlations suggests that the correlation between daily expenditure and test scores may be negative correlated because of the relationship to percentage of FRPM students.

![alt text](https://github.com/smohan04/School-Funding/blob/main/img/SAT_FRPM_Scatter.png)
![alt text](https://github.com/smohan04/School-Funding/blob/main/img/ACT_FRPM_Scatter.png)
#### Note:
Both scatter plots show a strong negative correlation between test scores and eligibility for Free and Reduced Price Meals.

As the districts with high daily_expenditure seem to have higher percentage_of_eligible_for_frpm. Districts with high percentage_of_eligible_for_frpm seem to be have lower ACT and SAT success rates. In congruence with the other two notes, districts with high daily_expenditure seem to have less success on the ACT and SAT.

## Conclusions and Recommendations
The Title I program and the LCFF were put into place to give each student equal opportunity to succeed. The data presented suggests the program is not doing enough to curb the difference between lower income students and their peers when it comes to ACT and SAT scores.

It has been suggested that even with the government funded program schools in lower-income areas are not getting enough funding.
* Some argue that allocating state funds based on attendance rather than enrollment disproprotionately hurts low income schools

The issue may be how the funds are allocated.
* Districts get funding based on poverty level but the allocation of funds is purely decided by the district

Or money may not be the solution to solving the problem. 
It is safe to say that the current funding program is not doing enough to help underprivlaged students prepare for college.

## Next Step
* Research how funds are allocated in school districts.
* Study how the intiatication of these programs affected SAT/ACT scores
