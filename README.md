# E-commerce Back End <!-- omit in toc -->
- [Description](#description)
- [Technologies Used](#technologies-used)
- [Intallation and Usage](#intallation-and-usage)
- [Submission Requirements](#submission-requirements)
  - [User Story](#user-story)
  - [Acceptance Criteria](#acceptance-criteria)
  - [Grading Criteria](#grading-criteria)
- [TO DO](#to-do)
## Description
## Technologies Used
## Intallation and Usage
## Submission Requirements
### User Story
```
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```
### Acceptance Criteria
```
GIVEN a functional Express.js API
WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the MySQL database
WHEN I open API GET routes in Insomnia Core for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia Core
THEN I am able to successfully create, update, and delete data in my database
```
### Grading Criteria
#### Deliverables - 10%  <!-- omit in toc -->
- [ ] GitHub repository containing application code
#### Walkthrough Video - 37%  <!-- omit in toc -->
- [ ] Demonstrates the functionality of the e-commerce back end
- [ ] Shows all of the technical acceptance criteria being met
- [ ] Demonstrates how to create the schema from the MySQL shell
- [ ] Demonstrates how to seed the database from the command line
- [ ] Demonstrates how to start the application’s server
- [ ] Demonstrates GET routes for all categories, all products, and all tags being tested in Insomnia Core
- [ ] Demonstrates GET routes for a single category, a single product, and a single tag being tested in Insomnia Core
- [ ] Demonstrates POST, PUT, and DELETE routes for categories, products, and tags being tested in Insomnia Core
#### Technical Acceptance Criteria - 40%  <!-- omit in toc -->
- [ ] Uses MySQL2 and Sequelize to connect to MySQL database
- [ ] Uses dotenv package to store sensitive data as environment variables
- [ ] Syncs Sequelize models to MySQL database on server start
- [ ] Includes column definitions for all four models:
  - [ ] Category
    - [ ] id: integer, not null, primary key, auto increment
    - [ ] category_name: string, not null
  - [ ] Product
    - [ ] id: integer, not null, primary key, auto increment
    - [ ] product_name: string, not null
    - [ ] price: decimal, not null, validates value is decimal
    - [ ] stock: integer, not null, default 10, validates value is numeric
    - [ ] category_id: integer, references Category's id
  - [ ] Tag
    - [ ] id: integer, not null, primary key, auto increment
    - [ ] tag_name: string
  - [ ] ProductTag
    - [ ] id: integer, not null, primary key, auto increment
    - [ ] product_id: integer, references Product's id
    - [ ] tag_id: integer, references Tag's id
- [ ] Includes model associations:
  - [ ] Product belongs to Category
  - [ ] Category has many Products
  - [ ] Product belong to many Tags through ProductTags
  - [ ] Tag belongs to many Products
#### Repository Quality - 13%  <!-- omit in toc -->
- [ ] Has unique name
- [ ] Follows best practices for file structure and naming conventions
- [ ] Follows best practices for class/id naming conventions, indentation, quality comments, etc.
- [ ] Contains multiple descriptive commit messages
- [ ] Contains a high-quality README with description and a link to a walkthrough video



## TO DO
- [ ] Define columns in Models:
  - [ ] Category
  - [ ] Product
  - [ ] ProductTag
  - [ ] Tag
- [ ] Set up Model relationships
- [ ] Complete routes
  - [ ] Category
  - [ ] Product
  - [ ] Tag
- [ ] Setup .env file with MySQL info