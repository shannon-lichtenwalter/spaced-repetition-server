# Spaced repetition API Server

## Created By: Julio Hernandez & Shannon Lichtenwalter

### Links 
See it Live: https://spaced-repetition-capstone-project.now.sh
Client Repo: https://github.com/shannon-lichtenwalter/spaced-repetition-client
Server Repo: https://github.com/shannon-lichtenwalter/spaced-repetition-server

### Introduction

This server is used in conjunction with the spaced-repetition learning platform front-end client.

### Technology Stack
This API server was built using Nodejs, Express, Javascript, and PostgreSQL. The server and database are deployed on Heroku. 

### Endpoints

#### /api/auth/token : 
    POST this endpoint verifies login is correct and returns JWT auth token. 

    PUT will refresh the JWT auth token for a logged in user.

#### /api/language :
    GET (/) this endpoint returns the language table data for a logged in user.
    GET (/head) this endpoint returns the headWord (next word to practice) for a logged in user.
    POST (/guess) this endpoint determines if a user's guess is correct or incorrect. It updates that database accordingly based on the spaced repetition learning algorithm and returns the next word for the user to practice.

#### /api/user:
    -POST: will add a new user (register) to the database