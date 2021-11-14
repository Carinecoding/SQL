# SQL


## COUNT(*) vs COUNT(1)

You may have seen various discussions about the differences between  `COUNT(*)`  and  `COUNT(1)`. And maybe trying to find the answer confused you even more. So, is there any difference? The simple answer is no – there is no difference at all.

The  `COUNT(*)`  function counts the ***total rows in the table***, including the  `NULL`  values. The semantics for  `COUNT(1)`  differ slightly; we’ll discuss them later. However, the results for  `COUNT(*)`  and  `COUNT(1)`  are identical.

Let’s test this claim using an example query. Suppose I have a table named  `**orders**`  that contains these columns:

-   `order_id`: The ID of the order.
-   `customer_id`: The ID of the customer who placed the order.
-   `order_value`: The total value of the ordered items, in euros.
-   `payment_date`: When the order was paid by the customer.

If I wanted to count the number of rows in the whole table, I’d use the  `COUNT()`  function in the following way:

    SELECT  COUNT(*) AS  number_of_rows
    FROM  orders;
    
[# What is the Difference Between COUNT(*), COUNT(1), COUNT(column name), and COUNT(DISTINCT column name)?](https://learnsql.com/blog/difference-between-count-distinct/)
