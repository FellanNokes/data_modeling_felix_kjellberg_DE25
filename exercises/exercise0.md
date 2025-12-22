# Exercise 0 - fundamental concepts of data modeling

These exercises are for you to learn fundamental concepts in data modeling. Many of them can be done with pen and paper, physical whiteboard or with an ERD software such as Lucidchart. It is good practice to work analogue as an important part of data modeling is to align various stakeholders with a mix of technical and business knowledge. It is also advised to discuss with your peers as data modeling usually is not done in solitude.

## 0. Library Bookly

A library called Bookly keeps track of books and members who borrow them. Each book has a title, author, and ISBN number. Each member has a membership ID, name, and contact information. A member can borrow multiple books, but each book can be borrowed by only one member at a time.

a) Identify the `entities` and `attributes` for each entity.

<img src="assets/entities.png" alt="entities" width="500">

b) Determine the `relationship` between member and books.

<img src="assets/relationship_books.png" alt="relationship" width="500">

c) Draw a `conceptual ERD` using crow foots notation.

## 1. Conceptual ERD to words

This is an ERD conceptual diagram that a database designer and the business stakeholders agreed upon in a car rental company called Carent.

<img src="https://github.com/kokchun/assets/blob/main/data_modeling/car_rental.png?raw=true" alt="course structure" width="500">

a) Describe the entities in this conceptual ERD.

**Customer:** Probably contains name, contact info and most likely and number ID

**Rental:** Probably contains customer_id, car_id, rental_date, return_date and staff_id or name

**Car:** Probably contains car_id make and model etc

b) Write out the relationship labels.

customer and car are linked to rental

c) Describe the relationships between the entities (one-to-many, one-to-one and many-to-many).

Each customer can make multiple rentals

Each car can be rented multiple times by different customers

d) Define the relationship statement for example: "A Customer can have one or more Rentals".

yes, same question as c

## 2. University management system

A university needs a system to manage students, courses, and professors.

- each student can enroll in multiple courses.
- each course is taught by one professor.
- a teacher can teach multiple courses.

a) Identify entities and their relationships

b) Come up with possible attributes for the entities

c) Draw conceptual ERD with cardinalities 

d) Define business rules (e.g. a student can enroll in max 4 courses)

<img src="assets/proffessor_student.png" alt="relationship" width="500">

## 3. Onshop

An e-commerce platform Onshop manages customers, orders, and products.

- a customer can place multiple orders.
- each order contains multiple products.
- a product can belong to multiple categories.

a) Identify key entities and their attributes (e.g., customer_name, order_date)

**Customer:**
- first_name
- last_name
- phone_number
- email
- adress
- customer_id (PK)

**Order**
- order_id(PK)
- order_date
- total_cost
- product_id(FK)
- customer_id(FK)

**Product**
- name
- price
- product_id

b) Sketch the conceptual ERD.

<img src="assets/orders.png" alt="relationship" width="500">

c) Define business rules

**Customer-order relationship**
- a customer can place zero, one or many orders
- each order must be placed by one customer
- an order cannot exist without a customer

**order-product relationship**
- an order must contain one or many products
- each product has a price and the order sums all the prices
- a order cannot have zero products

**order rules** 
- each order has a unique order_id
- order_date must be recorded
- each order must have a sum of the total_cost

**customer rules**
- must have first and last name
- must have a email address that is validated upon creating an account.
- must have a address

**product rule**
- has a unique id
- has a price
- has a name

## 4. Theoretical questions

a) What is a conceptual data model, and why is it important?

b) Storing age in a database, is that a good idea, why?

c) What are the three types of data structures, and how do they differ?

d) Give examples of how each data structure is used in real-world applications

e) What is cardinality in data modeling, and why is it important?

f) What are the different steps of data modeling?

g) What factors influence the choice between using an RDBMS and NoSQL?

## Glossary
Fill out the meaning of the terms below:

| Glossary         | Meaning |
| ---------------- | ------- |
| RDBMS            |         |
| relational model |         |
| conceptual model |         |
| logical model    |         |
| physical model   |         |
| ERD              |         |
| data modeling    |         |
| data integrity   |         |
| data consistency |         |
| field            |         |
| attribute        |         |
| data type        |         |
| data redundancy  |         |
| transaction      |         |
| cardinality      |         |
| one-to-one       |         |
| one-to-many      |         |




<!-- ## 0. Convert this table data into json data

You have an SQL table that looks like this

```sql
CREATE TABLE Employees (
    employee_id INT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    department VARCHAR(50),
    salary INT
);

INSERT INTO Employees VALUES (1, 'Hakan', 'Hakansson', 'HR', 30000);
INSERT INTO Employees VALUES (2, 'Bob', 'Bobson', 'IT', 35000);
```

a) Start with writing out the table with the data

b) Convert this into semi-structured JSON format. Do it manually not programmatically.

## 1. Convert json-file to tables

You have this json data, convert it into three tables: Hospital, Department and Doctor. Fill these tables with data. Do this manually and not programmatically.

```json
{
  "hospital": "Sjukhusstock",
  "address": "Drottninggatan 3, Stockholm",
  "departments": [
    {
      "name": "Kardiologi",
      "doctors": [
        { "id": 1, "name": "Dr. Abra Abrahamson" },
        { "id": 2, "name": "Dr. Erika Eriksson" }
      ]
    },
    {
      "name": "Neurologi",
      "doctors": [{ "id": 3, "name": "Dr. Sven Svensson" }]
    }
  ]
}
``` 
-->