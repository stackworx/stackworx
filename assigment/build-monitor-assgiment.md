---
layout: default
title: Build Monitor Assignment
permalink: project-build-monitor
---

The goal of this assignment is to create a simple build monitor.
It is often convenient to create an endpoint 

[See](/project-setup) here for initial project setup

This is a simple React assignment to test your javascript proficiency. 
First download the project zip from [here](https://drive.google.com/file/d/0BwuuF0OKfFqucG84WkE0TXNjYk0/view?usp=sharing)
Unzip the file and run the following commands

```
yarn 
yarn start
```

This should open the project in your browser. If it does not navigate to [localhost:3000](http://localhost:3000)

#### Requirements
 * The application will receive a list of server health check endpoints.
 * The endpoints should be checked every x seconds (Make this 5 minutes)
 * The endpoint will be an http URL that you must invoke a ```GET``` request on, any return code other than 200 means a health check failure
 * The check must be done using the request library 
 * The application must store the last endpoint check result
 * Each server must be represented as a block.
 * The health check block will be green for UP and red for DOWN, GREY for other (E.g. request completely failed for example due to not having internet).
 * Clicking on any block must display the last response payload from the health endpoint.

### Bonus Requirements:
 * Use flex box to make the server blocks size dynamically (E.g. let the user pick the number of rows and columns)
 * Implement a method to group and differentiate environments, e.g. production vs testing
 * Fire all health checks simultaneously, not sequentially

### Hints
 * Use [httpstat](http://httpstat.us/) to test common failures
 

#### Endpoints
 * [Test 1](https://test.cognition-app.com/api/status)
 * [Test 2](https://ord.dev.stackworx.io/graphql)
 * [Test 3](https://api.durf.dev.stackworx.io/graphql)
 * [Test 4](https://prima.run/health)
 * [Test 5](https://stackworx.io/)