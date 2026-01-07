# ADR-004: Choice of Authentication Mechanism

## Status
Accepted – 03/11/2025

## Context and Problem Statement
The Complaint Management System (CMS) requires a secure and reliable authentication mechanism to support multiple user roles,
including Consumers, Help Desk Agents, Support Persons, Managers, and System Administrators.

The authentication solution must enforce role-based access control (RBAC), protect user credentials and sessions,
and integrate seamlessly with the Laravel-based backend. In addition, the solution must be achievable within the
project timeline while adhering to standard security practices such as secure session handling, password hashing,
input validation, and controlled error reporting.

Given that the CMS is a multi-tenant system managing sensitive customer and organisational data,
selecting an appropriate authentication mechanism is critical to ensure security, maintainability,
and long-term scalability.

## Considered Options
1. Laravel Built-In Session Authentication (Laravel Breeze)
2. Manual PHP Session-Based Authentication (Custom Built)
3. Cryptography-Only Authentication Mechanisms

## Pros and Cons of the Options

### Laravel Built-In Session Authentication (Laravel Breeze)

**Pros:**
- Secure by default and follows Laravel security best practices
- Provides ready-made authentication scaffolding
- Uses secure password hashing and session management
- Integrates seamlessly with Laravel middleware and policies
- Supports role-based access control aligned with CMS requirements
- Reduces development time and implementation risk

**Cons:**
- Requires familiarity with Laravel authentication workflows
- Less flexible than a fully custom-built authentication system

---

### Manual PHP Session-Based Authentication

**Pros:**
- Full control over authentication logic
- Simple conceptual model for beginners

**Cons:**
- Security mechanisms must be implemented manually
- High risk of introducing vulnerabilities
- No built-in support for role-based access control
- Increased development and testing effort

---

### Cryptography-Only Authentication Approaches

**Pros:**
- Provides secure password storage mechanisms

**Cons:**
- Does not provide a complete authentication solution
- Does not address session management or access control
- Introduces unnecessary complexity for the scope of this project

## Decision Outcome
Laravel Built-In Session Authentication using Laravel Breeze was selected as the authentication mechanism for the CMS.

## Justification
This solution provides a secure, scalable, and well-documented authentication mechanism that aligns directly with
the chosen Laravel framework and three-tier architecture.

Laravel Breeze ensures secure session-based authentication, enables clean implementation of role-based access control
through middleware, and minimises development effort while maximising security. This approach avoids unnecessary
complexity such as custom cryptographic workflows or token-based authentication, which are not required for the
current scope of the CMS.

## Consequences

**Positive:**
- Secure password hashing and automatic session management
- Consistent enforcement of role-based access control (RBAC)
- Reduced likelihood of security vulnerabilities
- Faster development and easier maintenance

**Negative:**
- Requires understanding of Laravel authentication conventions
- Tight coupling with Laravel may increase migration effort in the future

## Confirmation
This decision was validated through architectural planning, alignment with project security requirements,
and review against module security principles and best practices.

## More Information
- Module Lecture: Security, Week 6
- Laravel Documentation: Authentication and Laravel Breeze
