---
title: "Boxes!"
date: "Summer 2011"
subtitle: "node.js"
tags: ["javascript", "html5", "node", "game"]
thumb: "boxes-thumb.png"
---

![A screenshot of the Boxes game](/images/portfolio/boxes.png)

One weekend during the summer of 2011, I thought to myself "I should learn HTML5..." So, I started on a project that would turn into more than I expected.

Because I really wanted to learn how everything worked, I basically started from scratch.
I started out by creating a simple HTML5 webpage that would draw a box on a Canvas.
Then, I figured out how to make the box move with JavaScript.
Fancy, I know.
For some reason, when I get to the point where I can see things moving and working, I usually get sucked in; this was no exception.
Soon came multiple boxes moving, and patterns came next, until I was having so much fun just doodling around I forgot that I was trying to write good code.

Once I got all the fiddling around out of my system, I took a step back and starting to refactor my code.
I made a box class, created update and paint loops, and cleaned up a lot of functions.
Then, I started to think about what I could actually do with this, and I decided that I could probably make a game out of this.
The most logical course of action was to create a snake-like game, because who doesn't know snake?
I figured out how use JavaScript to use my arrow keys as controls, and added in trailing boxes and dots to the game.
Eventually, I had a game.

After that, my mind wandered to other things and I thought that I could do more, and make it multiplayer.
I thought "I should learn Node.js, that's been all the rage these days...", so I did.
I downloaded Node.js and started looking up tutorials that would help me stream data between computers realtime.
I decided to use websockets, so I settled on socket.io and started to work.
At first, I used a simple method of every computer simply broadcasting its x,y location,
but after a few of my clever friends figured out how to abuse that, I implemented cheat detection.
The server would process all of the data instead of the client, so even if a client said that it had moved to the ball,
the server would detect if it moved too fast or jumped locations.
Finally, after a little tweaking I had my game.

Now, if we jump to current day, I wanted to put my game somewhere hosted that wasn't my local 8 year old webserver, so I looked up node.js hosting.
Finally, I found one I liked, Heroku, I deployed my app and found out that it doesn't actually support websockets.
Searching around some more, I found no suitable alternatives that support websockets, so I launched my own instance of Amazon EC2, and manually ran it there.
Voila!

To play Boxes, visit my website [http://boxes.glentaka.com](http://boxes.glentaka.com)

For those who want to see my source code and how I did it, go to [http://github.com/glentakahashi/boxes](http://github.com/glentakahashi/boxes)