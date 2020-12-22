
# School Funding Affects on ACT AND SAT Scores

### Problem Statement
How effective are government funding programs in assisting lower-income students prepare for college?

Research on school funding in the state of California, where does the money come from for school funding:

58% of school funds come from the state
21% come from local property tax
12% other local sources
8% from federal sources
1% from the lotttery (source)
At the state and federal level, there are programs in place to help support districts with a high number of lower-income students.

Title I (Federal Program)- provides federal aid program for low income school districts(source)
Local Control Funding Formula (LCFF)- formula which is used to determine how much state funds school districts receive. School districts with higher levels of poverty, foster care and/or districts with ESL students receive more state funding. (source)

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



As the districts with high daily_expenditure seem to have higher percentage_of_eligible_for_frpm. Districts with high percentage_of_eligible_for_frpm seem to be have lower ACT and SAT success rates. In congruence with the other two notes, districts with high daily_expenditure seem to have less success on the ACT and SAT.



### Conclusions and Recommendations

The Title I program and the LCFF were put into place to give each student equal opportunity to succeed. The data presented suggests the program is not doing enough to curb the difference between lower income students and their peers when it comes to ACT and SAT scores.

It has been suggested that even with the government funded program schools in lower-income areas are not getting enough funding.

Some argue that allocating state funds based on attendance rather than enrollment disproprotionately hurts low income schools
The issue may be how the funds are allocated.

Districts get funding based on poverty level but the allocation of funds is purely decided by the district
Or money may not be the solution to solving the problem. It is safe to say that the current funding program is not doing enough to help underprivlaged students prepare for college.
