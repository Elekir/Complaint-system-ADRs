## ADR-004: Choice of Authentication

## Status
Draft – 03/11/2025


## Context and Problem Statement
Access control and secure authentication for various user roles are necessary for the Complaint Management System (CMS).
While complying to standard security procedures like input validation, secure session handling, and safe error reporting,
the authentication system must be easy enough to deploy within the project timeline.

Role-based functionality, such as the ability for customers to file complaints, agents to allocate support persons,
and administrators to onboard organisations, must also be supported by the selected solution.

## Considered Options
1. Laravel’s Built-In Session Authentication
2. Manual PHP Session-Based Login (Custom Built)
3. Cryptography Approaches

## Pros and Cons of the Options


### Laravel Built-In Authentication:
**Pros:**
-  Quick to execute with integrated scaffolding
-  Good documentation and community assistance
-  Secure by default
-  contains role-based access control middleware which aline with the CMS

**Cons:**
-  needs to become familiar with certain new Laravel features.

### Custom PHP Session-Based Authentication:
**Pros:**
-  Very easy to understand for a beginner
-  there is no need for learning curv
-  Maximum control over login flow


**Cons:**
-  Security features must be manually implemented.
-  Absence of integrated role management
-  Vulnerabilities are more easily introduced by mistake.

### Encryption:
**Pros:**
-  offers safe password storing
  
**Cons:**
-  Not a complete solution for authentication
-  increases complexity without resolving access control issues
-  Not necessary for this project’s scope


## Decision Outcome
Laravel’s Built-In Session Authentication is selected.

Justification:
- Provides the most secure login strategy with minimal complexity
- Perfectly supports multi-role access through Laravel guards/middleware
- Quicker development and lower implementation risk
- avoids needless complication like cryptographic access mechanisms and token management.

This approach maintains a reasonable coding effort while guaranteeing safe authentication.

## Consequences
**Positive:**
- Secure password hashing
- Session management that is automatic
- Easy implementation of role-based access control (RBAC)
- minimises security flaws when compared to manually writing authentication

**Negative:**
- takes some effort to comprehend Laravel's authentication method
- Certain customisations could call for a better understanding of Laravel
- Depends on Laravel architecture, making migration to pure PHP harder later


## Confirmation
After evaluating development time, security expectations, and the Proof of Concept scope,
this choice was verified as appropriate and validated per module security criteria.

## More Information

- Lecture: Security-Lecture, Week 6
- Laravel Documentation: Authentication 
