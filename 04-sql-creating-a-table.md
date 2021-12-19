# SQL – Creating a Table

The following is an example of SQL used to create a table:

```sql
-- create the oc_product table
CREATE TABLE `oc_product` (
 `product_id` int(11) NOT NULL AUTO_INCREMENT,
 `model` varchar(64) NOT NULL,
 `sku` varchar(64) NOT NULL,
 `quantity` int(4) NOT NULL DEFAULT '0',
 `stock_status_id` int(11) NOT NULL,
 `image` varchar(255) DEFAULT NULL,
 `manufacturer_id` int(11) NOT NULL,
 `shipping` tinyint(1) NOT NULL DEFAULT '1',
 `price` decimal(15,4) NOT NULL DEFAULT '0.0000',
 `status` tinyint(1) NOT NULL DEFAULT '0',
 `viewed` int(5) NOT NULL DEFAULT '0',
 `date_added` datetime NOT NULL,
 `date_modified` datetime NOT NULL,
 PRIMARY KEY (`product_id`)
);
```

This is a cut down copy of the SQL used to create the product table in the popular eCommerce 
solution Opencart. 

*I do not expect you to be creating tables of this size or complexity on the course (it is only here as a point of reference.)*

The syntax can be broken down into several simple segments:

The first line, instruct the SQL parser to create a table called oc_product.

![creating-table-1](https://user-images.githubusercontent.com/49883951/146683598-b793abe7-64bb-4f88-b502-3393a100f9f1.PNG)
