---
title: Check-in 3
description: 
date: 
tags:
layout: layouts/post.njk
---

## Links for term-glossary repo: 
https://github.com/briangan123/term-glossary

https://term-glossary.vercel.app/

## Link to github documentation repo: 
https://github.com/briangan123/Documentation


# API Endpoint Documentation

## Add Word
File Name: addTerm.js

Purpose it serves: The purpose of this file is to add a term the user inputs and add it to the database of terms.

Data Required: Term, Definition, and Context, all of which are varchar variables.

Data Returned: It will give a return the new word the user inputted (for now), and will return the id of the newly added term.

<img width="616" alt="Screen Shot 2022-03-31 at 1 11 18 PM" src="https://user-images.githubusercontent.com/97694891/161111938-b087d0dd-31e2-4229-b5d0-576b87bf9591.png">



## View List
File Name: viewList.js

Purpose it serves: Allows users to view the current list of terms they have compiled.

Data Required: No new information is required for this. The user clicks a button that signals a query to the Planet-Scale database.

Data Returned: All instances in the table.

<img width="743" alt="Screen Shot 2022-03-31 at 1 11 54 PM" src="https://user-images.githubusercontent.com/97694891/161112042-5c3b6b08-be4b-4e2e-a761-c2fa1414e9d5.png">



## Remove Word
File Name: removeTerm.js

Purpose it serves: Removes a term from the glossary.

Data Required: The button requests the id of the word which then signals a SQL query to the Planet-Scale database to delete the term. 

Data Returned: Responds with 200 success if the term is deleted successfully.

<img width="597" alt="Screen Shot 2022-03-31 at 1 12 19 PM" src="https://user-images.githubusercontent.com/97694891/161112115-2115c333-eec9-49a2-92f5-6e8bf37d1c79.png">


## Frontend
This week we didnt really add much to the gui of the frontend. We were focusing more how to get the basics working before we start to get more creative with how it looks.

#### Getting the Endpoints to run without errors
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0dfwkfs29664l8m3knnn.png)

So far We have setup the add button as well as the view all button but are running into the error shown above when trying to add data to the data base. 

Just for context, If you ar looking at our Vercel site, We are going to remove the edit line that is there and want to implement it into the view all portion once we get it running. Our idea is to have an edit button or icon next to each definition so they you can search through the list and find what you want to edit.

#Questions:

1. How are we connecting the .env file to the frontend. More so how is the ".env" file implemeted into the front end so our site is able to connect with the data base.
2. would the edit.js be similar to remove word.js file except the sql is just different?
3. Is there a way to test the backend files without having the front end fully working?
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vkc62wx76tactmqcvcfb.png)
4. for the image above, this is the code that we have for adding a new word to the dictionary. I am just confused if the error we are getting shown 2 images above is due to this code or if we are missing something that could be causing the error 500 in the console.


