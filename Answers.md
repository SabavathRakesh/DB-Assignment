1st) The relationship between the "product" and "product_category" entities is typically a one-to-many relationship, where one product can belong to only one category, but one category can have multiple 
            products. This relationship is established through the `category_id` field in the "product" table, which likely serves as a foreign key referencing the `id` field in the "product_category" table. This 
             means that each product record in the "product" table will have a corresponding category record in the "product_category" table, linking them together.


2nd) To ensure that each product in the "Product" table has a valid category assigned to it, you can enforce referential integrity using a foreign key constraint. Specifically, you would set up a foreign key 
      constraint on the `category_id` field in the "Product" table, referencing the `id` field in the "Product_Category" table. This constraint would ensure that any value entered into the `category_id` 
      field in the "Product" table must already exist in the `id` field of the "Product_Category" table. This way, you prevent the insertion of invalid category IDs into the "Product" table, thereby ensuring that 
      each product has a valid category assigned to it.
