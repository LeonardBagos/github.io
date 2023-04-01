---
title: How Data Analysis Helped Me Reduce Rejection Rates in My Previous Company
slug: project1
date: '2023-01-15'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  url: /images/Capture.PNG
  altText: Case study 1
  styles:
    self:
      borderRadius: large
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
          url: /images/cxcz.png
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
**Disclaimer**: Certain information has been withheld or redacted due to privacy concerns and confidentiality. Using of codes for products and rejects are necessary since disclosure of such sensitive information is restricted by the law or the company’s policy.

***“Data analytics can reveal trends and patterns that may otherwise go unnoticed amongst the mass of information organizations hold.”***

![](https://miro.medium.com/v2/resize:fit:700/1*Ds_YhKKtdCeGFooL8Sazjg.png)

Around May of last year in my previous company, I encountered an unusual problem regarding high rejection of our products. As a quality analyst, I not only ensure that the products we produce meet the set standards, but I also assist production in minimizing defect rejection while increasing productivity. My role as an analyst is not limited to quality assurance; I also assist in process optimization by taking significant actions in response to a problem that may arise during production. Because of this, the issue of high rejection of our products did not escape my critical eye.

![](https://miro.medium.com/v2/resize:fit:700/1*mOVIkF0x_MalkW2Mn1IcMw.png)

Going back to the situation, we faced a high rejection of a certain product “TB” due to some defects and non-conformances. By that time, I am aware that it is unusual but I can’t provide numbers or data for my supervisor on how it was different from our past runs. This lack of information has made it difficult for my supervisor to understand the severity of the problem.

![](https://miro.medium.com/v2/resize:fit:700/1*5AOeqp1aFTZCZZIZuLlaKg.png)

**That is when my data-savvy attitude resurfaced and my journey into data analytics began.**

![](https://miro.medium.com/v2/resize:fit:700/1*eHvIStDKZRE-rT6ss_8bLw.png)

My data analysis, like any other problem-solving method, began with gathering information about our current situation and collecting data from previous runs. I collect necessary data like total bottles inspected per month and the total bottles rejected during inspection. They were classified according to the type of reject and the production line from which they were produced. I included all the regular products for comparison of the rejection rates because I wanted to create a document that would be helpful for future analysis of all products.

![](https://miro.medium.com/v2/resize:fit:461/1*Rt81pmm4EO83VobmdGrdvQ.png)

Following data collection, I used an Excel formula to compute the percent reject and total rejects per types and product line. Now, I created a visualization showing the trends in overall percentage reject from January to May using pivot tables generated from the raw data. I discovered a rising trend for it, which peaked in May, the current scenario at the time. The percentage rejection increased from **3.24%** the previous month to **4.12%** overall. We can say that there is a significant difference and that something unusual occurred.

![](https://miro.medium.com/v2/resize:fit:539/1*hTUG0X24Tfknyv_FL3zvXQ.png)

However, the overall percentage rejection rate does not reveal which product or factor is driving the upward trend. That’s why I made a chart that compares the performance of each product over time. As can be seen, product “TB” also peaks in May at **16%**. It has also the highest rejection rates among all the products.

![](https://miro.medium.com/v2/resize:fit:456/1*FDvJTJhaPmwejnrTT4a2dQ.png)

Thus, I focus on product “TB” and identify what type of rejects and which specific rejects are contributing to the sudden increase. We discover that **“Label”** rejects, specifically** “T” and “WR”** rejects contributed greatly compared to other kind of rejects. **95%** of the rejects were mainly due to label rejects. So, we closely monitor these rejects and make corrective actions to reduce it. We also made root cause analysis for this issue: Are there new labels introduced in the production? What is the quality of glue we are using, maybe it was expired? or Was there new machine parts that have been used? Those were just examples of how we troubleshoot the problem at that time. We also compared it to product **“EBL”** since they were both produced from the same line.

![](https://miro.medium.com/v2/resize:fit:542/1*PoUklnKNEip_zEaIuo5pxQ.png)

We noticed that unlike “TB”, product **“EBL”** remarkably decrease its percent rejection during the month of May. That is why we focused only on product “TB” and conducted study on its variants. The graph below shows the** 5 variants of TB **and their percent rejection of the top 2 rejects. Comparing them let us determine which TB variant has a notably higher rate of rejection than the others.

![](https://miro.medium.com/v2/resize:fit:360/1*RlT1l69wo2sPX8OwQa_lHg.png)

I conducted study into how these TB variants differ from one another, such as the characteristics of their packaging raw mats and machine handling parts, among other things. However, that is outside the scope of this blog. I simply use my findings from that study to achieve my main goal: to reduce rejects in the months following the May incident.

![](https://miro.medium.com/v2/resize:fit:700/1*IjeJ1-v_-6ENa4i_PBpnNQ.png)

To make the story short, like how I anticipated the patterns would be, there was a notable decrease after closely monitoring TB product and its variants following the May incident. Even during the peak season in the production from October to December, the analysis is useful and made a great contribution in the reduction of rejects.

![](https://miro.medium.com/v2/resize:fit:486/1*uqEHuf25p_lpZb6642Xgew.png)

After using my analysis and determining which product should be closely monitor, the overall rejection rate fell from **3.50% to 2.94% **from the first half versus the second half of the year. This equates to a **16%** reduction in rejects. Meanwhile, product TB has a year-to-date average rejection rate of only **8.16% **from **15.56%** in May. From **10.89%** for the first half to **5.43%** on the second half. This was equivalent to **50%** reduction of rejects for TB products.

![](https://miro.medium.com/v2/resize:fit:562/1*Wsamm8_jwE9OeVyt0vuyPA.png)

Overall, there was a significant decrease on the overall rejection of our products at the end of the year. By using Excel to create a dashboard and analyze trends, I was able to reduce rejection rates and improve the overall quality of our products.

![](https://miro.medium.com/v2/resize:fit:700/1*ejUptykMThd4fbDi2jdnXA.png)

Data analysis proved to be an invaluable tool in my role as a quality analyst. With data analysis, I was able to identify patterns that caused higher rejection rates. By narrowing down the issue to one product, I was able to create targeted solutions to reduce the overall rejection rate. By creating a dashboard in Excel, I was able to spot trends quickly and adjust production accordingly. This allowed me to proactively address issues before they could cause major problems. By tracking the rejection rates over time, I was able to measure the effectiveness of my solutions. This allowed me to see the progress we were making in reducing rejection rates and adjust strategies accordingly.

**RECOMMENDATIONS:**

Although we made significant decrease in the rejection of “TB” products, we should also track the status of other products. For example, unlike TB and EBL from Line 1, other lines seem to have an increase in the percent rejection. To compare, ***Line 1 has a decrease of 40%, while line 2 and line 3 has an increase of 26% and 49% respectively.***

![](https://miro.medium.com/v2/resize:fit:475/1*WoBB7IagFAcjP80f9Mxbkg.png)

Just like what we did for Line 1, we should identify which products are contributing to the increase of rejection for line 2 and 3.

![](https://miro.medium.com/v2/resize:fit:541/1*pqJoYuLvXcLx81tSl-oapg.png)

Even though **CMLJ **(red line) shows a significant decrease, we can see that product **SN and SM** increase in percent rejection.

Ensure that all of the products follows the trend of TB. Monitor the percent rejection of all the products in the future. If there is an unusual increase of rejection for a certain line, narrow it down to a specific product and identify the causes of it. This will allow us to proactively address issues before they could cause major problems.

Here is the walkthrough in our dashboard:

<https://youtu.be/fQZRdidd12E>









