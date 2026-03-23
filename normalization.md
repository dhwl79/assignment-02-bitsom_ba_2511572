## Anomaly Analysis
- Insert Anomaly : An insert anomaly occurs when one cannot insert new data into a table because some other, unrelated data is missing or incomplete. [Columns Involved : product_id, product_name, order_id]

- Update Anomaly : Update anomalies occur when the same data is repeated in multiple rows, and changes are made in some but not all instances. [Columns Involved : customer_id, customer_city]

- Delete Anomaly : Delete anomalies occur when deleting a certain row inadvertently leads to the deletion of other important data. [Columns Involved : order_id, customer_id, product_id]

## Normalization Justification
Keeping all data in a single table may seem simple initially, but it leads to serious data integrity and maintenance issues. In the given dataset, storing customers, products, orders, and sales representatives together creates redundancy. For example, customer details like name and city are repeated for every order, increasing storage usage and making updates difficult.

This design leads to update anomalies. If a customer changes their city, it must be updated in multiple rows, increasing the risk of inconsistent data. Similarly, insert anomalies occur when we cannot add a new product or customer without an associated order. Delete anomalies are also critical, removing an order may unintentionally delete important customer or product information.

Normalization solves these issues by splitting the data into multiple related tables such as customers, products, orders, and order_items. Each table stores only relevant data, reducing redundancy and improving consistency. Relationships are maintained using foreign keys, ensuring data integrity.

Although normalization may seem complex initially, it significantly improves scalability, maintainability, and accuracy of the database. Therefore, normalization is not over-engineering but a necessary step in designing efficient and reliable database systems.