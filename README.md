# Fishing App

The Fishing App began as an independent project for the university senior capstone and continues to be a work of passion. The ultimate aim of the project was to gain experience developing a real-world application that addressed real-world development concerns such as security and user experience. The Fishing App was deployed to the Web during March and April 2024 for open testing and to showcase in numerous presentations. The source code is private, but this document details some high-level aspects of the SDLC relevant to the Fishing App.

## What is Fishing App?

Fishing App is a web application that allows users to record their own fishing journeys & catch records in their own private & secure database. Time, geographic coordinates, & weather-related data are automatically generated, leaving the user more time to catch their limit. The upcoming Fishing Trip Planner feature will combine the user's historical data & the forecasteed weather of the planned trip to provide fishing recommendations and strategies to catch more fish. Fishing App's mission is to give anglers the means to catch more fish.

![Screenshot of the Fishing App landing page hero for desktop that shows largemouth bass swimming in a lake with text describing the primary purpose of the application](/screenshots/fa-landingpage-hero-desktop.PNG?raw=true "Fishing App landing page hero section")

![Screenshot of the Fishing App manage trips dashboard view on desktop that shows fishery information and catch data for the user as well as buttons and inputs that allows the user to manage that data](/screenshots/fa-managetrips-desktop.PNG?raw=true "Fishing App manage trips dashboard view on desktop")

<div float="left">
    <img src="screenshots/fa-managetrips-mobile.PNG" width="300"/>
    <img src="screenshots/fa-signup.PNG" width="300"/>
</div>

## Objectives

- Research & identify appropriate industry-leading technologies to support implementation of the application
- Design & implement robust server capable of processing client requests & SQL database queries
- Design & implement client UI & functionality, involving basic authentication & CRUD operations related to keeping a fishing log
- Research, design, & implement security measures to secure client & server
- Research deployment technologies & strategies
- Deploy application to the Web

## Methodology Overview

- Adapted from Agile principles (https://agilemanifesto.org)
- Primary emphasis on iterative development & simulated customer collaboration
- Cycle: design -> prototype -> implement -> refactor -> test -> debug -> evaluate

## Tech Stack

- Client
  - Vite, React, TailwindCSS
- Server
  - Maven, Spring Boot, Spring Data JPA, Spring Security (with JWT)
- Database
  - PostgreSQL
- Containerization
  - Docker
- Tools
  - GitHub, Postman API, DBeaver
- Deployment
  - Cloudflare Suite, HetrixTools Uptime Monitor

## Server Implementation Overview

- Layered architecture
  - Presentation layer
  - Service layer
  - Data Access layer
    - Domain Model
    - Repository

Broad example of Trip architecture:

A client POST request arrives at the TripController. The JSON data is validated and sanitized, then processed into a TripDto. The TripDto is sent to the TripService where business logic is applied. The TripService uses the TripMapper to convert the TripDto to a TripEntity and sends the TripEntity to the TripRepository. The TripRepository interacts with the database to create the TripEntity in the database.

Security implementation includes Spring Security with JSON Web Tokens, and all passwords are salted and hashed in the database.
