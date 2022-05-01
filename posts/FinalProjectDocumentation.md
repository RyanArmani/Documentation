---
title: Final Project Documentation
description: This is for the Final Project
date: 
tags:
  - Final Project Documentation
layout: layouts/post.njk
---

# Final Project Documentation
The term glossary project allows users to add, view, and delete terms from a database. This database is leveraged through Planet Scale, a serveless database platform that is compatible with MySQL. As such, our code enables us to utilize SQL queries to perform specific actions depending on what task needs to be done. These are found in the form of API endpoints, of which the term glossary has four. These are the addTerm, removeTerm, termFinder, and ViewList javascript endpoints. 

The goal of the addTerm api endpoint is to add a term, definition, and context to a database, all of which is information entered by the user. The addTerm endpoint imports the PlanetScale Database. It then utilizes a handler passing an http request and response. The http request stores the term, definition, and context that will be added by the user. An array named terms acts to store the three aforementioned variables of the request query. Finally, after establishing a connection to the PlanetScale Database, a SQL query inserts the term, definition, and context into the database, and assigns it a unique autoincremented numerical id so that the database can execute commands on this specific entry.

The add-term-form responds to the user clicking the add-term button on the web application. Once a user clicks this button, the values entered into the term, definition, and context text boxes are stored as variables. A fetch command then connects to the addTerm api endpoint and executes the code using the term, definition, and context values acquired. The resulting data is then returned.

The removeTerm api endpoint aims to remove an entry in the database entirely, identifying a specific entry using the unique autoincremented ID each added entry is assigned by the addTerm api endpoint. After importing the PlanetScale Database, a handler function passes an http request and response, with the request retrieving the ID of the term in question. After connecting to the PlanetScale Database, a SQL query is executed that deletes the entry with the same ID as the one returned by the handler. A 200 response is returned if the code is successful. 

The termFinder api endpoint aims to retrieve a specific term and its definition/context based on a user's input. After importing the PlanetScale api endpoint, a handler function passes an http request and response, with the request retrieving the term entered by the user in the web application. After a connection to the database is secured, a SQL query is executed that aims to return any term within the database that matches the one provided by the user. 

The viewList api endpoint aims to retrieve all contents currently within the database. After importing the PlanetScale Database, a handler function passes an http request and response,. Once a connection is established with the database, a query is run that selects all the contents in the database, which is returned by the response. 

The term-finder is utilized in the retrieval if a specific term specified by the user. Importing LitElement, html, and css creates a base class for our web application (more information on lit can be found in the resources). A constructor is made which passes the variables id (Number), listMap (array), term (String), definition (String), and contrxt (String). Respectively, these variables are set as either null for integers, blank for strings, or an empty array for arrays. The findTerm method utilizes the term input by the user and passes it through the 'api/termFinder'. This data is returned in the form of an array. The render method runs on each update which updates the html of the page to register and returns the results if there are any matches in the database or none at all. 

The term-list is utilized in the deployment of the deletion of a term, viewing a specific term, as well as the viewing of all terms. Importing LitElement, html, and css creates a base class for our web application (more information on lit can be found in the resources). A constructor is made which passes the variables id (Number), listMap (array), term (String), definition (String), and contrxt (String). Respectively, these variables are set as either null for integers, blank for strings, or an empty array for arrays. The method getList uses a fetch command on 'api/viewList', which retrieves and returns the result of the viewList api endpoint. The method deleteTerm takes an argument 'e', which is the entry that is clicked on. The selected entry's ID is then acquired and returned. The entry's ID is then run through the removeTerm api endpoint within a fetch command, and the modified list is then returned. Regardless of which method is used, the render method runs on each update which updates the html of the page to register and visualize any changes which may have occurred in the database. 

## OpenAPI Document:
https://app.swaggerhub.com/apis/Group-5-IST402/term-glossary-edit/1.0.0

## Links for term-glossary repo: 
https://github.com/briangan123/term-glossary

https://term-glossary.vercel.app/

## Link to github documentation repo: 
https://github.com/briangan123/Documentation

## Background resources
Vercel: https://vercel.com/docs
Planet Scale: https://docs.planetscale.com/
OpenAPI (Swagger): https://swagger.io/docs/specification/about/ 
Lit: https://lit.dev/docs/v1/

#### Requirements for the Back end
Build a microservice that stores and processes vocabulary terms

POST / READ This service can be passed a text / HTML string of text, identify words that match the glossary

POST / CREATE needs to be able to take word, textual definition, and any links desired

GET / READ needs to accept a parameter for returning 1 term / definition or ALL

Pervasive data store in a jsonbin.io or actual data store of your choice


#### Requriements for the Front end

Create a demo page / space that has the ability to add new words to the glossary via a small form POST
The ability to hit a button and present all words in the glossary with their definitions via a dl tag (https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dl)
The ability to take a block of HTML on the page and send off to the microservice for processing.
The front end needs to then get the words that match, find them in the text of the HTML, and then automatically apply a vocab-term tag (https://www.npmjs.com/package/@lrnwebcomponents/vocab-term) which when clicking the word, would show the definition positioned near it.
Demo should include an area where the user can type text and hit "process" and it augments the typed text, presenting matches for the vocab word in context


## Brainstorm

#### Simplified Workflows of api endpoints
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oadydewm00pkcuvkzcav.jpg)

#### Backend Visual V1

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8o1cld4owcgyshmpqxwk.JPG)

## Questions
Do we want the user to delete or edit inputs for words or definitions?
Who or what acts as quality control to prevent any ill intent inputs into the database?
Do we want to add multiple definitions for words?
Are we supposed to find a use a current dictionary API? or are we supposed to figure out how to create one?
How do we connect our code to reference the jsonbin.io? Are we supposed to create a bin or a collection?
