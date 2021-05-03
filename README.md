# E-commerce Back End <!-- omit in toc -->
- [Description](#description)
- [Technologies Used](#technologies-used)
- [Intallation and Usage](#intallation-and-usage)
- [User Story](#user-story)
- [Acceptance Criteria](#acceptance-criteria)
## Description
The E-commerce Backend is strictly a backend application that uses Sequelize to query an inventory database. The database contains information for products, categories of products, and tags.

The database is a series of related tables, described by the following picture:
![relational table flowchart](assets/database-map.PNG)

Users can get all information from a table, get an item from a table by id, update information in a table, and lastly delete any item. This makes the application total CRUD!
## Technologies Used
- express: used to create a server using JavaScript
- dotenv: used to store sensitive information including MySQL password and username in environment variables
- MySQL2: used to create databases and tables, and run queries
- Sequelize: used to create SQL queries in JavaScript
## Intallation and Usage
After cloning the repository, users will have to create a .env file and store the DB_NAME, DB_USER, and DB_PW as the values used to connect to their MySQL database.

Then users should `npm i` to download the necessary dependencies for the application. Then users should run `npm run seed` to seed their database with values, and lastly run `npm start` to start the server.

Once the server is running, users can will be able to make db request using the port that the server is running on. By default, the application runs on port 3001.
## User Story
```
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
```
## Acceptance Criteria
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