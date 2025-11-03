## ADR-001: Choice of Technology

## Status
Accepted – 27/10/202

## Context and Problem Statement
The Complaint Management System (CMS) will be a web-based solution intended for banks and telecom businesses. 
It should support accessibility features such as screen readers and dark mode, be compatible with future chatbot 
integration. A suitable technological measure is necessary to make the system easy to use, maintainable, accessible and realistic delivery within the project timeframe.

## Considered Options
1. React (JavaScript Framework)
2. Node.js (JavaScript Runtime for Backend)
3. PHP with MySQL (XAMPP Usage)

## Pros and Cons of the Options


### React:
**Pros:**
-  Modern and widely used frontend framework
- Excellent for building dynamic, responsive user interfaces
-  Functions effectively with scalable systems and APIs

**Cons:**
-  A more difficult learning curve and a complicated building environment
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

### PHP with MySQL (XAMPP usage):
**Pros:**
-  Easy to use and well supported for small-to-medium-sized web applications
-  XAMPP makes local hosting and deployment simple.
-  MySQL integration is simple and reliable
-  familiar with it as there will not be large learning curve because of time limit
-  PHP is compatible with HTML, CSS, and JS to create an accessible front-end design.
-  easier to understand and use for testing and prototypes

  
**Cons:**
-  Less modern than JavaScript-based stacks
-  Limited dynamic UI capabilities compared to React


## Decision Outcome
The final technology set up chosen is  PHP with MySQL (XAMPP system).
This option ensures that the CMS can be developed, tested, and presented 
within the project timeline by providing a reasonable balance of functionality,
familiarity, and simplicity.

Selected technology Components:

- Frontend: HTML, CSS, JavaScript (WCAG-compliant and responsive)
- Backend: PHP
- Database: MySQL (via XAMPP local server)
- Version Control: GitHub
  
Without making the setup too complicated, this method enables essential system functions
including feedback submission, complaint registration, and accessibility features.

## Consequences
**Positive:**
- Faster development and easier debugging
- Ideal for proof-of-concept validation
- Integrates smoothly with accessibility tools like screen readers

**Negative:*
- Manual API Integration:

## Confirmation
This decision was confirmed through project planning discussions and Feedback from the module tutor 

supported using PHP/MySQL due to the achievable learning curve

## More Information

