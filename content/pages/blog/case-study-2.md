---
title: >-
  An Exploratory Analysis of Client Disputes Using Excel Functions and SQL
  Queries
slug: project2
date: '2023-03-05'
excerpt: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante lorem,
  tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at auctor sapien.
  Etiam at cursus enim. Suspendisse sed augue tortor. Nunc eu magna vitae lorem
  pellentesque fermentum. Sed in facilisis dui.
featuredImage:
  url: /images/logo.png
  altText: Case study 2
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
      - title: About Company
        subtitle: >-
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ante
          lorem, tincidunt ac leo efficitur, feugiat tempor odio. Curabitur at
          auctor sapien.
        image:
          url: /images/cxcz-d69d04ec.png
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
> **PROBLEM OVERVIEW:**

Yellevate, a company that specializes in providing marketing services to mid-sized companies has been dealing with client disputes for several years. Clients who express dissatisfaction with the company’s services and refuse to pay for them are defined as having a dispute, according to Yellevate.

Disputes have resulted in a significant financial burden for the company. The statistics show that nearly** 20% of disputes** raised against Yellevate resulted in payment opt-outs, leading to a **5% annual loss of revenue.** Therefore, a thorough analysis will be of great importance to the company’s top executives, as it will be used to devise a plan to address the root causes of these disputes and minimize their impact on the company’s financial performance.

![](https://preview--super-goose-0a036.stackbit.dev/images/logo-56678d68.png)

> **OBJECTIVES:**

The primary objective of this analysis is to identify the root causes of these disputes and propose actionable strategies to resolve them. It involves thoroughly examining this data to identify patterns and trends that might be contributing to these disputes.

Executives at the company decided that we need to obtain the following information to identify the circumstances around the dispute problem:

· The processing time in which invoices are settled.

· The processing time for the company to settle disputes.

· Percentage of disputes received by the company that were lost.

· Percentage of revenue lost from disputes.

· The country where the company reached the highest losses from lost disputes.

> **METHODOLOGY:**

**Data Collection:**

Data were obtained from the company. The database includes the following features: customer id, country, invoice number, invoice date, due date, invoice amount (in USD), disputed, disputed that were lost, settled date, number of days the invoices were settled, and the number of days the invoices were settled late. A total of 2466 observations were retrieved.

Create a new database and create a new table using CRUD operator and import the dataset in PostgreSQL.

![](https://miro.medium.com/v2/resize:fit:511/1*kcdVBY6fG5xibVc-t8lfeg.png)

**Data Cleaning:**

After the data were collected; they were examined and processed from technical to understandable. When this table is provided to clients, they must understand what the numbers 0 and 1 signifies in ‘‘disputed’’ and ‘‘dispute lost’’ column.

![](https://miro.medium.com/v2/resize:fit:700/1*RfKBTSOL-PmqiEgxnAXGvQ.png)

**Data Analysis:**

The cleaned data were analyzed through a comparative approach using PostgreSQL queries and Excel function and pivot analysis. In order to investigate further the issue, the database was treated with various aggregate functions such as using count, sum, max/min, average, and round functions. Below is the comparison of the analysis using SQL and Excel based on the five main goals:

![](https://miro.medium.com/v2/resize:fit:700/1*p4tC4jT7RM35aaGSg_JM-A.png)![](https://miro.medium.com/v2/resize:fit:700/1*jAoQSyhuAWRgAJjKedMDdw.png)

> **FINDINGS:**

Once the answers were finalized, pivot charts have been made to support the answer on our data analysis goals.

1.  **The processing time in which invoices are settled**

![](https://miro.medium.com/v2/resize:fit:661/1*3O0yRHyx2E3LaAldLQu6oQ.png)

This figure represents an average across the five countries that Yellevate served. **Russia **clearly leads all countries with an average settlement time of 29 days. On the other hand, **China** has the shortest average settlement time of **23 days**. Overall, as indicated by the red dashed line, it takes Yellevate **26 days** on average to settle the invoices. The processing time is settled **4 days** earlier than the due date (30 days). This means that most of the services rendered by Yellevate were successfully delivered and most customers are satisfied with them.

**2. The processing time for the company to settle disputes**

![](https://miro.medium.com/v2/resize:fit:657/1*LYbiwS_cYkIXwdzIfapL0w.png)

Yellevate takes an average of **36 days** to settle disputed invoices. It takes longer to process since both parties are compromised. The client can opt out their payment based on the result of the settlement. If the company wins, they are required to pay even if they are dissatisfied with the service. This means that if the client disagrees with the invoice, it will take the company an average of **6 days longer** than the due date (30 days) to resolve the dispute.

**3. Percentage of disputes received by the company that were lost**

![](https://miro.medium.com/v2/resize:fit:569/1*kr9GDDy4LmoELO0uxckJNg.png)

Yellevate was unable to successfully defend **101 out of 571** disputed invoices, resulting in payment opt-out, representing a loss rate of approximately **17.69%**. This is close to the problem overview’s estimated statistic of 20%.

**4. Percentage of revenue lost from disputes**

![](https://miro.medium.com/v2/resize:fit:625/1*ndmsu2YJQBmg5TWpIgImmQ.png)

Revenue of **$690,167 **was lost out of $14.8 million worth of total invoices. As a result, the revenue lost rate is **4.67%.** This is, once again, close to the estimated 5% annual revenue loss.

**5. The country where the company reached the highest losses from lost disputes (in USD)**

![](https://miro.medium.com/v2/resize:fit:700/1*NF_I1zDqCJxCa1hfqFPYjg.png)

Here, we can see the individual countries’ revenue losses. **France** is highlighted in red, with the highest revenue loss from disputes amounting to **$526,264**. When compared to other countries’ losses, there is a significant difference.

**ADDITIONAL INSIGHTS**

Aside from the primary data analysis goals, additional insights have been generated to assist in the resolution of the disputes. Following an examination of revenue losses by country, the study delves deeper into revenue losses by client. The top ten clients to whom Yellevate lost are listed below.

![](https://miro.medium.com/v2/resize:fit:700/1*45Mfr8RB-t3vvR4cwbhoIw.png)

Yellevate lost a total of **11 disputes** and with highest revenue loss of **$88,124** to customer 9725-EZTEJ.

**ADDITIONAL INSIGHTS**

One of the important measures to determine if the Yellevate is doing well with the invoices is the settlement rate. This comprises data about the count of delayed settlements versus total number of invoices telling if the company has an acceptable invoice settlement rate

![](https://miro.medium.com/v2/resize:fit:642/1*oIBMedyXSCElDxEGRC0o2g.png)

Out of a total of **2,466 invoices**, **877** of them were delayed, resulting in an on-time settlement rate of approximately 64%.

Next is to determine if the company is doing well with the disputed invoices. One of the reasons why invoices were disputed and lost can be the late settlement.

![](https://miro.medium.com/v2/resize:fit:624/1*KYuAxWdKYPXgr-XbYJmEvA.png)

Out of the 507 disputed invoices, **67% of them (385)** were settled late. This is a significant percentage that could lead to the company’s losses.

> **RECOMMENDATIONS:**

Taking into consideration the findings and discussions, below are the probable recommendations and strategies to deal with disputes effectively.

· **Accomplish invoices within 30-day deadline**

Ensure that the 30-day processing time will be strictly implemented. If possible, shortening of the processing time is beneficial. Make a log of invoices that were settled late and list down the reasons for not accomplishing the deadline. Provide ways to prevent missed deadlines on future invoices.

· **Improve Customer Experience**

Give client a notification ahead of time whenever there will be a delay in the processing of their invoices. Invest in training its staff to better understand and handle clients’ needs and concerns, which can help prevent disputes from arising in the first place.

· **Investigate Challenges in each Country**

Determine the reasons behind the highest number of disputes lost in France. Meanwhile, closely monitor and improve its service delivery in other four countries to prevent further disputes. Model China, the country that generates the highest revenue but minimal lost disputes.

· **Identify Trends in Dispute Activity among Clients**

Recognize patterns in filing disputes among clients where the company lost the most invoices. Make a list of all the reasons for their disputes. Closely track their future activities and make sure the root causes listed don’t happen again. Devise a strategy to attract new clients.

· **Review Contract and Terms of Agreement**

Make sure that everything is clear: pricing, discounts, payment terms, agreement on late payments and dispute resolution, among others. Hire a lawyer to check terms of agreement to ensure that there will be no loop hole that can be used by client to evade payment.

Here is the final interactive dashboard I have made on excel.

![](https://preview--super-goose-0a036.stackbit.dev/images/sa-f49abb56.png)

Kindly message me if you want have your own copy of the excel file.

Check here the video recording of our full report:

https://youtu.be/K7h5dKnGj1c





