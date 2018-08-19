---
layout: default
title: Backend Build Monitor Assignment
permalink: backend-build-monitor-assgiment
---

## Build Monitor Assignment

The goal of this project is to creat a simple server that aggregates website health checks.

See [here](/project-setup) for initial project setup

First download the project zip from [here](https://drive.google.com/file/d/1Csz4ObcCayXBIVNGe6G2pCEZO8D3cB36/view?usp=sharing).
Unzip the file and and examine the instructions in the Readme

### Requirements

- Use the [got](https://github.com/sindresorhus/got) library to do a get request against the server health check URI's embedded in the project. Consider any non 2xx response a failure
- These results should be automatically fetched every 5 minutes (hint: use a lower value during testing)
- Make sure the fetch request timeout is lower than 5 minutes
- Make the health check calls in parallel
- Store the last successful health check time in `lastTimeUp`
- Ensure the checker is de-registered when the server shuts down
- Add an error field to Server object which contains the status code and response body when the health check fails

Example Error Response:

```
{
  "data": {
    "servers": [
      {
        "id": 1,
        "name": "Server1",
        "healthCheckUri": "https://api.durf.dev.stackworx.io/health",
        "status": "DOWN",
        "error": {
          "status": 500,
          "body": "An Internal Server Error Occured"
        }
      }
    ]
  }
}
```

### Bonus Requirements (Difficulty in brakets):

Bonus requirements for extra credit. Not listed in any particular order

- Persist the server status and last up time somewhere so that they are not lost between server restarts (5)
- Abstract all the code into a server layer and keep that code separate from the GraphQL code (2)
- Add a filter paramter to the server field so that a user can request results for only specific servers (2)
- Add a filter to only fetch servers with a specific status. E.g. DOWN (2)
- Creat a mutation to disable the checking of a server (10)

### Help

Send an email to <assignment@stackworx.io> if you get stuck

### Hints

- Use [httpstat](http://httpstat.us/) to simulate failures
- Graphql Resolvers can be async or return promises
- Use an IDE that understands typescript
