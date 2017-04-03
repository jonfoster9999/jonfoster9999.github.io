---
layout: post
title:  "Rails app with a jQuery front-end"
date:   2017-04-03 01:53:50 +0000
---


I had an amazing time working on this project. Working with four(!) languages going back and forth (html, css, javascript, ruby) PLUS different frameworks (erb, jQuery, rails)  in a project really makes the gears in your brain turn and forces you to constantly stop and assess where you are in the context of your app. Many times I felt myself reaching for Rails tools while I was in the middle of a Javascript function. While it felt a little confusing and frustrating at times, I found it so helpful because I had to think of ways to get data to where I needed it between these languages. 

For example, in one function I required the current user Id in order to make a comparison in a function so that I could keep a feature I had built in the original Rails project. I ended up manually adding the current user id to an object that I was going to serialize and pass anyway, so I could grab it in the javascript side:

	def projects
		@obj = {}
		@projects = Project.all
		@obj[:projects] = @projects
		@obj[:current_id] = current_user.id
		render json: @obj
	end

While I have no idea if this was technically correct, it worked and I was able to keep my feature. Being forced to think like this was really helpful and I think flexed my critical thinking muscles. As I mentioned, sense of context was really the most challenging part of this project to me, and through the confusion I think I was able to loosen some mental knots.

Another interesting part of this project was some of the tangents it set me on while trying to make certain features work. I have a certain feature where I was wanting to do a $.get request while inside of a success callback from a $.post request in order to update a related, but unattached, part of the view. I was being returned a "promise" object, which I had to spend a good amount of time researching how to handle. I learned that I could pass the success function as a callback to the function that was making the $.get request with the code that was dependent on the return value of the $.get request. It ended up working great and now I feel like I'm a little further along in understanding the scary "promise" territory of asynchronous Javascript that I had previously read about.

All in all I was able to keep all the features I had and enhance some by incorporating jQuery into the front end. It was a great experience and I learned a ton. The video for my project is here:

https://www.youtube.com/watch?v=CoQ4qD1DTrQ&feature=youtu.be


