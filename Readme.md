#SWE642 ASSIGNMENT_3 

#ANUSHA BHAVANAM
G01348764

# Student Survey Application

The Student Survey Application is a full-stack web application that allows students to fill out a survey form to provide feedback about their campus visit. It also provides a feature to view all surveys recorded to date. The application is built using Angular for the frontend and Spring Boot for the backend, with data storage handled through JPA.

## Table of Contents
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Usage](#usage)

## Getting Started

### Prerequisites
- Node.js 16 and npm (Node Package Manager) should be installed to run the frontend application.
   ```
   brew install node@16 
   
   ```
- Installing Angular:

```
     Installing it locally:
    npm install  @angular/cli
```
- Java Development Kit (JDK 17) and Maven should be installed to run the Spring Boot backend application.

  ```
  brew tap adoptopenjdk/openjdk
  brew install --cask adoptopenjdk17

  ```

- An appropriate database in this case MySQL should be set up and accessible.

### Installation
1. Unzip the file.
2. Navigate to the "frontend" directory and run the following commands:
   ```
   npm install
   ng serve
   ```
   This will install the required dependencies and start the Angular development server.
3. Navigate to the "backend" directory and run the following commands:
   ```
   mvn spring-boot:run
   ```
   This will start the Spring Boot backend application.

## Features
- Welcome homepage with links to "Student Survey" and "List All Surveys."
- Student Survey form with various input fields and validation for required fields.
- RESTful API to store survey data in the database.
- List All Surveys page to view all recorded surveys.

## Development

Frontend Development using Angular:

- Started the project by generating an Angular template using the Angular CLI.
- Utilized the Angular Material module to enhance the user interface.
- Created two components in the project, one for the survey form and the other for displaying previous responses.
- Used the Angular CLI command `ng g c <component-name>` to easily generate the components.
- Developed a service to handle communication with the backend using the Angular CLI command `ng g s <service-name>`.

Provisioning a MySQL Database in AWS RDS:

- Created a new database in AWS RDS (Amazon Web Services Relational Database Service).
- Configured security groups to allow access to the provisioned database from any location.

Backend Development using Spring Boot:

- Set up the Spring Boot project by creating a project template.
- Filled in the MYSQL URL in the application.properties file, which connects the application to the MySQL database created in AWS RDS.
- Designed a Student Class as a model to represent the structure of the table in the MySQL database.
- Created a Restfulcontroller class to manage the RESTful routes for the application.
- Configured the pom.xml file to produce a WAR (Web Application Archive) artifact.
- Built the WAR file using Maven with the command `mvn compile war:war`.
- Defined API routes: `/student/responses` for fetching all responses and `/student/submitResponse` for submitting a response.


## Technologies Used
- Frontend:
  - Angular 16 (JavaScript framework for building user interfaces)
  - HTML, CSS, TypeScript (Languages for building the frontend)
- Backend:
  - Spring Boot (Java framework for building the backend)
  - JPA (Java Persistence API for object-relational mapping)
- Database:
  - MySQL (Relational database used with JPA for data storage)


## Usage
1. Access the application through a web browser by visiting `http://localhost:4200/`.
2. On the homepage, you can click the "Student Survey" link to fill out the survey form.
3. After filling out the form, click the "Submit" button to record the survey.
4. Click the "List All Surveys" link to view all surveys recorded to date.


