---
title: Final Project Documentation
description: This is for the FinalProject
date: 
tags:
  - First post
layout: layouts/post.njk
---

# Final Project Documentation

## OpenAPI Document:

## Links for term-glossary repo: 
https://github.com/briangan123/term-glossary

https://term-glossary.vercel.app/

## Link to github documentation repo: 
https://github.com/briangan123/Documentation

## Background resources
https://app.swaggerhub.com/apis/Group-5-IST402/term-glossary-edit/1.0.0

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

#### Frontend Visual V1
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rmlbreevdgks5n01betc.jpg)

#### Backend Visual V1

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8o1cld4owcgyshmpqxwk.JPG)

## Questions
Do we want the user to delete or edit inputs for words or definitions?
Who or what acts as quality control to prevent any ill intent inputs into the database?
Do we want to add multiple definitions for words?
Are we supposed to find a use a current dictionary API? or are we supposed to figure out how to create one?
How do we connect our code to reference the jsonbin.io? Are we supposed to create a bin or a collection?
