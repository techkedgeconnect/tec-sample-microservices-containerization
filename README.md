# microservices-architect-config-starter
Microservices Architecture Configuration Starter Sample







Architecture of sample multiple microservices developed in different technologies
 - Spring Boot
 - Node.js
 - Python
 - React.js in a project

 The microservices are connected by an API Gateway using Netflix Zuul.

## Application Architecture

The application consists of 6 different Microservices

- [shoes-microservice-spring-boot](https://github.com/sarat9/microservices-architect-config-starter/tree/main/shoes-microservice-spring-boot)  - Spring Boot App with Shoe data

- [offers-microservice-spring-boot](https://github.com/sarat9/microservices-architect-config-starter/tree/main/offers-microservice-spring-boot)  - Spring Boot App with Offers data

- [cart-microservice-nodejs](https://github.com/sarat9/microservices-architect-config-starter/tree/main/cart-microservice-nodejs)  - Node.js App with Cart data

- [wishlist-microservice-python](https://github.com/sarat9/microservices-architect-config-starter/tree/main/wishlist-microservice-python)  - Python App with Wishlist data

- [zuul-api-gateway](https://github.com/sarat9/microservices-architect-config-starter/tree/main/zuul-api-gateway)  - API gateway that proxies all the microservices

- [ui-web-app-reactjs](https://github.com/sarat9/microservices-architect-config-starter/tree/main/ui-web-app-reactjs)  - Single Page Application that provides the UI








![MicroService Architeture ](https://miro.medium.com/max/1050/1*kSLJKEl3X-gKNTpO1l7SQg.png)# Microservices Architecture Sample!

Microservices
Crafting Microservices has now become an industry standard for any new API development, and almost all the organizations are promoting it. 
Microservices are; 
- Decentralized
- Independent 
- Loosely coupled

Before we go into why we need microservices. Lets understand the problems of traditional monolitic approach.

# Problems of monolithic code 
  - Large monolithic code base is complicated to understand and maintain as it grows
  - Scaling becomes challenging
  - It is tightly coupled
  - Extremely difficult to change technology or language or framework (hybrid technologies) because everything is tightly coupled and depend on
    each other
  - Inability to change tech stack will affect business badly and make it lose lot of modern tech solutions
  - It is difficult to refactor your code base - no fault isolation, if any single function fails, the entire application goes down
  - If a particular function consumes more resources such as memory, the entire application feels the pain

# Why go for Microservices
  - A microservices architecture takes single responsibility principle approach
  - Microservices are small, independent, and loosely coupled
  - Microservices are decentralized, highly maintainable, independently deployable
  - Do one thing well - it is always organized around business capabilities
  - Agility, scalability, availability, reusability
  - Improves fault isolation
  - Eliminates long-term commitment to a single technology stack, Code for different services can be written in different languages
  - Can be developed, deployed, and maintained independently
  - Services can also be deployed independently of each other and hence its easy to identify hot services and scale them independent of whole application
  - Development Team Scaling - Each service is a separate codebase, which can be managed by a small development team
  - Development Speed: Microservices are often quite small in size. Due to the size, adding new features in Microservices are usually faster


Feel Free to contribute.. 
