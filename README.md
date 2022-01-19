# Data Science Intern Challenge for Shopify

## Question One
### a. Based on the initial AOV provided in the assignment, it was clear that there must be outliers of some kind skewing the data. With some data exploration and cleaning, it was easy to identify the outliers and remove them from the data in order to calculate an AOV that more accurately reflects sales in the shoe stores. This can be seen in [question_one.ipynb](https://github.com/twolightsabovethesea/shopify-data-science/blob/main/question_one.ipynb). 
### b. The metric that I would report for this dataset really depends on the question that needs to be answered or the problem that needs to be solved. Are we looking to evaluate the performance of different stores? Find a pattern in AOV as it relates to item prices? Determine whether customers who spend more in one transaction or customers who make multiple smaller purchases actually spend more in total on average? Without knowing what the goal is, it would be pointless to pick a metric at random.
### c. After cleaning the data, the AOV as originally requested turns out to be $302.58.

## Question Two
### a. After a quick  select * query on the Shippers table to check the ShipperID for Speedy Express, the query "SELECT count(OrderID) FROM orders where ShipperID = 1;" tells us that Speedy Express shipped a total of 54 packages. ![Image](https://github.com/twolightsabovethesea/shopify-data-science/blob/main/images/query_a.png)
### b. A more complex query including a join was needed for part b. The following query reveals that Callahan had the most orders, coming in at 216: "SELECT Orders.EmployeeID, Employees.LastName, sum(Orders.EmployeeID) as Total FROM Orders LEFT JOIN Employees ON Orders.EmployeeID = Employees.EmployeeID GROUP BY Orders.EmployeeID ORDER BY Total DESC;". ![Image](https://github.com/twolightsabovethesea/shopify-data-science/blob/main/images/query_b.png)

