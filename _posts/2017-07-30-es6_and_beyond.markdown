---
layout: post
title:  "ES6 & Beyond"
date:   2017-07-30 21:24:13 +0000
---


I had a great find while walking the streets of NYC yesterday. Discarded on the side of the street with a sign reading "free" were two books. I took a closer look and saw that the titles were "The Complete C# Guide" and "ES6 & Beyond". I knew I was enthusiastic about programming before, but I found out just how hardwired that enthusiasm had become when I involuntarily yelped "oh my God!".  I felt like I had just won the lottery. 

The ES6 book is great so far. In my studies I've read about the new features in ES6 a lot, but much of it has just been swirling around in my head, intermingled with all of the other stuff I've been learning. It's fantastic to read the information all focused into one book. 

I'm only two chapters in, but already I know that some features (which I read a little bit about in the past) have sunken in with me. It's funny how that works sometimes. You may read about some syntax or feature 3 or 4 times, but that time where it really sinks in, you know it will stick with you. 

The spread (...) operator is a super useful feature and allows for easier implementation of certain techniques in a much more intuitive way than ES5. The spread can be used in the parameters of a function like so:

    function someFunction(...args){ 
		
		}
		
In this way, any arguments passed will become part of the local variable "args", which will then be a real life array, unlike the odd array-like "arguments" property from before. Conversely, you could pass the spread as an argument to a function like this: 

    someOtherFunction(...[1, 2, 3, 4]);
		
This will have the same effect that 

    someOtherFunction.apply(null, [1, 2, 3, 4]) 
		
would have. It will "splat" the elements of the array and pass them in as individual arguments.

I plan on reading this book from cover to cover as it is very well written and breaks each issue down. I'm so glad I found it!


		
