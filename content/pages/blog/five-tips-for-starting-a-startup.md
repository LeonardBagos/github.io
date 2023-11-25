---
title: "Analyzing of the Operating performance for\_ Ecommerce Company"
slug: project4
date: '2023-02-20'
excerpt: >-
  Sit ratione eligendi et quis distinctio et maiores accusantium aut accusamus
  facere sit repellat quidem qui alias nostrum et earum enim. Cum quis sint eos
  dolor quas ad odit ipsum qui quia eius.
featuredImage:
  url: /images/eCommerce-Cartoon.png
  altText: Thumbnail
  type: ImageBlock
  styles:
    self:
      borderRadius: medium
bottomSections: []
isFeatured: true
isDraft: false
seo:
  metaTitle: 5 Tips for Starting a Startup
  metaDescription: You can add the excerpt and main keywords of your blog post here.
  socialImage: /images/abstract-feature1.svg
  type: Seo
colors: bg-light-fg-dark
styles:
  self:
    flexDirection: col
    textAlign: center
type: PostLayout
---
![](/images/Screenshot%202023-03-09%20202510.png)

Interact with the dashboard here: <https://www.novypro.com/project/olistperformance>

**Introduction**

Olist, an e-commerce company from Brazil, has requested a complete analysis of their operating performance. They want a detailed report covering three main parts: general dashboard, delivery performance, and product quality.

**About the Dataset**

The dataset has information on 100,000 orders from 2016 to 2018 made at multiple marketplaces in Brazil. The orders include details such as order status, price, payment, freight performance to customer location, product attribute, and reviews written by customers. The geolocation data is associated to Brazilian zip codes with latitude and longitude coordinates.

This is real commercial data, it has been anonymized, and references to the companies and partners in the review text have been replaced.

**Data Analysis Goals**

1.  Explore the company’s product volume, sales, and customer satisfaction rating for products.

2.  Analyze delivery performance.

3.  Investigate product ratings and discover product categories that are prone to customer dissatisfaction.

**Data Preparation**

The dataset includes 9 csv files imported to Power BI, it includes customer and sellers’ information, geolocation, items, purchases and reviews.

The dataset is loaded and transformed in Power Query Editor. Most of the dataset needed their headers to be promoted as Power Query wasn’t able to recognize those immediately. Most data also needed their data types to be changed. I went ahead and replaced jargons with proper terms for easy understanding especially the “product_category_name_translation” query. In sellers and customers tables, abbreviated name of each states with their full state names. I also computed some measures like number of bad reviews using DAX analysis.

![](https://miro.medium.com/v2/resize:fit:683/1*I_HGrBnxVptNrs0idU-D7g.png)![](https://miro.medium.com/v2/resize:fit:687/1*BhhWq0-mUhrJ70JYNsvthg.png)

I also added calculated columns to show the average time/days in processing the orders, dispatching the orders and delivering it to the customers.

**Data Modelling**

For data modelling, I used the *star schema* having the “order_items” as the fact table since it stored most of the values that is related to the other tables such as product id, customer id, oder id and sellers id.

![](https://miro.medium.com/v2/resize:fit:544/1*RnAa2dIEytrrp4VcdhACgA.png)

I did not establish a connection for “geolocation” because it will be having a many-to-many cardinality that will complicate the relationships. Instead, I used merge queries to add important columns like latitude and longitude from geolocation to seller and customer tables.

**Data Visualization**

After preparing and modelling our data, we can now create our dashboard to achieve our data analysis goals. Kindly watch this short walkthrough in our Power Bi Dashboard.

<https://youtu.be/1B99ZkSaU9k>

> **SALES AND PRODUCTION VOLUME DASHBOARD**

I created the first page of the dashboard showcasing information about the company’s total sales, total products sold, and average product rating using visualization cards.

![](https://miro.medium.com/v2/resize:fit:700/1*TU78fOq0Pt5n-xeax5vEdQ.png)

Through this dashboard, we can view the total sales, the number of orders, the sales performance over the course of the months, the sum of the sales on a geographical map by states, and finally the top 10 most popular product categories across various years.

The business team using such a dashboard can quickly identify and evaluate any *anomaly in the sales performance*, such as a sudden drop and surge in order due to seasonality, for example. In addition, they can use the *geolocation map to decide to expand into cities of interest or to concentrate on a particular product category in each different city due to the fact that a particular product category has the highest sales at this particular city*.

> **DELIVERY PERFORMANCE DASHBOARD**

Secondly, we need to create a dashboard for the analysis of our delivery performance for it is one of the main factors for sales growth and customer satisfaction.

![](https://miro.medium.com/v2/resize:fit:700/1*VZRWju8xMcxNF-A57m932w.png)

One of the most important KPI is the estimated delivery time that we promise our clients that we will deliver accordingly, due to the fact that giving a wrong estimated delivery time can result in canceled orders, bad reviews, and unfortunately, customers leaving our service. Hence it is really important to keep a dashboard to monitor such metrics.

We can see that in the first operational year (2016) in September we were maybe promising the wrong estimated delivery time, which translated as we see in a larger percentage of canceled deliveries, but on a positive note, we can see that in the following year (2017) we overcame this issue since we are providing an estimated time for our clients but we are delivering the orders much earlier on average, which again translated into way less canceled orders. *That is just one example on how to utilize this dashboard. You can surely made other insight out of it.*

> **CUSTOMER SATISFACTION DASHBOARD**

To improve our performance, we must value our customer by analyzing their feedbacks and satisfaction rating.

![](https://miro.medium.com/v2/resize:fit:700/1*lnT3x1shqMfKkEOA4kP4Kg.png)

Customer satisfaction review is very vital to improve a company’s performance. *You can check whether we get higher number of good reviews compared to bad reviews. You can also concentrate on products with good rating because it may contribute to higher sales. Lastly, you must consider checking products that are prone to customer dissatisfaction to improve it’s product quality.*

**Insights**

The analysis’ findings indicate that Olist E-commerce gained a total of 99,440 orders. The business has a 90% delivery success rate after delivering roughly 89,940 items. Their product ratings range from 2.5 stars to 4.67 stars, with the average rating being 4.09 stars. In the order of review score distribution, 1 Star reviews are third, which suggests that there may be issues with product quality in specific product categories. Delivery efficiency could impact review ratings, and success rate could definitely be increased.

**Recommendations**

1.  Investigate delivery delays and undelivered orders. Analyzing geographic locations could bring insights about certain challenges with demographics, accessibility, and possible route optimization. Tracking fleet performance with the use of telematics can help identify issues before they become a problem.

2.  Providing a proper shipment tracking system aids in having clear and concise communication between customers, sellers and couriers. Regular updates can set proper expectations among customers and specific delivery instructions of customers can be properly accommodated. By establishing trust and communication, both parties can work together to resolve any issues that may arise.

3.  Regularly monitor and analyze customer reviews to gain insights in product quality and identify areas for improvement. Dashboards can be used to identify patterns in customer reviews. This will provide a data-driven approach to enhance customer experience.



