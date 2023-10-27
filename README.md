# databricks

### Link to download the data:

* https://merkle-de-interview-case-study.s3.eu-central-
1.amazonaws.com/de/user.csv
  
* https://merkle-de-interview-case-study.s3.eu-central-
1.amazonaws.com/de/order.csv
  
* https://merkle-de-interview-case-study.s3.eu-central-
1.amazonaws.com/de/item.csv
  
* https://merkle-de-interview-case-study.s3.eu-central-
1.amazonaws.com/de/event.csv

### Assignment: Create a data lake which consists of different layers:

#### Bronze:

1. Contains external tables for all prerequisite files
2. All attributes are of STRING type. No transformations are applied

#### Silver:

1. Contains all datasets from the first layer
2. All attributes have a common naming convention
3. All attributes have proper datatypes based on the attribute name and common logic
3. All struct collection attributes are flattened and transformed into proper data types
4. Fact tables are properly partitioned based on meaningful attributes

#### Gold: 
1. For every year (based on the created_at attribute)
 * Total number of items sold in a particular year
 * Rank of an item based on the total number of items sold in a particular year
 * Total sales from an item in a particular year
 * Rank of an item based on the total sales in a particular year
2. Total number of items sold in all years
3. Rank of an item based on the total number of sales
4. Total sales of an item in all years
5. The rank of an item based on the total sales

#### Gold:
top_buyers data mart with top 20 customers who contributed on
the total sales the most with additional attributes:
* Total sales contributed
* Rank based on the total sales
* The last order creation date
* The overall most viewed item of a customer
