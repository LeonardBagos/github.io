---
title: Cleaning the Dirtiest Data I’ve Seen Using Deep SQL and Power BI Knowledge
slug: project3
date: '2023-03-27'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  url: /images/sdd.PNG
  altText: Case study 3
  styles:
    self:
      borderRadius: x-large
  type: ImageBlock
bottomSections:
  - title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
    type: DividerSection
  - items:
      - title: Leonard Bagos
        subtitle: >-
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante
          lorem, tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at
          auctor sapien.
        image:
          url: /images/cxcz-4408d4ba.png
          altText: Company logo
          styles:
            self:
              margin:
                - ml-3
          type: ImageBlock
        colors: bg-light-fg-dark
        styles:
          self:
            padding:
              - pt-6
              - pl-6
              - pb-6
              - pr-6
            textAlign: left
            borderColor: border-neutralAlt
            borderStyle: none
            borderWidth: 0
            borderRadius: none
            flexDirection: row
        type: FeaturedItem
    variant: small-list
    colors: bg-light-fg-dark
    styles:
      self:
        margin:
          - mb-20
        padding:
          - pt-0
          - pl-0
          - pb-0
          - pr-0
        justifyContent: center
      subtitle:
        textAlign: center
    type: FeaturedItemsSection
isFeatured: true
colors: bg-light-fg-dark
styles:
  self:
    padding:
      - pt-5
      - pl-5
      - pb-5
      - pr-5
    textAlign: center
    borderColor: border-light
    borderStyle: none
    borderWidth: 0
    borderRadius: none
    flexDirection: col
type: PostLayout
---
> **INTRODUCTION:**

In today’s world, data plays a crucial role in every industry. Be it medical, finance, or education, the insights drawn from data help businesses make informed decisions. But what if the data is too dirty to make any sense of it? As a data analyst, I have come across many datasets that were challenging to work with. However, the dataset I worked on for a medical company’s HR department was the dirtiest I had ever seen.

The datasets consisted of attendance records of employees, which were filled with incomplete information, ghost employees, missing time-outs, and too many time-ins. It also included various predetermined schedules within the same day, a row with too many schedules and too many employees combined in one, incomplete filing of leave requests, and payroll. The data was a mess, and I knew it would take a lot of effort to clean it up.

But a cleaned data is futile if it isn’t used for specific goal. So, before the cleaning process, let us know the main goal of this analysis.

> **PROBLEM STATEMENT:**

The main task is to analyze the attendance data of the employees to identify patterns of employee tardiness, absenteeism, and indiscipline. The analysis will be used to address any issues and improve employee attendance and punctuality in the company.

The specific goals of the analysis are as follows:

· Identify the most disciplined and undisciplined employees and divisions:

· Create a visualization with the analysis of weekdays and months when the most employees were late/absent.

· Determine which heads of departments tend to forgive employees for lack of discipline. Identify if any favorites for any heads of departments exist.

> **METHODOLOGY:**

**DATA CLEANING**

Like every data cleaning process, we started by importing our datasets to our preferred tools. We utilized the mostly used tools in cleaning: PostgreSQL and Power BI Query. This is to validate or counter check the outputs of each process. So, let us now discuss how we clean and prepare each dataset; this includes the process of filtering out some irrelevant values and deleting some duplicates.

![](https://miro.medium.com/v2/resize:fit:700/1*EE7tQsPZIfKgHhq7mlocaw.png)![](https://miro.medium.com/v2/resize:fit:700/1*LMi9DLcOWedQU7aAJMmi8w.png)![](https://miro.medium.com/v2/resize:fit:700/1*mASeaxoqQ8M29qCAbYSCvg.png)

***This is just a one of the dataset that has been cleaned. There are 5 more to clean. So, to check the complete process of data cleaning, please click the link below:***

<https://drive.google.com/file/d/15pTtAKG6yUXXV1HjDVYLjrbGlH7C3e6g/view?usp=share_link>

After we have cleaned the 5 datasets, there still one process that is vital for our data analysis. We need to merge the Schedule and Attendance tables. We used the schedule as the main table, pulling out the matches from attendance table, leaving some rows with no records in the attendance part. This can be done using LEFT OUTER JOIN. We did this using both PostgreSQL and Power BI Query.

**DATA MODELLING**

We believe that using a merged Schedule and Attendance table as the fact table, along with only one dimension table for Users, can be an effective approach for our analysis.

![](https://miro.medium.com/v2/resize:fit:700/1*XwdZIhY_S_w-Gj2vk0zKww.png)

By consolidating the Schedule and Attendance tables into one fact table, we can simplify the schema and reduce the number of tables we need to manage. This can lead to easier maintenance and improved query performance. Additionally, having only one dimension table for Users can also simplify the schema and make it easier to manage. Having only one dimension table for Users can also help ensure data consistency and accuracy, as there is only one source for user profile information. This can help prevent issues that may arise from having multiple sources of conflicting or inconsistent data.

> **DAX ANALYSIS:**

Now that the data has been thoroughly cleaned and prepared, we can proceed to the DAX analysis. But let me first go through some key terms that will be used throughout the entire analysis. You must be familiar with these terms in order to comprehend the approach. Some terms may not be widely used because they were created specifically for this study.

**Key Terms:**

**a.** **Absenteeism Rate **— refers to the percentage** **when the employees don’t show up to work when they are scheduled to.

b. **Tardiness Rate **— refers to the percentage of “time in” where the employee is late. Late is when the employee check in 10 minutes after his/her official time.

c. **Undertime Rate** — refers to the percentage of “time out” where the employee left earlier than his/her official time out.

**d.** **Failure-to-Log Out Rate — **refers** **to the percentage of occurrences where the employee forget to “time out”.

In our analysis, we consider employees with different types of schedule like “free”, “leave” or “work”. **FREE **means schedule that doesn’t have a strict time in or time out. **LEAVE **means employee can report to work but without strict time since he/she is supposedly on leave. **WORK **means a strict schedule the employee should follow.

We need some measures for us to be able to determine whether the employee is late or undertime and it is based on the differences of the actual time in or time out with respect to the scheduled time.

To get the difference of schedule time and actual time in minutes, we used the formula below:

![](https://miro.medium.com/v2/resize:fit:700/1*8CeVN7vj464hi8xW9SgYhg.png)

But the above formula has limitations, since it will not consider the different types of schedule. That is why we create new column named “Strict Time” to filter only those whose schedule is “Work” and filter out tardiness and undertime when it is more than 2 hours or 120 minutes.

![](https://miro.medium.com/v2/resize:fit:700/1*YSdqEUIiIsEYcA3o1q3P4A.png)

Now, to identify who is late and who left early, we add two columns to count for tardiness and undertime.

![](https://miro.medium.com/v2/resize:fit:570/1*N9-zwbKOEb64JfX1pvuBRA.png)

We need the total shifts/events that the tardiness or undertime has likely to happen for us get the percentages. Therefore, we calculate for total time ins and total time outs using these measures:

![](https://miro.medium.com/v2/resize:fit:638/1*7JamcDdxWe989TYv7uK7Xg.png)

Now, we can compute for the tardiness and undertime rate using the following expressions, make sure to convert the format to percentage:

**Tardiness Rate:**

![](https://miro.medium.com/v2/resize:fit:700/1*mHWcioyuyzoesEnTpirLtQ.png)

**Undertime Rate:**

![](https://miro.medium.com/v2/resize:fit:700/1*80NT6QUPA_NlrTI9-rVNvA.png)

On the other hand, we can compute for the Failure-to-Log Out Rate by getting the difference between the Log In and Log Out and dividing it by total Log Ins.

**Failure-to-Log Out Rate :**

![](https://miro.medium.com/v2/resize:fit:700/1*BnfOEoMvYMRS5_9_TzciOQ.png)

Lastly, to identify who is absent, we add a calculated column using DAX. We applied certain conditions to determine the absent.

1\. First, the schedule type must be **“Work”**. Leave and free schedules just like having no strict time in and time out, reporting to duty is not required.

2\. Second, the attendance date must be **“Null” **signifying that if there is no record in the attendance but have one in schedule, the employee is absent.

3\. Lastly and most important, the calculation for each employee will just start in the oldest date recorded in their attendance and will stop until the most recent date. The **“MINX”** filter signifies that the oldest date will be the employee’s first day and **“MAXX” **filter signifies that the most recent date will be the employees’ last day. We did this to remove all of the predetermined dates that is not covered during the days an employee actually works in the company.

![](https://miro.medium.com/v2/resize:fit:700/1*2ez5URDUGJb0Jv5V7Rs_XA.png)

Now to compute for the Absenteeism rate, we need to know the total shifts the employee should actually work. This can be done by adding the total shift (from the total Time Ins) and the total record of absences.

![](https://miro.medium.com/v2/resize:fit:670/1*deOkviUPeMHMKWeGfq-oGg.png)

To compute the Absenteeism rate, divide the sum of the absences by the the total shifts. Always make sure to change the format to percentage.

**Absenteeism Rate:**

![](https://miro.medium.com/v2/resize:fit:700/1*tVa3sVNQrs0js1sAdS29ng.png)

***We are not yet done. If you want the complete process of DAX analysis, you can view it here:***

******<https://drive.google.com/file/d/1JPoVrc15dOmtAv7iKnV1-dEU8UA6qa1d/view?usp=share_link>

**DATA VISUALIZATION**

We can now proceed on to our data visualization after preparing and modeling the dataset and generating all necessary measurements for our analysis using DAX. Our dashboard construction is driven by our data analysis objectives. We developed a dashboard for each of the three tasks the CEO formulated in order to respond to them.

***Click here to view the full discussion of data visualization. It comprehensively discuss each charts and its uses for the analysis.***

<https://drive.google.com/file/d/1vBICyXADUL-3PK4gUKz1wqUU_dACgSGT/view?usp=share_link>

Now we can proceed to our findings:

> **FINDINGS AND INSIGHTS**

Based on the gathered data and developed dashboards, here are the findings and insights generated to answer the three main tasks:

***Task 1: Identify the most disciplined and undisciplined employees and division.***

![](https://miro.medium.com/v2/resize:fit:639/1*icBUI9BPZYGxJwyJpEUX8A.png)****

**“The most undisciplined employee and position are members of the most undisciplined department.”**

**FINDINGS:**

*   **PBF **is the most undisciplined department with the highest absenteeism, tardiness and undertime rate among other departments: **31%**, **30%** and **9%** respectively. On the other hand, **Pharmacy** is the most disciplined department having the lowest rates.

*   **Warehouse staffs **are the most undisciplined of all the positions having 31% absenteeism rate, 15% tardiness rate, 6% undertime rate and 2% failure-to-log out rate. They are all members of PBF Department.

*   The table chart shows that there are various individuals at the top of each metric, but **Employee 128325** has the biggest impact on the performance of her department and the entire company, with rates of 34% absenteeism, 92% tardiness, 28% undertime, and 26% failure-to-log-out. Surprisingly, she works for the PBF Department. **Employee 129675**, **84509, 84699, **on the other side, are the most disciplined having no records in any of the metrics.

**Additional Findings:**

· **Male employees** are more undisciplined compare to female employees with rates of 21% absenteeism and 7% tardiness.

· **Mobile source** causes 76% of overall employees’ tardiness.

***Task 2: Create a visualization with the analysis of weekdays and months when the most employees were late/absent (either for vacation or sick leave).***

![](https://miro.medium.com/v2/resize:fit:678/1*KnmjSugS59EMZ4PsqtuFZg.png)******

***“Saturday is the day, September is the month when the most employees were absent.”***

**FINDINGS:**

· **Saturday** has the highest number of absences with a total of 224 and 53 tardiness. **Thursday** has the highest total of tardiness with 87 and 202 absences, followed by Friday with 78 and 201 absences. The day with the least number of absences is **Sunday **with a total of 164 and 39 tardiness.

· The month with the highest number of absences is **September 2022 **with 252 counts while **July 2022** is the month with the highest tardiness with 58 counts.

· The average number of employees with absences is **10 per week** and **20 per month**; **14%** and **27%** of the total employees respectively.

**Additional Findings.**

· Overall, **82% (60/73)** of the total employees has a record of absences.

· Most of the employees were late at **8:00am** shift while most of the recorded early outs were at **3:00pm**. It was find out that there were also high recorded late time ins during **2nd shift at 3:00pm**.

***Task 3: Which heads of departments tend to forgive employees for lack of discipline? Are there any favorites for any heads of departments (perhaps some employees are always forgiven for being late, given time off, etc.)?***

![](https://miro.medium.com/v2/resize:fit:670/1*_U85S5EIb2bGoL4LHX1TxA.png)******

***“Medical Department approved highest number of leave requests, with second highest absenteeism rate yet their average gross pay remains unaffected.”***

**FINDINGS:**

· **Medical Department **has the highest average gross pay and the least deduction,** **whereas **PBF** has the largest salary deduction due to having the highest absenteeism rate.

· **Employee 74049** and** 74044, **both from **Medical Department**, has **18** approved leave requests with 9% absenteeism rate and **2** approved leave request with 26% absenteeism rate respectively, yet their gross pay remains unaffected.

· **Head **of the **Medical Department** approved 28 leave requests, highest among all departments. **Employee 74049 (Medical) and 88357 (PBF) **have the most granted leave requests (each has **18**), with 1 pending and 6 rejected request, respectively. **Employee 74049** has been granted 15 sick leave and 3 compensatory leave requests.

**Additional Findings:**

· **90 leave requests** have been filed, 33 of them are compensatory while 26 are sick leave requests. This is relatively smaller compared to the number of “leave-type” schedules.

> **RECOMMENDATIONS**

Based on our findings, the group has made recommendations to the client in order to reduce the number of instances of undisciplined behavior committed by its employees, thereby lowering the absenteeism, tardiness, undertime and failure-to-log out rate.

***From Task 1:***

· Provide training or support for the most undisciplined department (PBF) and its employee to improve their attendance and punctuality. This includes coaching and counseling that will reevaluate their staffing and schedules to prevent future disruptions to the team’s workflow and productivity.

· Set specific limits for absenteeism and tardiness rate to identify when a certain area indicates a high level and when action is required to address that problem. Update each department on their performance on a regular basis, and alert those who are performing beyond the limit.

· Establish a centralized system or technology to automate the attendance and tardiness tracking process. Try Biometric machines instead of mobile or front end. This can improve accuracy and efficiency while also lowering the risk of errors.

***From Task 2:***

· Plan a month or week ahead to anticipate potential staffing shortages and proactively address them, such as by arranging for substitute workers or adjusting the schedule to better accommodate employee needs. Identify the reason behind high numbers of absenteeism on Saturdays and on September 2022.

· Incentivize employees who maintain good attendance and punctuality records. Offer paid time-off or bonuses to employees who consistently show up on time and who has perfect attendance in a quarter or in month.

***From Task 3:***

· Train managers and supervisors to recognize the importance of consistent and fair enforcement of attendance and punctuality policies. This can help to prevent resentment and mistrust among employees who may feel unfairly targeted or treated.

*“In conclusion, cleaning up the dirtiest data I had ever seen was a challenging task. But with deep knowledge of Power BI and SQL, I was able to clean up the data and make it usable. By creating visualizations, I was able to provide insights that helped the HR department make informed decisions. As a data analyst, I take pride in cleaning up dirty data and making it useful for businesses.”*

Here are the dashboards:

Dashboard 1:

![](https://miro.medium.com/v2/resize:fit:700/1*IDs5bZYaEDBIQKjki6YKAw.png)

Dashboard 2

![](https://miro.medium.com/v2/resize:fit:700/1*pTYMMsIBDvri3VT_yG6e5A.png)

Dashboard 3



![](https://miro.medium.com/v2/resize:fit:700/1*o7GO4To4xy5Gysky2FNhpg.png)

*Check out the interactive dashboard here:*

<https://www.novypro.com/project/undisciplinedemployee>







