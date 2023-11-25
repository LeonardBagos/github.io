---
type: PostLayout
slug: project5
date: '2023-11-20'
excerpt: >-
  Sit ratione eligendi et quis distinctio et maiores accusantium aut accusamus
  facere sit repellat quidem qui alias nostrum et earum enim. Cum quis sint eos
  dolor quas ad odit ipsum qui quia eius.
featuredImage:
  url: /images/ff.png
  altText: Thumbnail
  type: ImageBlock
  styles:
    self:
      borderRadius: medium
content: |+


bottomSections: []
isFeatured: true
isDraft: false
seo:
  metaTitle: How to Write a Blog Post That Will Get You More Traffic
  metaDescription: You can add the excerpt and main keywords of your blog post here.
  socialImage: /images/abstract-feature2.svg
  type: Seo
colors: bg-light-fg-dark
styles:
  self:
    flexDirection: col
    textAlign: center
title: Analyzing the Impacts of Daily Commuting in NCR using Python Machine Learning
---
*Predicting the impacts of daily commuting and gauging commuter satisfaction though  Data Science, encompassing statistical
analysis with Excel, feature engineering via SQL, and machine learning implemented with Python*

![](https://miro.medium.com/v2/resize:fit:700/1*UoDuXrOeO8SzLUtTHfqWLg.png)

Interact with the dashboard here: <https://www.novypro.com/project/pwccallcentertrend>

The digital revolution and our fast-changing world requires a skills revolution. And it’s not just about the digital skills. The skills revolution is about helping people build their digital awareness, emotional intelligence and creativity to fully participate in the digital future workplace — and it needs to start now.

> **Task:**

It’s omnipresent: telecom marketing. Better price here. Better service there. Best for small businesses here. Best for young urbanites there. But what do customers really want? Our client, a big telecom company needs to know. This email just arrived for you:

![](https://miro.medium.com/v2/resize:fit:700/0*pic605yUKgnchwkF.png)

Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset. Get creative!

**Possible KPIs include (to get you started, but not limited to):**

*   Overall customer satisfaction

*   Overall calls answered/abandoned

*   Calls by time

*   Average speed of answer

*   Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

> **Process:**

First, import the data to Power BI. Before we load the data, we need to make sure that the data is clean. Click Transform Data.

I noticed that there are a lot of null values for the \*speed of answer in the second’s \*column, so I filtered to only show the null values and observed the data. As I can see in the filtered data, all calls were not answered therefore having null values for the average talk duration is valid. I didn’t change the null values to 0 because if the agent failed to answer the call, then there shouldn’t be any values for average talk duration and satisfaction rating. Making it zero will affect their KPI.

![](https://miro.medium.com/v2/resize:fit:700/0*Q9hyBtDRs-xaHZ79.png)

I noticed the *AvgTalkDuration* column is in Date/Time format which should be in duration. Change the data type to Time only, and then I added a new custom column and then subtracted the *AvgTalkDuration* column by 00:00:00.

![](https://miro.medium.com/v2/resize:fit:700/0*WQjfUrpGqCTg7aRV.png)

I renamed the new column to *Average Talk Duration* and changed the data type to duration and then show only seconds. The time column has date values in it, so I changed the data type to Time only.

> Analysis:

I have created measures to answer the questions and provide different KPI or metrics. To summarize all the stats of the agents, I decided to insert a table that will show their total calls, answered calls, queue time, call time, % Answered Calls and overall satisfaction rating.

![](https://miro.medium.com/v2/resize:fit:700/1*yuc8GlGq7ONwcKEJom5Gmg.png)

Then, I created a column and bar chart that shows the total calls, answered calls and resolved calls. It shows that every Monday and Saturday, agents have higher resolved calls than the rest of the day of the week.

![](https://miro.medium.com/v2/resize:fit:700/1*BKiLlEUpyjLvPJoO7nG6Dw.png)

The last visualization is a doughnut chart showing all the call topics.

![](https://miro.medium.com/v2/resize:fit:265/1*tEGeT1UEzx5UkLFjb8Yzfw.png)

Finally, I designed the dashboard and created the background using PowerPoint. Here is the final result:

![](https://miro.medium.com/v2/resize:fit:700/1*UoDuXrOeO8SzLUtTHfqWLg.png)

> Insights:

Based on the analysis, it appears that this call center has a relatively high rate of abandoned calls and a low overall satisfaction rating. This suggests that there may be issues with the call center’s ability to handle the volume of calls it receives, as well as potential problems with the quality of service provided to customers. Improving the call center’s answer rate and average response time, as well as increasing customer satisfaction, may be necessary to ensure the success of the business.

> Recommendations:

1.  Identify and address the root cause of the high rate of abandoned calls. This could be due to a variety of factors, such as long wait times, complicated issues, or a lack of available agents. Once the underlying issue has been identified, steps can be taken to improve the call center’s performance.

2.  Increase the number of available agents to handle the volume of calls. This could involve hiring additional agents, implementing a system for routing calls to multiple call centers, or utilizing technology such as virtual agents or chatbots to assist with customer inquiries.

3.  Improve the call center’s average response time. This could be achieved through training and coaching for agents, implementing more efficient processes and technologies, or increasing the number of available agents to reduce wait times for customers.

4.  Focus on increasing customer satisfaction. This could involve regularly surveying customers to gather feedback and identify areas for improvement, implementing customer service best practices, and providing ongoing training and support for call center agents.

5.  Consider implementing a call-back system for abandoned calls. This could allow customers who are unable to wait on hold to leave their contact information and request a call back at a more convenient time. This could help to reduce the number of abandoned calls and improve the overall customer experience.

