# Big Data Project
Intro: This is an individual project I completed for a Data Science class. With New York City Middle School data provided by the New York City Department of Education, we were tasked with extrapoloting insights and attributes through as part of our analysis. Our objective of interest was determining the most important attributes middle schools should have for individual student admission into one of eight highly selective high schools. 



# Questions and Results:

# 1) What is the correlation between the number of applications and admissions to HSPHS?

<img width="676" alt="Screen Shot 2022-04-19 at 12 27 40 AM" src="https://user-images.githubusercontent.com/97006483/163920129-20a85dd7-d222-4ffa-a4c2-e345fd0010c2.png">




# 2) What is a better predictor of admission to HSPHS? Raw number of applications or application rate?

Here I created two linear models and then used sk learn to calculate the regression. The application number had a greater correlation. Intuitively speaking, this makes sense: if you have a high rate of applications, from a small, cruddy school, then you are if a worse boat than a school that is a large, high-end school that sends out a high volume of applications. This is because the application number is a measure of count while the rate is more like an average.


![Screen Shot 2022-06-02 at 2 30 36 AM](https://user-images.githubusercontent.com/97006483/171577447-91c1a437-417e-4f3e-ba52-878a007ebe23.png)


# 3) Which school has the best *per student* odds of sending someone to HSPHS?

<img width="886" alt="Screen Shot 2022-04-19 at 1 14 53 PM" src="https://user-images.githubusercontent.com/97006483/164059157-c2e2499d-6190-4a2a-8d78-9fd6f99079e1.png">



# 4) Is there a relationship between how students perceive their school (as reported in columns L-Q) and how the school performs on objective measures of achievement (as noted in columns V-X).

There is a very weak relationship. I first calculated the principal components for (L-Q) and then (V-X). PC1 (of L-Q) correlates well with each of (L-Q) individually. So I decided to use PC1 to represent this range of variables. I then used PC1 to see how well it correlated to each of W-X and found that it was very weak across the board.


<img width="799" alt="Screen Shot 2022-04-19 at 1 15 50 PM" src="https://user-images.githubusercontent.com/97006483/164059290-2d86af67-1b51-4b95-88a3-aa79cde8e66f.png">
<img width="808" alt="Screen Shot 2022-04-19 at 1 16 02 PM" src="https://user-images.githubusercontent.com/97006483/164059316-f87bf03b-6213-4ab0-92fd-b293bae41d91.png">

<img width="639" alt="Screen Shot 2022-04-19 at 1 16 13 PM" src="https://user-images.githubusercontent.com/97006483/164059345-71ca8ff5-f347-4619-8a8f-33ee4a4368ca.png">


# 5) Test a hypothesis of your choice as to which kind of school (e.g. small schools vs. large schools or charter schools vs. not (or any other classification, such as rich vs. poor school)) performs differently than another kind either on some dependent measure, e.g. objective measures of achievement or admission to HSPHS (pick one).

# My Hypothesis: The mean scores for math is higher for charter schools than it is for non-charter schools. 

<img width="792" alt="Screen Shot 2022-04-19 at 1 17 49 PM" src="https://user-images.githubusercontent.com/97006483/164059616-fe3f7549-0078-436e-849c-d7b166c35168.png">


# 6) Is there any evidence that the availability of material resources (e.g. per student spending or class size) impacts objective measures of achievement or admission to HSPHS?

# Claim: The correlations do not support the claim that availability of material resoures have any bearing on objective measures of achievement or admission to HSPHS. In fact, the correlations suggest the opposite. 

<img width="519" alt="Screen Shot 2022-04-19 at 1 18 38 PM" src="https://user-images.githubusercontent.com/97006483/164059737-bcf89b43-3638-4f05-833a-aab3290a6292.png">

# Findings: We reject the null hypothesis that the mean math scores are equal for Charter schools v.s. Noncharter schools. The two schools perform differently, with charter schools performing slightly better than noncharter (55% and 38%, respectively).

# 7) What proportion of schools accounts for 90% of all students accepted to HSPHS?

<img width="624" alt="Screen Shot 2022-04-19 at 1 20 26 PM" src="https://user-images.githubusercontent.com/97006483/164060009-d603fdd2-6e64-4c52-bbe0-4991334216ee.png">


# 8) Build a model of your choice – clustering, classification or prediction – that includes all factors – as to what school characteristics are most important in terms of a) sending students to HSPHS, b) achieving high scores on objective measures of achievement?

Model: 

I Performed PCA and then ran multiple regression to determine the most important school characteristics in sending students to HSPHS.
a. The most important factors for sending students to HSPHS were based on student achievement in the form of math and reading scores. In addition, the percentage of Asian students at the school mattered, as the scores and Asian percentages are likely correlated with one another, given that this demographic of students could possibly perform better on those tests compared to other races. Avg. class size and student achievement mattered mildly as well

<img width="809" alt="Screen Shot 2022-04-19 at 1 22 53 PM" src="https://user-images.githubusercontent.com/97006483/164060416-9c5dc72f-11c8-443f-88ef-967a2296d233.png">

b. Rigor of instruction, number of applications, Supportive environment, per pupil spending. Collaborative teachers, strong family community ties. These factors represented most of the variation.

<img width="759" alt="Screen Shot 2022-04-19 at 1 24 04 PM" src="https://user-images.githubusercontent.com/97006483/164060600-b7678484-c89b-4ef5-a84a-247edbd804dd.png">






# 9) Write an overall summary of your findings – what school characteristics seem to be most relevant in determining acceptance of their students to HSPHS?

# Findings:

The schools that performed the best in terms of sending their students to HSPHS embodied many of the same features. Student achievement, as a form of objective student success, seemed to have the greatest bearing on acceptance to the school. From this variable alone, we can conclude that schools that have higher test scores have better equipped, prepared, and trained students coming from learning and communal environments that are more conducive to learning and general student success.



# 10) Imagine that you are working for the New York City Department of Education as a data scientist (like one of my former students). What actionable recommendations would you make on how to improve schools so that they a) send more students to HSPHS and b) improve objective measures or achievement. 




a. The most important thing to do would be to create more challenging courses for the students. Unfortunately, when dealing with low-income schools the students may not be as prepared or on the same level as students from more affluent backgrounds. The best course of action would be to provide students with smaller more upclose instruction that allows them to discover their strengths and push them to the max. This would boost student achievement and confidence, later having an affect on their scores.


b. They could train the teachers to be more collaborative, as this mattered for the test score performance. Paired with a supportive and collaborative classroom learning environment, the students would receive more hands on learning with the skills they need to perform well. It would also serve to address any weaknesses they may have with the material.
