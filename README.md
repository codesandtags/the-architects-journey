# The architects journey

This repository has been create with the goal to add documentation in my software architecture journey and design patterns knowledge throught Front-End, Back-End and UI/UX.


## Global Design Principles and Design Patterns

* [Design principles and patterns by Robert C. Marting](https://fi.ort.edu.uy/innovaportal/file/2032/1/design_principles.pdf)
* [Design Patterns Ebook](https://sourcemaking.com/design_patterns)
* [TDD](https://medium.com/@bethqiang/the-absolute-beginners-guide-to-test-driven-development-with-a-practical-example-c39e73a11631)
* [Computer Science Destilled](https://sourcemaking.com/computer-science-distilled)
* [Role and responsibilities for an architect](https://syndicode.com/2017/10/24/the-role-skills-and-duties-of-a-software-architect/)
* [Software Architecture Quality Attributes](https://syndicode.com/2018/05/03/12-software-architecture-quality-attributes/)
* [Feature Toggle / Flag](http://featureflags.io/)
* [Clean Code Summary Robert C. Martin](https://gist.github.com/wojteklu/73c6914cc446146b8b533c0988cf8d29)


# [Cloud Design Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/)

## Availability
* Deployment stamps
* Geodes
* Health Endpoint Monitoring
* Queue Based Load Levering
* Throttling 

## Data Management
* Cache-Aside
* CQRS
* Event Sourcing
* Index Table
* Materialized View
* Sharding
* Static Content Hosting
* Valet Key

## Design and Implementation
* Ambassador
* Anti Corruption Layer
* CQRS
* Back End for Front-end
* Compute Resource Consolidation
* External Configuration Store
* Gateway Aggregation
* Gateway Offloading
* Gateway Routing
* Leader Election
* Pipes and Filter
* Sidecar
* Static Content Hosting
* Strangler

## Messaging
* Asynchronous Request-Reply
* Claim Check
* Choreography
* Competing Consumer
* Pipes and Filter
* Priority Queue
* Publisher-Subscriber
* Queue Based Load Levering
* Scheduler Agent Supervisor
* Sequencial Convoy

## Management and Monitoring
* Ambassador
* Anti Corruption Layer
* External Configuration Store
* Gateway Aggregation
* Gateway Offloading
* Gateway Routing
* Health Endpoint Monitoring
* Sidecar
* Strangler

## Performance and Scalability
* Cache-Aside
* CQRS
* Choreography
* Event Sourcing
* Geodes
* Index Table
* Deployment stamps
* Materialized View
* Priority Queue
* Queue Based Load Levering
* Sharding
* Static Content Hosting
* Throttling 

## Resiliency 
* Bulkhead
* Circuit Breaker
* Compensating Transaction
* Leader Election
* Retry
* Scheduler Agent Supervisor
* Health Endpoint Monitoring
* Queue Based Load Levering

## Security
* Federated Identity
* Gatekeeper
* Valet Key


# [Principles of Microservices](https://samnewman.io/talks/principles-of-microservices/)
1. Culture of automation
2. Hide implementation details
3. Decentralise all the things
4. Deploy independently
5. Isolate Failure
6. Highly Observable
7. Modeled around business domain


## API Versioning strategies
* By URL
* By Query Params
* By Custom Headers
* By Content negotiation

# [Microservices Patterns](https://microservices.io/patterns/microservices.html)

## Application Architecture Patterns
* Monolithic
* Microservices

## Decomposition
* Decompose by business capabilities
* Decompose by subdomain
* Self-contained service
* Service per team

## Refactoring to MicroServices
* Strangler application
* Anticorruption Layer

## Data Management
* Database per service
* Shared database
* SAGA
* API Composition
* CQRS
* Domain Event
* Event Sourcing

## Transactional Messaging
* Transactional Outbox
* Transactional log tailing
* Polling publisher

## Testing
* Service component Test
* Service Integration Contract
* Consumer side contract test

## Deployment Patterns
* Multiple Service Instances
* Single Service Instance per Host
* Service Instance per VM
* Service per Container
* Serverless Deployment
* Service Deployment Platform

## Cross cutting concern
* MicroService Chassis
* Externalized configuration

## Communication Style
* Remote Procedure Invocation
* Messaging
* Domain Specific Protocol
* Idempotent Consumer

## External API
* API Gateway
* BackEnd for Front-end

## Service Discovery
* Client side discovery
* Server side discovery
* Service registry
* Self registration
* Third party registration

## Reliability
* Circuit Breaker

## Security
* Access Token

## Observability
* Log Aggregation
* Application Metrics
* Audit Logging
* Distributed Tracing
* Exception Tracking
* Health check API
* Log deployment and changes

## UI Patterns
* Server Side UI composition
* Client Side UI composition


## DevOps

* [Cloud Native Interactive Landscape](https://landscape.cncf.io/)


## Front-End

### Front-End Architecture
* [Scalable Front-End Architecture Fundamentals](https://blog.codeminer42.com/scalable-frontend-1-architecture-9b80a16b8ec7)
* [Scalable Front-End Architecture Common Patterns](https://blog.codeminer42.com/scalable-frontend-2-common-patterns-d2f28aef0714)
* [Scalable Front-End Architecture The state layers](https://blog.codeminer42.com/scalable-frontend-3-the-state-layer-b23ed69ca57c)
* [What I expect from a Front-End Architecture](https://medium.com/statuscode/what-i-expect-from-a-front-end-architecture-31b9be4498af)
* [Concerns of Front-End Architecture](https://benmccormick.org/2019/01/07/the-concerns-of-fe-architecture/)
* [Best practice in React Architecture](https://www.sitepoint.com/react-architecture-best-practices/)
* [Create a React boilerplate](https://www.freecodecamp.org/news/how-to-set-up-deploy-your-react-app-from-scratch-using-webpack-and-babel-a669891033d4/)
* [Front-End Resources based on ZTM](https://zerotomastery.io/resources/)
* [The modern tutorial for JavaScript](https://javascript.info/) and [Watch and Code](https://watchandcode.com/p/practical-javascript)


### Micro Front-End
* [Micro Front-Ends approach](https://martinfowler.com/articles/micro-frontends.html)

### JavaScript
* [Understanding the coercion in JavaScript](https://www.freecodecamp.org/news/js-type-coercion-explained-27ba3d9a2839/)
* [Curry and function composition](https://medium.com/javascript-scene/curry-and-function-composition-2c208d774983)
* [7 Principles of Rich Web Applications](https://rauchg.com/2014/7-principles-of-rich-web-applications)
* [JavaScript Design Patterns - Addy Osmani](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)
* [Module Pattern and module systems](https://auth0.com/blog/javascript-module-systems-showdown/)
* [JavaScript Specifications](https://tc39.es/)

### Accessibility / WCAG / ARIA
* [Design Patterns for accessibility with widgets](https://www.w3.org/TR/wai-aria-practices/#aria_ex)
* [JavaScript and Node Testing best practices](https://github.com/goldbergyoni/javascript-testing-best-practices)
* [NodeJS best practices](https://github.com/goldbergyoni/nodebestpractices)

## Back-End
* [Hexagonal Architecture by Javier Vélez](http://www.javiervelezreyes.com/ni-nueva-ni-arquitectura-ni-hexagonal/)
* [MicroServices Patterns](https://microservices.io/index.html)
* [Back For Front-End BFF](https://samnewman.io/patterns/architectural/bff/)

## UI/UX
* [UI / UX Design Patterns](http://ui-patterns.com/patterns)

## Programming Paradigms
* [Alan Kay on the Meaning of “Object-Oriented Programming”](http://userpage.fu-berlin.de/~ram/pub/pub_jf47ht81Ht/doc_kay_oop_en)
* [OOP hard criticism](https://medium.com/better-programming/object-oriented-programming-the-trillion-dollar-disaster-%EF%B8%8F-92a4b666c7c7)


# Books & Articles
* [Books in software Architecture](https://medium.com/@nvashanin/books-in-software-architecture-6ad974e524ce)
* [Medium articles about architecture](https://medium.com/@nvashanin/the-path-to-becoming-a-software-architect-de53f1cb310a)
