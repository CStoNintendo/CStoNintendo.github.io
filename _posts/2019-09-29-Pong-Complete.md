---
layout: post
title:  "Pong Complete (Minimum Viable Product Edition)"
date:   2019-09-29 20:47:56 -0600
categories: jekyll update
---

![Pixi-Pong-Clone](/assets/img/pixi-pong-clone.png)

<br>

# Pong Complete!! (Minimum Viable Product)

[See The Game in Action](https://pixi-pong-clone.herokuapp.com)

[Peel Over My Code](https://github.com/CStoNintendo/pixijs-Pong-Clone)

To control the paddle, use your computer's up and down keys!!

## Some Slight Changes..

Hello, all. I know that it has been awhile since my last update, but I have been working on this project whenever I have had a break from school and family, and a lot changed from when I wrote up that document detailing my plan of attack.

A wise professor once told me that if you were going to make a project to show off to potential employers, put it on the web. This isn't to say that these potential employers aren't capable of compiling programs and viewing them themselves, but that during an interview you can pull up the website on your phone and show it to the recruiter/interviewer. Pretty solid advice.

I am currently taking Computer Graphics from this professor and all of our projects use WebGL (the website version of OpenGL [kind of a paraphrase]), and at this time I wanted to put my best foot forward on my first project and use something a bit more streamlined than the most primitive rendering engine (Web/OpenGL). I had the tiniest bit of work before in a rendering framework called PixiJS, that is a WebGL using rendering framework. I decided to rewire my project to use this instead of being in C++. Please note, that PixiJS is not a "Game Engine", and almost everything had to be done by hand, with more hand-holding than WebGL, but much less hand-holding than a game engine.

## Pitfalls

Some of the pitfalls I faced during the development of this project was figuring out the PixiJS API mostly. Getting the current x and y locations from my rendered objects to work on boundaries as well as collision detection took me much longer than I had initially anticipated. However, after continually trying and learning to Debug using the Chrome Debugger, I figured it out. ProTip for all of you looking to start with PixiJS, on your Pixi Graphics object, use the getBounds() method and then dereference the x or y value from there. Also, a good exercise for me was Javascript as a whole, a few functions of mine did not have closing parenthesis and no errors were were flagged in my Console, which took me a bit of time to figure out.

## What I Learned

Throughout these 10 days, I have greatly increased my fluency in Javascript and comfortability using the PixiJS rendering framework. 

## The Future

There are quite a bit more I want to incorporate into this project. Firstly, I need to implement touch/click controls so that people will be able to play this game on their phones instead of just on Desktop/Laptops for the vast majority of people in the world. This will make me content with this Minimum Viable Product.

Other features that I want to implement include: adding sound effects to play when the ball collides (bleeps and bloops), a starting screen that allows the player to select their difficulty, as well as and end screen that will allow the player to press a button that would reset the game. I have already implemented a Stub of a switch case that would allow for different paddle lengths, ball speeds and enemy paddles speeds depending on the selected difficulty.

## Closing Thoughts

This project felt like a great excersize in getting my feet wet in the Graphics/Game Programming field and makes me excited to go further and get started on my next game. I will report back soon when I know what I want my next game to be. Thanks for reading!
