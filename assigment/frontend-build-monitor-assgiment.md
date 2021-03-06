---
layout: default
title: Frontend Build Monitor Assignment
permalink: frontend-build-monitor-assgiment
redirect_from: "/project-build-monitor/"
---

## Build Monitor Assignment

The goal of this assignment is to create a simple build monitor.
It is often convenient to create an endpoint that can be used to check
the current status of a server or environment. With an endpoint like this
implemented it can be monitored externally and can aid is diagnosing
the source of issues quickly.

See [here](/project-setup) for initial project setup

This is a simple React assignment to test your javascript proficiency.
First download the project zip from [here](https://drive.google.com/file/d/0BwuuF0OKfFqucG84WkE0TXNjYk0/view?usp=sharing).
Unzip the file and run the following commands

```bash
yarn
yarn start
```

This should open the project in your browser. If it does not navigate to [localhost:3000](http://localhost:3000)

#### Requirements

- The application is only required to work in new versions of chrome
- The application will receive a list of server health check endpoints.
- The endpoints should be checked every x seconds (Make this 5 minutes)
- The endpoint will be an http URL that you must invoke a `GET` request on, any return code other than 200 means a health check failure
- The check must be done using the request library
- The application must store the last endpoint check result
- Each server must be represented as a block.
- The health check block will be green for UP and red for DOWN, GREY for other (E.g. request completely failed for example due to not having internet).
- Clicking on any block must display the last response payload from the health endpoint.

### Bonus Requirements:

- Use flex box to make the server blocks size dynamically (E.g. let the user pick the number of rows and columns)
- Implement a method to group and differentiate environments, e.g. production vs testing
- Fire all health checks simultaneously, not sequentially
- Show the total uptime - how long the endpoint has been reported as up

### Hints

- Use [httpstat](http://httpstat.us/) to test common failures
- You are welcome to display the response from the endpoint but you don't have to process it

### Help

Send an email to <assignment@stackworx.io> if you get stuck

### Learning Resources

- [React Docs](https://reactjs.org/)
- [React Beginners Guide](https://egghead.io/courses/the-beginner-s-guide-to-reactjs)

#### Endpoints

- [Test 1](https://cognition.dev.stackworx.cloud/api/status)
- [Test 2](https://ord.dev.stackworx.io/health)
- [Test 3](https://api.durf.dev.stackworx.io/health)
- [Test 4](https://prima.run/health)
- [Test 5](https://stackworx.io/)
- [Test 6](https://stackworx.io/)
