---
type: PostLayout
title: Calculating Business Metrics For Delivery Company Using Dax Measures
slug: project6
date: '2023-03-14'
excerpt: >-
  Sit ratione eligendi et quis distinctio et maiores accusantium aut accusamus
  facere sit repellat quidem qui alias nostrum et earum enim. Cum quis sint eos
  dolor quas ad odit ipsum qui quia eius.
featuredImage:
  url: /images/Fastest-courier-services-in-India-044df328.png
  altText: Thumbnail
  type: ImageBlock
  styles:
    self:
      borderRadius: medium
content: >-
  Etiam facilisis lacus nec pretium lobortis. Praesent dapibus justo non
  efficitur efficitur. Nullam viverra justo arcu, eget egestas tortor pretium
  id. Sed imperdiet mattis eleifend. Vivamus suscipit et neque imperdiet
  venenatis.


  > Vestibulum ullamcorper risus auctor eleifend consequat.


  ![Placeholder
  Image](https://assets.stackbit.com/components/images/default/post-4.jpeg)


  In malesuada sed urna eget vehicula. Donec fermentum tortor sit amet nisl
  elementum fringilla. Pellentesque dapibus suscipit faucibus. Nullam malesuada
  sed urna quis rutrum. Donec facilisis lorem id maximus mattis. Vestibulum quis
  elit magna. Vestibulum accumsan blandit consequat. Phasellus quis posuere
  quam.


  Vivamus mollis in tellus ac ullamcorper. Vestibulum sit amet bibendum ipsum,
  vitae rutrum ex. Nullam cursus, urna et dapibus aliquam, urna leo euismod
  metus, eu luctus justo mi eget mauris. Proin felis leo, volutpat et purus in,
  lacinia luctus eros. Pellentesque lobortis massa scelerisque lorem
  ullamcorper, sit amet elementum nulla scelerisque. In volutpat efficitur
  nulla, aliquam ornare lectus ultricies ac. Mauris sagittis ornare dictum.
  Nulla vel felis ut purus fermentum pretium. Sed id lectus ac diam aliquet
  venenatis. Etiam ac auctor enim. Nunc velit mauris, viverra vel orci ut,
  egestas rhoncus diam. Morbi scelerisque nibh tellus, vel varius urna malesuada
  sed. Etiam ultricies sem consequat, posuere urna non, maximus ex. Mauris
  gravida diam sed augue condimentum pulvinar vel ac dui. Integer vel convallis
  justo.
bottomSections: []
isFeatured: true
isDraft: false
seo:
  metaTitle: Track the right analytics for your business
  metaDescription: You can add the excerpt and main keywords of your blog post here.
  socialImage: /images/abstract-feature3.svg
  type: Seo
colors: bg-light-fg-dark
styles:
  self:
    flexDirection: col
    textAlign: center
---
Calculating some business metrics such as average delivery time using dax measures in Power BI

![](https://cdn-images-1.medium.com/max/800/1*0bxCT9pZI8G8mRLHn7Ca4A.png)

Interact with the dashboard here:<https://www.novypro.com/project/indianfooddelivery>

**Task Description:**

You work as a data analyst in an Indian delivery company. Top managers want to expand the business to other countries in Asia, so they asked you to make a report about delivery time to compare the company’s performance with competitors. Data is presented in a .csv file, with fields such as time of delivery, order date, traffic, weather, location, and other information.

**Data Analysis Goals**

Build a dashboard showing how vehicle type, type of order, weather conditions, and road traffic affect the average time taken for delivery.

Calculate the following measures and add them to the dashboard:

a. The median time that is taken for delivery

b. Average time for delivery for sunny and stormy weather

c. Difference between the average delivery time of ordinary scooters and motorcycle

**Data Preparation**

The first column to clean is the *Weatherconditions* column. Just transform the column and then **Extract using Text After Delimiter** option. Next, extract the time in the *Time_taken(min)* column using Text after Delimiter as well. I also changed the *time_taken(min)* column to time data type.

The *Order_Date* and *Time_ordered* columns are in text data type so change them to date and time respectively. After changing the data type of *Time_ordered* column, there are a lot of errors due to null empty values. Select all cells and then right-click, then chose Remove Errors. For *type_of_vehicle* column, replace the values for *electric_scooter* to *electric scooter*.

Lastly, delete columns that are not relevant.

**Analysis**

Create the required measures using DAX analysis.

a. **The median time that is taken for delivery**

![](https://cdn-images-1.medium.com/max/800/1*PkS6PLDIRr4WnxxyZKBe5g.png)

b. **Average time for delivery for sunny and stormy weather**

Average delivery time for Sunny

![](https://cdn-images-1.medium.com/max/800/1*ipSJykgFWae_juCSvHc0SQ.png)

Average delivery time for Stormy![](https://cdn-images-1.medium.com/max/800/1*AgOZ7Wbm4Q4n6aYhmDBp1g.png)

c. **Difference between the average delivery time of ordinary scooters and motorcycle**

Average Delivery Time for Motorcycles

![](https://cdn-images-1.medium.com/max/800/1*Xy1L_y-cqJRh0ZjsXWaLgg.png)

Average Delivery Time for Scooter![](https://cdn-images-1.medium.com/max/800/1*CnejYe7_GDTfo7MIru3s7w.png)

Difference between average delivery time for motor and scooter

![](https://cdn-images-1.medium.com/max/800/1*4zQhCwMG5ax4YSkvJ-dCxw.png)

After calculating the required measure, create your dashboard and add these measures.

![](https://cdn-images-1.medium.com/max/800/1*0bxCT9pZI8G8mRLHn7Ca4A.png)

You can gain direct insights from the dashboard above. Try making your own.

**Recommendations:**

*As a data analyst, what would you suggest to the delivery company so they can collect better data and get more precise results?*

It is important to have well-defined data collection processes in place that specify what data should be collected, how it should be collected, and who is responsible for collecting it. This will ensure consistency in data collection and reduce errors and discrepancies.

Delivery companies should leverage technology to collect data, such as using GPS tracking devices, barcodes, and scanners to track deliveries and shipments. This will help to automate data collection, reduce manual errors, and increase accuracy.

Delivery companies should ensure that data is accurate, complete, and up-to-date. This involves regular data cleansing and validation processes to eliminate errors and inconsistencies. Data visualization tools can help delivery companies interpret complex data and communicate insights more effectively. This can enable decision-makers to make more informed decisions based on data-driven insights.

By implementing these suggestions, delivery companies can improve their data collection processes, obtain more precise results, and make more informed decisions based on data-driven insights.
