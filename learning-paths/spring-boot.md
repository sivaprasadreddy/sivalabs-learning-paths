# Spring Boot Learning Path

[Spring Boot](https://spring.io/) is the most popular framework in the Java world to build enterprise applications.
Also, Spring Boot is the most sought-after skill to get hired as a Java developer.

Here is my recommended approach to learn Spring Boot.

## 1. Prerequisites: What you should already know
1. If you are completely new to Java, then directly jumping on to Spring Boot is NOT recommended.
2. First, learning Core Java and get familiar with Java ecosystem.
3. Get familiar with the installation of JDK and using the build tools like Maven or Gradle.
4. Get familiar with using IDEs like IntelliJ IDEA, Eclipse/STS, VS Code

## 2. If you are new to Spring itself
Spring Boot is an opinionated framework built on top of various Spring portfolio projects.

So, if you are completely new to Spring itself, 
I would recommend first to learn a few Spring Core concepts:
  * Dependency Injection
  * Spring Bean Configuration
  * Bean Scopes
  * Aspect Oriented Programming (AOP)


What you need to know before starting with Spring Boot: [Spring Boot Missing Guide](https://www.youtube.com/playlist?list=PLuNxlOYbv61jZL1IiciTgWezZoqEp4WXh)

You don't have to master every detail of these concepts in-depth.
But having a decent understanding of these concepts will make it easy to understand Spring Boot.

## 3. You are familiar with Spring framework and want to learn Spring Boot
Once you are familiar with Spring core concepts, then you can begin your journey to learn Spring Boot.

> [!IMPORTANT]  
> Spring Boot is an opinionated framework built on top of various other Spring projects with convention-over-configuration approach.
> So, if you are not familiar with underlying technologies such as JPA/Hibernate, Kafka, etc then Spring Boot looks like magic.
> While learning as a beginner, you may have to proceed further without understanding how exactly things work behind the scenes.
> Once you got it working, you may have to go back and explore further how Spring Boot is auto-configuration makes it working.
> Learning every Spring Boot integrated technology first is not practical.
> This is a Chicken-Egg problem, so you need to follow along the tutorial or video first and then understand how it works later.

### Stage 1
In Stage 1, you learn the fundamentals of Spring Boot.

* [Getting Started with Spring Boot](https://www.sivalabs.in/getting-started-with-spring-boot/): Learn how to create a Spring Boot application and 
  build a basic HelloWorld style REST API. Then learn how to run the Spring Boot application.
* **Build a basic CRUD REST API:** Create a basic REST API performing CRUD(Create, Read, Update, Delete) operations using a HashMap based storage.
  The goals of this exercise are:
  * Get familiar with how to implement API handler methods for different types of HTTP methods using
  **@GetMapping, @PostMapping, @PutMapping, @DeleteMapping** annotations.
  * Understand how to use **@PathVariable, @RequestBody** to work with URL path variables, HTTP request body.
  * To keep it simple, store the data in a HashMap with key as primaryKey and object as the value. 
* **Understand Spring Boot Core Features**:
  Spring Boot provides some features out of the box which are commonly used in building web and enterprise applications.
  
  * **Spring Boot Logging**: Spring Boot automatically provides logging support with SLF4J and Logback.
    You may want to configure it to suit your application needs. So, you need to understand how to customize the default logging configuration.
    * **Resources:**
      * [Spring Boot Logging Tutorial](https://www.sivalabs.in/spring-boot-logging-tutorial/)
      * [Spring Boot Tips : Part 3 - How to implement Logging in SpringBoot applications](https://www.youtube.com/watch?v=tmj6QphzAPo)

  * **Spring Boot Application Configuration**: Spring Boot provides support for providing the application configuration properties in a wide variety of ways.
    But you mostly like will be using three or four approaches to provide default configuration and overriding the configuration.

    * [Spring Boot Application Configuration Tutorial](https://www.sivalabs.in/spring-boot-application-configuration-tutorial/)
    * [Spring Boot Tips : Part 2 - Managing Application Configuration Properties In The Right Way](https://www.youtube.com/watch?v=4OX7hbAGuRE)
  
  * **Spring Boot Profiles**: Profiles is a concept in Spring framework which helps in configuring the application differently for different environments.
    In real projects, you typically want to configure your application with different property values for different environments (dev, qa, prod).
    You can use Spring profiles to customize/configure your application per-environment and enable the desired profile when starting the application.
    Spring Boot makes is easy to use profiles with some default conventions.

    * [Spring Boot Profiles Tutorial](https://www.sivalabs.in/spring-boot-profiles-tutorial/)

  * **Spring Boot Testing**: Testing is an integral part of any professional software development.
    Spring Boot provides excellent support for testing.

    * [Spring Boot Testing Tutorial](https://www.sivalabs.in/spring-boot-testing-tutorial/): This tutorial will give an overview of Spring Boot's testing support.
      But when you use databases or Kafka, etc then you can use the [Testcontainers](https://testcontainers.com/) library for testing. You can learn this in the next stage.

After completing these tutorials, you should have a good grasp on Spring Boot basics.

### Stage 2
In Stage 2, you learn how to work with SQL databases, how to handle database transactions, 
how to test your application when using a database.
You should also learn how to handle exceptions gracefully.
Finally, you will learn some best practices while building REST APIs using Spring Boot.

**Prerequisites:** 
* You should be familiar with JDBC if you want to use **JdbcTemplate** or **JdbcClient**
* You should have at least some basic knowledge of JPA if you want to use **Spring Data JPA**

Spring Boot provides higher-level abstractions to make it easy to work with Databases.
You can use newer **JdbcClient** or older **JdbcTemplate** to execute SQL queries without writing low-level boilerplate code.

* [Spring Boot JdbcClient Tutorial](https://www.sivalabs.in/spring-boot-jdbcclient-tutorial/)
* [Spring Boot JdbcTemplate Tutorial](https://www.sivalabs.in/spring-boot-jdbctemplate-tutorial/)

Database transaction management is a crucial part of any real world application using an SQL database.
Spring Boot makes it straightforward to apply transaction boundaries using **@Transactional** annotation.
But it is crucial to understand how the transaction management works to avoid some common gotchas.

* [Spring Boot Database Transaction Management Tutorial](https://www.sivalabs.in/spring-boot-database-transaction-management-tutorial/)

In real world projects, it is highly recommended to use database migration tools like **Flyway** or **Liquibase** to apply any database changes.
Again, Spring Boot makes it very straightforward to use those database migration tools with it's auto-configuration support.

* [Spring Boot Flyway Database Migration Tutorial](https://www.sivalabs.in/spring-boot-flyway-database-migration-tutorial/)

JPA/Hibernate is the most popular ORM library in Java.
Spring Data JPA provides a higher-level abstraction on top of JPA that simplifies performing CRUD operations, pagination, etc.

Before learning Spring Data JPA, I highly recommend learning JPA basics of how to configure entities.
To keep it simple, you can focus on working with a single entity without any OneToMany, ManyToOne, ManyToMany relations.

This is the right time to learn some best practices while building REST APIs such as following REST API conventions,
using proper status codes, etc.
Also, now is the right time to learn how to test REST APIs by writing integration tests or repository tests by using Testcontainers.

* [Spring Boot REST API Best Practices - Part 1 : Implementing Get Collection API](https://www.sivalabs.in/spring-boot-rest-api-best-practices-part-1/)
* [Spring Boot REST API Best Practices - Part 2 : Implementing Create and Update APIs](https://www.sivalabs.in/spring-boot-rest-api-best-practices-part-2/)
* [Spring Boot REST API Best Practices - Part 3 : Implementing FindById and DeleteById APIs](https://www.sivalabs.in/spring-boot-rest-api-best-practices-part-3/)

It's very important to handle exceptions and return meaningful responses in case of failures.
Spring Boot provides different approaches to handle exceptions.

* [Spring Boot REST API Best Practices - Part 4 : Exception Handling in REST APIs](https://www.sivalabs.in/spring-boot-rest-api-best-practices-part-4/)

To learn more about testing the Spring Boot applications, you can refer the following resources:
* [Java Testing Made Easy](https://www.youtube.com/playlist?list=PLuNxlOYbv61jtHHFHBOc9N7Dg5jn013ix)
* [Philip Riecks Blog](https://rieckpil.de/)
* [Testcontainers Guides](https://testcontainers.com/guides/)

To learn more about JPA/Hibernate and Spring Data JPA:

* [Vlad Mihalcea Blog](https://vladmihalcea.com/blog/)
* [Thorben Janssen Blog](https://thorben-janssen.com/)

By now, you should have good enough knowledge to build a REST API backing with a database in a professional way.

### Stage 3
In Stage 3, you can learn Spring Security, Event Handling, and Job Scheduling.

Securing the web application or REST APIs is a very common requirement.
Spring Security is a highly configurable, customizable framework for implementing security.
The "highly configurable and customizable" nature of Spring Security also comes with a steep learning curve.

* The official [Securing a Web Application Guide](https://spring.io/guides/gs/securing-web) helps you to be familiar with Spring Security basics.
* The [Getting started with Spring Security and Spring Boot](https://reflectoring.io/spring-security/) article by [Tom Hombergs](https://x.com/TomHombergs) is an excellent comprehensive tutorial to learn Spring Security.
* An excellent article on [How to Secure your REST APIs with Spring Security & JSON Web Tokens (JWTs)](https://www.danvega.dev/blog/spring-security-jwt) by [Dan Vega](https://x.com/therealdanvega)

> [!TIP]  
> Securing microservices using OAuth 2 is an advanced concept which you can learn in the next stage(s).

Publishing and consuming events is a good practice to decouple the producer and consumer.
Spring provides support for publishing and consuming events using an annotation-based programming model.

* [Spring Boot Application Events Explained](https://reflectoring.io/spring-boot-application-events-explained/)

Running background jobs is another common requirement in enterprise applications.
Spring Boot provides job scheduling feature out of the box, but also supports integration with Quartz and JobRunr.

* [Scheduling Tasks](https://spring.io/guides/gs/scheduling-tasks)
* [Quartz Scheduler](https://docs.spring.io/spring-boot/reference/io/quartz.html)
* [JobRunr with Spring Boot](https://www.jobrunr.io/en/documentation/configuration/spring/)

### Stage 4
In Stage 4, you can focus on learning how to build microservices and secure them with OAuth 2.

By now you know how to build a monolithic application using Spring Boot.
Now, you can focus on building microservices using Spring Boot, Spring Cloud, etc.

* [Spring Security OAuth 2.0 Series](https://www.sivalabs.in/spring-security-oauth2-tutorial-introduction/)
* [Spring Boot Microservices Course](https://www.youtube.com/playlist?list=PLuNxlOYbv61g_ytin-wgkecfWDKVCEDmB)
* [Spring Boot and OAuth2 Guide](https://spring.io/guides/tutorials/spring-boot-oauth2)
* [Securing a REST API with OAuth 2.0 Spring Academy Course](https://spring.academy/courses/spring-academy-secure-rest-api-oauth2)

### Stage 5
In stage 5, you can focus on what is required for your project and be able to use them with Spring Boot.
Your project may be using Kafka, RabbitMQ, Spring Batch, etc. 
With the knowledge you gained by now, you shouldn't have a problem in learning how to integrate them with Spring Boot.

At this stage, I would recommend focusing on learning Architecture concepts.

* [Spring Modulith](https://docs.spring.io/spring-modulith/reference/): An approach to building modular monolithic applications using Spring Boot.

    * [Spring Modulith Crash Course : Building Modular Monoliths using Spring Boot](https://www.youtube.com/watch?v=FkP2aZiBrhg)
    * [The Modern Monolith, with Spring Modulith](https://www.youtube.com/watch?v=Pae2D4XcEIg)

* **Domain Driven Design (DDD)**
  * [Architecturally evident Spring applications with jMolecules](https://www.youtube.com/watch?v=-I7KiV_6f-s)
  * [Modular monoliths](https://www.youtube.com/watch?v=kbKxmEeuvc4)
  * [Implementing Domain Driven Design with Spring](https://www.youtube.com/watch?v=VGhg6Tfxb60)
  * [Clean Architecture with Spring](https://www.youtube.com/watch?v=cPH5AiqLQTo)

* [Microservices.io](https://microservices.io/)

## Resources
* [Spring Website](https://spring.io)
* [Spring Academy](https://spring.academy/)
* [Spring Boot Guides](https://spring.io/guides)
* [Spring IO YouTube channel](https://www.youtube.com/@SpringIOConference)
* [Spring Developer YouTube channel](https://www.youtube.com/@SpringSourceDev)
* [Josh Long YouTube channel](https://www.youtube.com/@coffeesoftware)
* [SivaLabs Blog](https://sivalabs.in)
* [SivaLabs YouTube channel](https://www.youtube.com/@sivalabs)
* [Thomas Vitale Blog](https://www.thomasvitale.com/)
* [Reflectoring Blog](https://reflectoring.io/)
* [Marco Behler Blog](https://www.marcobehler.com/)
* [Vlad Mihalcea Blog](https://vladmihalcea.com/blog/)
* [Philip Riecks Blog](https://rieckpil.de/)
* [Piotr's TechBlog](https://piotrminkowski.com/)
