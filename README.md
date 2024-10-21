# Fishing App

Fishing App is a web application for maintaining a logbook of fishing catches and planning future fishing trips. The app automatically generates time, geographic coordinates, and weather data when a user adds a new catch. The Fishing Trip Planner feature is currently being worked on. This feature will combine the user's historical data and the forecasted weather of the date of the planned trip to provide recommendations for fishing locations and lure / bait strategies.

## Source Code

Server: https://github.com/dkwelcher/fishingapp-server<br>
Client: https://github.com/dkwelcher/fishingapp-client

## Screenshots

![Screenshot of the Fishing App landing page hero for desktop that shows largemouth bass swimming in a lake with text describing the primary purpose of the application](/screenshots/fa-landingpage-hero-desktop.PNG?raw=true "Fishing App landing page hero section")

![Screenshot of the Fishing App manage trips dashboard view on desktop that shows fishery information and catch data for the user as well as buttons and inputs that allows the user to manage that data](/screenshots/fa-managetrips-desktop.PNG?raw=true "Fishing App manage trips dashboard view on desktop")

<div float="left">
    <img src="screenshots/fa-managetrips-mobile.PNG" width="300"/>
    <img src="screenshots/fa-signup.PNG" width="300"/>
    <img src="screenshots/fa-login.PNG" width="300" />
</div>

## Methodology Overview

- Adapted from Agile principles (https://agilemanifesto.org)
- Cycle: design -> prototype -> implement -> refactor -> test -> debug -> evaluate

## Tech Stack

- Client
  - Vite, React, TailwindCSS, JavaScript
- Server
  - Maven, Spring Boot, Java
- Database
  - PostgreSQL
- Containerization
  - Docker
- Tools
  - GitHub
- Testing
  - JUnit5, Cypress (soon)

## Current To-Do List (Week of 10/21/2024)

- Refactor React components (some components need to be broken down into smaller components)
- Assess need for Redux / Context
- Write Cypress tests for client source code
- Write additional JUnit tests for server source code
