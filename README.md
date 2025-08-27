Of course. Here is the revised `README.md` in English, incorporating the 80/20 principle and providing direct links to online datasets for each micro-project.

This structure makes your repository a powerful tool for guided learning and a very practical portfolio.

-----

# Data Engineering & Databases Repository ⚙️

Welcome to my personal repository dedicated to the world of data engineering and database management. This project serves a dual purpose:

1.  **Professional Portfolio**: To showcase my skills and tangible projects in data modeling, storage, manipulation, and management.
2.  **Learning Guide**: To structure my personal development path by separating skills into **Beginner** and **Advanced** tiers, with a specific project to validate each level.

This README acts as a living document and a roadmap for my journey.

-----

## 1\. SQL and Relational Modeling

### 🌱 Beginner Level

This level focuses on the essential commands for interacting with any relational database.

#### 🎯 80/20 Objectives:

  - [ ] **`SELECT`, `FROM`, `WHERE`**: Fetching and filtering data.
  - [ ] **`JOIN`**: Combining data from multiple tables (`INNER`, `LEFT`).
  - [ ] **`GROUP BY` & `COUNT`, `SUM`, `AVG`**: Aggregating data.
  - [ ] **`ORDER BY`**: Sorting results.
  - [ ] **`INSERT`, `UPDATE`, `DELETE`**: Manipulating records.
  - [ ] **`CREATE TABLE`**: Defining a simple table with primary and foreign keys.

💡 **Micro-Project: Library Database**

> **Objective:** Create a mini-system to manage books and authors.
>
> 1.  **Dataset:** For this project, you can create the data yourself. It's a great exercise in data modeling.
> 2.  **Task:**
>       * Create two tables: `Authors` (author\_id, author\_name) and `Books` (book\_id, title, author\_id).
>       * Insert a few of your favorite authors and their books.
>       * Write a query that returns a list of all books with their author's name.

-----

### 🚀 Advanced Level

This level demonstrates a deeper understanding of SQL for complex analysis and performance.

#### 🎯 80/20 Objectives:

  - [ ] **Window Functions (`OVER PARTITION BY`)**: Calculating over subsets of data (e.g., `ROW_NUMBER`, `RANK`, `LEAD`, `LAG`).
  - [ ] **Common Table Expressions (CTEs - `WITH ... AS`)**: Writing clean and readable complex queries.
  - [ ] **Advanced Subqueries**: Using subqueries in `SELECT`, `FROM`, and `WHERE` clauses effectively.
  - [ ] **Transactions (`BEGIN`, `COMMIT`, `ROLLBACK`)**: Ensuring data integrity during multi-step operations.
  - [ ] **`EXPLAIN`**: Analyzing the query execution plan to identify bottlenecks.
  - [ ] **Indexing**: Understanding and creating indexes to speed up read operations.

💡 **Micro-Project: Sales Analysis**

> **Objective:** Analyze a sales dataset to extract complex insights.
>
> 1.  **Dataset:** Use the **Superstore Sales Dataset** from Kaggle. It's a classic and perfect for this kind of analysis.
>       * **Link:** [Kaggle Superstore Sales Dataset](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting)
> 2.  **Task:**
>       * Load the data into a `sales` table in PostgreSQL.
>       * Write a single query using a CTE and a window function to find the top 3 best-selling products within each `Category` for the year 2017.
>       * Run `EXPLAIN ANALYZE` on your query, create a relevant index (e.g., on the order date and category), and show how the execution plan improves.

-----

## 2\. NoSQL Databases: MongoDB

### 🌱 Beginner Level

This level covers the fundamentals of the document-oriented model.

#### 🎯 80/20 Objectives:

  - [ ] **Understand the Document/Collection model**.
  - [ ] **`find()`**: Querying for documents with simple filters (`{ key: "value" }`).
  - [ ] **Projections**: Selecting specific fields to return in a query.
  - [ ] **`insertOne()` & `insertMany()`**: Inserting documents.
  - [ ] **`updateOne()` with `$set`**: Updating specific fields within a document.

💡 **Micro-Project: Restaurant Finder**

> **Objective:** Create a collection to store and query restaurant data.
>
> 1.  **Dataset:** Use the **Sample MongoDB Restaurants Dataset**. This is a standard BSON dump used in MongoDB's own documentation.
>       * **Link:** Download the `restaurants.json` file from this [GitHub Gist](https://www.google.com/search?q=https://gist.github.com/jgassen/5903550). You can import it using `mongoimport`.
> 2.  **Task:**
>       * Import the `restaurants.json` data into a `restaurants` collection.
>       * Write a query to find all restaurants in the "Manhattan" borough that serve "Italian" cuisine.
>       * Write another query, but this time return only the `name` and `address` fields for the results.

-----

### 🚀 Advanced Level

This level focuses on data aggregation and performance optimization in MongoDB.

#### 🎯 80/20 Objectives:

  - [ ] **Aggregation Pipeline**: Mastering the key stages (`$match`, `$group`, `$sort`, `$project`).
  - [ ] **Querying Arrays**: Using operators like `$in`, `$all`, and `$elemMatch`.
  - [ ] **Indexing**: Creating single-field and compound indexes to optimize query performance.
  - [ ] **Advanced Update Operators**: Using `$inc` (increment), `$push` (add to array), `$pull` (remove from array).

💡 **Micro-Project: Analyzing Restaurant Grades**

> **Objective:** Use the Aggregation Pipeline to analyze restaurant inspection grades.
>
> 1.  **Dataset:** Use the same **Sample MongoDB Restaurants Dataset** from the beginner project. The `grades` array is perfect for this.
> 2.  **Task:**
>       * Build an Aggregation Pipeline that calculates the average score (`grades.score`) for each borough.
>       * The pipeline should first `$unwind` the `grades` array.
>       * Then, it should `$group` the documents by `borough` and calculate the average score using `$avg`.
>       * Finally, `$sort` the results to show the borough with the highest average score first.

-----

## 3\. Geospatial Data with PostGIS

### 🌱 Beginner Level

This level covers the basics of storing and querying spatial data.

#### 🎯 80/20 Objectives:

  - [ ] **Geometry Types**: Knowing `POINT`, `LINESTRING`, and `POLYGON`.
  - [ ] **Creating a Geospatial Table**: Using a `geometry` type column.
  - [ ] **`ST_Distance()`**: Calculating the distance between two geometries.
  - [ ] **`ST_Contains()` / `ST_Within()`**: Checking for spatial relationships.

💡 **Micro-Project: Find Nearby Pubs**

> **Objective:** Store points of interest and find the ones closest to a specific location.
>
> 1.  **Dataset:** Use the **Open Pubs dataset from GetTheData**. It's a simple CSV with latitude and longitude.
>       * **Link:** [GetTheData - Open Pubs](https://www.getthedata.com/open-pubs)
> 2.  **Task:**
>       * Create a `pubs` table with a `geom` column of type `geometry(Point, 4326)`.
>       * Import the data, using `ST_MakePoint(longitude, latitude)` to create the geometry.
>       * Pick a point in the UK and write a query to find the 5 nearest pubs to that location using `ST_Distance`.

-----

### 🚀 Advanced Level

This level focuses on spatial analysis and performance.

#### 🎯 80/20 Objectives:

  - [ ] **Coordinate Systems (SRID)** and `ST_Transform()`: Understanding and converting data between different coordinate reference systems.
  - [ ] **Spatial Indexes (GiST)**: Creating a spatial index and understanding its impact on performance.
  - [ ] **Spatial Analysis Functions**: Using `ST_Buffer` (create a buffer zone), `ST_Union` (merge geometries), and `ST_Intersects` (check for overlap).

💡 **Micro-Project: London Tube Stations within Boroughs**

> **Objective:** Combine point and polygon data to perform a spatial join.
>
> 1.  **Datasets:**
>       * **Polygons:** London Boroughs boundaries from the **London Datastore**. Download the Shapefile.
>           * **Link:** [London Datastore - Borough Boundaries](https://data.london.gov.uk/dataset/statistical-gis-boundary-files-london)
>       * **Points:** A list of London Tube stations with coordinates.
>           * **Link:** [Kaggle - London Tube Stations](https://www.google.com/search?q=https://www.kaggle.com/datasets/boardpack/london-tube-stations)
> 2.  **Task:**
>       * Import both datasets into PostGIS tables (use `shp2pgsql` for the shapefile).
>       * Ensure both tables use the same SRID, using `ST_Transform()` if necessary.
>       * Write a query that counts how many tube stations (`points`) are located within each London borough (`polygon`). This will require a spatial join using `ST_Contains` or `ST_Within`.
>       * Ensure your spatial columns have GiST indexes.
