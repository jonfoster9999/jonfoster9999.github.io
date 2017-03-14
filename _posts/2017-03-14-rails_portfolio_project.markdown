---
layout: post
title:  "Rails Portfolio Project"
date:   2017-03-14 00:57:23 +0000
---



I had an amazing time working on my Rails portfolio project. This project was significant to me because I felt some concepts that were slightly eluding me click in for the first time. This project really prompted me to dig in to reading documentation and forced me to push through some problems that were baffling to me. 

As I go through the Flatiron curriculum I take a lot handwritten notes, and they really paid off in this project. I have heard Avi say in the tutorials that programming isn't really about knowing every single answer but about being resourceful and being able to look things up. That really hit home with me in this project! I felt like the curriculum thus far has given me a great knowledge of the micro as well as macro level view of the problems faced in Ruby development, so whenever I didn't know the specific syntax or code to write in a given situation, I DID know what general idea I had to accomplish, making it easier to scope my research for the answer to the problems I was facing. 

My project is a website where one can sign up and post an Arts&Crafts project. The user can set the description and title of the project, add supplies with prices, and recieve ratings and reviews on their project. The user can also browse other users' projects and post reviews/ratings.

I had a lot of fun with the associations in this project. One interesting relationship was the user's relationship to reviews. I wanted to be able to both see a list of reviews that a user has recieved on his/her projects, as well as a list of reviews that the user himself/herself had posted. To do this, I turned to a method I saw in one of the Learn tutorial videos in aliasing relationships. In doing so I had access to both a "user.reviews" and a "user.authored_reviews" method. Likewise, a review object can respons to "review.user" and "review.author", both of which are instances of a User. To do this I also had to use the delegate method we learned in one of the previous labs. This threw me for a few loops but was well worth it as I felt working through the confusion really solidified some concepts for me!

Another thing that was interesting to me was that when I got to the point where I wanted to render collections into partials, I realized I was struggling in how to implement it, even though I was able to pass labs on it just a week or two ago! I realized I do this sometimes; focus on turning the tests green even more than grasping the concept itself. Doing this task out in the wild felt different to me than doing it in the comfort of a lab. All ended up well as I consulted my handwritten notes and some documentation online. 

I can't express how much fun I'm having learning all this stuff! It's a lot to take in but I feel I've learned more in the two and a half months I've been in Flatiron than I have anywhere else about anything else. Feeling very excited to continue and keep learning!

