# Java-Machine-Test
Category-Product_CRUD_API

DATABASE DESIGN

The database used: PostgreSQL

PostgreSQL is a powerful, open-source, object-relational database system known for its reliability, feature set, and performance. It supports SQL (relational) and JSON (non-relational) querying, making it highly flexible for various applications.

Since we are working on a Spring Boot project with PostgreSQL, we will use application.properties (or application.yml) to configure the connection to the PostgreSQL database.

My database design of Category and Product entity follows a typical relational database model with a one-to-many relationship between the two entities. Here's a brief overview:

Tables:

1. Category Table:

Primary Key: The Category table has an id column, which is the primary key, and it's automatically generated using the GenerationType.IDENTITY strategy.

Columns:

id (Primary Key)
name (Category name)

2. Product Table:

Primary Key: The Product table has an id column generated using GenerationType.IDENTITY.

Foreign Key: It contains a foreign key (category_id) that links each product to its respective category.

Columns:

id (Primary Key)
name (Product name)
price (Price of the product)
category_id (Foreign key referencing Category)

Relationships:

One-to-Many (Category to Products):

A single category can have many products.
This relationship is implemented in the Product table by having a category_id column, which is a foreign key that references the id column in the Category table.



