# MongoDB Queries

This exercise focuses on performing queries on a MongoDB database that manages information about restaurants in New York City. Here, you will find queries to carry out various operations on the restaurants collection.

## About

This repository contains queries designed to interact with a MongoDB database. These queries are part of the Sprint 5.4 assignment for the Node.js specialization at IT-Academy.

## Getting Started

Before executing these queries, ensure that you have a MongoDB database up and running. Additionally, make sure you have a collection named "restaurants" populated with the provided data.

## Prerequisites

To execute the queries, you'll need:

- MongoDB installed on your machine
- Access to a MongoDB instance with the "restaurants" collection

## Usage

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/mongodb-queries.git

    Navigate to the cloned directory:

    bash

    cd mongodb-queries

    Open a terminal or command prompt and run the desired queries using the MongoDB shell or a MongoDB client of your choice.

    Ensure that you replace any placeholders in the queries with actual values as per your database schema.

Queries

Query 1: Find Restaurants by Cuisine

    javascript

        // Example query to find all restaurants serving Italian cuisine
            db.restaurants.find({ cuisine: "Italian" })

    This query retrieves all restaurants that serve Italian cuisine.

Query 2: Find Restaurants with a Score Greater Than 8

    javascript

        // Example query to find restaurants with a score greater than 8
            db.restaurants.find({ "grades.score": { $gt: 8 } })

    This query retrieves restaurants with a score greater than 8.

Query 3: Find Restaurants Open on Sundays

    javascript

        // Example query to find restaurants open on Sundays
            db.restaurants.find({ "hours.Sunday": { $exists: true } })

    This query retrieves restaurants that are open on Sundays.

Query 4: Find Restaurants Closed on Tuesdays

    javascript

        // Example query to find restaurants closed on Tuesdays
            db.restaurants.find({ "hours.Tuesday": "Closed" })

    This query retrieves restaurants that are closed on Tuesdays.

Query 5: Find Restaurants with More Than 100 Inspections

    javascript

        // Example query to find restaurants with more than 100 inspections
            db.restaurants.find({ "grades": { $size: { $gt: 100 } } })

    This query retrieves restaurants that have had more than 100 inspections.

...
Contributing

Contributions are welcome! If you have suggestions for improving the queries or additional queries to add, please open an issue or submit a pull request.
License

This project is licensed under the MIT License.