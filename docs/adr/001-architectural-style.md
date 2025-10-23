## ADR-001: Choice of Architectural Style 

## Status
Accepted – 20/10/2025


## Context and Problem Statement
For major telecom and banking customers, ABC Limited is creating a multi-tenant Complaint Management System (CMS).  
The system has to support future integration with chatbot services, manage millions of users, and be available 24/7.
It will mostly be a web-based application, with mobile access coming later. To guarantee scalability, maintainability,
security and inclusiveness, a suitable architectural style is needed so the system can be bult sufficiently

## Considered Options
1.Monolithic Architecture  
2. Three-Tier Architecture  

## Pros and Cons of the Options


### Monolithic Architecture:
**Pros:**
-  Simple to deploy as a single unit
-  faster to develop initially
**Cons:**
-  Poor scalability and maintainability
-  Difficult to adopt new technologies or integrate future chatbot services

### Three-Tier Architecture:
**Pros:**
-  Clear separation of concerns
-  Well-suited for web applications  
- Supports scalability and modular growth
**Cons:**
-  A little more work to keep communication between tiers
-  Requires strict development to prevent breaking the tiers


## Decision Outcome
The Three-Tier Architecture was selected.  
 It offers the right balance of simplicity, scalability, and maintainability.  
 It naturally supports the intended container structure:

 - **UI tier:** Web front-end
 - **server tier:** Backend API
 - **Database tier:** Database

This solution is consistent with current web application best practices, allowing for a simple 
transition to chatbot integration in the future, as well as multi-tenant requirements

## Consequences
**Positive:**
- Provides a clear structure for future feature additions
- best approacht for the CMS System as it provides the requirements of multi roles
- Supports independent scaling of tiers
**Negative:**
- more setup complexity than monolithic architecture
- demands that layering principles be strictly followed.

## Confirmation
This conclusion was validated through early prototype planning and confirmed as suitable 
in consultation with the module professor.

## More Information
- Module Lecture: *Architectural Styles*, Week 2.  
