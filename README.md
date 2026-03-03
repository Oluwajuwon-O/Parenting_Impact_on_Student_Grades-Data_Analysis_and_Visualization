# Impact of Parenting on Student's Performance
## by Oluwajuwon Oyalude


## Dataset
>The dataset to be analyzed contains two subsets of student performance in two distinct subjects in two Portuguese schools. The subjects are maths and portuguese. It also contains information about their parental background. These data relate to the state of their relationships and their profession. The data was collated using questionnaires. I analyzed the data on the portuguese subject.
The dataset was tidy enough, the only wrangling I performed was obtaining the average of the 3 provided grades of the students which I then chose as my main variable of interest.
There are 649 students in the dataset with 33 columns. They are
1. school - student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)
2. sex - student's sex (binary: 'F' - female or 'M' - male)
3. age - student's age (numeric: from 15 to 22)
4. address - student's home address type (binary: 'U' - urban or 'R' - rural)
5. famsize - family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)
6. Pstatus - parent's cohabitation status (binary: 'T' - living together or 'A' - apart)
7. Medu - mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)
8. Fedu - father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)
9. Mjob - mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
10. Fjob - father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'at_home' or 'other')
11. reason - reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')
12. guardian - student's guardian (nominal: 'mother', 'father' or 'other')
13. traveltime - home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour)
14. studytime - weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours, or 4 - >10 hours)
15. failures - number of past class failures (numeric: n if 1<=n<3, else 4)
16. schoolsup - extra educational support (binary: yes or no)
17. famsup - family educational support (binary: yes or no)
18. paid - extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)
19. activities - extra-curricular activities (binary: yes or no)
20. nursery - attended nursery school (binary: yes or no)
21. higher - wants to take higher education (binary: yes or no)
22. internet - Internet access at home (binary: yes or no)
23. romantic - with a romantic relationship (binary: yes or no)
24. famrel - quality of family relationships (numeric: from 1 - very bad to 5 - excellent)
25. freetime - free time after school (numeric: from 1 - very low to 5 - very high)
26. goout - going out with friends (numeric: from 1 - very low to 5 - very high)
27. Dalc - workday alcohol consumption (numeric: from 1 - very low to 5 - very high)
28. Walc - weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)
29. health - current health status (numeric: from 1 - very bad to 5 - very good)
30. absences - number of school absences (numeric: from 0 to 93)
31. G1 - first period grade (numeric: from 0 to 20)
32. G2 - second period grade (numeric: from 0 to 20)
33. G3 - final grade (numeric: from 0 to 20)
34. avg_G - mean of all grades

They are mostly categorical variables of ordinal and nominal types.


## Summary of Findings
> Univariate Analysis
- The distribution of the grades of `avg_G` is approximately normal, but slightly skewed towards the left. Some students had average grades less than 6.0.
- `Pstatus`: Over 500 parents are living together. The number of those living apart isn't up to 100
- The trend in the distribution of `Fjob` is the same as Mjob, only that the difference between services & at_home is higher in Fjob than in Mjob
- `guardian`: A very high number of students have their mother as their guardian than father. This suggests that mothers are caring for their wards than fathers.
- `famsup`: The number of students who have family support outweighs those who don't
- Comparing `Fedu` and `Medu`, the mothers have higher level of education than the fathers. This can be seen by comparing the counts for education levels 3 & 4
- `famrel`: Most (over 300) of the students say they have "Very good" relationship with their parents. about 180 of them say they have excellent. A little over 100 are neutral (neither good nor bad). Around 30 say 'Bad', and the rest have very bad about their relationship with their parents.

> Bivariate Analysis: Investigating the columns against the performance of the students (`avg_G`)
- Investigating `Pstatus`: The performance of students whose parents are together isn't very different from those living apart
- In both `Fjob` and `Mjob`: the students whose parents are teachers had the best performance generally.
- `guardian`: Even though there are many who have their mothers as their guardians. Students who have their fathers as their guardians performed better generally. Although, the preceding got the highest scores. Students who had their father or mother as their guardian performed better than those who didn't. Students with people other than their parents, as their guardians performed the poorest.
- `famsup`: apparently, students with family support performed better than those who didn't but with very little difference.
- Looking at `Fedu` & `Medu`, it is observed that, the higher the level of education of the parents, the better the performance of their children (the students). However, students whose parents have no education are seen to be highly competitive (they didn't perform poorly). None of them got below 8 when compared with their counterparts.
- `famrel`: Generally, the better the quality of family relationships, the better the performance of students. However, students who had 'very good' family relationships performed better than those with 'excellent' family relationships.
When comparing the relationship between strength of student family relationship and student guardian
- No where across the spectrum are fathers more than mothers. For students with very bad family relationships, their fathers are almost absent and this affects their academic performance as seen before.
- Furthermore, the ratio of mothers to fathers as student guardians is very large especially in family relationships: 'very good' and 'excellent'. This further contributed to the theory that mothers tend to be there for their wards more than fathers.


> Multivariate Analysis:
- When Fathers are present as the guardian of the students, the better the quality of the relationship and consequently, the better the performance of students.
- Generally, as the level of the father education increases, the higher the students performance. Furthermore, Teachers are the most educated of the professions in our dataset. Very few or Zero teachers had low education levels. This also had an effect on the performance of the students, students whose parents were teachers had the best performance. For those who were at home, and had higher education, they were almost at par with the students whose parents were teachers. Similar trend as fathers education is found in mothers education when compared in respect to their jobs and their child(s) performance. However, students whose mothers have higher education but stay at home generally perform poorly than those whose mothers' occupation is teaching, as opposed to the trend found in the fathers job.
- Surprisingly , when facetted by jobs, the median average-score of student who don't get family support is higher than those who get family support. This explains the little difference in the aggregated medians.



## Key Insights for Presentation
- Students who have their parents as their guardians had better academic performance than those who do not.
- Most of the students had their mothers as their guardians, this tells that mothers tend to be there for their children than the fathers. 
This is commendable. Interestingly, analysis showed that the median grades of students whose fathers are their guardians is higher than 
those of the other students.
