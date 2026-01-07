## ADR-002: Choice of Technology Stack

## Status
Accepted – 27/10/202

## Context and Problem Statement
The Complaint Management System (CMS) is a web-based application intended for banks and telecom organisations.
The system must support accessibility features such as screen readers and dark mode, role-based access control,
and future extensibility such as chatbot integration.

A suitable technology stack is required to ensure the system is maintainable, scalable, secure, and achievable
within the project timeframe, while aligning with the selected three-tier architecture.


## Considered Options
1. React (JavaScript Framework)
2. Node.js (JavaScript Runtime for Backend)
3. Laravel (PHP Framework) with MySQL
## Pros and Cons of the Options


### React:
**Pros:**
-  Modern and widely used frontend framework
- Excellent for building dynamic, responsive user interfaces
-  Functions effectively with scalable systems and APIs

**Cons:**
-  Not recommended for short deadlines and inexperienced
-  involves extra backend configuration


### Node.js:
**Pros:**
-  Uses JavaScript for both frontend and backend therefore single language development
-  For real-time web applications, quick, scalable, and effective
-  widle used in moduren websites specally for systems like CMS 


**Cons:**
- Requires significant JavaScript understanding
- Setup and integration with databases, frameworks, etc adds complexity
- limited time to learn it in time for the project of CMS

### Laravel (PHP Framework) with MySQL:
**Pros:**
- Laravel provides a structured MVC framework, improving maintainability and code organisation
- Built-in support for authentication, routing, validation, and security
- MySQL integration is reliable and well-supported
- XAMPP/Laragon enables simple local development and testing
- Familiar technology, reducing learning overhead within project constraints
- Supports accessibility-compliant front-end development using HTML, CSS, and JavaScript


  
**Cons:**
- Less modern front-end experience compared to React-based stacks
- Some features require manual configuration compared to full JavaScript ecosystems
-  A learning curve and a complicated building environment

## Decision Outcome
The final technology stack selected for the CMS is Laravel (PHP Framework) with MySQL.
This choice provides a balance between structured development, scalability, and development efficiency,
while remaining achievable within the project timeframe.

Laravel supports the three-tier architectural design through clear separation of presentation,
business logic, and data access layers. It also provides built-in mechanisms for authentication,
role-based access control, and validation, which align with the CMS requirements.


Selected technology Components:

Frontend: HTML, CSS, JavaScript (WCAG-compliant and responsive)
Backend: Laravel (PHP Framework)
Database: MySQL
Local Development Environment: Laragon
Version Control: GitHub
  
Without making the setup too complicated, this method enables essential system functions
including feedback submission, complaint registration, and accessibility features.

## Consequences
**Positive:**
- Faster development and easier debugging
- Ideal for proof-of-concept validation
- Integrates smoothly with accessibility tools like screen readers

**Negative:**
- Some integrations (e.g. future chatbot services) may require additional configuration
- Front-end interactivity is more limited compared to JavaScript-heavy frameworks

## Confirmation
This decision was confirmed through project planning discussions and Feedback from the module tutor 


## More Information

