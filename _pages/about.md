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

This initial approach placed no limits on how the tree branches grew; they grew on top of each other, and to arbitrary distances. As the tree branched off exponentially, the program struggled to run, so I modified the code to prevent the branches from intersecting and growing past the edge of the screen.

Over time, I slowly added more and more details to the simulator. I drew the tree branches thicker near the base and thinner in the farthest branches. I added apples and leaves to the trees. I used random generation strategies to make the simulation organic; for example, farther from the base of the tree, branches, apples, and leaves grow more frequently. Eventually, I added weather to the simulator, and I added inchworms which are animated to crawl up the trees.

&nbsp;

Gobblet (Dec. 2022)
======
{% include youtube.html id="G4yr9P4P2Gk" %}

&nbsp;

This project simulates a computer playing against itself in the game of Gobblet.

Gobblet is a one-on-one game where one player controls the black pieces and the other player controls the white pieces. A player wins by using their pieces to make 4-in-a-row along a row, column, or diagonal of the 4x4 board. The catch is that the pieces are shaped like upside-down cups and come in four sizes, meaning a player can cover an opponent’s piece by placing a larger piece on top of it.

I drew the pieces as concentric circles so that you can visualize which pieces have “gobbled” up other pieces, though in the physical game you can only see the topmost, biggest piece.

The computer approximates the best move at each point of the game using a recursive algorithm which considers a small number moves into the future. The computer has a perfect memory of which pieces have gobbled up other pieces, another justification for drawing gobbled-up pieces as smaller concentric circles.

Site-wide configuration
======
The main configuration file for the site is in the base directory in [_config.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_config.yml), which defines the content in the sidebars and other site-wide features. You will need to replace the default variables with ones about yourself and your site's github repository. The configuration file for the top menu is in [_data/navigation.yml](https://github.com/academicpages/academicpages.github.io/blob/master/_data/navigation.yml). For example, if you don't have a portfolio or blog posts, you can remove those items from that navigation.yml file to remove them from the header. 

Create content & metadata
------
For site content, there is one markdown file for each type of content, which are stored in directories like _publications, _talks, _posts, _teaching, or _pages. For example, each talk is a markdown file in the [_talks directory](https://github.com/academicpages/academicpages.github.io/tree/master/_talks). At the top of each markdown file is structured data in YAML about the talk, which the theme will parse to do lots of cool stuff. The same structured data about a talk is used to generate the list of talks on the [Talks page](https://academicpages.github.io/talks), each [individual page](https://academicpages.github.io/talks/2012-03-01-talk-1) for specific talks, the talks section for the [CV page](https://academicpages.github.io/cv), and the [map of places you've given a talk](https://academicpages.github.io/talkmap.html) (if you run this [python file](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.py) or [Jupyter notebook](https://github.com/academicpages/academicpages.github.io/blob/master/talkmap.ipynb), which creates the HTML for the map based on the contents of the _talks directory).

**Markdown generator**

I have also created [a set of Jupyter notebooks](https://github.com/academicpages/academicpages.github.io/tree/master/markdown_generator
) that converts a CSV containing structured data about talks or presentations into individual markdown files that will be properly formatted for the academicpages template. The sample CSVs in that directory are the ones I used to create my own personal website at stuartgeiger.com. My usual workflow is that I keep a spreadsheet of my publications and talks, then run the code in these notebooks to generate the markdown files, then commit and push them to the GitHub repository.

How to edit your site's GitHub repository
------
Many people use a git client to create files on their local computer and then push them to GitHub's servers. If you are not familiar with git, you can directly edit these configuration and markdown files directly in the github.com interface. Navigate to a file (like [this one](https://github.com/academicpages/academicpages.github.io/blob/master/_talks/2012-03-01-talk-1.md) and click the pencil icon in the top right of the content preview (to the right of the "Raw | Blame | History" buttons). You can delete a file by clicking the trashcan icon to the right of the pencil icon. You can also create new files or upload files by navigating to a directory and clicking the "Create new file" or "Upload files" buttons. 

Example: editing a markdown file for a talk
![Editing a markdown file for a talk](/images/editing-talk.png)

For more info
------
More info about configuring academicpages can be found in [the guide](https://academicpages.github.io/markdown/). The [guides for the Minimal Mistakes theme](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (which this theme was forked from) might also be helpful.
