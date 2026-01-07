# ADR-005: Choice of Data Storage

## Status
Accepted – 12/11/2025

## Context and Problem Statement
The Complaint Management System (CMS) requires a reliable, scalable, and structured data storage solution to manage
complaints, users, organisations, assignments, status updates, and audit-related information.

Given the multi-tenant nature of the system and the need to support role-based access, reporting, and future scalability,
the data storage mechanism must provide strong data consistency, clear relational modelling, and seamless integration
with the Laravel backend.

The selected solution must also be achievable within the project timeframe, support rapid development and testing,
and align with industry-standard practices for transactional systems.

## Considered Options
1. MySQL Relational Database
2. NoSQL Database (e.g. MongoDB)
3. Flat File / JSON-Based Storage

## Pros and Cons of the Options

### MySQL Relational Database

**Pros:**
- Strong support for structured relational data
- Enforces data integrity through constraints and relationships
- Well-suited for transactional systems such as complaint management
- Seamless integration with Laravel via Eloquent ORM
- Mature tooling support (phpMyAdmin, Laragon)
- Widely used and well-documented

**Cons:**
- Schema changes require migrations
- Less flexible for unstructured data compared to NoSQL solutions

---

### NoSQL Database (e.g. MongoDB)

**Pros:**
- Flexible schema design
- Suitable for unstructured or rapidly changing data

**Cons:**
- Weaker support for relational data and complex joins
- Additional learning curve and setup complexity
- Less suitable for strongly transactional workflows
- Over-engineered for the current CMS requirements

---

### Flat File / JSON-Based Storage

**Pros:**
- Simple to implement for small-scale prototypes

**Cons:**
- No inherent data integrity or relationship enforcement
- Poor scalability and performance
- Not suitable for multi-user, multi-tenant systems
- High risk of data inconsistency and corruption

## Decision Outcome
The MySQL relational database was selected as the primary data storage solution for the CMS.

## Justification
MySQL provides a robust and reliable relational data model that aligns closely with the domain requirements of the CMS,
including users, roles, organisations, complaints, assignments, and status histories.

When combined with Laravel’s Eloquent ORM, MySQL enables clean domain modelling, efficient querying, and strong data
integrity through foreign keys and constraints. This approach supports the system’s transactional nature while
remaining simple enough to implement, test, and maintain within the project timeline.

## Consequences

**Positive:**
- Strong data consistency and referential integrity
- Clear mapping between domain model and database schema
- Efficient querying for reporting and dashboards
- Easy local development and testing using Laragon and phpMyAdmin

**Negative:**
- Schema evolution requires careful migration management
- Less flexibility for storing highly unstructured data

## Confirmation
This decision was validated through alignment with the system’s data design, ERD modelling,
and successful implementation within the Laravel development environment.

## More Information

- Laravel Documentation: Eloquent ORM and Database Migrations
- MySQL Documentation

