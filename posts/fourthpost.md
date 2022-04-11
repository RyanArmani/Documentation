---
title: This is my fourth post.
description:
date: 
tags: 
layout: layouts/post.njk
---

## Front END
This week we have worked out some of the big issues that had us at a stand still.
For this week, We have gotten our ADD user end Point and View all Endpoint working 
in the console.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/q7d9gicbkpn3ipea1ojl.png)
Listed in this image above shows what happends in the console when you input your fields and click on the add button

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ppevheafss5e0bu9ihkm.png)
Here is the results for when we click on the view all button. The only issue that we dont quiet understand with this is that when we click on the view all button it will only show blank spaces unless we have inputs in the Text fields.

## Backend
This week we were able to connect the front end inputs and save them into the backend. Then we hit the addTerm endpoint and were able to add the data to the planetscale db.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oi6acesvetiw3ir4diwq.png)
The above image shows the entries in the planetscale db.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7uapz1unq2mxsm3zmyv3.png)
 The above image shows the code to capture the inputs and calls the api to input the entries into the db.
 

## What we need to work on this week
1. Figure out how to disable empty entries
2. Setting up and figuring out how we are going to use the term-finder.js code that is liked with planetscale
3. We need to setup an accent card or something where we will display all defintions with their attributes in the fields
4. Work on the remove button once we have our data viewed on the page for everyone to see.
5. Fix the view all bugs


## Questions
1. For listing all items in the data base would you reccomend using an accent card?
2. How can teammates test the site locally? When they run "vercel dev" and "vercel pull", it shows them options to set up their own vercel site instead of spinning up the main vercel site. (they are in the correct directory too)
3. How can we reset the id# when we clear the database? 
4. How should the delete button be implemented? What should the logic look like so that there is a delete button next to each entry when the "view all" button is pressed? 

## API documentation in progress
1. https://app.swaggerhub.com/apis/Group-5-IST402/term-glossary/1.0.0#/