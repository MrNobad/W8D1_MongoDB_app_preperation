# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
--Express router?

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?
--Client responsible for logic (JavaScript) and look (CSS), server responsible for REST requests and fetch requests to the MongoDB?

3. What are the the responsibilities of server.js?
--it handles all the Cross-Origin Resource Sharing?

4. What are the responsibilities of the `gamesRouter`?
the gamesRouter handles all the CRUD actions to the MongoDB

5. What process does the the client (front-end) use to communicate with the server?
--???

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs
--the second argument is an init. It is used to call the method, body and headers from the MongoDB in this application?

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
--/:id I think, which is ObjectId

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
--To maps to the objects in our application code as they are unstructured, unlike a table.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
--ObjectId finds the instance specifically so we can work with the objects inside. It also creates instances with specific 24 byte hex strings. Without using ObjectId we could never find anything specific.

Add to your diagram the dataflow for removing a game.
