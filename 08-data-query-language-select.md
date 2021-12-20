# Data Query Language - SELECT

One of the most powerful SQL commands is SELECT, over the next few examples we are going to 
demonstrate various searches, with the aim of providing the building blocks for data extraction 
useful not only in SQL but in almost any reference to data you may come across.

All examples in this section are provided in the file 

**NOTE**: As all examples are provided in a single file, you will need to uncomment and comment 
relevant lines within the file as you progress through the examples.

Basic syntax for SELECT:

```
SELECT * FROM <table>;
```

This is requesting that all fields (this is what the * denotes) from the table specified. For example:

```sql
-- simple select
SELECT * FROM `orders`;
```

This will return all fields, and all rows in the table \`orders\`.

## SELECT ... WHERE

If we now wanted to extract all records where the newsletter field held a value of 1 i.e. the customer 
is registered to receive a newsletter, we would change the SQL as per example 2:

```sql
-- example 2 - where customers are registered to receive the newsletter
SELECT * FROM `orders` WHERE newsletter = 1 
```

You will now notice that the results pane only shows records where newsletter = 1.

## Comparison Operators

WHERE uses a comparison operator, the following table lists common comparison operators:

- = Equal to
- \> Greater than
- < Less than
- \>= Greater than or equal to
- <= Less than or equal to

We can now use the comparison operators to do more complex queries such as selecting all 
customers who were born before 26th February 1960.

**NOTE**: Dates in MySQL follow the format:

```YYYY-MM-DD```

So the SQL for this search is:

```sql
-- example 3 - show sales by customers born before 26th February 1960
SELECT * FROM `orders` WHERE `date_of_birth` < '1960-02-26';
```

