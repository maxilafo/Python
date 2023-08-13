### Data Validation

Dataset contains 15.000 rows and 8 columns, before cleaning and validation.

- week: No missing values, numeric values between 1 and 6 weeks. No cleaning needed.
- sales_method: Misstyped values were found and fixed (ex: 'em + call' replaced to 'Email + call'), also  all values were capitalized. No data missing.
- customer_id: No duplicated values found. No cleaning needed.
- nb_ sold: No missing values, numeric values between 7 and 16. No cleaning needed. 
- revenue: Contains 1.074 missing values. Due it's not possible to have sold products and 0 revenue, we dropped them. Numeric values.
- years_as_customer: Company was founded on 1984, so no customer can be older than 39 years. 2 values found above 39 years, we dropped them. Numeric values.
- nb_site_visits: numeric values, no missing data. No cleaning needed.
- state: 50 different character values. No cleaning needed.

Ater the validation of the dataset, it contains 13.924 rows and 8 columns without missing values.

### How many customers were there for each approach?
The most used sales method was the email, with almost 7.000 customers, followed by Calls with 4.800 customers, and lastly by Email + Call, with 2.200 customers.
<p align="center">
<a href="https://imgbb.com/"><img src="https://i.ibb.co/zQfdtDm/Image1.png" alt="Image1" border="0"></a>
</p>
### What does the spread of the revenue look like?
The spread of revenue is very varied, but we can identify two big groups of revenue, between the ranges 25-60 and more in usd 70-120 USD, and a smallest one in the range 160-190 usd.
<p align="center">
<a href="https://imgbb.com/"><img src="https://i.ibb.co/4pWtk9v/Image2.png" alt="Image2" border="0"></a>
</p>

These groups are explained by the method used for the sales. These methods almost don't overlap each other, except on the 125 usd zone, but making the revenue groups identifiable in the graph below.
<p align="center">
<a href="https://imgbb.com/"><img src="https://i.ibb.co/b2PSs8c/Image3.png" alt="Image3" border="0"></a>
</p>

We don't have register of the price of each product sold to each customer, but the ratio of revenue over number of new products sold shows below clear groups of possible price ranges of the products.

This suggest that probably the most expensive products were sold by Email + Call method, and by Email only the mild-expensive products. This should be validated with further information about the product prices.
<p align="center">
<a href="https://imgbb.com/"><img src="https://i.ibb.co/nmCYW0R/Image4.png" alt="Image4" border="0"></a>
</p>

### Was there any difference in revenue over time for each of the methods?
<p align="center">
<a href="https://imgbb.com/"><img src="https://i.ibb.co/1fFYW3y/Image5.png" alt="Image5" border="0"></a>
</p>

Email only method are very successful at first instance, but will decay over time. Although the second mail sent helped to sustain revenues for a week, they don't seem to be enough to reverse the trend.

While the Email + Call method starts with the lowest performance, it sustains an increasing trend, with a call at 3rd week that helps to boost the revenues.

The Call method have sustained revenues over the time, but low. Being the Call method the one who requires lot of efforts, we should question if it worth.

To evaluate the performance of each sales method in relation to their effort, based in the information provided, we assigned a time effort value to each method:
-  30 min to Call only
-  10 min to Email + Call
-  1 min to Email only

Then we calculate the ratio between revenue and time.
<p align="center">
<a href="https://imgbb.com/"><img src="https://i.ibb.co/myWZGQ2/Image6.png" alt="Image6" border="0"></a>
</p>

Email is the most dominant profitable strategy (97.13 USD/min), followed by Email + call (18.37 USD/min), and finally a low ratio of Call only method (1.59 USD/min).  
Overall ratio is 7.58 USD/min (dashed red line), this mean value is highly skewed due the Call method.

### Other customer details findings:

Those customers who visited the most our website yielded more revenue. So the website should be promoted in order to increase the revenues.
<p align="center">
<a href="https://imgbb.com/"><img src="https://i.ibb.co/hcrTRmd/Image7.png" alt="Image7" border="0"></a>
</p>

## Business Metrics

Since the goal is to select the best approaches for sales strategy, by improving the revenue while lowering the effort put, I suggest to use the **overall ratio Revenue / Time.**

Based on the data provided, currently the overall ratio is 7.58 USD/min.  
The higher this value, the better the approach used on each new product sales strategy.

### Recommendations

In order to improve the business metric:
- I would recommend to focus on Email method, which is the most profitable strategy, and mix it with Email + call for getting 		higher revenues.
- I would strongly disadvice to use the Call only method. Due the way in which customers buy products are changing, revenue is 		low. Also requires much more effort than other methods, so the performance is poor.
- I would recommend to promote the website, due there is a positive correlation between website visits and revenue.

Recommendations about Data Collection for in-depth analysis:
   * Check for missing data on revenue column
   * Include more data about each new product sold, including their prices.
