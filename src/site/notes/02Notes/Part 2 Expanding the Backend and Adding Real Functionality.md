---
{"dg-publish":true,"permalink":"/02-notes/part-2-expanding-the-backend-and-adding-real-functionality/","tags":["#notes/atomic"]}
---

**Link to Course**: [[02Notes/Curriculum Building a Modern Web App UCR Starter Project\|Curriculum Building a Modern Web App UCR Starter Project]]

Introduce real software engineering practices: 
- layered architecture
- databases
- migration
- testing
- refactoring.

---
##  Backend Architecture Understanding Layers 

Here students learn how to break down an application into separate layers

- [[Layered Backend Architecture (Data / Service / Web)\|Layered Backend Architecture (Data / Service / Web)]]
  - [[Data Layer (Models & ORM)\|Data Layer (Models & ORM)]]
  - [[Service Layer (Business Logic)\|Service Layer (Business Logic)]]
  - [[Web Layer (Routes & Schemas)\|Web Layer (Routes & Schemas)]]

## Databases 

Students go from “what is SQL?” to fully integrated models + migrations.

- [[Database Overview (SQL vs NoSQL)\|Database Overview (SQL vs NoSQL)]]
- [[Introduction to SQLModel\|Introduction to SQLModel]]
- [[Database Migrations with Alembic\|Database Migrations with Alembic]]
- [[Database Comparison (SQLite, PostgreSQL, Mongo)\|Database Comparison (SQLite, PostgreSQL, Mongo)]]

---
## Cloud Integration (Firebase)

Add real-world capabilities like cloud file storage + third-party auth.

- [[What is Cloud Storage\|What is Cloud Storage]]
- [[What Is Firebase\|What Is Firebase]]
- [[Using Firebase Storage with FastAPI\|Using Firebase Storage with FastAPI]]
- [[Firebase Authentication with Python SDK\|Firebase Authentication with Python SDK]]

## First Refactor

A professional-quality codebase requires configuration, settings, and logs. 

- [[Understanding Environment Variables\|Understanding Environment Variables]]
- [[Pydantic Settings for Config Management\|Pydantic Settings for Config Management]]
- [[Adding Logging to FastAPI\|Adding Logging to FastAPI]]

---

## Testing Your Application

Teach them test-driven design

- [[Why Testing Matters\|Why Testing Matters]]
- [[Pytest Basics\|Pytest Basics]]
- [[Unit Tests vs Integration Tests vs End-to-End Tests\|Unit Tests vs Integration Tests vs End-to-End Tests]]
- [[How to Test Databases using SQLModel and Pytest\|How to Test Databases using SQLModel and Pytest]]
- [[How to Test API EndPoints using FastAPI and Pytest\|How to Test API EndPoints using FastAPI and Pytest]]

----
# Resources
