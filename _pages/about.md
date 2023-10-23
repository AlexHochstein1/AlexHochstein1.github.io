---
permalink: /
title: "Introduction"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

This portfolio contains video demos of projects that I coded for fun in my spare time. Each project was coded in Java.

&nbsp;

Origami Simulator (Sep. 2023)
======
{% include youtube.html id="O_kQ1C4yZCE" %}

&nbsp;

This interactive simulator allows the user to fold 2D origami.

In order to fold a region R of the origami, which involves reflecting R over a fold line, a three-step recursive algorithm is used. First, any regions which overlap with R, and therefore are in the way of R being folded, are recursively folded. Second, the region R itself is folded. Third, any regions attached to R are recursively folded.

&nbsp;

Nature Simulator (Apr. 2023)
======
{% include youtube.html id="oQ_uG5Pf7wM" %}

&nbsp;

This simulator began with a simple idea: I thought I could draw a tree by first drawing a line segment as the base of the tree, then drawing line segments that branch off of the base of the tree at random angles, and continuing to draw line segments that branch off the other line segments at random angles.

This initial approach placed no limits on how the tree branches grew; they grew on top of each other, and to arbitrary distances. As the tree branched off exponentially, the program struggled to run, so I modified the code to prevent the branches from intersecting and prevent them from growing past the edge of the screen.

I added many details to the simulator over time. I added apples and leaves to the trees. I used random generation strategies to make the simulation organic; for example, farther from the base of the tree, branches, apples, and leaves grow more frequently. Eventually, I added weather to the simulator, and I added inchworms which are animated to crawl up the trees.

&nbsp;

Gobblet (Dec. 2022)
======
{% include youtube.html id="G4yr9P4P2Gk" %}

&nbsp;

This project simulates a computer playing against itself in the game of Gobblet.

Gobblet is a one-on-one game where one player controls the black pieces and the other player controls the white pieces. A player wins by using their pieces to make 4-in-a-row along a row, column, or diagonal of the 4x4 board. The catch is that the pieces are shaped like upside-down cups and come in four sizes, meaning a player can cover an opponent’s piece by placing a larger piece on top of it.

I drew the pieces as concentric circles so that you can visualize which pieces have “gobbled” up other pieces, though in the physical game you can only see the topmost, biggest piece.

The computer approximates the best move at each point of the game using a recursive algorithm which considers a small number moves into the future. The computer has a perfect memory of which pieces have gobbled up other pieces—another justification for drawing gobbled-up pieces as smaller concentric circles.

To approximate the best next move at a depth of D moves, the computer considers all of its possible moves: for each possible move, the computer recursively approximates the sequence of best moves for the next (D - 1) moves into the future, and records the outcome at the end of that sequence of moves. The computer chooses the move with the best future outcome.
