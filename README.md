

# Data Engineering & Databases Portfolio


## SQL & Relational Databases (PostgreSQL)

For a data scientist, the **80/20 of SQL is mastering data retrieval and aggregation**. The vast majority of daily tasks, from simple data extraction to complex feature engineering, can be accomplished with a solid command of `SELECT` statements, various `JOIN` types, and `GROUP BY` clauses. Advanced functions are powerful but are needed far less frequently than these core workhorses.

My SQL skills are demonstrated through an **[Advanced Sales Analysis](https://www.google.com/search?q=./1_SQL_Relational_Modeling/Advanced_Project/)** project, where I used window functions and CTEs to identify top-selling products.

### 🌱 Beginner

  - [x] `SELECT`, `FROM`, `WHERE` to query data
  - [x] `INSERT`, `UPDATE`, `DELETE` to manipulate data
  - [x] `ORDER BY` to sort results
  - [x] `CREATE TABLE` with basic data types (`VARCHAR`, `INT`, `DATE`)

### 🚧 Intermediate

  - [x] `JOIN` operations (`INNER`, `LEFT`, `RIGHT`) to combine tables
  - [x] `GROUP BY` with aggregate functions (`COUNT`, `SUM`, `AVG`)
  - [x] Basic subqueries
  - [ ] Data integrity with constraints (`PRIMARY KEY`, `FOREIGN KEY`, `NOT NULL`)
  - [ ] `HAVING` clause to filter aggregated results

### 🚀 Advanced

  - [ ] Window Functions (`ROW_NUMBER`, `RANK`, `LEAD`, `LAG`)
  - [ ] Common Table Expressions (CTEs) for query readability
  - [ ] `EXPLAIN` and `EXPLAIN ANALYZE` to analyze query performance
  - [ ] Transaction management (`BEGIN`, `COMMIT`, `ROLLBACK`)
  - [ ] Indexing strategies (B-Tree) and performance tuning
  - [ ] Temporary tables

-----

## NoSQL Databases (MongoDB)

The **80/20 principle for MongoDB in data science involves efficiently querying nested documents and preparing data for analysis**. Mastering basic `find` queries to filter data and understanding the structure of the Aggregation Pipeline (especially `$match`, `$group`, and `$unwind`) provides the tools to handle the majority of semi-structured data challenges without getting lost in administrative complexities.

My proficiency with NoSQL is showcased in a project involving a **[Restaurant Grade Aggregation Pipeline](https://www.google.com/search?q=./2_NoSQL_MongoDB/Advanced_Project/)**. This required building a multi-stage pipeline to analyze nested data.

### 🌱 Beginner

  - [ ] Understanding the Document/Collection model
  - [ ] `insertOne()` and `insertMany()` to create documents
  - [ ] Basic `find()` queries to retrieve documents
  - [ ] `updateOne()` with the `$set` operator to modify fields

### 🚧 Intermediate

  - [ ] Using projections to return specific fields
  - [ ] Advanced query operators (`$in`, `$gt`, `$ne`)
  - [ ] Handling nested documents and arrays
  - [ ] Array update operators (`$push`, `$pull`)
  - [ ] Basic indexing (single-field)

### 🚀 Advanced

  - [ ] The Aggregation Framework (`$match`, `$group`, `$unwind`, `$sort`)
  - [ ] Compound indexing strategies
  - [ ] Performance tuning and analyzing query execution
  - [ ] Using `$lookup` to perform joins between collections

-----

## Geospatial Data (PostGIS)

For most data science applications, the **80/20 of PostGIS is performing spatial joins and distance calculations**. Knowing how to efficiently determine which points are inside which polygons (e.g., `ST_Contains`) and calculating distances between features (`ST_Distance`) unlocks the answers to the most common location-based business questions, from customer mapping to proximity analysis.

I applied foundational geospatial concepts in a project to **[Find Nearby UK Pubs](https://www.google.com/search?q=./3_PostGIS_Spatial_Analysis/Beginner_Project/)**, which involved storing and querying over 50,000 geographic points.

### 🌱 Beginner

  - [x] Understanding core geometry types (`POINT`, `LINESTRING`, `POLYGON`)
  - [ ] Creating a table with a `geometry` column
  - [ ] Ingesting data using `ST_MakePoint` or `ST_GeomFromText`
  - [ ] Basic understanding of Coordinate Reference Systems (CRS)

### 🚧 Intermediate

  - [ ] Spatial querying with `ST_Distance`
  - [ ] Relational functions like `ST_Contains`, `ST_Intersects`, `ST_Within`
  - [ ] Using `ST_DWithin` for optimized distance searches

### 🚀 Advanced

  - [ ] Transforming data between different CRSs (`ST_Transform`, SRID)
  - [ ] Performance optimization using Spatial Indexes (GiST)
  - [ ] Analytic functions like `ST_Buffer`, `ST_Union`, `ST_Centroid`
  - [ ] Combining spatial and non-spatial queries for complex analysis
