# Marina API
 	By: Terence Tang
 	tangte@oregonstate.edu
 	CS 493 Cloud Application Development
 	6/1/2021

## Files Included:
    - server.js (marina app)
    - package.json
    - postman test collection
    - postman environment file
    - app.yaml (gcloud config file)

## Description:
    REST API for simulating a marina which contains three entities: users, boats and loads 
    (cargo).  Users are allowed to create accounts and authenticate via an implementation 
    of Auth0.  Boat entities provide basic CRUD functionality, but is a protected resource that requires the presence of a valid JWT via bearer auth token to access. Loads are an 
    unprotected resource that may be created or deleted at any time.  

    Regarding entity relationships in this application, users are modeled as owners of boats, 
    where each owner can own numerous boats and each boat can only have one owner.  Boats on 
    the otherhand can hold numerous loads, with each load being restricted to being only on one
    boat at a time.  Loads themselves can either be on land or on a boat.  
   
    The implemented API allows for management of users, boats and loads the relationship between 
    them via REST API calls.

    Final program hosted on Google Cloud via App Engine and utilizing Google Datastore.

## Environment Requirements:
    - Implemented in javascript
    - Requires NPM for package installation
    - Requires Google Cloud SDK for gcloud app deployment and datastore mgmt

## Installation
Below are the instructions on how to start up a Node.js application for Assignment #9 - Portfoliio Project.
Note: As this program utilizes Auth0 as an authentification platform, you will need to provide a client_ID and client_secret for your Auth0 app to utilize this functionality.

* [Setup] - Use npm install - Supplied package.json contains all dependencies needed.
* [Running locally] - Express server application will run on local host 8080 
* http://localhost:8080

## Setup

Before you can run or deploy the sample, you need to do the following:

1.  Install dependencies:

    $ npm install

## Running locally

    $ npm start o or $ node server.js

## Deploying to App Engine

    gcloud app deploy
