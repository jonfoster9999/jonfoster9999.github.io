---
layout: post
title:  "Getting started with MEAN stack"
date:   2017-08-13 14:49:04 +0000
---


Getting started with the MEAN stack can be intimidating. It is a robust stack which lets you create complete projects from start to finish. The MEAN stack stands for MongoDB, Express, Angular, and NodeJS. At first glance this can seem overwhelming, as there are seemingly four different technologies to get a handle on before you can even start. However, I've found that with some basic knowledge of JavaScript, getting started doesn't have to be painful. 

NodeJS is basically a standalone JavaScript environment where you can write applications, and in this context a backend. If you come from writing JS in the browser, this is rather seemless as all the syntax is the same. Of course, JavaScript in the backend introduces some new concepts that are not used when writing frontend scripts in the browser. However, many of these concepts where introducted to us here at Flatiron as we learned about building backend applications in Rails. 

That is where Express comes in. Express is a JavaScript framework that one only need "require" in their Node application to get routing and server logic. Take this bit of code:

//app.js ->

    const express = require('express');
		const app = express();
		const port = 3000;
		
		app.get("/", (req, res) => {
		   res.send("Hello World");
		});
		
		app.listen(port, () => {
		  console.log("server running on port " + port);
		});
		
Looks pretty simple right? This code alone will start a server when app.js is run, and even print "Hello World" in the browser upon visiting http://localhost:3000/ . The route is provided with the express app "get" method (not surprisingly, other route methods can just as easily be created, ie 'post') and creates a similar environment that we're used to with Rails controllers. Of course this is the simplest possible implementation. In a real and complex app, routes would be outsourced to their own folders and files. 

Getting a server started is just that easy. Next week I will talk about what I've learned regarding connecting the Mongo database and Angular app.

