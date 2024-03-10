1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.

A). 
Firstly, Let's see the Entities:

a). Product:
     Represents individual products in the system. It likely contains attributes such as id, name, description, SKU, category_id, inventory_id, price, and more.
     
b). Product_Category:
     Represents different categories or types of products. It might have attributes like id, name, and possibly additional information related to the category.
	 
	 
 Relationship : The relationship between the "Product" and "Product_Category" entities in the diagram is a "one-to-many" relationship.

The relationship between these two entities is established through a foreign key.
The id attribute in the Product_category entity serves as a foreign key.
This foreign key references the primary key category_id in the Product entity.
Establishing the connection between the two entities, allowing the database to enforce referential integrity and to query products by their category.





2. How could you ensure that each product in the "Product" table has a valid category assigned to it?

A).
There are several approaches to ensure each product in the "Product" table has a valid category assigned to it, the most reliable method is

Adding Database Constraints   :- Use database constraints to enforce referential integrity between the "Product" and "Product_Category" tables.

This means the database will reject any attempt to insert into a product_category table with a id that doesn't exist in the "Product" table category_id.

In MySQL: 
         Add a PRIMARY KEY constraint on the category_id column in the "Product" table referencing the FOREIGN KEY (id) of the "Product_Category" table.


