---
layout: post
title:  "Final Project"
date:   2017-04-11 02:41:48 +0000
---


This project was unbelievably fun to tackle. I found it to be the most challenging and complex of all the projects (which I was expecting out of a final project). Getting started was the hardest part and I found myself off to several false starts. The configuration of the "universe" of the project was a bit puzzling to me at first, to have the angular app situated inside the rails app such that it's comfortably communicating with itself was definitely a challenge. I used a random video that I found on youtube (which I believe was from a former Flatiron student!) to get me in the ballpark.

Even though I read about it in the curriculum, I really realized the importance of the "/#/" domain versus the "/" domain, and how I could communicate between the two with json. Getting ui-router set up was a little wonky at first but once I got to the point where I felt the app was living in it's own comfortable universe inside the rails app I took a breather and regrouped.

I decided to make a movie database type app in the vein of fandango. I wrote out my models and relationships clearly on paper before I began building them which I had seen in a lot of the tutorials from Flatiron, that really helped. I spent a lot of time seeding the database with data to make it feel like a real project.

The requirements list was daunting but I enjoyed the challenge of taking on each one, step by step. I used a lot of online resources including the Angular documentation, Stack Overflow, and Google. 

The most exciting part of the project was when I was presented with a situation where I felt I was repeating myself. Of course we had to do a fair amount of work on directives in the curriculum, but I wasn't sure I knew how to handle them outside of the vaccuum of a lab. What was cool was that I used a directive because I actually felt like I needed it in my project rather than trying to force it in there to showcase for a project, and it came out really cool. The directive itself has a filter in it which takes an argument of a genre, so when placing the directive in the html I am able to pass in the movies object was well as the genre I wish to filter by, making the entire movies index (by category) page look something like this:

    <div class="movies__main">
        <genre-group genre="Drama", movies="movies"></genre-group>
        <genre-group genre="Family", movies="movies"></genre-group>
        <genre-group genre="Comedy", movies="movies"></genre-group>
        <genre-group genre="Action", movies="movies"></genre-group>
        <genre-group genre="Horror", movies="movies"></genre-group>
    </div>
		
	In a tutorial earlier in the curriculum I watched Avi write some awesome code and then say something like, "That's some sexy code, I'd definitely buy that code a drink!" That cracked me up! This little snippet here is the first time I felt like that about something I wrote. It felt great!
	
	All in all I had a great time writing this program. There is still some refactoring to do but I'm proud of the work I put in and look forward to many more coding adventures! 
	
A video demo of the project is here:

https://www.youtube.com/watch?v=h1_d1Q_kF3s&feature=youtu.be

