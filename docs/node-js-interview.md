---
title: Node.js Interview Questions
data: 2022-08-02
---

![图片](../png/node-js-interview/Node.js_Architecture_Workflow.png)
# Node.Js
## What is Node.Js?
Node.Js is an extremely powerful JavaScript runtime environment for running web applications outside the client's browser. Developers use Node.js to create server-side web applications, and it is perfect for data-intensive applications since it uses an asynchronous, event-driven model.

## What is event loop?
OK, The Event Loop allows nodejs to perform non-blocking io operations.

The Event Loop is a queue of callback functions. When an async 
function executes, the callback function is pushed into the queue. 
The JavaScript engine doesn't start processing the event loop until 
the code after an async function has been executed.
So even though nodejs is single thread. The event loop allows nodejs to still perform multiple operations.

## What do you understand about callbacks?
A callback is a function passed as an argument to another function.

callbacks are most often used with asynchronous functions.

For example, when you create a function to load a file, you cannot use the content before it is fully loaded. This is a good time to use a callback.

## What is callback hell?
callback hell is a problem that arises usually when developers try to implement asynchronous processes one after another.
There are a lot of ways to solve callback hell:
The general strategy is modularization. You can break up callbacks into independent functions.

You can also use async + await or generators + promises to avoid callback hell.

## What kind of framework has been used with node.js?
I'm familiar with Koa.js.
Koa is a very small framework that provides us with a minimal interface to build our applications. 
A Koa application is an object containing an array of middleware
functions that are composed and executed in a stack-like manner.

## pm2 ?
[](https://medium.com/we-code-we-write/why-and-how-you-should-use-pm2-for-a-node-js-application-in-production-5fa19dd3a856)
Automatic process restarts and keeping alive

assert 应用就结束了

PM2 enables you to keep applications alive forever, reloads them without downtime, helps you to manage application logging, monitoring, and clustering.

# Database
## What databases are you familiar with?
I'm familiar with MongoDB.
MongoDB is a non-relational database. It stores data in the key-value pair. It doesn't have much structure but it's more flexible.

## Explain the term "indexing" in MongoDB.
Indexes help MongoDB to query faster.
An Index stores a small part of the data set in a form that is easy to traverse. The index stores the value of the specific field or set of fields, ordered by the value of the field as specified in the index.

## What do you mean by Transactions?
A transaction is a logical unit of processing in a database that includes one or more database operations, which can be read or write operations. Transactions provide a useful feature in MongoDB to ensure consistency.

## sql injection or nosql injection？

```
Example 

User.findOne({
    "name" : req.params.name, 
    "password" : req.params.password
}, callback); 

If req.params.password is { $ne: 1 }, the user will be 
retrieved without knowing the password ($ne means not 
equals 1).
```

use Mongoose Driver
As it follows a schema, if the password is a string field, it will convert the object { $ne: 1 } to string and no damage will be done. In this case, you don't need to sanitize, just remember to set a proper schema.


# Computer Science

## Thread pool

# Security

# docker



# Resume
## [Resume Template](https://www.beamjobs.com/)


# Reference:

[1] [Top 50+ Node.js Interview Questions and Answers for 2022](https://www.simplilearn.com/tutorials/nodejs-tutorial/nodejs-interview-questions)

[2] [What-is-node-js](https://www.simform.com/blog/what-is-node-js/#section2)


worker thread ?
数据库的话就是