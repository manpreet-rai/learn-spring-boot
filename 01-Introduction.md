# Java Spring Framework

With Spring Boot, Spring Data JPA, Hibernate and Spring Security

Manpreet Rai (Course by Chad Darby)

Prerequisites
- Java Programming Language
- Java Development Kit (JDK) 17 or up
- IDE (Eclipse, Netbeans or IntelliJ IDE)

Spring framework is highly configurable but it is tedious to manage such project with so many dependencies. 

Solution: **Spring Boot**

#### Spring Boot

It is an opinionated framework management solution by spring team, which allows minimum headache of managing dependencies manually. 

Spring boot offers following advantages:
- Easier to get started with Spring
- Minimize manual configuration
  - Performs auto-config based on properties and JAR classpath
- Help resolve dependency issues using Maven/Gradle
- Provides multiple embedded servers:
  - Like Tomcat, Jetty, Undertow etc

Spring boot is not a different framework from Spring. It is a way of managing and creating the Spring apps an easy way. Behind the scenes, Spring Boot uses Spring.

#### Spring Initializr

Spring boot team provides an online tool for creating base project with facility to add dependencies and customize it on the same page. You can visit https://start.spring.io to use this tool to customize the project to your needs and download the starter project.

## Spring Boot Up and Running

Let's create a basic spring boot project where we create a controller and see Spring in action. Project overflow is shown as:

```mermaid
graph TD
    A["1\. Create starter project at Spring Initializr"] --> B["2\. Open project in IDE"]
    B --> C["3\. Add Controller code"]
    C --> D["4\. Build and Run"]
    D --> E["5\. Deployment"]
```

#### 1. Configure Starter Project
Visit the https://start.spring.io website and choose the following configuration for our starter project:
![image](https://github.com/user-attachments/assets/88865bfa-4d6e-4496-a6a7-6410a22206be)

- Project - Maven
- Language - Java
- Spring Boot - 3.4.4 (Choose release verison)
- Project Metadata
  - Group - com.example (or choose as your needs)
  - Artifact - demo
  - Name - demo
  - Description - Demo project for Spring Boor
  - Package name - com.example.demo
  - Packaging - **Jar**
  - Java - **24** (Choose latest)

Now on right side, you can add dependencies. Choose the following:
- Spring Web
- Spring Boot Dev Tools (Optional - For auto building project)

Once you are happy with configuration, just **Generate and Download** project.

#### 2. Open project in IDE
We are using "IntelliJ IDEA Ultimate" here, you can choose any of these:
- Eclipse
- Netbeans
- IntelliJ IDEA
- VSCode

Spring team also provide helpful IDE Plugins and tools as "Spring Tool Suite" package. You can use these to help you with Spring.

Once you download your project **zip** file, just extract it somewhere on your system path and open it up in your IDE. Let the IDE download all the required packages and finish loading.

**Optional - Configure auto build and hot reload**

If you added "Spring Dev Tools" as dependency and if you are using "IntelliJ IDEA" you can configure project auto-compile when saving source code. To do so, open **Settings** > **Build, Execution, Deployment** > **Compiler** and enable **Build project automatically**
![image](https://github.com/user-attachments/assets/6ec10642-0494-49a4-808b-8b5a1e8d1b0f)

Also, you need to go to **Settings** > **Advanced Settings** > Under Compiler Heading > enable **Allow auto-make to start even if developed application is currently running**
![image](https://github.com/user-attachments/assets/c8ba939b-b117-4f9b-bf28-3cdf64c8032c)

#### 3. Add Controller
The downloaded project is quite empty by default. Let's create a **Rest Controller**. It receives a request and responds accordingly.

To create a simple rest controller, let's add a Java class under **src/main/java/com/example/demo/** path as **DemoController.java**. This file contents are as shown below:
```java
package com.example.demo;

import org.springframework.web.bind.annotation.RestController;
import org.springframework.web.bind.annotation.GetMapping;

@RestController                 // spring annotation to create REST controller
public class DemoController {

    @GetMapping("/")            // receives GET request at '/' home path
    public String sayHello() {
        return "Hello from Spring Boot!";
    }
}
```


![image](https://github.com/user-attachments/assets/687953fa-9b0e-4b32-839d-a1623cfd5a60)























































































