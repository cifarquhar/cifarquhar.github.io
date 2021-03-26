---
title: Building a game with Spring and Electron - Part 1
tags: [Spring, Electron, Java, JavaScript, Tutorial, Games]
style: 
color: 
description: Learning how to make Rock, Paper, Scissors the hard way
---

## Setting the scene...

I absolutely love over-engineering things. I know that's maybe a controversial opinion, but hear me out. I don't work day-to-day as a developer, I teach complete beginners how to code. That means a lot of "can we do X with Y?"-type questions which often cover scenarios I hadn't ever considered. I do a lot of poking and prodding around the edges of what we teach and that's grown into a desire to do a lot of poking and prodding at the edges of my own knowledge.

Which is why I enjoy overthinking a problem. When I try to build stuff like the app I'll talk about here I'm not trying to streamline it and shoot for maximum efficiency. Instead I'm trying to see if I *can* make something work, and hopefully break a few things while I'm at it to see how they work...

That brings me to here: a short series of posts describing how I went about building an app to play Rock-Paper-Scissors against the computer. This will ultimately grow into something else, but before I go wild with the bells and whistles I need to prove the concept.

## Tech choices

The front end was an easy choice for me. I've been interested in learning about [Electron](https://www.electronjs.org/) for a while so that went straight to the front of the queue. I could have stuck with a browser-based game here, but that would have been less exciting for me. 

Decisions about the back end were harder. I use [Spring](https://spring.io/) when I'm teaching so that's where my instincts led me at first, but I've also recently heard about [Quarkus](https://quarkus.io/) and I'm keen to learn more about it. The big difference in speed (Quarkus is **much** faster) was a big temptation, but I decided to stick with Spring. I enjoy pushing myself to learn new tech, but it's also important to take it one step at a time. Learning two new things at once has the potential to turn into a debugging nightmare!

## What makes this special?

So far, so straight-forward: it's a JS app talking to a Java app, right? It would be, but I had a couple of extra steps planned:

- I don't want the player to have to be connected to the internet in order to play. That means my server running the game logic can't be hosted online, it has to be local.
- ...which means the user has to start the Spring app on their computer in order to play. Not insurmountable, but a big step up from simply clicking an icon to start an app.
- But can I tie the two together, so that the Spring app starts and stops when the Electron app does?

And that's the big challenge for me here. Perhaps there's a much simpler way of doing it, but this series will describe the way I found to do it and reflect on what I might change next time.

## What's the end game here?

I said I'd over-engineer it and for such a simple game I *definitely* have! What I've learned from this will feed in to other projects though, which was always the big picture here. I've got ideas for other apps I want to build where the Java back end will be doing something much more complex so while I could have done everything here in JavaScript and not had to worry about a separate server, I think it's been a worthwhile experience.

## What's next?

- [Part 2](/blog/rock-paper-scissors-2) - Setting up the back end in Spring
- Part 3 - Adding the game logic
- Part 4 - Building my first Electron app
- Part 5 - Starting and stopping the processes together
- Part 6 - Preparing the finished app