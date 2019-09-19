---
layout: post
title:  "Architecture Plan for Pong"
date:   2019-09-19 13:47:56 -0600
categories: jekyll update
---

# Software Architecture Plan for My OpenGL Pong Clone

Whew, what a title. This past day I finally got OpenGL up and running a black screen, which means it is working! I never knew that linking C++ libraries was such a pain, but I am running this on Windows and not my Linux machine (which I hear is as simple as running a few CMake files). I originally began writing this article thinking I would do a formal Software Architecture document, but I have instead opted to do a less formal Planning document that will detail Class Hierarchy and my plan of attack for coding out this project.

<br>

## Features

### Priority 1

1. The user will be able to move the paddle up and down the screen
2. When the ball makes contact with User/Oponent's paddles, the x-direction will flip.
3. When a User/AI-Opponent scores ten points, the game will end displaying a You Won/You Lost message.

### Priority 2

1. Have Different Game Scenes for: Main Menu, Game, and Win/Losing Screen with Restart Button.
2. Sound Effects played when ball has a collision and when a point is gained.

### Priority 3

1. Have difficulty levels that determine the speed that the AI paddle moves.

<br>

## Class Hierarchy

There will be a standalone class Game that will contain the current state of the game, and will deal with all of the OpenGL rendering calls.

screenObject
* This class will deal with anything that is rendered on the screen, it will require an x and a y coordinate to be told where to draw. All background objects will be called this as they don't need anything else to work.

collideableObject
* This class extends the screenObject class, and will be the basis for the paddles and ball. This class will have methods to check for collisions.

playerPaddle
* Extends the collideableObject class and has methods to: Detect player input and respond accordingly.

enemyPaddle
* Extends the collideableObject class and has methods to: move to where the y-axis of the ball is (at most likely a slower speed).

Ball
* Extends the collideableObject class and has methods to: Regenerate to the center after falling off of the screen (x-axis wise), change it's current x-direction when collides with playerPaddle or enemyPaddle.

<br>

## Current Questions I Have

* I think that I will need to generate random y values for the ball when it regenerates to the center so that it does not only travel in a straight line back and forth, I wonder how best to implement this would be.... I am thinking that possibly only having it generate velocity values that would make it so that it doesn't end up going straight up and down either.

* Is there a way in OpenGL to scale the size of the windows down? I want to make this look very blocky and pixelate, and not high resolution at all. 