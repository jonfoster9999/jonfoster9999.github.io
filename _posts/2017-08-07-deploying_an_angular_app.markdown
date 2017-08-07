---
layout: post
title:  "Deploying an Angular App"
date:   2017-08-07 03:31:24 +0000
---


I've recently been working a lot in Angular 4. This framework employs TypeScript (instead of JavaScript) to power the components. As a result, the TypeScript needs to be compiled into JavaScript to work in the browser. While developing, the Angular CLI spins up it's own server so you can see your project on your local machine. Each time you save a change the TypeScript needs to recompile and your project is reloaded into the browser. This all happens pretty quickly and you get instant feedback on whether or not you are writing correct TypeScript code.

Like most frameworks, things work a little differently in production. I recently finished some projects that I decided I wanted to go live with. The applications worked fine on the local machine but I quickly became confused as to how they would function on a remote server. After all, the Angular CLI was responsible for creating the server I needed to view my files. I couldn't just place the app on another server without figuring out how to correctly serve the files. After some research I found out that it is not that difficult. 

When deploying, for example, a Rails application to Heroku, you are deploying the server/backend itself. The code you wrote that defined your application's behaviour gets placed on Heroku and handles the requests. With Angular, you basically have a bunch of nice front end code but no real logic to serve them up. You can create a very simple node server to run your app off of. 

The first things to be aware of are the changes you need to make to your package.json file. Angular defaults many of the dependencies to the devDependencies section, and Heroku needs some of these in the production dependencies to work. Be sure to move over the @angular/compiler-cli, and the typescript dependency to production dependencies. You must explicitly also tell the Angular app to 'build' once it is installed on the Heroku server. This build creates the compiled files needed to run in the browser. This can be accomplished with this line in the package.json 'scripts' section:

"postinstall": "ng build --aot -prod"

We must also tell the app that we plan to use a Node server. Piggy back this onto the end of your package.json file: 

  "engines": {
    "node": "8.0.0",
    "npm": "5.0.1"
  }

Now we need to create the simple node server to handle our files. We need to install express as a dependecy by typing 'npm install express --save" in the command line. Once we do that, we can create our simple 'server.js' file:

    const express = require('express');
    const app = express();
    const path = require('path');

    app.use(express.static(__dirname + '/dist'));

    app.listen(process.env.PORT || 8080);

    app.get('/*', function(req, res) {
      res.sendFile(path.join(__dirname + '/dist/index.html'));
    });
		
All that's left is to tell the app to launch this script when we want to run the app. Back in package.json scripts, we can include:

    "start": "node server.js" 
		
That's it! I've deployed two Angular apps so far this way with very little trouble.


